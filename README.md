# sell
微信小程序


#	API 列表

#	商品列表（详情）：
	API :
    GET /sell/buyer/product/list 
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
#	创建订单API：
	uri:/sell/buyer/order/create
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
