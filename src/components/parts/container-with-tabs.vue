<template>
    <div>
        <header>
            <nav>
                <router-link
                    v-for="(tab,index) in renderTabs"
                    :key="tab.name"
                    :to="tab.to"
                    :style="{zIndex:mobileMode?'':`${9-index}00`}"
                    :class="{'router-link-active':active===tab.name}"
                    :data-name="tab.name"
                    v-html="tab.text"
                ></router-link>
            </nav>
        </header>
        <article :style="{minHeight:mobileMode?false:renderTabs.length*150+'px'}">
            <div class="container-with-tabs--slot">
                <slot></slot>
            </div>
        </article>
    </div>
</template>

<script>
export default {
    name :'container-with-tabs',
    props:{
        tabs :Array,
        active:String,
    },
    computed:{
        renderTabs(){
            var index =this.tabs.findIndex(tab=>tab.name===this.active);
            var tabs =Array.from(this.tabs);

            if(!~index ||this.mobileMode)return tabs;
            tabs.unshift(this.tabs[index]);
            return [...new Set(tabs)];

        },
    },
    data(){return{
    }},
    mounted(){},
};
</script>

<style lang="scss" scoped="scoped">
@import "~pea-styles/scss/variable.scss";
.container-with-tabs{
    *{
        box-sizing:border-box;
    }
    header{
        nav{
            a{
                text-decoration: none;
            }
        }
    }
    article{
        background-color:$peaCoolWhite;
        box-shadow: -1px 5px 7px #4e4e4e;
    }
    width:100%;
    &.container-with-tabs__mobile{
        header{
            nav{
                background-color: $peaGray;
                text-align: center;
                flex-direction:row;
                display: flex;
                a{
                    &.router-link-active{
                        background-color: $peaCoolWhite;
                        color:$peaBlank;
                        cursor: default;
                    }
                    color:#fff;
                    padding: 0.2em 0;
                    margin:0;
                    border-left:1px solid $peaCoolWhite;
                    &:nth-child(1){
                        border-left:none;
                    }
                    flex-grow:1;
                    height: auto;
                    width:auto;
                }
            }
        }
    }
    &.container-with-tabs__desktop{
        position: relative;
        header{
            nav{
                position: absolute;
                top:0;
                left:-43px;
                display: flex;
                flex-direction:column;
                a{
                    &.router-link-active{
                        background-image: url('/static/img/tabs/tabs__active.png');
                        color:#666;
                        z-index :1100 !important;
                        cursor: default;
                    }
                    &:first-child{
                        margin-top:0;
                    }
                    letter-spacing:3px;
                    color:#fff;
                    text-decoration: none;
                    display: block;
                    padding:19px 0 45px 11px;
                    margin-top:-32px;
                    width:56px;
                    background: url('/static/img/tabs/tabs.png') no-repeat;
                    background-size: 100% 100%;
                    border-bottom-left-radius: 80px 110px;
                    writing-mode:vertical-lr;
                    padding-top: 20px;
                    padding-bottom: 50px;
                }
            }
        }
        article{
            z-index :1000;
            position: relative;
        }
    }
}
</style>