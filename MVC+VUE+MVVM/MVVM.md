#MVVM

前言

在介绍MVVM框架之前，先给大家简单介绍一下MVC、MVP框架（由于本博文主要讲解MVVM，所以MVC和MVP将简化介绍，如果需要我将在以后的博文中补充进来）。

MVC框架：

![](/picture/9.png)

    M-Model : 业务逻辑和实体模型(biz/bean)
    V-View : 布局文件(XML)
    C-Controller : 控制器(Activity)

相信大家都熟悉这个框架，这个也是初学者最常用的框架，该框架虽然也是把代码逻辑和UI层分离，但是View层能做的事情还是很少的，很多对于页面的呈现还是交由C实现，这样会导致项目中C的代码臃肿，如果项目小，代码臃肿点还是能接受的，但是随着项目的不断迭代，代码量的增加，你就会没办法忍受该框架开发的项目，这时MVP框架就应运而生。

MVP框架：

![](/picture/10.png)

    M-Model : 业务逻辑和实体模型(biz/bean)
    V-View : 布局文件(XML)和Activity
    P-Presenter : 完成View和Model的交互

MVP框架相对于MVC框架做了较大的改变，将Activity当做View使用，代替MVC框架中的C的是P，对比MVC和MVP的模型图可以发现变化最大的是View层和Model层不在直接通信，所有交互的工作都交由Presenter层来解决。既然两者都通过Presenter来通信，为了复用和可拓展性，MVP框架基于接口设计的理念大家自然就可以理解其用意。

但MVP框架也有不足之处:

1.接口过多，一定程度影响了编码效率。

2.业务逻辑抽象到Presenter中，较为复杂的界面Activity代码量依然会很多。

3.导致Presenter的代码量过大。

MVVM框架：

![](/picture/11.png)

    M-Model : 实体模型(biz/bean)
    V-View : 布局文件(XML)
    VM-ViewModel : DataBinding所在之处，对外暴露出公共属性，View和Model的绑定器

对比MVP和MVVM模型图可以看出，他们之间区别主要体现在以下两点：

1.    可重用性。你可以把一些视图逻辑放在一个ViewModel里面，让很多View重用这段视图逻辑。 在Android中，布局里可以进行一个视图逻辑，并且Model发生变化，View也随着发生变化。

2.    低耦合。以前Activity、Fragment中需要把数据填充到View，还要进行一些视图逻辑。现在这些都可在布局中完成， 甚至都不需要再Activity、Fragment去findViewById（）。这时候Activity、Fragment只需要做好的逻辑处理就可以了。
