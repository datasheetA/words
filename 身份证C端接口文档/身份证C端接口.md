##人员信息C端录入接口
###概述
本协议适用于C端录入人员信息及人脸模板. 接入的账户为项目管理员.
###协议版本
v0.1
##同步数据接口标准
###1. 接口返回统一说明 
采用JSON格式返回
例如
```
{
	code:${code},
	msg:string
}
```
###发送参数：
接口提交时统一在header 上加入token 参数，token 参数在登录之后会返值
###1. 登录接口 
URL：/system/loginApi.whtml
入力：用户名，密码 格式: JSON
格式：JSON
```
{
	userName：string,
	password:string
}
```
params
参数名       |参数类型       |描述|约束条件
------------|-----------|-----------|-----------
userName       |string        |登录名|*
password       |string        |密码|*
出力：
Params
参数名       |参数类型       |描述
------------|-----------|-----------
code       |string        |返回代码
msg       |string        |返回信息
token       |string        |返回token
projectId     |long  |返回该用户对应的项目ID
projectName     |String  |返回该用户对应的项目名称

返回：json
```
{
	code:${code},
	msg:xxx,
	token:"xxx",
	project:xxxx,
	projectName:"xxx"
}
```
###2.班组信息
URL：/client/addGroupInfo.whtml
入力：项目班组信息
格式: JSON
```
{
"group":{
	"projectId":"xxx",
	"projectName":"xxx",
	"name":"xxx",
	...
	"createUser":"xxx"
}
}
```
入力参数：
参数名       |参数类型       |描述|约束条件
------------|-----------|-----------|-----------
projectId       |Long        |项目ID|*
projectName       |string        |项目名称|*
name       |string        |班组名称|*
teamLeader       |string        |联系人|*
contract       |string        |联系方式|*
teamIdNumber       |string        |班组长身份证号码|
responseIdNumber       |String     |责任人身份证号码|
memo       |String       |备注|
createUser       |String       |创建人|
说明：B端接收到创建人后，需要转换成创建人ID，再进行保存。
出力格式:json
```
{
	"result":"0|1"
	}
```
出力参数params:
参数名       |参数类型       |描述
------------|-----------|-----------
result       |string        |0失败，1成功

###3.编辑班组信息
URL：/client/editGroupInfo.whtml
入力：项目班组信息
格式: JSON
```
{"group":{
	"projectId":"xxx",
	"projectName":"xxx",
	"name":"xxx",
	...
	"createUser":"xxx"
}}
```
入力参数：
参数名       |参数类型       |描述|约束条件
------------|-----------|-----------|-----------
projectId       |long        |项目id|*
projectName       |string        |项目名称|*
name       |string        |班组名称|*
teamLeader       |string        |联系人|*
contract       |string        |联系方式|
teamIdNumber       |string        |班组长身份证号码|
responseIdNumber       |String     |责任人身份证号码|
memo       |String       |备注|
createUser       |String       |创建人|
说明：
    B端接收到创建人后，需要转换成创建人ID，再进行保存。
出力：人员基本信息，包括：身份证照片
出力格式:json
```
{
	"result":"0|1"
	}
```
出力参数params:
参数名       |参数类型       |描述
------------|-----------|-----------
result       |string        |0失败，1成功


###4.编辑工人信息
URL：/client/editUser.whtml 
入力：人员信息
格式: JSON
```
{"user":{
	"userId":"xxx",
	"name":"xxx",
	...
	"personType":"xxx"
}
}
```
入力参数：
参数名       |参数类型       |描述|约束条件
------------|-----------|-----------|-----------
userId       |String    |身份证号|*
name       |String   |人员姓名|
ptype       |Integer     |人员类型|
gender       |Integer    |性别|
birthday       |String   |生日|
photo       |string     |身份证图片|base6
mobile       |string    |电话号码|
