# springboot
开发springboot项目 步骤：
1.新建项目，添加组件支撑
编辑Maven项目的pom.xml
2.配置相关属性；
编辑springboot的全局配置文件==yml/properties
3.实现项目的功能代码-
注解+java代码实现功能；


jsp web 项目
1.添加组件职支撑
3个依赖；
1个必须，
添加tomcat组件依赖支撑
jstl   sevlet tomcat


2.配置相关属性
yml配置物理视图名的前缀和后缀
 mvc:
    view:
      prefix: /WEB-INF/views/
      suffix: .jsp
3.实现项目的功能代码 
注解+ java代码


3,jsp  web 项目
1.添加组件支撑
  3个依赖
  1个必须
  添加（内嵌）tomcat组件依赖支撑
  2个可选
  jstl    servlet
配置相关属性：
  mvc:
    view:
      prefix: /WEB-INF/views/
      suffix: .jsp


User本类   
Dao  插入sql语句
    1.接口中创建方法；
    2.到实现类重载接口方法
    3.

MVC 具体详解
1、dao层
dao层主要做数据持久层的工作，负责与数据库进行联络的一些任务都封装在此，dao层的设计首先是设计dao层的接口，然后在Spring的配置文件中定义此接口的实现类，然后就可以再模块中调用此接口来进行数据业务的处理，而不用关心此接口的具体实现类是哪个类，显得结构非常清晰，dao层的数据源配置，以及有关数据库连接参数都在Spring配置文件中进行配置。
2、service层
service层主要负责业务模块的应用逻辑应用设计。同样是首先设计接口，再设计其实现类，接着再Spring的配置文件中配置其实现的关联。这样我们就可以在应用中调用service接口来进行业务处理。service层的业务实，具体要调用已经定义的dao层接口，封装service层业务逻辑有利于通用的业务逻辑的独立性和重复利用性。程序显得非常简洁。
3、controller层
controller层负责具体的业务模块流程的控制，在此层要调用service层的接口来控制业务流程，控制的配置也同样是在Spring的配置文件里进行，针对具体的业务流程，会有不同的控制器。我们具体的设计过程可以将流程进行抽象归纳，设计出可以重复利用的子单元流程模块。这样不仅使程序结构变得清晰，也大大减少了代码量。
4、view层
view层与控制层结合比较紧密，需要二者结合起来协同开发。view层主要负责前台jsp页面的显示。

5、它们之间的关系：
Service层是建立在DAO层之上的，建立了DAO层后才可以建立Service层，而Service层又是在Controller层之下的，因而Service层应该既调用DAO层的接口，又要提供接口给Controller层的类来进行调用，它刚好处于一个中间层的位置。每个模型都有一个Service接口，每个接口分别封装各自的业务处理方法。 
    
    
    
    
    
    
       
