# secretary
������Ŀ

## ��̨������ server

�������ݿ⣬����Ҫ���� sql �ļ�


```
// ��װ����
cnpm i 

node app.js

���ʵ�ַ��

http://localhost:3000/

```

### ���⼰���

#### ���ݿ��ṹ����

���ݿ��б�ṹ�����⣬��ô���������ݿ�ṹ


SQL ��䣬�������ֶ�:

```
CREATE TABLE `recoder` (`recoder_id` bigint(255) auto_increment NOT NULL PRIMARY KEY,`user_id` bigint(255) NOT NULL,`is_remove` int(10) NOT NULL DEFAULT '0',`is_public` int(10) NOT NULL DEFAULT '0',`is_finish` int(10) NOT NULL DEFAULT '0',`title` varchar(255) NOT NULL,`des` varchar(255) NOT NULL,`date` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,`alert_time` bigint(255) NOT NULL DEFAULT '0',`status` int(10) NOT NULL DEFAULT '0',`lat` bigint(255) NOT NULL DEFAULT '0',`lng` bigint(255) NOT NULL DEFAULT '0',`address` varchar(255) NOT NULL)
```

#### �������쳣


(node:7300) UnhandledPromiseRejectionWarning: Unhandled promise rejection (rejection id: 1): Error: ER_TABLE_EXISTS_ERROR: Table 'recoder' already exists


new Promise((_, reject) => reject(new Error('woops')))
.catch(new Function());



�ο����ϣ�
https://objcer.com/2017/12/27/unhandled-promise-rejections-in-node-js/


#### ˢ��ҳ��


```
// ������� $state
angular.module("starter.controllers",[])
	.controller("recoderController",function ($scope,$state,DBManager,$ionicLoading,$timeout,timeTool,$ionicListDelegate,$rootScope,HTTPManager) {
	
	
// ���ô���,���¼���ҳ��
$state.reload();
```



### �ӿ���postman������

�� postman �����ļ���

    С���� ��Ŀ.postman_collection.json


# ionic ���ʽ APP����

```
// ��װ����
cnpm i

// ���������ģ��������Ŀ
ionic serve

```


## ���ش洢

```
openDatabase

```
