## 1. 批量发送人员信息
### 1.1 JSON格式
### 1.2 请求说明
> 请求方式：POST<br>
请求URL ：/userproject/queryUserInfoToLed

### 1.3 请求参数(无)

### 1.4 返回结果


```  
{
  [{"userName": "000000",
"userId": "000000",
"projectId": 11111111,
"ProjectName": "000000",
"mobile": "000000",
"workKind": "000000",
 "workKindName": "000000",
"classNo": "000000",
"photo": "000000",
"createDate": "000000"}]
}
```
### 1.5 返回参数
字段       |字段类型       |字段说明
------------|-----------|-----------
userName       |string        |人员姓名
userId       |string        |身份证号
projectId       |long        |项目ID
ProjectName       |string        |项目名
mobile       |string        |手机号码
workKind       |int        |工种值
workKindName       |string        |工种名
classNo       |string        |班组
photo       |string        |身份证照片(base64)
createDate       |string        |录入时间


## 2.根据身份证号，上传单个人员信息
### 2.1 JSON格式
### 2.2 请求说明
> 请求方式：POST<br>
请求URL ：/userproject/getUserInfoByIdToLed

### 2.3 请求参数
字段       |字段类型       |字段说明
------------|-----------|-----------
userId       |string        |身份证号
projectName  |string        |项目名称
### 2.4 返回结果


```  
{"userName": "000000",
"userId": "000000",
"projectId": 11111111,
"ProjectName": "000000",
"mobile": "000000",
"workKind": "000000",
 "workKindName": "000000",
"classNo": "000000",
"photo": "000000",
"createDate": "000000"
}
```
### 2.5 返回参数
字段       |字段类型       |字段说明
------------|-----------|-----------
userName       |string        |人员姓名
userId       |string        |身份证号
projectId       |long        |项目ID
ProjectName       |string        |项目名
mobile       |string        |手机号码
workKind       |int        |工种值
workKindName       |string        |工种名
classNo       |string        |班组
photo       |string        |身份证照片(base64)
createDate       |string        |录入时间


## 3.过滤重复数据
### 3.1 已上传的数据，将ID号保存在tf_f_user_upload中，再次上传数据时，已上传的数据不再进行上传。
### 3.2 表结构：
字段       |字段类型       |字段说明
------------|-----------|-----------
ng_id       |Number(18)      |主键
ng_user_id       |Number(18)        |用户ID
Create_date       |date        |录入时间
memo      |Varchar2(255)       |备注

## 4. 根据项目名称，查询该项目目前的进场人数。
### 4.1 JSON格式
### 4.2 请求说明
> 请求方式：POST<br>
请求URL ： /userproject/getPrjectUserCount

### 4.3 请求参数
字段       |字段类型       |字段说明
------------|-----------|-----------
projectName  |string        |项目名称
### 4.4 返回结果


```  
{
"userCount": 11111111
}
```
### 4.5 返回参数
字段       |字段类型       |字段说明
------------|-----------|-----------
userCount       |int        |项目进场人数


## 5.根据项目名称，查询出该项目已进场的人员信息。
### 5.1 JSON格式
### 5.2 请求说明
> 请求方式：POST<br>
请求URL ：  /userproject/queryUserInfoByNameToLed

### 5.3 请求参数
字段       |字段类型       |字段说明
------------|-----------|-----------
projectName  |string        |项目名称
### 5.4 返回结果


```  
{"userName": "000000",
"userId": "000000",
"projectId": 11111111,
"ProjectName": "000000",
"mobile": "000000",
"workKind": "000000",
 "workKindName": "000000",
"classNo": "000000",
"photo": "000000",
"createDate": "000000"
}
```
### 5.5 返回参数
字段       |字段类型       |字段说明
------------|-----------|-----------
userName       |string        |人员姓名
userId       |string        |身份证号
projectId       |long        |项目ID
ProjectName       |string        |项目名
mobile       |string        |手机号码
workKind       |int        |工种值
workKindName       |string        |工种名
classNo       |string        |班组
photo       |string        |身份证照片(base64)
createDate       |string        |录入时间