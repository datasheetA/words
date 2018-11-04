## 1.新增项目信息
### URL: /project/projectInfo/insertExternal
### Method:POST
#### Params
参数名                       |参数类型         |字段说明           |约束条件
----------------------------|-----------------|------------------|------------------
body                        |                 |                  |     
	operationFlag           |string         |状态标志             |insertExternalProject
	projects                |array          |                    |     
	    org                     |object         |部门信息             |
	        name                |string         |名称                 |
	        level               |int            |组织等级             |1
	        parentId            |int            |父id                 |0 
	        instroduction       |string         |企业描述             |
	        platform            |int            |来源标记             |2
	        relationOrgId       |int            |主键                 |
		    user                |object          |人员信息             |
		        code            |string         |用户编码             |
		        phone           |string         |用户手机号           |
		        name            |string         |用户名               | 
		        password        |string         |密码                 |
		        platform        |int            |来源标记             |2
		        relationUserId  |int            |主键                 |
		        status          |int            |状态                 |0
		projectInfo             |object           |项目信息           |
			relationId          |int              |主键               |
			name                |string           |项目名称           |
			phase               |string           |项目状态           |
			progress            |string           |项目进展           |
			activityType        |string           |项目活动类型       |
			isKey               |int              |重点项目           |
			position            |string           |项目区域           |
			address             |string           |工程地点           |
			type                |int              |项目类别           |
			qualityCode         |string           |质量报监编号       |
			securityCode        |string           |安全报监编号       |
			beginDateContract   |timestamp        |合同开工日期       |
			endDateContract     |timestamp        |合同竣工日期       |
			beginDate           |timestamp        |开工日期           |
			endDate             |timestamp        |竣工日期           |
			instroduction       |string           |项目简介           |
			builder             |string           |施工单位           |
			surveyor            |string           |勘察单位           |
			supervisor          |string           |监理单位           |
			constuctor          |string           |建设单位           |
			constuctorOrgCode   |string           |建设单位组织机构代码|
			constuctorCode      |string           |建设单位编码        |
			buildingSize        |decimal(12,1)    |建筑面积           |
			buildingCost        |decimal(12,1)    |工程造价(万元)      |
			contractNo          |strign           |合同备案编码        |
			identifier          |string           |项目编码            |
			winBiddingFile      |string           |中标通知书          |
			contractFile        |string           |备案合同            |
			manager             |string           |项目经理            |
			managerPhone        |string           |联系电话            |
			fixDays             |string           |定额工期            |
			content             |string           |施工内容            |
			managementAuditStatus|string          |监管审核状态        |
			managementAuditMemo  |string          |审核备注            |
			protectNo            |string          |安全施工措施备案号   |
			license              |string          |施工许可证号         |
			pictureFile          |string          |项目图片             |
			code                 |string          |项目代码             |
			state                |string          |状态                 |
			superviseAgency      |string          |监督机构             |
			builerCode           |string          |施工单位代码         |
			supervisorCode       |string          |监理单位代码         |
			desinger             |string          |设计单位名称         |
			buildingFloor        |int             |建筑层数             |
			structure            |string          |结构类型             |
			isCreate             |int             |是否进行中           |
			socialProvieCode     |string          |参保证明编号         |
			socialProvieDate     |timestamp       |参保日期             |
			injuryAuditStatus    |string          |工伤保险中心审核状态  |
			injuryAuditMemo      |string          |工伤保险中心审核备注  |
			source               |string          |数据来源             |
			implementStatus      |string          |设备实施状态         |
			implementMemo        |string          |设备实施备注         |
			responsiblePerson    |string          |项目责任人           |
			responsiblePersonPhone|string         |项目责任人联系电话    |
		    buildProjectCode      |string         |建设项目编码         |
		    placePoint            |string         |经纬度               |
		    district              |int            |地区                 |945
		    platform              |int            |平台                 |2
		    user              |object          |人员信息             |
		        code          |string          |用户编码             |
		        phone         |string          |用户手机号           |
		        name          |string          |用户名               | 
		        password      |string          |密码                 |
		        platform      |int             |来源标记             |2
		        relationUserId|int             |主键                 |
		        status        |int             |状态                 |0
	
