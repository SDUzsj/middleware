# SSM相关

## 背景介绍

      SSM框架，是Spring + Spring MVC + MyBatis的缩写，Spring依赖注入DI来管理各层的组件，使用面向切面编程AOP管理事物、日志、权限等。SpringMVC代表了Model(模型)View(视图)Controller(控制)接收外部请求,进行分发和处理。Mybatis是基于jdbc的框架,主要用来操作数据库,并且将业务实体和数据表联系起来。

## 知识剖析

### SSM整合思路

spring在进行管理时，是很有条理的，每个层都由spring管理，然后不同的层可以调用其它层，Handler调用service，service调用mapper等。

1整合dao层。mybatis和spring整合，通过spring管理mapper接口。使用mapper的扫描器自动扫描mapper接口在spring中进行注册。

2整合service层。通过spring管理 service接口。使用配置方式将service接口配置在spring配置文件中。实现事务控制。

3整合springmvc。由于springmvc是spring的模块，不需要整合。

### Spring

Spring是一个开源框架，它由Rod Johnson创建。它是为了解决企业应用开发的复杂性而创建的。

 Spring使用基本的JavaBean来完成以前只可能由EJB完成的事情。
 
 然而，Spring的用途不仅限于服务器端的开发。从简单性、可测试性和松耦合的角度而言，任何Java应用都可以从Spring中受益。
 
 目的：解决企业应用开发的复杂性
 
 功能：使用基本的JavaBean代替EJB，并提供了更多的企业应用功能
 
 范围：任何Java应用

### SpringMVC流程：
服务器发送Http request请求，请求被前端控制器（DispatcherServlet）捕获。
前端控制器根据xml文件中的配置（或者注解）对请求的URL进行解析，得到请求资源标识符（URI）。然后根据该URI，调用处理器映射器（HandlerMapping）获得处理该请求的Handler以及Handler对应的拦截器，最后以 HandlerExecutionChain 对象的形式返回。前端控制器根据获得的Handler，选择一个合适的处理器适配器（HandlerAdapter）去执行该Handler。处理器适配器提取request中的模型数据，填充Handler入参，执行处理器（Handler）（也称之为Controller）。Handler(Controller)执行完成后，向处理器适配器返回一个ModelAndView对象，处理器适配器再向前端控制器返回该ModelAndView对象（ModelAndView只是一个逻辑视图）。
根据返回的ModelAndView，前端控制器请求一个适合的视图解析器（ViewResolver）（必须是已经注册到Spring容器中的ViewResolver）去进行视图解析，然后视图解析器向前端控制器返回一个真正的视图View（jsp）。

前端控制器通过Model解析出ModelAndView中的参数进行解析，最终展现出完整的View并通过Http response返回给客户端。

### MyBaits
#### Mybatis是什么?

    Mybatis是一个支持普通SQL查询,存储过程和高级映射的优秀持久层框架.


#### 为什么用Mybits?

        Mybatis去掉几乎所有JDBC代码和参数的手工设置以及对结果集的检索封装.Mybatis可以使用简单的XML或者注解进行配置和原始映射,以将接口和Java的POJO映射成数据库中的记录


#### MyBaits有什么特点?

1.MyBaits作为持久层,其主要思想是将程序中的大量SQL语句剥离出来,配置在配置文件中,以实现SQL的灵活配置

在主流的ORM中,无论是Hibernate还是JPA,都对数据库结构提供了较为完整的封装,提供了从POJO到数据库表的全套映射机制.程序员往往只要定义好POJO到数据库表的映射关系,即可以通过HIbernate或者JPA提供的方法完成持久化操作,自动生成对应的SQL并调用JDBC接口加以执行


