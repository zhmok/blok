
# 规范描述


以下是个人理解

### **POJO**
>Plain Ordinary Java Object  简单的无规则的对象   
>纯粹的 java 对象. 只有属性字段及 setter 和 getter 方法  
>属于统称

### **PO**
>Persistant Object 持久对象  
>主要由ORM(对象关系映射)概念衍生  
>与数据库表结构一一对应  
>用于表示 一个对象 对应(映射) 数据库表对应的一条记录  
>我们使用工具生成的那些实体类属于 PO

### **DAO**
>Data Access Object 数据访问对象  
>为业务层提供接口. 用于访问数据库. 通常和 PO 结合使用

### **BO**
>Business Object 业务对象
>我们定义的Service 都属于一个业务对象



### **VO** 
>View Object 视图对象  
>主要用于展示层  
>
>Value Object 值对象
>使用非常广泛  
>
>借鉴 alipay sdk中的请求和相应
>请求/响应使用  xxxRequest xxxResponse 来命名


### **DO**
>Domain Object 领域对象  
>由领域驱动设计衍生 这个概念比较模糊  
>举个例子  
>我有一个类 UserDO 表示一个领域对象 一个UserService 表示用户业务对象  
>这时候 查询用户列表 应该是属于用户业务里的一项操作  
>但是一些属于用户的操作 虽然也属于用户的业务 但是应该被放在 UserDO里面  
>如: 用户的查询操作. 无论查看什么信息 都应该被抽象成用户的动作  
>用户的购买操作. 无论购买什么东西 都应该被抽象成用户的动作  
>有时候一个领域对象也可以作为一个业务对象

---
### **DTO**
>Data Transfer Object 数据传输对象

### **AO**
>Application Object 应用对象
>Action Object 活动对象

### **Query**
>数据查询对象 各层接收上层的查询请求. 
>注意超过2个参数的查询必须封装 禁止使用Map类或者 Object 来传输






## 命名规约
>数据对象:xxxDO        xxx即为数据表名
>数据传输对象:xxxDTO   xxx为业务领域相关的名称
>展示对象:xxxVO.       xxx一般为网页名称
>POJO是DO/DTO/BO/VO的统称 .禁止命名成xxxPOJO

>POJO、TO、AO 一般不会使用



