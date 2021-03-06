##Spring快速入门（开发工具为Myeclipse）
* **下载Jar包**
 * Spring Jar包
[http://repo.springsource.org/libs-release-local/](http://repo.springsource.org/libs-release-local/)
 * commons-logging （日志）
[http://ebr.springsource.com/repository/app/bundle/version/detail?name=com.springsource.org.apache.commons.logging&version=1.1.1](http://ebr.springsource.com/repository/app/bundle/version/detail?name=com.springsource.org.apache.commons.logging&version=1.1.1)
 * apache-log4j （日志）
[http://ebr.springsource.com/repository/app/bundle/version/detail?name=com.springsource.org.apache.log4j&version=1.2.16](http://ebr.springsource.com/repository/app/bundle/version/detail?name=com.springsource.org.apache.log4j&version=1.2.16)
 * Junit（用于单元测试）
[http://junit.org/junit4/](http://junit.org/junit4/)

* **将下载下来的Jar包导入项目中**<br/>
导入结果如下图：<br/>
![](http://i.imgur.com/86u9aDV.png)

再在src目录下添加如下文件（log4j属性文件）<br/>
![](http://i.imgur.com/DAVDfb1.png)

* **创建一个Java文件**<br/>
![](http://i.imgur.com/VlTqNJ2.png)<br/>
此类就作为一个JavaBean

* **创建一个applicationContext.xml文件**<br/>
![](http://i.imgur.com/iSiGCdg.png)<br/>
首先应该从spring-framework-4.0.0.RELEASE\docs\spring-framework-reference\html中找到xsd-config.html找到其中的beans表标签并复制（主要是用到它的约束）
![](http://i.imgur.com/KBoXyTf.png)<br/>
applicationContext.xml文件中的bean标签就对应一个JavaBean对象，其中包含属性标签；当Spring框架加载时，会自动创建一个Bean对象（反射）。

* **创建一个测试类**<br/>
![](http://i.imgur.com/YILCKvM.png)<br/>
ClassPathXmlApplicationContext("applicationContext.xml的路径")<br/>
getBean("applicationContext.xml文件中bean标签的id")


