<template>
    <div>
        <article-header title="个人简历" :description="headerDescription" />
        <profile-card :information="cardInfo">
            <radar-img
                title="Dominance (D), Influence (I), Steadiness (S), and Conscientiousness (C)."
                :radar-value="JobRadarInfo"
            ></radar-img>
        </profile-card>
        <block-collapsible lang="md" title="求职意向">
            Web前端应用设计开发、JavaScript应用开发。

            熟练掌握JavaScript及Vue生态使用，熟悉Node.js后台开发
        </block-collapsible>
        <block-collapsible lang="md" title="技术剖面" class="skill-profile">

            软件工程专业，自2014年8月开始独立自学Web开发技术。Javascript狂热爱好者！自学期间读完超过10本技术书籍！

            <radar-img :radar-value="SkillRadarInfo"></radar-img>

            - **扎实稳固**的HTML+CSS：<br />曾不依赖前端框架类库独自完成超过5k行代码的前端UI，不借助JS实现响应式兼容移动端。
            - **游刃有余**的JavaScript：<br />曾用原生JavaScript写过数千行的，拥有完整的事件模型、异步管理、数据绑定、健全的模块化设计。

            享受写原生Js时的快感，但也喜欢修改/使用现有轮子。读jQuery源码、编译BootStrap、配置webpack。

            熟练使用Vue.js全家桶，熟悉node.js生态。用Vue.js写过多个项目，并拥有较多的客户群体。

            用 npm script 打造超溜的前端工作流


            技术狂人，好读书，活跃于：

            - 个人博客：[jshao.org.cn](https://jshao.org.cn/)
            - Github：[github.com/jshao1993](https://github.com/jshao1993/)

        </block-collapsible>
        <block-justify title="工作">
            <block-justify-row lang="md" title="浙江省水利河口研究院（杭州定川信息技术有限公司）">
                2015.8 - 至今，Web前端

                ---

                - 负责前端规范制定
                - 负责引进新的技术
                - 负责前端技术的更新Jquery->Angularjs->VueJs->ReactJS
                - 负责各个框架通用组件和业务组件的封装
                - 开展各类培训会，紧跟技术潮流
                - 参与产品讨论，共同制定产品规范及功能
                - 工作认真，2-3天发布一篇[技术博客](http://jshao.org.cn/)

                ---

                离职原因：

                1. 环境太过悠闲，工作氛围、技术氛围不够浓厚
                1. 技术狂热爱好者，想迎接新的挑战
            </block-justify-row>
        </block-justify>
        <block-collapsible lang="md" title="自我评价" :folded="true" v-if="false">
            好胜心强，崇尚竞争。喜欢第一名的畅快淋漓，也不讨厌失败后的惨痛教训！

            富有童心，积极乐观。永远保持一颗好奇心不断向前，擅长融入新环境，交际虽略显笨拙，但却真实。
        </block-collapsible>
        <block-justify title="技能">
            <block-justify-row lang="md" title="HTML+CSS">
                扎实稳固的HTML(HTML5)+CSS(CSS3)基础，喜欢自己写原生的HTML+CSS实现与众不同的效果。

                熟练使用float与flex布局，能够使用原生HTML+CSS实现响应式，同时兼容电脑与手机访问。

                熟练使用Bootstrap前端框架、SCSS预处理、字体图标、雪碧图等常用前端技术。
            </block-justify-row>
            <block-justify-row lang="md" title="Java Script">
                游刃有余的JavaScript。

                熟悉ES5、ES6标准，掌握Js高级特性。可以原生Js实现异步状态管理、getter/setter实现动态数据绑定等。

                熟悉TypeScript，并应用于最新的Vue项目之中

                即使不使用jQuery也可以熟练操作DOM、BOM，读过jQuery源码。

                熟悉Vue.js生态，熟练使用Vue全家桶，理解MVVM数据驱动思想。
            </block-justify-row>
            <block-justify-row lang="md" title="Node.js">
                熟悉用Node.js，包括前端工具与Web后台部分，并将Node.js作为计算机日常维护脚本来使用。

                熟悉webpack，可以自己配置webpack多入口、热加载等。
            </block-justify-row>
            <block-justify-row lang="md" title="设计">
                具有基本的设计功底，了解基本的设计原则，研究过相关书籍。

                熟练使用Photoshop等设计工具。

                对于用户体验有比较深刻的理解，经常做出“看起来不是特别漂亮，但用起来却意外**舒服**”的产品。
            </block-justify-row>
            <block-justify-row lang="md" title="其他">
                - 了解算法与数据结构
                - 较不错的软件工程思想
                - 了解HTTP协议
                - 熟练使用Git、Github
                - 良好的演讲与活动组织能力
            </block-justify-row>
            <block-justify-row lang="md" title="读书">

                - 《JavaScript高级程序设计》
                - 《ECMAScript6 入门》
                - 《Web全栈工程师的自我修养》
                - 《你不知道的Javascript上（中）（下）》
                - 《Github入门与实践》
                - 《Javascript语言精粹》
                - 《Javascript忍者秘籍》
                - 《JavaScript设计模式与开发实践》
                - 《数据结构》
                - 《图解HTTP》
                - 《深入理解ES6》

            </block-justify-row>
        </block-justify>
        <block-justify title="项目">
            <block-justify-row lang="md" title="舟山市水质监测系统">
                2017年8月独立完成。

                - 精心的设计
                - 利用 Vue生态，设计大量原创UI组件
                - Vue.js生态实现SPA
                - 使用ES8 async/await 进行异步管理
                - 自行实现dispatch和broadcast派发与广播方法
                - 封装了具有数据数据校验功能的的表单组件
                - 封装了组合多选框组件（CheckboxGroup & Checkbox）
                - 封装了全局提示组件（$Alert）
                - 封装了树型组件
                - 完成了大概30个页面
                - 技术栈：ES6、Vue.js、Node.js

                因涉及源代码的知识产权，你可以[查看实例](http://web.dcyun.com:48255/)来查看项目。

                - 账号：admin
                - 密码：dcxx123456

            </block-justify-row>
            <block-justify-row lang="md" title="浙江省水利工程标准化运行管理平台">
                2017年5月配合多个后台人员协同完成。

                - 庞大的设计
                - 传统BootStrap+jQuery组合
                - 涉及页面100个多
                - 采用原生javascript开发多个小插件

                独立负责前端框架的搭建，各种方法的封装，已产品的模式进行开发，涉及使用的水利局单位多达上百个。

                因涉及源代码的知识产权，你可以[查看实例](http://bzh.dcyun.com:10000/)来查看项目。

                - 账号：admin_bf
                - 密码：dcxx123
            </block-justify-row>
            <block-justify-row lang="md" title="浙江省防汛防台系统">
                2016年10月协同多名成员共同完成，采用前后端分离。

                此项目是刚刚接触AngularJs的过渡项目

                - 良好的响应式设计
                - 不使用Node.js构建的SPA
                - 采用Angularjs和Bootstrap等第三方类库

                项目开发中担任Leader，主要负责全部框架搭建、通用及业务组件的封装、代码规范的制定及前端JavaScript工具库开发。

                [项目地址](http://jshao.org.cn/)
            </block-justify-row>
            <block-justify-row lang="md" title="省级山洪灾害监测预警系统">
                2016年3月和公司10多名成员共同完成，历时3个多月。

                - 庞大的设计
                - 传统BootStrap+jQuery组合

                负责其中4个大模块（水雨情监测、防汛值班、基础信息、后台管理）：

                - 完成了大概56个页面

                因涉及源代码的知识产权，你可以[查看实例](http://115.231.121.139:8080/ZSMFMWSYS/login.aspx)来查看项目。

                - 账号：admin
                - 密码：zsfb2002
            </block-justify-row>
            <block-justify-row lang="md" title="水库安全巡查管理平台">
                2015年9月带领公司另2名后台成员完成。

                - 健全的模型与设计
                - 整站Ajax通信
                - 没有用媒体查询兼容移动端访问
                - 采用Jquery第三方类库框架
                - 超过10000行代码

                项目开发中担任Leader，主要负责全部网站设计及前端JavaScript工具库开发。

                因涉及源代码的知识产权，你可以[查看实例](http://dcxc.org.cn/login)来查看项目。

                - 账号：dsadmin
                - 密码：dsadmin
            </block-justify-row>
        </block-justify>

        <!-- <block-collapsible lang="md" title="其他链接" class="other-link po-print-hidden">

            - [花生PeA in Github](https://github.com/pea3nut)
            - [花生PeAの博客](http://blog.pea3nut.com)
            - [花生PeA in 掘金](https://juejin.im/user/58fed8a7a22b9d0065b13e30)

        </block-collapsible> -->
    </div>
</template>

<script>
import {formatDate} from 'pea-scripts/dist/function.browser.js';
export default {
    extends :require('@/components/abstract/page.vue'),
    name :'page-job',
    data(){return{
    }},
    computed:{
        cardInfo(){
            var reArr =[{
                label:'姓名',
                text:'张浩',
            },{
                label:'性别',
                text:`男`,
            },{
                label:'年龄',
                text:`${this.getPeA3nutAge()}（1993.8出生）`,
            },{
                label:'户口',
                text:'浙江省 金华市',
                print:false,
            },{
                label:'毕业院校',
                text:'杭州师范大学（2011-2015）',
            },{
                label:'所学专业',
                text:'软件工程（学士）',
            },{
                label:'婚姻状况',
                text:this.Info['marriage'],
                print:false,
            },{
                label:'政治面貌',
                text:'共青团员',
                print:false,
            },{
                label:'微信',
                text:'15868807953',
            },{
                label:'E-mail',
                text:'411371012[at]qq.com',
            },{
                label:'希望地区',
                text:'杭州',
                print:false,
            },{
                label:'现状态',
                text:this.Info['now_state_job'],
                print:false,
            }];
            return reArr;
        },
        headerDescription(){
            return[{
                label:'下载',
                text:`
                    <a href="/static/resource/resume/pea3nut-web-resume.pdf" target="_blank">正常版</a>
                    /
                    <a href="/static/resource/resume/pea3nut-web-image-resume.png" target="_blank">单页图片版</a>
                `,
            },{
                label :'最后更新',
                text :formatDate(this.LastUpdateTime,{hasTime:false,fillZeroOfDate:true}),
            }];
        },
    },
};
</script>