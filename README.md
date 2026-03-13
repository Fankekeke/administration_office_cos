### 基于SpringBoot + Vue的学校行政办公管理系统.

智慧校园管理、智慧办公、学校协同办公。

###### 管理员：
学校管理、待办任务、考勤记录、会议记录、部门管理、共享文档、财务申请、留言列表、请假申请、消息信息、用户通知、岗位管理、员工管理。

###### 学校：
学校信息、员工待办、考勤记录、会议记录、部门管理、文件管理、财务审核、留言记录、请假审核、消息记录、员工通知、岗位管理、员工管理、财务支付。

###### 员工：
我的考勤、我的任务、会议记录、共享文件、财务申请、留言发布、请假申请、员工沟通、我的消息。

##### 组织架构与人事基础
###### 学校/部门管理： 建立多层级校组织架构，规范部门划分，为行政审批提供底层权限支撑。

###### 员工/岗位管理： 维护教职工全量档案，明确岗位职责，支撑学校人力资源的精细化调配。

###### 学校信息/通知： 统一发布校级官方资讯与公告，确保行政指令及时传递给全体教职工。

##### 行政协同与日常办公
###### 待办任务/沟通： 系统自动推送工作待办，支持员工间在线沟通，提升跨部门协同效率。

###### 会议记录： 实现会议全过程数字化，在线保存纪要与决策，沉淀学校行政办公智库。

###### 共享文档/文件： 建设校内资源共享中心，支持各类行政文件的分级存储、下发与调阅。

##### 考勤与考评体系
###### 考勤记录/我的： 实时同步员工出勤、迟到等数据，为行政管理提供客观的绩效考核依据。

###### 留言发布/记录： 提供校内民主反馈渠道，支持意见建议的在线提交与回复，优化校园环境。

##### 审批流与财务管控
###### 请假申请/审核： 规范请假流程，支持员工在线提交申请、主管实时审批，自动同步考勤。

###### 财务申请/审核： 数字化处理经费报销与资源申领，强化财务管控，确保账目流向清晰可查。

###### 财务支付： 管理端直接对接支付环节，实现在线打款与流水存档，提升财务处理效率。

##### 信息交互与消息提醒
###### 消息信息/记录： 聚合系统提醒与通知历史，确保审批进度、任务变更等关键节点不遗漏。

#### 安装环境

JAVA 环境 

