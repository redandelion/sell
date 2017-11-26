# sell
微信小程序


#	API 列表

#	商品列表（详情）：GET
	API :
    uri: /sell/buyer/product/list 
    参数： 无             
    返回值：                               
	    {     
          "code": 0,
          "msg": "成功",
          "data": [
		    {
		      "name": "我的最爱",
		      "type": 1,
		     "foods": [
			{
			  "id": "id22131",
			  "name": "烤良鸡翅",
			  "price": 12.5,
			  "description": "西班牙风味",
			  "icon": "http://165465161.jpg"
			}
		      ]
		    }
		 ]
	    }
#	创建订单API：POST
	uri: /sell/buyer/order/create
	参数：
		name:"我是大爷"
		phone:15454845685
		address:北理工
		openid:sadsaf1115641465165
		items:[{
			productId:"123456",
			productQuantity:3
		}]
	返回值：
		{
		  "code": 0,
		  "msg": "成功",
		  "data": {
		    "orderId": "1511667150077554503"
		  }
		}
	
#	查询订单列表API: GET
	uri: /sell/buyer/order/list
	参数：
		openid：sadsaf1115641465165
		page：（值可以为空）默认为第0页
		size：（值可以为空）页面大小默认为10条数据
	返回值：
		{
		  "code": 0,
		  "msg": "成功",
		  "data": [
		    {
		      "orderId": "1511574918448685724",
		      "buyerName": "我是大爷",
		      "buyerPhone": "15245254565",
		      "buyerAddress": "北理工",
		      "buyerOpenid": "sadsaf1115641465165",
		      "orderAmount": 45,
		      "orderStatus": 0,
		      "payStatus": 0,
		      "createTime": 1511574918,
		      "updateTime": 1511574918
		    },
		    {
		      "orderId": "1511671508556506623",
		      "buyerName": "我是二爷",
		      "buyerPhone": "15245254565",
		      "buyerAddress": "北理工",
		      "buyerOpenid": "sadsaf1115641465165",
		      "orderAmount": 45,
		      "orderStatus": 0,
		      "payStatus": 0,
		      "createTime": 1511671507,
		      "updateTime": 1511671507
		    }
		  ]
		}
#	查询订单详情API: GET
	uri: /sell/buyer/order/detail
	参数：
		openid：sadsaf1115641465165
		orderId:1511672826603710195		
	返回值：
		{
		  "code": 0,
		  "msg": "成功",
		  "data": {
		    "orderId": "1511672826603710195",
		    "buyerName": "我是大爷",
		    "buyerPhone": "15245254565",
		    "buyerAddress": "北理工",
		    "buyerOpenid": "sadsaf1115641465165",
		    "orderAmount": 57.5,
		    "orderStatus": 0,
		    "payStatus": 0,
		    "createTime": 1511672825,
		    "updateTime": 1511672825,
		    "orderDetailList": [
		      {
			"detailId": "1511672826649496283",
			"orderId": "1511672826603710195",
			"productId": "123456",
			"productName": "燕窝",
			"productPrice": 15,
			"productQuantity": 3,
			"productIcon": "http://15154515.jpg"
		      },
		      {
			"detailId": "1511672826741990055",
			"orderId": "1511672826603710195",
			"productId": "id12515",
			"productName": "烤良鸡翅",
			"productPrice": 12.5,
			"productQuantity": 1,
			"productIcon": "http://1544515.jpg"
		      }
		    ]
		  }
		}
#	取消订单API: POST
	uri: /sell/buyer/order/cancel
	参数：
		openid：sadsaf1115641465165
		orderId:1511671508556506623	
	返回值：
		{
		  "code": 0,
		  "msg": "成功"
		}







