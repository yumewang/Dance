# API Define for iOS app

### 1. 用户登陆

	功能说明：用户在输入账号与密码后，检查密码是否正确、状态是否为 active，两个条件同事满足后实现登陆的操作
    URL：https://xxx/v1/login
    请求方式：POST
    
请求参数：

| 参数名        | 类型   |  必须  | 说明 |
| :--------:   | :-----:  | :----:  |-----|
| name | String | Yes | 用户账号的登陆标识 |
| password | String | Yes | 用户账号的登陆密码 |

服务器返回参数：

	{
		Permissions:[
		{
			_id: "545c204639211f28025fa687",
			action: "delete",
			subject: "stationManage",
			__v: 0
		},
		{
			_id: "545c204639211f28025fa683",
			action: "search",
			subject: "accountManage",
			__v: 0
		},
	],
	
	userInfo:{
			_id": "5493e8670dabb66831ed2ae4",
			"username": "18888888888",
			"realname": "陈程",
			"status": "active",
			"belongs": "5493e83869d6c161316b40ca",
			"userType": "MaintenanceCompanyStaff",
			"createdDate": "2014-12-19T08:57:11.928Z"
		}
	}
	
Or

	{
		msg: "#err:You password have error!",
		code: 10012
	}
	
Or

	{
		msg: "#err:You account is not active!",
		code: 10013
	}