### 1、OA项目中EmployeesQuestion类是做什么用的，对应的表名及结构是什么

<问题描述>
OA项目中EmployeesQuestion类是做什么用的，对用的表名及结构是什么
</问题描述>

<回答>
EmployeesQuestion 类是员工问题表类，对应类名：com.bean.EmployeesQuestion.java，此处描述自己输入，EmployeesQuestion类对应的表名为：employeesQuestion；
具体字段有（类字段名、中文名、数据库表字段名、字段类型）：
    

    questionSubject、问题主题目、questionSubject、String；    
    
    additionalNotes、问题补充说明、additionalNotes、String；    
    
    questionPictures、问题图片、questionPictures、String；    
    
    questionsAnswered、问题回答、questionsAnswered、String；    
    
    answerAttachment、问题回答附件、answerAttachment、String；    
    
    displayRange、问题显示范围，对应com.data.ENUM.类、displayRange、enum；    
    
    questionClassificationId、问题分类ID、questionClassificationId、Integer；    
    
    questionTime、提问时间、questionTime、Date；    
    
    answerTime、回答时间、answerTime、Date；    
    
    questioner、提问者ID、questioner、String；    
    
    answerer、回答者ID、answerer、String；    
    
    automaticReply、是否为自动回复，对应com.data.ENUM.类、automaticReply、enum；    
    
    createdTime、创建时间、createdTime、Date；
    
    modifiedTime、修改时间、modifiedTime、Date；
    
    modifiedCount、修改次数、modifiedCount、String； 
    
    status、状态，对应com.data.ENUM.EnumBaseStatus类、status、enum；

</回答>

### 2、OA项目中员工问题表是如何增加或申请

<问题描述>
OA项目中员工问题表是如何增加的
</问题描述>

<回答>
业务层：
先登录OA前台
路径：财务专区 --> 工作流管理 --> 起草申请 --> 员工问题表申请

新增接口： /employeesQuestion/add.mvc
新增方法： com.web.controller.WebEmployeesQuestionController.add
新增页面: /WEB-INF/jsp/employeesQuestion/employeesQuestionadd.jsp

保存接口： /employeesQuestion/addProcessOK.mvc
保存方法： com.web.controller.WebEmployeesQuestionController.addProcessOK


管理员层：
先登录OA后台
路径：人事行政 --> xxxxx --> 增加员工问题表
路径：工资管理 --> xxxxx --> 增加员工问题表
路径：成本统计 --> xxxxx --> 增加员工问题表
路径：项目协议 --> xxxxx --> 增加员工问题表
路径：到款发票 --> xxxxx --> 增加员工问题表
路径：系统设置 --> xxxxx --> 增加员工问题表

新增接口： /manage/employeesQuestion/add.mvc
新增方法： com.web.controller.manage.EmployeesQuestionController.add
新增页面: /manage/employeesQuestion/employeesQuestionadd.jsp

保存接口： /manage/employeesQuestion/addOK.mvc
保存方法： com.web.controller.manage.EmployeesQuestionController.addOK

</回答>


### 3、OA项目中员工问题表如何查询

<问题描述>
OA项目中员工问题表如何查询
</问题描述>

<回答>
业务层：
先登录OA前台
路径：工作流管理 --> 员工问题表列表

列表接口： /employeesQuestion/list.mvc
列表方法： com.web.controller.WebEmployeesQuestionController.list
列表页面: /WEB-INF/jsp/employeesQuestion/employeesQuestionlist.jsp


筛选条件：                                                


列表页功能：导出excel、查看、编辑


管理员层：
先登录OA后台
路径：人事行政 --> xxxxx --> 员工问题表列表
路径：工资管理 --> xxxxx --> 员工问题表列表
路径：成本统计 --> xxxxx --> 员工问题表列表
路径：项目协议 --> xxxxx --> 员工问题表列表
路径：到款发票 --> xxxxx --> 员工问题表列表
路径：系统设置 --> xxxxx --> 员工问题表列表

列表接口： /manage/employeesQuestion/list.mvc
列表方法： com.web.controller.manage.EmployeesQuestionController.list
列表页面: /manage/employeesQuestion/employeesQuestionlist.jsp


筛选条件：                                                

列表页功能：导出excel、查看、编辑


</回答>

### 4、OA项目如何导出员工问题表信息

<问题描述>
OA项目如何导出员工问题表信息
</问题描述>
<回答>
业务层：
先登录OA前台
路径：工作流管理 --> 人事类 --> 员工问题表（申请）列表 --> 导出
路径：工作流管理 --> 财务类 --> 员工问题表（申请）列表 --> 导出
路径：工作流管理 --> 业务类 --> 员工问题表（申请）列表 --> 导出
路径：工作流管理 --> 行政类 --> 员工问题表（申请）列表 --> 导出

接口：/employeesQuestion/list.mvc
方法：com.web.controller.WebEmployeesQuestionController.list
页面: /WEB-INF/jsp/employeesQuestion/employeesQuestionList.jsp
页面方法：download()