Node.js环境 [https://nodejs.org/en/] 选择14.17

Yarn 打开cmd， 输入npm install -g yarn !!!必须安装完毕nodejs

Mysql 数据库 [https://blog.csdn.net/qq_40303031/article/details/88935262] 一定要把账户和密码记住

redis

Idea 编译器 [https://blog.csdn.net/weixin_44505194/article/details/104452880]

WebStorm OR VScode 编译器 [https://www.jianshu.com/p/d63b5bae9dff]

#### 采用技术及功能

后端：SpringBoot、MybatisPlus、MySQL、Redis、
前端：Vue、Apex、Antd、Axios

平台前端：vue(框架) + vuex(全局缓存) + rue-router(路由) + axios(请求插件) + apex(图表)  + antd-ui(ui组件)

平台后台：springboot(框架) + redis(缓存中间件) + shiro(权限中间件) + mybatisplus(orm) + restful风格接口 + mysql(数据库)

开发环境：windows10 or windows7 ， vscode or webstorm ， idea + lambok


#### 前台启动方式
安装所需文件 yarn install 
运行 yarn run dev

#### 默认后台账户密码
[管理员]
admin
1234qwer

#### 项目截图
暂无

|  |  |
|---------------------|---------------------|
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/76e07b26-a48b-451f-98bd-7ec68fc6ce0f.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/c6924690-3dea-4947-9d10-6fa617c4bcc3.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/23e4629a-c098-409c-94b2-37ed2c1f51e1.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/c0cafb24-72d5-450c-86cc-8e156de89f49.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/8fd99501-30b0-4607-b7a8-9848d5ae0c1f.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/bcba2d4d-262f-4df2-97ba-4a71d4bd6072.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/8d425260-04af-4758-a2b8-bf021cb8dd73.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/b9014664-eb00-418d-a52b-cd94e4cbf0a9.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/1ec4eda8-dee4-40da-8c70-0a4399681aa8.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/b63ff514-d56d-417b-8dd4-8eefc88a27c9.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/0cd74bef-750a-49da-99ae-1a26f9b18f88.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/b8dd7e23-b9ca-409b-a6fb-1022a2a270a2.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/ff0b3bc7-3c7f-43bb-a8cb-300413ca3503.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/19568e7c-b11c-4dff-91c2-a5050213be7f.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/f952258e-6d6d-49f5-a83c-9992d0d26874.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/4658cd17-a190-4b2e-aaf7-154cb684192f.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/f497daa0-4f7c-4607-ab8f-d501dc6d6983.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/612afdf9-7095-4563-8c11-58beaddd9618.png) |
| ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/f06fb988-f596-4db3-aa98-329ac957898d.png) | ![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/98a21ff8-f48a-4cc3-ae99-1063d1a4e5be.png) |

![](https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/work/936e9baf53eb9a217af4f89c616dc19.png)


#### 演示视频

暂无

#### 获取方式

Email: fan1ke2ke@gmail.com

WeChat: `Storm_Berserker`

`附带部署与讲解服务，因为要恰饭资源非免费，伸手党勿扰，谢谢理解😭`

> 1.项目纯原创，不做二手贩子 2.一次购买终身有效 3.项目讲解持续到答辩结束 4.非常负责的答辩指导 5.**黑奴价格**

> 项目部署调试不好包退！功能逻辑没讲明白包退！

#### 其它资源

[2025年-答辩顺利通过-客户评价🍜](https://berserker287.github.io/2025/06/18/2025%E5%B9%B4%E7%AD%94%E8%BE%A9%E9%A1%BA%E5%88%A9%E9%80%9A%E8%BF%87/)

[2024年-答辩顺利通过-客户评价👻](https://berserker287.github.io/2024/06/06/2024%E5%B9%B4%E7%AD%94%E8%BE%A9%E9%A1%BA%E5%88%A9%E9%80%9A%E8%BF%87/)

[2023年-答辩顺利通过-客户评价🐢](https://berserker287.github.io/2023/06/14/2023%E5%B9%B4%E7%AD%94%E8%BE%A9%E9%A1%BA%E5%88%A9%E9%80%9A%E8%BF%87/)

[2022年-答辩通过率100%-客户评价🐣](https://berserker287.github.io/2022/05/25/%E9%A1%B9%E7%9B%AE%E4%BA%A4%E6%98%93%E8%AE%B0%E5%BD%95/)

[毕业答辩导师提问的高频问题](https://berserker287.github.io/2023/06/13/%E6%AF%95%E4%B8%9A%E7%AD%94%E8%BE%A9%E5%AF%BC%E5%B8%88%E6%8F%90%E9%97%AE%E7%9A%84%E9%AB%98%E9%A2%91%E9%97%AE%E9%A2%98/)

[50个高频答辩问题-技术篇](https://berserker287.github.io/2023/06/13/50%E4%B8%AA%E9%AB%98%E9%A2%91%E7%AD%94%E8%BE%A9%E9%97%AE%E9%A2%98-%E6%8A%80%E6%9C%AF%E7%AF%87/)

[计算机毕设答辩时都会问到哪些问题？](https://www.zhihu.com/question/31020988)

[计算机专业毕业答辩小tips](https://zhuanlan.zhihu.com/p/145911029)

#### 接JAVAWEB毕设，纯原创，价格公道，诚信第一

`网站建设、小程序、H5、APP、各种系统 选题+开题报告+任务书+程序定制+安装调试+项目讲解+论文+答辩PPT`

More info: [悲伤的橘子树](https://berserker287.github.io/)

<p><img align="center" src="https://fank-bucket-oss.oss-cn-beijing.aliyuncs.com/img/%E5%90%88%E4%BD%9C%E7%89%A9%E6%96%99%E6%A0%B7%E5%BC%8F%20(3).png" alt="fankekeke" /></p>
