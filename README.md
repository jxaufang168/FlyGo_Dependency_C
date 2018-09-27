# FlyGo_Dependency_C
文档地址：https://www.flygo520.com/docs/maven/maven-1alvhicr94q39

# 聚合项目和继承项目区别

1、在语意上聚合项目父项目和子项目关系性较强。
2、在语意上单纯继承项目父项目和子项目关系性较弱

|<center>名称</center>|<center>关系性</center>|<center>是否包含子项目</center>|
|:----    |:---|:---|
|聚合项目 |关系性强  |父项目包含子项目，强关联  |
|继承项目 |  关系弱|父项目不包含子项目，弱关联|

# 父类声明 dependencyManagement 依赖

应用场景：父项目声明需要依赖的jar包，子项目不用完全继承父项目的依赖的Jar包。

1、作用:声明可能使用到的所有jar
>[info]在父项目声明依赖的Jar包，子项目需要把依赖的Jar配置到pom.xml中，父项目管理所有依赖Jar包的版本信息。

2、子项目中只需要有坐标的 `<groupId>` 和 `<artifactId>`,`<version>`继承父项目
3、在父项目中 `<properties>` 把所有版本好进行统一管理
`<properties>`子标签名称自定义，${名字} 引用标签的值

父项目的相关配置

![父项目的相关配置](https://www.flygo520.com/uploads/maven/images/m_f4b70af5301a826a2a971c6e717c871a_r.png#size=360x0)

子项目的相关配置

![子项目的相关配置](https://www.flygo520.com/uploads/maven/images/m_c5eade2b500a12293ba4361b88059ae2_r.png#size=360x0)

# 演示Demo源码地址
https://github.com/jxaufang168/FlyGo_Dependency_C

