<h1 align=center><font color=blue>app用户接口</font></h1>

<font size=4 color=red>

1. [新增用户](#add)
2. [用户列表](#data_grid)
3. [搜索用户](#data_search)
4. [查找所有用户](#all_user)
5. [修改简报](#update)
6. [删除简报](#delete)
7. [根据用户ID查找friend](#user_friend)
8. [统计用户图表](#drawmap)
9. [统计省级用户图表](#province_drawmap)
10. [统计新增用户数量](#s_user_count)
11. [获取用户收藏列表](#user_collection) 
12. [获取用户名片](#user_card)
13. [查询用户评论过的帖子](#user_comment_post)
14. [查询用户评论过的新闻](#user_comment_news)
15. [搜索用户评论](#user_comment_search)
16. [获得我的群信息](#user_group)
17. [搜索用户的群组](#user_group_search)
18. [查询用户点赞信息](#user_thumbup)


</font>

<br/>
<span id="add"></span>
##新增用户

####请求url: 
> /api/user/add

####请求方式: 
> post

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
User | true | com.zsx.model.pojo.User | 用户实体类

####权限值：
> app:add

####返回示例

	{
	    "code": 1,
	    "message": "成功"
	}


<br/>
<span id="data_grid"></span>
##用户列表

####请求url: 
> /api/user/dataGrid

####请求方式: 
> post

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
current | false | Integer | 当前页码
size | false | Integer | 每页条数 
source | false | String | 用户来源，ios，Android，web

####权限值：
> app:dataGrid

####返回示例

	{
    "code": 1,
    "message": "成功",
    "pages": 1,
    "total": 1,
    "current": 1,
    "data": [
        {
          。。。  
        }
    ],
    "size": 10
	}

<br/>
<span id="data_search"></span>
##搜索用户列表

####请求url: 
> /api/user/dataSearch

####请求方式: 
> post

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
current | false | Integer | 当前页码
size | false | Integer | 每页条数 
source | false | String | 用户来源，ios，Android，web
areaCode | false | Integer | 区域code
name | false | String | 用户的登录名、昵称、实名
startTime | false | Date | 注册大于的时间
endTime | false | Date | 注册小于的时间

####权限值：
> app:search

####返回示例

	{
    "code": 1,
    "message": "成功",
    "pages": 1,
    "total": 1,
    "current": 1,
    "data": [
        {
          。。。  
        }
    ],
    "size": 10
	}


<br/>
<span id="all_user"></span>
##查找全部用户

####请求url: 
> /api/user/all/user

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -

####权限值：
> app:dataGrid

####返回示例

	{
    "code": 1,
    "message": "成功",
    "pages": 1,
    "total": 1,
    "current": 1,
    "data": [
        {
          。。。  
        }
    ],
    "size": 10
	}



<br/>
<span id="update"></span>
##更新用户


####请求url: 
> /api/user/update

####请求方式: 
> post

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
User | true | com.zsx.model.pojo.User | 用户实体类

####权限值：
> app:edit

####返回示例

	{
	    "code": 1,
	    "message": "成功"
	}



<span id="delete"></span>
##删除用户


####请求url: 
> /api/user/delete

####请求方式: 
> post

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
ids | true | Integer[] | 简报id数组

####权限值：
> app:delete

####返回示例

	{
	    "code": 1,
	    "message": "成功"
	}


<span id="user_friend"></span>
##删除用户

####请求url: 
> /api/user/friend/{userId}

####请求方式: 
> post

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
userId | true | Long | 用户ID
isEntire | false | String | 是否返回全部数据 all or others
current | false | Integer | 当前页码
size | false | Integer | 每页条数

####权限值：
> app:friend

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}

<span id="drawmap"></span>
##统计用户图表

####请求url: 
> /api/user/drawMap

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -

####权限值：
> hometown:dataGrid

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}


<span id="province_drawmap"></span>
##统计省级用户图表

####请求url: 
> /api/user/province/drawMap

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -

####权限值：
> hometown

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}


<span id="s_user_count"></span>
##统计新增用户数量

####请求url: 
> /api/user/statistic/new/user/{dayNumber}/{type}/{isAll}

####请求方式: 
> post

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
dayNumber | true | Integer | 1：昨日 7：七天 30：一月
type | true | Integer | 0：all 1：ios 2：android
isAll | true | Integer | 0：否 1：是

####权限值：
> userCount

####返回示例

	{
	    "code": 1,
	    "data": 0,
	    "message": "SUCCESS"
	}

<span id="user_collection"></span>
##统计省级用户图表

####请求url: 
> /api/web/user/collection/{userId}

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
userId | true | Long | 用户ID
t | true | Integer | 	1:新闻 2:政务 3:招商 4:办事 5:帖子
c | false | Integer | 当前页码
s | false | Integer | 每页条数

####权限值：
> 

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}

<span id="user_card"></span>
##获取用户名片

####请求url: 
> /api/web/user/card/{userId}

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
userId | true | Long | 用户ID

####权限值：
> 

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}


<span id="user_comment_post"></span>
##查看用户评论过的帖子

####请求url: 
> /api/web/user/comment/post/{userId}

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
c | true | Integer | 当前页码
s | true | Integer | 每页数据数

####权限值：
> 

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}

<span id="user_comment_news"></span>
##查看用户评论过的新闻

####请求url: 
> /api/web/user/comment/news/{userId}

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
c | true | Integer | 当前页码
s | true | Integer | 每页数据数

####权限值：
> 

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}


<span id="user_comment_search"></span>
##搜索用户评论

####请求url: 
> /api/web/user/comment/search/{userId}

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
c | false | Integer | 当前页码
s | false | Integer | 每页数据数
content | false | String |评论内容
createTime | false | Integer | 评论时间

####权限值：
> 

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}

<span id="user_group"></span>
##获取用户群组

####请求url: 
> /api/web/user/group/{userId}

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
userId | true | Long | 用户ID

####权限值：
> 

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}


<span id="user_group_search"></span>
##搜索用户的群组

####请求url: 
> /api/web/user/group/search/{userId}

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
name | false | String | 群组名称
userId | true | Long | 用户ID
current | false | Integer | 当前页码
size | false | Integer | 每页条数

####权限值：
> 

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}

<span id="user_thumbup"></span>
##获得用户的点赞信息

####请求url: 
> /api/web/user/thumbup/{userId}

####请求方式: 
> get

####参数：

参数 | 必选 | 类型 | 说明
- | :-: | :-: | -
userId | true | Long | 用户ID
current | false | Integer | 当前页码
size | false | Integer | 每页条数

####权限值：
> 

####返回示例

	{
	    "code": 1,
	    "message": "成功",
	    "pages": 1,
	    "total": 1,
	    "current": 1,
	    "data": [
	        {
	          。。。  
	        }
	    ],
	    "size": 10
	}





