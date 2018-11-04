## 身份证加密接口文档说明
## 概述 
本接口适用于第三方平台接入实名制项目,数据传输过程中对重要信息进行加密，
不能明文传输，加强安全管理。  
	
## 版本
v1.0
## 接口使用说明 
### 1．将我们提供的 jar 包(Encryption)导入工程中 
### 2．工程中 import com.saier.erp.page.utils.Encryption; 
### 3．方法调用 

#### 1 方法名称 : encryptAES
参数 | 参数类型 | 描述|约束条件  
 ----|------|------ |------     
 userId | string| 身份证 |*
### 2 返回类型 :String
### 4.示例：
  String decontent = Encryption.encryptAES("320681199006121227");    
decontent  : 2ArG+Q3OpfHwDeaIIG4SkQ4xnMElPMYthiNko0N2TRU= 
 
