如何新增描述文档模板：

### 1. OA项目中XXXXX是如何增加或申请

<问题描述>

OA项目中XXXXX是如何增加或申请

</问题描述>

<回答>

业务层：

先登录OA前台

新增XXX

新增接口：/xxx/add.mvc

新增方法：包路径.类名.方法名

保存接口：/xxx/addOK.mvc

保存方法：包路径.类名.方法名

新增页面：/WEB-INF/jsp/xxx/xxx.jsp

管理员层：

先登录OA后台

新增接口：/manage/xxx/add.mvc

新增方法：包路径.类名.方法名

保存接口：/manage/xxx/addOK.mvc

保存方法：包路径.类名.方法名

新增页面：/xxx/xxx.jsp

</回答>

### 2. OA项目中XXXX类是做什么用的，对应的表名及结构是什么

<问题描述>

OA项目中XXXX类是做什么用的，对应的表名及结构是什么

</问题描述>

<回答>

XXXXX类是XXXX类，对应类名：com.bean.XXXX.java，用于XXXXX，XXXXX类对应的表名为：xxxxxx；

具体字段有（类字段名、中文名、数据库表字段名、字段类型）：

示例：

supplierContactApplyId、主键ID、supplierContactApplyId、Integer；

status、状态、status、包路径.对应枚举  enum；

applyPerson、申请人、person_id、对应 包路径.对应类名；

</回答>

### 3. 描述一下当前页面的筛选条件
必须按照如下格式： xxxx(xxxx)、xxxx(xxxxx)
### 4. 描述一下当前列表页面中有哪些操作  必须按照格式 ： xxxx 、xxx
