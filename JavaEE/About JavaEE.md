#关于JavaEE

##作为程序员，为什么选择 Java

想必有很多初学者不知选择什么语言入门。在尝试了 C、C++、C#、Python、PHP 后，决定把 Java作 为第一门深入学习的编程语言。这个路着实有点长…

不过放心，你可以大胆地选择 Java。如果说 C++ 是编程界的曹操，那 Java 就是司马懿，近三十年踏惊涛骇浪如履平地，熬死了无数对手。

诞生之初，Java 饱受争议。而如今，那些受到攻击的弱点一个个被解决甚至反超对手。人们开始惊叹 Java 的生命力，长期以来，Java雄踞编程语言排行榜首位，拥有最多的受众、最大的市场、最活跃的社区。

TIOBE 编程语言排行榜：https://www.tiobe.com/tiobe-index/

最近有一则消息，JDK 11中将会引入新的GC（Garbage Collection，垃圾回收）算法 ZGC，能够处理 TB 级别的 HEAP GC，GC 停顿时间不超过10s，意味着，几乎所有的民用场合，都可以用Java来写了，而且可以随心所欲地造对象，不用像以前一样小心翼翼了。

当然，每个时期都有冉冉升起的新星。现在 Python 如日中天，Go 野心勃勃，选择Java 的你，可以选择看热闹了。

##关于JavaEE

###JavaEE 概念

Java EE，Java 平台企业版（Java Platform Enterprise Edition），之前称为Java 2 Platform, Enterprise Edition (J2EE)，2018年3月更名为 Jakarta EE(这个名称应该还没有得到群众认可)。是 Sun 公司为企业级应用推出的标准平台，用来开发B/S架构软件。Java EE 可以说是一个框架，也可以说是一种规范。

JavaEE 是 Java 应用最广泛的部分。

###JavaEE 与 JavaSE 的区别与联系

JavaEE 是在 JavaSE 的基础上构建的，是对 JavaSE 的扩展，增加了一些更加便捷的应用框架。

除了 EE 和 SE，还有为移动端而生的 JavaME，但目前应用不算广泛。三者的关系可以用下图概括：

![](/picture/16.png)

###JavaEE主要技术

JavaEE 号称有十三种核心技术。它们分别是：JDBC、JNDI、EJB、RMI、Servlet、JSP、XML、JMS、Java IDL、JTS、JTA、JavaMail和JAF。

简单介绍下需要重点关注的技术。

###JDBC

Java 数据库连接，（Java Database Connectivity，JDBC）是 Java 语言中用来规范客户端程序如何来访问数据库的应用程序接口，提供了诸如查询和更新数据库中数据的方法。
JNDI

Java 命名和目录接口（Java Naming and Directory Interface，JNDI），是 Java 的一个目录服务应用程序界面（API），它提供一个目录系统，并将服务名称与对象关联起来，从而使得开发人员在开发过程中可以使用名称来访问对象。
EJB

企业级 JavaBean（Enterprise JavaBean, EJB）是一个用来构筑企业级应用的服务器端可被管理组件。

###Servlet

Servlet（Server Applet），是用 Java 编写的服务器端程序。其主要功能在于交互式地浏览和修改数据，生成动态 Web 内容。

狭义的 Servlet 是指 Java 语言实现的一个接口，广义的 Servlet 是指任何实现了这个 Servlet 接口的类，一般情况下，人们将 Servlet 理解为后者。
JSP

###JSP（全称JavaServer Pages）

是由 Sun 公司主导创建的一种动态网页技术标准。JSP 部署于网络服务器上，可以响应客户端发送的请求，并根据请求内容动态地生成 HTML、XML 或其他格式文档的 Web 网页，然后返回给请求者。

###JavaEE框架

JavaEE 拥有广泛市场的原因之一就是可以使用多种框架来使开发变得简单。对于框架的选择多种多样，目前比较常见的框架组合有 SSH和SSM。在后面的章节中会作详细介绍。另外Spring本身也提供了多种层次的框架供选择，可以到Spring官网了解详情。

Spring： https://spring.io/

###SSH

Structs + Spring + Hibernate

###SSM

Spring +SpringMVC + MyBatis
