# DesignResCollection
  提供同一个App的不同架构实现，对其进行对比分析，方便大家选取使用  
  项目启发来自谷歌的同类框架项目 https://github.com/googlesamples/android-architecture  
  
  
## 代码示例 [持续开发中...]

  显示设计网站中收集来的资源的一个应用DesignResCollection，不同结构对应不同的[_结构后缀]。  
比如基本的MVP结构就是 DesignResCollection_MVP。不同结构的具体介绍请查看对应文件夹中的README.md  
  
  
### 已开发完成的示例

  * [DesignResCollection_MVC/](https://github.com/boredream/DesignResCollection/tree/master/DesignResCollection_MVC) - Model-View-Controller 结构。
  * [DesignResCollection_MVP/](https://github.com/boredream/DesignResCollection/tree/master/DesignResCollection_MVP) - Model-View-Presenter 结构。其中包含了针对P层的junit逻辑测试代码以及针对V层的Espresso页面测试代码。
  
### 待开发的示例

  * [DesignResCollection_MVP-Dagger2/](https://github.com/boredream/DesignResCollection/tree/master/DesignResCollection_MVP-Dagger2) - 基于 Model-View-Presenter 结构，添加Dagger2框架。
  * [DesignResCollection_LeanCloud/](https://github.com/boredream/DesignResCollection/tree/master/DesignResCollection_MVP-Dagger2) - 基于 LeanCloud 服务，不用自己写后台服务端代码，非全栈开发也可以完成完整网络应用。
  * [DesignResCollection_IM/](https://github.com/boredream/DesignResCollection/tree/master/DesignResCollection_MVP-Dagger2) - 基于 LeanCloud 服务，实现IM及时聊天业务，提供最基本的IM相关功能。
  * [DesignResCollection_Espresso/](https://github.com/boredream/DesignResCollection/tree/master/DesignResCollection_MVP-Dagger2) - 单独抽取出来一个项目，详细介绍Espresso针对各种常用场景的测试写法。
  
  
### 其他相关示例
  * [DesignResCollection（ing...）](https://github.com/boredream/DesignResCollectionApp) - 完整App代码，不断丰富完善中，实现一个最终完整版。本项目中的示例是基于此项目做了功能和页面上的精简，便于演示不同代码结构。
  * [DesignCollectionCloudEngine](https://github.com/boredream/DesignCollectionCloudEngine) - 部署在LeanCloud上的云代码项目，用于定时爬取数据保存到LeanCloud中为应用提供数据来源的。
  

## 开发计划
* 2016.8.17 ~ 9.20（已完成）
[DesignResCollection_MVP/](https://github.com/boredream/DesignResCollection/tree/master/DesignResCollection_MVP)

* 2016.9.20 ~
[DesignResCollection_MVP-Dagger2/](https://github.com/boredream/DesignResCollection/tree/master/DesignResCollection_MVP-Dagger2)


## 通用依赖框架

  * 使用LeanCloud作为后端服务，比较简单，无需自行开发。  
  * 使用LeanCloud的Restful-API接口。（不用LeanCloud的Android SDK，更贴近于实际开发中用开发接口文档的情景）  
  * 网络框架部分使用Retrofit2.0 + RxJava。  
  * 图片使用Glide。  
  * [代码助手Model ](https://github.com/boredream/bdcodehelper)常见工具类、功能等都封装到了这个依赖Model中，一来为了方便，二来让注意力更集中在项目框架结构上。
  * 使用Espresso进行UI页面交互测试
  * 使用mockito对Presenter分别进行真实接口数据测试以及mock模拟数据测试
  

## 到底使用哪种框架使用在我自己的app中？

  每个框架示例中都有一个README，你可以先查看下每种的特点。  
最终项目里还会对比下所有框架的优缺点列出来，方便你根据自己具体情况进行全面的比较选取。  
  
  
## 应用截图
<img src="https://github.com/boredream/DesignResCollection/blob/master/screenshoot/device-2016-08-17-142555.png" width="300" height="530">
<img src="https://github.com/boredream/DesignResCollection/blob/master/screenshoot/device-2016-08-17-142654.png" width="300" height="530">
<img src="https://github.com/boredream/DesignResCollection/blob/master/screenshoot/device-2016-08-17-142712.png" width="300" height="530">
<img src="https://github.com/boredream/DesignResCollection/blob/master/screenshoot/device-2016-08-17-142739.png" width="300" height="530">
  
  
## 使用

下载~ 解压~ Open对应框架项目的文件夹


## 为什么要做这样一个项目 

  Android 的框架多用MVC模型进行开发，而其中的Activity经常承担了大量的V和C的工作，既处理逻辑又处理UI。  
因此Activity中很容易聚集大量代码，造成结构复杂混乱、测试维护困难等诸多不便。  
  
  这个项目就是为了帮助解决这个问题的。其中将提供一个相同的应用程序，然后使用不同的框架实现之。  

  您可以使用本项目中的示例代码作为参考，或者直接作为项目的架子在此之上继续开发自己的项目。  
本项目中，主要关注的重点在于代码的结构框架、测试以及可维护性。  
但是要注意，这里提供了不同的架构，各自有自己的优缺点。因此在选取时要根据自己的需要选择对应的框架结构。  
比如你只是一个简单的App，不需要单元测试，功能UI都比较少，那直接MVC结构即可。  
