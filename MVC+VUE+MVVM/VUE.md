#VUE

Vue 是一套用于构建用户界面的渐进式javascript框架，与其它大型框架不同的是：Vue被设计为可以自底向上逐层应用。Vue的核心库只关注视图层，不仅易于上手，还便于与第三方库或既有项目整合，另外一个方面,当Vue与现代化的工具链以及各种支持类库结合使用时，Vue也完全能够为复杂的单页应用提供驱动。

Vue.js是用于构建交互式的Web界面的库，它提供MVVM数据绑定和一个可组合的组件系统，具有简单、灵活的API。从技术上讲，Vue.js集中在MVVM模式上的视图模型层(viewModel)，并通过双向数据绑定连接视图（view） 和模型（model）。实际的DOM操作和输出格式被抽象出来成指令和过滤器。相比其他的MVVM框架，Vue.js更容易上手，它让你通过简单而灵活的API创建由数据驱动的UI组件。

Vue.js是一个构建数据驱动的Web界面的库，Vue.js的目标是通过尽可能简单的API实现响应的数据绑定和组合的视图组件。

Vue.js自身不是一个全能框架——它只聚焦于视图层非常容易与其它库或已有项目整合。另一方面，在与相关工具和支持库一起使用时，Vue.js也能完美地驱动复杂的单页应用。

##响应的数据绑定

Vue.js的核心是一个响应的数据绑定系统，它让数据与DOM保持同步非常简单，在使用JQ手工操作DOM时，我们的代码常常是命令式的、重复的、易错的。Vue.js拥抱数据驱动的视图概念，通俗地讲它意味着我们在普通HTML模板中使用特殊的语法将DOM绑定到底层数据，一旦创建了绑定DOM将于数据保持同步。每当修改了数据，DOM便相应地更新。这样我们应用中的逻辑就几乎都是直接修改数据了，不必与DOM更新搅在一起，这让我们的代码更容易撰写、理解与维护。

![](/picture/picture8.png)

view：视图层。viewModel：vm实例（视图模型层）。model：数据模型层。

## 组件系统

组件（component）是Vue.js最强大的功能之一。组件可以扩展HTML元素，封装可重用的代码。在较高层面上，组件是自定义元素，Vue.js的编译器为它添加特殊功能。在有些情况下，组件也可以表现为用  is  特性进行了扩展的原生HTML元素。

所有的Vue组件同时也都是Vue的实例，所以可接受相同的选项对象、并提供相同的生命周期钩子。

组件系统是用Vue.js构建大型应用的基础。可以用独立可复用的小组件来构建大型应用。几乎任意类型的应用界面都可以抽象为一个组件树。