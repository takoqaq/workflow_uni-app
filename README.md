### 使用uniapp创建一个多端的workflow App

#### 项目说明

开发一个简单的基于安卓移动平台的工作流系统。

##### 客户端要求

* 需要进行登录，才能使用系统。
* 能查询和自己相关工作流。（比如有请假、报销等多个工作流）
* 能基于某个流程发起一个新的操作。（比如开始提交请假，报销动作）
* 能查看自己手头的工作当前的状态。（比如可以查到当前的请假已经到了第二层审批）
* 对于需要自己审批的步骤，能推送到自己手机上。（比如下属提交请假申请后，主管能在手机上看到系统推送的，需要自己审批的提醒信息）【推送功能未完成】

##### 服务端要求 【未上传】

* 需要管理用户的数据。（比如管理登录名，密码，Email，手机等信息，以及员工所属的部门等。）

*  能独立定义工作流的各个操作。（比如可以单独定义审批，审核等步骤。）

* 能定义工作流中的每个状态。（比如可以单独定义已批准，已审核等状态。）

* 利用上面定义的操作和状态，能把多个操作和状态灵活串成不同的流。比如当前定义请假为3个步骤，报销为4个步骤。以后由于制度调整，可以把请假修改为N个步骤也可以。

* 能够管理每个工作流相关的数据。（比如查看到请假流里面，已经有N条请假，并可以查看这N条请假当前的状态）

* 在每次流的状态有变化时，应该将提醒信息推送到下一个操作的人员手中。（比如员工的请假，需要推送提醒信息给主管。）

#### 项目技术

项目基于uni-app进行多端开发，搭配uView框架进行建设。

#### 项目运行

`npm run dev:%PLATFORM% `

`npm run build:%PLATFORM%`

`%PLATFORM%` 取值如下：

| 值                      | 平台                                                         |
| ----------------------- | ------------------------------------------------------------ |
| app-plus                | app平台生成打包资源（仅支持npm run build:app-plus，也就是App平台运行调试不支持cli方式，需在HBuilderX中运行调试） |
| h5                      | H5                                                           |
| mp-alipay               | 支付宝小程序                                                 |
| mp-baidu                | 百度小程序                                                   |
| mp-weixin               | 微信小程序                                                   |
| mp-toutiao              | 字节跳动小程序                                               |
| mp-qq                   | qq 小程序                                                    |
| mp-360                  | 360 小程序                                                   |
| quickapp-webview        | 快应用通用                                                   |
| quickapp-webview-union  | 快应用联盟                                                   |
| quickapp-webview-huawei | 快应用华为                                                   |