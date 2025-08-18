
接口1:查询版本列表   
根据project_id执行Get请求
参数:
project_id
Return:
```{
	"code":0,
	"data":
		[
			{
				"id":111                   //版本id
				 "name":"v1.0.0"           //版本名
				 "description": "测试"     //描述
				 "project_id":1            //关联项目id
				 "start_date": "2024-07-10 00:00:00"   // 开始时间
				 "release_date":"2024-07-10 00:00:00"  //发布时间
				 "released"  : "true"      //是否已发布
				 "sequence" : 1            //版本序列号
			}
		],
	"msg": "请求成功"
	}
```