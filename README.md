# secretary
秘书项目

## 后台服务器 server

创建数据库，不需要导入 sql 文件


```
// 安装依赖
cnpm i 

node app.js

访问地址：

http://localhost:3000/

```

### 问题及解决

#### 数据库表结构问题

数据库中表结构的问题，那么，更新数据库结构


SQL 语句，中自增字段:

```
CREATE TABLE `recoder` (`recoder_id` bigint(255) auto_increment NOT NULL PRIMARY KEY,`user_id` bigint(255) NOT NULL,`is_remove` int(10) NOT NULL DEFAULT '0',`is_public` int(10) NOT NULL DEFAULT '0',`is_finish` int(10) NOT NULL DEFAULT '0',`title` varchar(255) NOT NULL,`des` varchar(255) NOT NULL,`date` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,`alert_time` bigint(255) NOT NULL DEFAULT '0',`status` int(10) NOT NULL DEFAULT '0',`lat` bigint(255) NOT NULL DEFAULT '0',`lng` bigint(255) NOT NULL DEFAULT '0',`address` varchar(255) NOT NULL)
```

#### 创建表异常


(node:7300) UnhandledPromiseRejectionWarning: Unhandled promise rejection (rejection id: 1): Error: ER_TABLE_EXISTS_ERROR: Table 'recoder' already exists


new Promise((_, reject) => reject(new Error('woops')))
.catch(new Function());



参考资料：
https://objcer.com/2017/12/27/unhandled-promise-rejections-in-node-js/


#### 刷新页面


```
// 引入组件 $state
angular.module("starter.controllers",[])
	.controller("recoderController",function ($scope,$state,DBManager,$ionicLoading,$timeout,timeTool,$ionicListDelegate,$rootScope,HTTPManager) {
	
	
// 调用代码,重新加载页面
$state.reload();
```



### 接口用postman来测试

用 postman 导入文件：

    小秘书 项目.postman_collection.json


# ionic 混合式 APP开发

```
// 安装依赖
cnpm i

// 在浏览器中模拟运行项目
ionic serve

```


## 本地存储

```
openDatabase

```
