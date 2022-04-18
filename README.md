# flowable ui

+ Flowable IDM: 身份管理应用。为所有Flowable UI应用提供单点登录认证功能，并且为拥有IDM管理员权限的用户提供了管理用户、组与权限的功能
+ Flowable Modeler: 让具有建模权限的用户可以创建流程模型、表单、选择表与应用定义
+ Flowable Task: 运行时任务应用。提供了启动流程实例、编辑任务表单、完成任务，以及查询流程实例与任务的功能
+ Flowable Admin: 管理应用。让具有管理员权限的用户可以查询BPMN、DMN、Form及Content引擎，并提供了许多选项用于修改流程实例、任务、作业等。管理应用通过REST API连接至引擎，并与Flowable Task应用及Flowable REST应用一同部署


+ 自动创建表
  + mysql的连接字符串中添加上nullCatalogMeansCurrent=true，将schema默认设置为当前连接的schema。

+ Flowable集成mysql启动时报错 java.time.LocalDateTime cannot be cast to java.lang.String
  + 由于mysql依赖版本过高
  ```
  In version <= 8.0.22 --> it's ok
  in version == 8.0.23 --> ClassCastException: class java.time.LocalDateTime cannot be cast to class java.lang.String
  <dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.18</version>
  </dependency>
  ```
  

+ [参考引用1](https://github.com/leelance/spring-howto/tree/dev/flowable/flowable-ui-67)
+ [参考引用2](https://blog.csdn.net/li6151770/article/details/123782678)