接口：/employeesQuestion/download.mvc
方法：com.web.action.WebEmployeesQuestionAction.download
方法：com.web.controller.web.WebEmployeesQuestionController.download

其中导出信息包含：
    问题主题目：questionSubject
    问题补充说明：additionalNotes
    问题图片：questionPictures
    问题回答：questionsAnswered
    问题回答附件：answerAttachment
    问题显示范围：displayRange
    问题分类ID：questionClassificationId
    提问时间：questionTime
    回答时间：answerTime
    提问者ID：questioner
    回答者ID：answerer
    是否为自动回复：automaticReply


管理员层：
先登录OA后台
路径：人事行政 --> xxxxx --> 员工问题表（申请）列表 --> 导出
路径：工资管理 --> xxxxx --> 员工问题表（申请）列表 --> 导出
路径：成本统计 --> xxxxx --> 员工问题表（申请）列表 --> 导出
路径：项目协议 --> xxxxx --> 员工问题表（申请）列表 --> 导出
路径：到款发票 --> xxxxx --> 员工问题表（申请）列表 --> 导出
路径：系统设置 --> xxxxx --> 员工问题表（申请）列表 --> 导出

接口： /manage/employeesQuestion/list.mvc
方法： com.web.controller.manage.EmployeesQuestionController.list
页面: /manage/employeesQuestion/employeesQuestionList.jsp
页面导出方法：download()

接口：/manage/employeesQuestion/download.mvc
方法：com.web.controller.manage.EmployeesQuestionController.download

其中导出信息包含：
    问题主题目：questionSubject
    问题补充说明：additionalNotes
    问题图片：questionPictures
    问题回答：questionsAnswered
    问题回答附件：answerAttachment
    问题显示范围：displayRange
    问题分类ID：questionClassificationId
    提问时间：questionTime
    回答时间：answerTime
    提问者ID：questioner
    回答者ID：answerer
    是否为自动回复：automaticReply

</回答>

### 5、OA项目如何查看员工问题表信息

<问题描述>
OA项目如何查看员工问题表信息
</问题描述>
<回答>
业务层：
先登录OA前台
路径：工作流管理 --> 人事类 --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：工作流管理 --> 财务类 --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：工作流管理 --> 业务类 --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：工作流管理 --> 行政类 --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮

接口：/employeesQuestion/modi.mvc
方法：com.web.controller.WebEmployeesQuestionController.modi
接口：/employeesQuestion/modiProcess.mvc
方法：com.web.controller.WebEmployeesQuestionController.modiProcess
页面: /WEB-INF/jsp/employeesQuestion/employeesQuestionModi.jsp


管理员层：
先登录OA后台
路径：人事行政 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：工资管理 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：成本统计 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：项目协议 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：到款发票 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：系统设置 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮

接口： /manage/employeesQuestion/modi.mvc
方法： com.web.controller.manage.EmployeesQuestionController.modi
页面: /manage/employeesQuestion/employeesQuestionModi.jsp



</回答>

### 6、OA项目如何修改员工问题表信息

<问题描述>
OA项目如何修改员工问题表信息
</问题描述>
<回答>
业务层：
先登录OA前台
注： 工作流申请相关的实体类只有在修订状态可以修改，在执行 modiProcessOK 方法后重新发起申请。
路径：工作流管理 --> 人事类 --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：工作流管理 --> 财务类 --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：工作流管理 --> 业务类 --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：工作流管理 --> 行政类 --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮

接口：/employeesQuestion/modiOK.mvc
方法：com.web.controller.WebEmployeesQuestionController.modiOK
接口：/employeesQuestion/modiProcessOK.mvc
方法：com.web.controller.WebEmployeesQuestionController.modiProcessOK
页面: /WEB-INF/jsp/employeesQuestion/employeesQuestionModi.jsp


管理员层：
先登录OA后台
路径：人事行政 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：工资管理 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：成本统计 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：项目协议 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：到款发票 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮
路径：系统设置 --> xxxxx --> 员工问题表（申请）列表 --> 点击“编辑（查看）”按钮

接口：/manage/employeesQuestion/modiOK.mvc
方法：com.web.controller.manage.EmployeesQuestionController.modiOK
页面: /manage/employeesQuestion/employeesQuestionModi.jsp



</回答>

### 7、OA项目如何终止员工问题表申请流程

<问题描述>
OA项目如何终止员工问题表申请流程
</问题描述>
<回答>
业务层：
先登录OA前台
注： 工作流申请相关的实体类只有在修订状态、申请中可以终止。
路径：财务专区 --> 工作流管理 --> 我的申请（工作流引擎 --> 点击“终止流程”按钮

接口：/process/stopProcess.mvc?taskId=
方法：com.web.controller.web.WebProcessController.stopProcess
页面: WEB-INF/jsp/process/applyList.jsp

回调实现：com.util.ibipower.process.callback.fun.EmployeesQuestionProcessStrategy

</回答>
