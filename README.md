<h1 align=center><font color=red>看逗逗app接口交接文档</font></h1>

基本配置
-------
<font size=4 >
**contextPath**: /fwmp

**服务端口**: port=8086

**根路径**: IP:{port}/fwmp

**swagger路径**：IP:{port}/fwmp/index.html

**上线配置**: 
	
- prod: 线上
- host: 本地
- prerelease: 预发布

**服务器位置目录**：/usr/local/software/springBoot/web

**redis和mybatis配置文件有注释**

**文件地址配置**（com.zsx.fwmp.web.controller.base.ServerController）：

>http://10.0.0.21:800/;    //本地路径

>http://image.2017zsx.com/;    //线上路径

>http://prerelease.iamge.2017zsx.com/;    //预发布路径

</font>

shiro详细配置
-------------
<font size=4 >

- eh缓存配置路径： config/ehcache-shiro.xml
- 采用默认session管理
- 接口访问拦截器：AjaxPermissionsAuthorizationFilter
- 单点登录配置：kickoutSessionControlFilter
- 开启shiro注解配置：advisorAutoProxyCreator
- shiro注解需要spring aop支持：authorizationAttributeSourceAdvisor

</font>
Exception全局处理
-----------------
	package com/zsx/fwmp/web/configuration/aop/ExceptionController

跨域配置
-------
	package com.zsx.fwmp.web.configuration.config.CorsConfig

springboot全局序列化和格式转换配置
--------------------------------
	package com.zsx.fwmp.web.configuration.config.CustomWebMvcConfigurerAdapter
	package com.zsx.fwmp.web.configuration.config.JsonSerialize
	package com.zsx.fwmp.web.configuration.config.WebAppConfig
	//WebAppConfig解决的是id超范围后的精度问题

文件上传
---------
**大小限制**

	package com.zsx.fwmp.web.configuration.config.MultipartConfiguration

**拦截器**

//修改文件时删除源文件
com.zsx.fwmp.web.configuration.interceptor.FileUploadInterceptor

Mybatis拦截器
-------------

> mybatis拦截器主要解决的是代理商区域权限的问题
> 具体可以查看*com.zsx.fwmp.web.configuration.interceptor*，有详细注释

定时任务
--------

<font size=4 >

- 定时发布软文
- 定时推送简报
- 每隔10分钟处理过期广告
- 原声定时任务

</font>









