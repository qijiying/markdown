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


接口链接
-------

[app用户接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/app%E7%94%A8%E6%88%B7%E6%8E%A5%E5%8F%A3.md)

[代理商接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E4%BB%A3%E7%90%86%E5%95%86%E6%8E%A5%E5%8F%A3.md)

[原声音乐接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E5%8E%9F%E5%A3%B0%E9%9F%B3%E4%B9%90%E6%8E%A5%E5%8F%A3.md)

[反馈接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E5%8F%8D%E9%A6%88%E6%8E%A5%E5%8F%A3.md)

[帖子接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E5%B8%96%E5%AD%90%E6%8E%A5%E5%8F%A3.md)

[广告接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E5%B9%BF%E5%91%8A%E6%8E%A5%E5%8F%A3.md)

[文件上传接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E6%96%87%E4%BB%B6%E4%B8%8A%E4%BC%A0%E6%8E%A5%E5%8F%A3.md)

[新闻接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E6%96%B0%E9%97%BB%E6%8E%A5%E5%8F%A3.md)

[服务号投稿接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E6%9C%8D%E5%8A%A1%E5%8F%B7%E6%8A%95%E7%A8%BF%E6%8E%A5%E5%8F%A3.md)

[服务号接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E6%9C%8D%E5%8A%A1%E5%8F%B7%E6%8E%A5%E5%8F%A3.md)

[服务号类别接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E6%9C%8D%E5%8A%A1%E5%8F%B7%E7%B1%BB%E5%88%AB%E6%8E%A5%E5%8F%A3.md)

[服务号粉丝接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E6%9C%8D%E5%8A%A1%E5%8F%B7%E7%B2%89%E4%B8%9D%E6%8E%A5%E5%8F%A3.md)

[权限接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E6%9D%83%E9%99%90%E6%8E%A5%E5%8F%A3.md)

[app版本接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E7%89%88%E6%9C%AC%E6%8E%A5%E5%8F%A3.md)

[简报接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E7%AE%80%E6%8A%A5%E6%8E%A5%E5%8F%A3.md)

[系统用户接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E7%AE%80%E6%8A%A5%E6%8E%A5%E5%8F%A3.md)

[角色接口](http://gitlab.2017zsx.com/lizhi/web-handover-document/blob/master/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E8%A7%92%E8%89%B2%E6%8E%A5%E5%8F%A3.md)











