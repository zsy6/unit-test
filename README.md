# unit-test-sample
[![build status](http://git.meicloud.com/cdp/unit-test-sample/badges/master/build.svg)](http://git.meicloud.com/cdp/unit-test-sample/commits/master) [![coverage report](http://git.meicloud.com/cdp/unit-test-sample/badges/master/coverage.svg)](http://git.meicloud.com/cdp/unit-test-sample/commits/master)

> 这是一个分层单元测试的样例工程，是搜集网络上各种单元测试思想和单元测试用例自学而写，也许自己理解的不对。    

###### 单元测试：是指对软件中的最小可测试单元进行检查和验证。
特性：
1. 单元测试不应该依赖外部系统；
2. 单元测试运行速度很快；
3. 单元测试不应该造成测试环境的脏数据；
4. 单元测试可以重复运行. 

###### 单元测试的流程包括

1. 初始化数据
2. 执行测试
3. 销毁数据

在真实的测试代码开发中，有几类问题会造成困扰：

1. 数据库环境的搭建
搭建一套完整的数据库往往比较耗时，然而一旦将数据库配置加入测试范围，就必须长期维护其稳定性；
这同时也会带来代码库同步的困扰。

2. 保证数据库的"干净"
大多数情况下，每个测试用例在启动前(初始化数据)都期望数据库是"干净"的状态；然而使用真实的数据库却很难保证这点，原因是：  
a. 多个应用可能会共享一个物理数据库；  
b. 测试用例在销毁数据时很难保证完全清除，可能一次意外的调试也会产生垃圾数据；  

H2内存数据库可以很好的解决上述问题，本身作为嵌入式数据库并不需要额外的看护成本；在程序退出时，所有数据都能保证完全清除。
#### 项目所涉及到的相关技术栈如下：
1. spring-boot
2. com.alibaba.druid
3. mybatis
4. com.h2database.h2
5. swagger2
6. junit
7. mockito
8. spring MockMvc
9. lombok

http://localhost:8080/swagger-ui.html