#### 示例

```json  
{
  "body":{
  	"operationFlag":"insertExternalProject",
  	"projects":[{
	  	"org":{
	  		"name":"XXXXXXXXXXXX公司",                  
	        "level" :1,                  
	        "parentId" :0,               
	        "instroduction":"XXXXXXXXXXXX公司XXXXXXXXXXXXXXX",           
	        "platform"  :2,                  
	        "relationOrgId": 37,
	        "user":{
		  		"code":"XXXXXXXXXXXX",              
		        "phone":"18976567879",                 
		        "name" :"XXXX",             
		        "password" :"XXXXXXXXXXXX",          
		        "platform" :2,             
		        "relationUserId" :87,
		        "status":0
		  	}
	  	},
	  	"projectInfo":{
	  		"relationId":56,          
			"name":"启东XXXXXX项目",                
			"phase":"主体",               
			"progress":"开工",           
			"isKey":1,               
			"position":"启东",            
			"address":"启东",             
			"type":1,               
			"qualityCode":"XXXXXXXXXX",         
			"securityCode":"XXXXXXXXXX",        
			"beginDateContract":"2018-09-20",   
			"endDateContract":"2018-12-20",     
			"beginDate":"2018-09-20",          
			"endDate":"2018-12-20",            
			"instroduction":"启东XXXXXX项目",      
			"builder":"XXXXXX建设",             
			"surveyor": "XXXXXX建设",           
			"supervisor":  "XXXXXX建设",        
			"constuctor": "XXXXXX建设",       
			"constuctorOrgCode": "XXXXXXXXXXXX",  
			"constuctorCode": "XXXXXXXXXXXX",     
			"buildingSize": 1987766,       
			"buildingCost":  87665,     
			"contractNo": "XXXXXXXXXXXX",        
			"identifier":  "XXXXXXXXXXXX",       
			"winBiddingFile": "XXXXXXXXXXXX",    
			"contractFile":"XXXXXXXXXXXX",        
			"manager":"XXXXXXXXXXXX",             
			"managerPhone": "XXXXXXXXXXXX",       
			"fixDays": "37",           
			"content":"XXXXXXXXXXXX",             
			"managementAuditStatus":1,
			"managementAuditMemo": "XXXXXXXXXXXX", 
			"protectNo":"XXXXXXXXXXXX",           
			"license":"XXXXXXXXXXXX",              
			"pictureFile": "XXXXXXXXXXXX",         
			"code":"XXXXXXXXXXXX",                 
			"state": "开工",               
			"superviseAgency":"XXXXXXXXXXXX",      
			"builerCode":"XXXXXXXXXXXX",           
			"supervisorCode": "XXXXXXXXXXXX",      
			"desinger": "XXXXXXXXXXXX",            
			"buildingFloor":24,        
			"structure": "XXXXXXXXXXXX",           
			"isCreate": 1,            
			"socialProvieCode":"XXXXXXXXXXXX",     
			"socialProvieDate": "XXXXXXXXXXXX",   
			"injuryAuditStatus": "XXXXXXXXXXXX",   
			"injuryAuditMemo":"XXXXXXXXXXXX",    
			"source": "XXXXXXXXXXXX",              
			"implementStatus": "XXXXXXXXXXXX",    
			"implementMemo": "XXXXXXXXXXXX",      
			"responsiblePerson": "XXXXXXXXXXXX",   
			"responsiblePersonPhone":"XXXXXXXXXXXX",
		    "buildProjectCode": "XXXXXXXXXXXX",
		    "placePoint":"XXXXXXXXXXXX",
		    "district":945,
		    "platform"  :2,  
			 "user":{
		  		"code":"XXXXXXXXXXXX",              
		        "phone":"18976567879",                 
		        "name" :"XXXX",             
		        "password" :"XXXXXXXXXXXX",          
		        "platform" :2,             
		        "relationUserId" :87,
		        "status":0
		  	}
	  	}
	  }]	
  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 2.更新项目信息
### URL: /project/projectInfo/updateExternal
### Method:POST
#### Params
参数名                       |参数类型         |字段说明           |约束条件
----------------------------|-----------------|------------------|------------------
body                        |                 |                  |
    operationFlag           |string           |状态标志           |updateExternalProject
	projectInfo             |object           |项目信息           |
		relationId          |int              |主键               |
		name                |string           |项目名称           |
		phase               |string           |项目状态           |
		progress            |string           |项目进展           |
		activityType        |string           |项目活动类型       |
		isKey               |int              |重点项目           |
		position            |string           |项目区域           |
		address             |string           |工程地点           |
		type                |int              |项目类别           |
		qualityCode         |string           |质量报监编号       |
		securityCode        |string           |安全报监编号       |
		beginDateContract   |timestamp        |合同开工日期       |
		endDateContract     |timestamp        |合同竣工日期       |
		beginDate           |timestamp        |开工日期           |
		endDate             |timestamp        |竣工日期           |
		instroduction       |string           |项目简介           |
		builder             |string           |施工单位           |
		surveyor            |string           |勘察单位           |
		supervisor          |string           |监理单位           |
		constuctor          |string           |建设单位           |
		constuctorOrgCode   |string           |建设单位组织机构代码|
		constuctorCode      |string           |建设单位编码        |
		buildingSize        |decimal(12,1)    |建筑面积           |
		buildingCost        |decimal(12,1)    |工程造价(万元)      |
		contractNo          |strign           |合同备案编码        |
		identifier          |string           |项目编码            |
		winBiddingFile      |string           |中标通知书          |
		contractFile        |string           |备案合同            |
		manager             |string           |项目经理            |
		managerPhone        |string           |联系电话            |
		fixDays             |string           |定额工期            |
		content             |string           |施工内容            |
		managementAuditStatus|string          |监管审核状态        |
		managementAuditMemo  |string          |审核备注            |
		protectNo            |string          |安全施工措施备案号   |
		license              |string          |施工许可证号         |
		pictureFile          |string          |项目图片             |
		code                 |string          |项目代码             |
		state                |string          |状态                 |
		superviseAgency      |string          |监督机构             |
		builerCode           |string          |施工单位代码         |
		supervisorCode       |string          |监理单位代码         |
		desinger             |string          |设计单位名称         |
		buildingFloor        |int             |建筑层数             |
		structure            |string          |结构类型             |
		isCreate             |int             |是否进行中           |
		socialProvieCode     |string          |参保证明编号         |
		socialProvieDate     |timestamp       |参保日期             |
		injuryAuditStatus    |string          |工伤保险中心审核状态  |
		injuryAuditMemo      |string          |工伤保险中心审核备注  |
		source               |string          |数据来源             |
		implementStatus      |string          |设备实施状态         |
		implementMemo        |string          |设备实施备注         |
		responsiblePerson    |string          |项目责任人           |
		responsiblePersonPhone|string         |项目责任人联系电话    |
	    buildProjectCode      |string         |建设项目编码         |
	    platform              |string         |来源                |2
	    placePoint            |string         |经纬度              |
	
#### 示例

```json  
{
  "body":{
  	"operationFlag":"updateExternalProject",
  	"projectInfo":{
  		"relationId":56,          
		"name":"启东XXXXXX项目",                
		"phase":"主体",               
		"progress":"开工",           
		"isKey":1,               
		"position":"启东",            
		"address":"启东",             
		"type":1,               
		"qualityCode":"XXXXXXXXXX",         
		"securityCode":"XXXXXXXXXX",        
		"beginDateContract":"2018-09-20",   
		"endDateContract":"2018-12-20",     
		"beginDate":"2018-09-20",          
		"endDate":"2018-12-20",            
		"instroduction":"启东XXXXXX项目",      
		"builder":"XXXXXX建设",             
		"surveyor": "XXXXXX建设",           
		"supervisor":  "XXXXXX建设",        
		"constuctor": "XXXXXX建设",       
		"constuctorOrgCode": "XXXXXXXXXXXX",  
		"constuctorCode": "XXXXXXXXXXXX",     
		"buildingSize": 1987766,       
		"buildingCost":  87665,     
		"contractNo": "XXXXXXXXXXXX",        
		"identifier":  "XXXXXXXXXXXX",       
		"winBiddingFile": "XXXXXXXXXXXX",    
		"contractFile":"XXXXXXXXXXXX",        
		"manager":"XXXXXXXXXXXX",             
		"managerPhone": "XXXXXXXXXXXX",       
		"fixDays": "37",           
		"content":"XXXXXXXXXXXX",             
		"managementAuditStatus":1,
		"managementAuditMemo": "XXXXXXXXXXXX", 
		"protectNo":"XXXXXXXXXXXX",           
		"license":"XXXXXXXXXXXX",              
		"pictureFile": "XXXXXXXXXXXX",         
		"code":"XXXXXXXXXXXX",                 
		"state": "开工",               
		"superviseAgency":"XXXXXXXXXXXX",      
		"builerCode":"XXXXXXXXXXXX",           
		"supervisorCode": "XXXXXXXXXXXX",      
		"desinger": "XXXXXXXXXXXX",            
		"buildingFloor":24,        
		"structure": "XXXXXXXXXXXX",           
		"isCreate": 1,            
		"socialProvieCode":"XXXXXXXXXXXX",     
		"socialProvieDate": "XXXXXXXXXXXX",   
		"injuryAuditStatus": "XXXXXXXXXXXX",   
		"injuryAuditMemo":"XXXXXXXXXXXX",    
		"source": "XXXXXXXXXXXX",              
		"implementStatus": "XXXXXXXXXXXX",    
		"implementMemo": "XXXXXXXXXXXX",      
		"responsiblePerson": "XXXXXXXXXXXX",   
		"responsiblePersonPhone":"XXXXXXXXXXXX",
	    "buildProjectCode": "XXXXXXXXXXXX",
	    "placePoint":"XXXXXXXXXXXX",
	    "platform":2
  	}
  	
  }
}
```

#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 3.更新企业信息
### URL: /sys/sysOrganization/updateExternal
### Method:POST
#### Params
参数名                       |参数类型       |字段说明           |约束条件
----------------------------|---------------|------------------|------------------
body                        |               |                  |
    operationFlag           |string         |状态标志           |updateExternalOrg
    org                     |object         |部门信息           |
        relationOrgId       |string         |主键               |
        name                |string         |名称               |
        instroduction       |string         |企业描述           |
        platform            |string         |来源               |2
#### 示例

```json  
{
  "body":{
  	"operationFlag":"updateExternalOrg",
  	"org":[{
  		"name":"XXXXXXXXXXXX公司",                               
        "instroduction":"XXXXXXXXXXXX公司XXXXXXXXXXXXXXX",                          
        "relationOrgId": 37,
        "platform": 2,
  	}]
  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```

## 4.更新系统用户信息
### URL: /sys/sysUser/updateExternal
### Method:POST
#### Params
   参数名           |参数类型        |字段说明              |约束条件
--------------------|---------------|---------------------|------------------
body                |               |                     |
  operationFlag     |string         |状态标志             |updateExternalUser
  user              |object         |人员信息             |
    code            |string         |用户编码             |
    phone           |string         |用户手机号           |
    name            |string         |用户名               | 
    password        |string         |密码                 |
    relationUserId  |int            |主键                 |
    platform        |string         |来源                 |2

```json  
{
  "body":{
  	"operationFlag":"updateExternalUser",
     "user":{
	  		"code":"XXXXXXXXXXXX",              
	        "phone":"18976567879",                 
	        "name" :"XXXX",             
	        "password" :"XXXXXXXXXXXX",          
	        "platform" :2,             
	        "relationUserId" :87,
	        "status":0
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 5.删除项目信息
### URL: /project/projectInfo/deleteExternal
### Method:POST
#### Params
   参数名           |参数类型        |字段说明           |约束条件
--------------------|---------------|------------------|------------------
body                |               |                    |
  operationFlag     |string         |状态标志             |deleteExternalProject
  project           |array          |人员信息             |
    relationIds     |string         |主键                 |
     platform       |string         |来源                 |2
```json  
{
  "body":{
  	 "operationFlag":"deleteExternalProject",
     "user":{
	        "relationIds" :"87,34",
	        "platform":2
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 6.删除企业信息
### URL: /sys/sysOrganization/deleteExternal
### Method:POST
#### Params
   参数名           |参数类型        |字段说明           |约束条件
--------------------|---------------|------------------|------------------
body                |               |                   |
 operationFlag     |string         |状态标志             |deleteExternalOrg
  org              |array          |人员信息             |
    relationOrgIds |string         |主键                 |
    platform       |string         |来源                 |2
```json  
{
  "body":{
  	"operationFlag":"deleteExternalOrg",
     "org":{
	        "relationOrgIds" :"87,23",
	        "platform":2
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 7.删除系统用户信息
### URL: /sys/sysUser/deleteExternal
### Method:POST
#### Params
   参数名           |参数类型        |字段说明           |约束条件
--------------------|---------------|------------------|------------------
body                |               |                     |
 operationFlag      |string         |状态标志             |deleteExternalUser
  user              |array          |人员信息             |
    relationUserIds |string         |主键                 |
    platform        |string         |来源                 |2
```json  
{
  "body":{
  	"operationFlag":"deleteExternalUser",
     "user":{
	        "relationUserIds" :"87,23",
	        "platform":2
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```

## 8.新增项目人员信息（工种为空时调用管理员）
### URL: /project/projectWorker/insertExternal（普通工人）
### URL: /project/projectAdministrator/insertExternal （管理员）
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|--------------- |------------------|------------------
body                        |                 |                  |
  operationFlag             |string           |状态标志           |insertExternalWorker/insertExternalAdministrator
     worker                 |object           |人员信息           |
        relationWorkerId    |int              |主键              |
		name                |string           |人员名称           |
		enterStatus         |string           |进场状态           |
		enterTime           |timestamp        |进场时间           |
		peopleType          |int              |人员类别           |
		documentType        |int              |证件类型           |
		identityCode        |string           |身份证号           |
		birthDate           |string           |生日               |
		sex                 |int              |性别              |
		nation              |string           |籍贯              |
		telephoneNumber     |string           |手机号码          |
		politicalStatus     |string           |政治面貌          |
		homeAddress         |string           |家庭住址          |
		tempAddre           |string           |暂住地址           |
		isAdd               |int              |是否加入公会       |
		addTime             |timestamp        |加入公会时间       |
		educationLevel      |string           |文化程度           |
		isSickness          |int              |是否有重大病史      |
		emergencyPeople     |string           |紧急联系人姓名      |
		emergencyTel        |string           |紧急联系人电话      |
		workStartTime       |timestamp        |开始工作时间        |
		accommodationType   |string           |工人住宿类型        |
		relationProjectId   |int              |所属总包项目        |
		contractorType      |int              |总包/分包           |
		subProjectId        |int              |分包项目            |
		relationWorkId      |int              |工种id              |
		relationTeamId      |int              |班组id              |
		platform            |string           |来源                |2
		projectMasterWorkType  |object           |                    |
		      platform      |int              |来源标记             |2
	          name          |string           |名称                |
	          relationWorkId|int              |主键                |
	    projectMasterTeam   |object           |                    |
		      platform      |int              |来源标记             |2
	          name          |string           |名称                |
	          relationProjectId|int           |主键                |
	          relationTeamId|int              |主键                |
#### 示例    
```json  
{
  "body":{
     "operationFlag":"insertExternalWorker",
     "operationFlag":"insertExternalAdministrator",
     "worker":{
	        "relationWorkerId": 26,              
		    "name": "xxxx",                
		    "enterStatus": "进场",         
		    "enterTime" : "2018-07-20",          
		    "peopleType" : 1,        
		    "documentType" : 1,       
		    "identityCode" : "XXXXXXXXXXXXXXXXXXXXXXXX",       
		    "birthDate" : "2018-02",          
		    "sex" : 1,              
		    "nation" : "xxxx",            
		    "telephoneNumber": "18792782223",     
		    "politicalStatus" : "xxxx",    
		    "homeAddress" : "xxxx",        
		    "tempAddre"  : "xxxx",         
		    "isAdd" : 1,              
		    "addTime" : "2018-07-20",            
		    "educationLevel" : "xxxx",     
		    "isSickness" : 0,         
		    "emergencyPeople" : "xxxx",   
		    "emergencyTel": "xxxx",       
		    "workStartTime"  : "2018-07-20",     
		    "accommodationType" : "xxxx",  
		    "relationProjectId" : 1,        
		    "contractorType" : 2,     
		    "subProjectId"  : 36,                
		    "platform"  : 2 ,
		    "relationWorkId" :87,
		    "relationTeamId" :12,
		     "projectMasterWorkType":{
			        "relationWorkId" :87,
			        "name":"XXXXXXXXXXXX",
			        "platform":2
			  	},
			 "projectMasterTeam":{
			        "relationTeamId" :12,
			        "name":"XXXXXXXXXXXX",
			        "relationProjectId": 78,   
			        "platform":2
			  	}      
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 9.更新项目人员信息（工种为空时调用管理员）
### URL: /project/projectWorker/updateExternal（普通工人）
### URL: /project/projectAdministrator/updateExternal （管理员）
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|--------------- |------------------|------------------
body                        |                |                  |
  operationFlag             |string          |状态标志           |updateExternalWorker/updateExternalAdministrator
    worker                  |object          |人员信息           |
        relationWorkerId    |int              |主键              |
		name                |string           |人员名称           |
		enterStatus         |string           |进场状态           |
		enterTime           |timestamp        |进场时间           |
		peopleType          |int              |人员类别           |
		documentType        |int              |证件类型           |
		identityCode        |string           |身份证号           |
		birthDate           |string           |生日               |
		sex                 |int              |性别               |
		nation              |string           |籍贯              |
		telephoneNumber     |string           |手机号码          |
		politicalStatus     |string           |政治面貌          |
		homeAddress         |string           |家庭住址          |
		tempAddre           |string           |暂住地址           |
		isAdd               |int              |是否加入公会       |
		addTime             |timestamp        |加入公会时间       |
		educationLevel      |string           |文化程度           |
		isSickness          |int              |是否有重大病史      |
		emergencyPeople     |string           |紧急联系人姓名      |
		emergencyTel        |string           |紧急联系人电话      |
		workStartTime       |timestamp        |开始工作时间        |
		accommodationType   |string           |工人住宿类型        |
		projectRelationId   |string           |所属总包项目        |
		contractorType      |int              |总包/分包           |
		subProjectId        |int              |分包项目            |
		platform            |string           |来源                |2
		relationWorkId      |int              |工种id              |
		relationTeamId      |int              |班组id              |
		projectMasterWorkType  |object           |                    |
		      platform      |int              |来源标记             |2
	          name          |string           |名称                |
	          relationWorkId|int              |主键                |
	    projectMasterTeam   |object           |                    |
		      platform      |int              |来源标记             |2
	          name          |string           |名称                |
	          relationProjectId|int           |主键                |
	          relationTeamId|int              |主键                |
	          type          |int              |区分 普通岗位1 管理岗位2 |


#### 示例    
```json  
{
  "body":{
  	"operationFlag":"updateExternalWorker",
  	"operationFlag":"updateExternalAdministrator",
     "worker":{
	        "relationWorkerId": 26,              
		    "name": "xxxx",                
		    "enterStatus": "进场",         
		    "enterTime" : "2018-07-20",          
		    "peopleType" : 1,        
		    "documentType" : 1,       
		    "identityCode" : "XXXXXXXXXXXXXXXXXXXXXXXX",       
		    "birthDate" : "2018-02",          
		    "sex" : 1,              
		    "nation" : "xxxx",            
		    "telephoneNumber": "18792782223",     
		    "politicalStatus" : "xxxx",    
		    "homeAddress" : "xxxx",        
		    "tempAddre"  : "xxxx",         
		    "isAdd" : 1,              
		    "addTime" : "2018-07-20",            
		    "educationLevel" : "xxxx",     
		    "isSickness" : 0,         
		    "emergencyPeople" : "xxxx",   
		    "emergencyTel": "xxxx",       
		    "workStartTime"  : "2018-07-20",     
		    "accommodationType" : "xxxx",  
		    "relationProjectId" : 1,        
		    "contractorType" : 2,     
		    "subProjectId"  : 36,      
		    "platform"  : 2 ,
		    "relationWorkId" :87,
		    "relationTeamId" :12,
		     "projectMasterWorkType":{
			        "relationWorkId" :87,
			        "name":"XXXXXXXXXXXX",
			        "platform":2
			  	},
			 "projectMasterTeam":{
			        "relationTeamId" :12,
			        "name":"XXXXXXXXXXXX",
			        "relationProjectId": 78,   
			        "platform":2,
			        "type":1
			  	}     
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 10.人员进场履历
### URL: /project/projectWorker/insertRecordExternal（普通工人）
### URL: /project/projectAdministrator/insertRecordExternal （管理员）
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|--------------- |------------------|------------------
body                        |                 |                  |
	    record              |array            |                    |
	          operationFlag |string           |状态标志           |insertRecordExternalWorker/insertRecordExternalAdministrator
		      platform      |int              |来源标记             |2
	          userProjectId |int              |用户项目ID           |
	          relationProjectId|int           |主键                 |
	          enterStatus   |int              |进场状态             |
	          enterTime     |timestamp        |时间                |
   
#### 示例    
```json  
{
  "body":{
     "record":[{
     	"operationFlag":"insertRecordExternalWorker",
		"enterStatus" :"退场",
		"userProjectId":23,
		"relationProjectId": 78,   
		"platform":2,
		"enterTime":"2018-02-09"
		}]
  	}
}
``` 

## 11.删除项目人员信息（工种为空时调用管理员）
### URL: /project/projectWorker/deleteExternal（普通工人）
### URL: /project/projectAdministrator/deleteExternal （管理员）
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|--------------- |------------------|------------------
body                        |                |                  |
  worker                    |array           |人员信息           |
        operationFlag       |string          |状态标志           |deleteExternalWorker/deleteExternalAdministrator
        relationProjectId   |int              |主键              |
        relationWorkerIds   |string           |主键              |
		platform            |string           |来源              |2

#### 示例    
```json  
{
  "body":{
     "worker":[{
            "operationFlag":"deleteExternalWorker" ,  
            "relationProjectId" : 20,           
		    "relationWorkerIds" : "20,23",       
		    "platform"  : 2         
	  	}]
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息               |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 12.更新班组信息
### URL: /dictionary/projectMasterTeam/updateExternal
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|-----------------|------------------|------------------
body                        |                 |                     |
  operationFlag             |string           |状态标志           |updateExternalTeam
  projectMasterTeam         |object           |                  |
		      platform      |int              |来源标记           |2
	          name          |string           |名称              |
	          relationTeamId|int              |主键              |
```json  
{
  "body":{
  	"operationFlag":"updateExternalTeam",
     "projectMasterTeam":{
	        "relationTeamId" :87,
	        "name":"XXXXXXXXXX",
	        "platform":2
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```

## 13.更新工种信息
### URL: /dictionary/projectMasterWorkType/updateExternal
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|-----------------|------------------|------------------
body                        |                 |                  |
  operationFlag             |string           |状态标志           |updateExternalWorkType
  projectMasterWorkType     |object           |                  |
		      platform      |int              |来源标记           |2
	          name          |string           |名称               |
	          relationWorkId|int              |主键               |
```json  
{
  "body":{
  	 "operationFlag":"updateExternalWorkType",
     "workTypeDictionary":{
	        "relationWorkId" :87,
	        "name":"XXXXXXXXXX",
	        "platform":2
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```

## 14.新增考勤机
### URL: /project/projectAttendance/insertExternal
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|--------------- |------------------|----------------
body                        |                 |                  |
  operationFlag             |string           |状态标志          |insertExternalAttendance
  attendance                |object           |考勤机            |
        relationDeviceId    |int              |主键              |
        relationProjectId   |int              |项目id            |
		deviceNo            |string           |设备编号          |
		manufactor          |string           |厂家              |
		platform            |string           |来源              |2

#### 示例    
```json  
{
  "body":{
  	 "operationFlag":"insertExternalAttendance",
     "attendance":{
	        "relationDeviceId": 26,    
            "relationProjectId": 78,           
		    "deviceNo": "xxxx", 
		    "manufactor":"xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",       
		    "platform"  : 2         
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```

## 15.更新考勤机
### URL: /project/projectAttendance/updateExternal
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|--------------- |------------------|----------------
body                        |                |                  |
  operationFlag             |string           |状态标志          |updateExternalAttendance
  attendance                |object           |考勤机            |
        relationDeviceId    |int              |主键              |
        relationProjectId   |int              |项目id            |
        deviceNo            |string           |设备编号          |
		manufactor          |string           |厂家              |
		platform            |string           |来源              |2

#### 示例    
```json  
{
  "body":{
  	 "operationFlag":"updateExternalAttendance",
     "attendance":{
	        "relationDeviceId": 26,    
            "relationProjectId": 78,           
		    "deviceNo": "xxxx", 
		    "manufactor":"xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",       
		    "platform"  : 2          
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```

## 16.删除考勤机
### URL: /project/projectAttendance/deleteExternal
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|--------------- |------------------|----------------
body                        |                 |                 |
  operationFlag             |string           |状态标志          |deleteExternalAttendance
  attendance                |array            |考勤机            |
        relationDeviceIds   |string           |主键              |
        relationProjectId   |int              |项目id            |
		platform            |string           |来源              |2

#### 示例    
```json  
{
  "body":{
  	 "operationFlag":"deleteExternalAttendance",
     "attendance":{
	        "relationDeviceIds": "26,67", 
	        "relationProjectId": 78,           
		    "platform"  : 2         
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 

#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}
```
## 17.新增考勤履历
### URL: /project/projectAttendanceDetail/insertExternal
### Method:POST
#### Params
   参数名                    |参数类型        |字段说明           |约束条件
----------------------------|--------------- |------------------|----------------
body                        |                |                  |
  operationFlag             |string           |状态标志          |insertExternalAttendanceDetail
  record                    |object           |考勤履历           |
        relationProjectId   |string           |项目id             |
        deviceNo            |string           |设备id             |
        relationUserId      |string           |设备id             |
        name                |string           |姓名              |
		identityCode        |string           |身份证编号        |
		nativePlace         |string           |籍贯              |
		workType            |string           |工种              |
		team                |string           |班组              |
	    attendanceTime      |timestamp        |考勤时间          |
		platform            |string           |来源              |2

#### 示例    
```json  

{
  "body":{
  	 "operationFlag":"insertExternalAttendanceDetail",
     "record":{
     	    "relationProjectId": 23,    
	        "deviceNo": "XXXXXXXXXXXXXX",    
            "name": "XXXX",           
		    "identityCode": "XXXXXXXXXXXXXXXXXXXXX", 
		    "nativePlace":"江苏",      
		    "workType":"工种",
		    "team":"班组", 
		    "attendanceTime":"2018-09-20",
		    "platform"  : 2         
	  	}
  	  }
}
```
#### 返回接口
#### Params
        参数名       |参数类型         |字段说明           |约束条件
--------------------|-----------------|------------------|------------------
        code        |string           |200               |
        message     |string           |信息              |
        success     |boolean          |true              | 


#### 示例        
```json  
{
  "code": "xxxx",
  "message": "xxxx",
  "suceess":true
}

二.智慧工地定时取数据接口
## 1.项目信息
### URL:/project/sendProjectToPM.whtml
### Condition:项目进展为"在建/开工"
### Params:参照推送时的项目信息
### Remark:企业信息在项目信息中包含
### 回传最大ID:
### URL:/project/getProjectToPM.whtml
### Params:{"code":1/0,"no":100}

## 2.人员信息
### URL:/userproject/sendUserToPM.whtml
### Condition:状态是"进场"的人员
### Params:参照推送时的人员信息
### Remark:工种信息，班组信息在人员信息中包含
### 回传最大ID:
### URL:/userproject/getUserToPM.whtml
### Params:{"code":1/0,"no":100}

## 3.考勤设备
### URL:/device/sendDeviceToPM.whtml
### Condition:有设备信息的设备
### Params:参照推送时的考勤设备信息
### 回传最大ID:
### URL:/device/getDeviceToPM.whtml
### Params:{"code":1/0,"no":100}

## 4.考勤记录
### URL:/device/sendRecordToPM.whtml
### Params:参照推送时的考勤设备信息
### 回传最大ID:
### URL:/device/getDeviceResultToPM.whtml
### Params:{"code":1/0,"no":100}

说明：code :1 成功 0 失败
      no:调第一个接口返回的最大id

