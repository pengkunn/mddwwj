
# 业务服务器接口


## 1.用户相关
### 1.1.用户登录
 URL: auth/login    

 输入
```json 
{"code":"test"}   
```

 输出  
```json 
{
    "errcode": 0,
    "user": {
        "id": 1,
        "wxOpenId": 0,
        "wxUnionId": 0,
        "name": "test",
        "headImgUrl": "0",
        "coin": 1004,
        "invitationCode": "32131",
        "createTime": "2017-11-09T15:33:42.000Z",
        "updateTime": "2017-11-15T13:54:20.000Z"
    }
}
```

### 1.2.用户登出

 URL: users/logout    

 输入  
```json 
 {}    
```
 输出  
```json 
{
    "errcode": 0
}  
```

### 1.3.获取用户信息

 URL: users/getUserInfo    

 输入  
```json 
 {}    
```
 输出  
```json 
{
    "errcode": 0,
    "user": {
        "id": 1,
        "wxOpenId": 0,
        "wxUnionId": 0,
        "name": "test",
        "headImgUrl": "0",
        "coin": 1004,
        "invitationCode": "32131",
        "createTime": "2017-11-09T15:33:42.000Z",
        "updateTime": "2017-11-15T13:54:20.000Z"
    }
}  
```

### 1.4.添加邮寄地址

 URL  : users/addAddress    

 输入  
```json 
{ "contact": "user1", "phone_number": "1234567", "province": "北京市","municipality":"北京市","county":"朝阳区", "address": "XX小区X号楼212"}
```
 输出  
```json 
{
    "errcode": 0,
    "address_id": 2
}  
```


### 1.5.更新邮寄地址

 URL  : users/updateAddress    

 输入  
```json 
{ "address_id":1, "user_id":1,"contact": "user1", "phone_number": "1234567", "province": "北京市","municipality":"北京市","county":"朝阳区", "address": "XX小区X号楼212"}
```
 输出  
```json 
{
    "errcode": 0
}   
```


### 1.6.删除邮寄地址

 URL : users/deleteAddress    

 输入  
```json 
{ "address_id":1, "user_id":1}    
```
 输出  
```json 
{
    "errcode": 0
} 
```

### 1.7.获取用户代币

 URL  : users/getCoin
 
 输入  
```json 
{}  
```
 输出  
```json 
{
    "errcode": 0,
    "coin": 1014
}
```

### 1.8.获取用户抓取娃娃排行

 URL  : users/getUserRank
 
 输入  
```json 
{}  
```
 输出  
```json 
{
    "errcode": 0,
    "rank": [
        {
            "name": "用户A",
            "img": "/images/a.png"
        },
        {
            "name": "用户B",
            "img": "/images/b.png"
        }
    ],
    "self_order": 18
}
```
###  1.9. 获取app下载地址
 URL  : users/getAppUrl
 
 输入  
```json 
{}  
```
 输出  
```json
{
    "errcode": 0,
    "url": "https://github.com/wizardforcel/markdown-simple-world/blob/master/1.md"
}
```
###  1.10. 兑换邀请码
 URL  : users/useInvitationCode
 
 输入  
```json 
{"invitation_code":"12355"}
```
 输出  
```json
{
    "errcode": 0,
    "add_coin": 15
}
```
###  1.11. 获取用户周卡信息
 URL  : users/getWeekCard
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "week_card": {
        "id": 1,
        "userId": 2,
        "cardType": 1,
        "expireTime": "2018-02-04T13:30:39.000Z",
        "createTime": "2017-12-06T13:30:39.000Z",
        "updateTime": "2017-12-06T13:32:12.000Z"
    }
}
```
###  1.12. 获取用户月卡信息
 URL  : users/getMonthCard
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "week_card": {
        "id": 2,
        "userId": 2,
        "cardType": 2,
        "expireTime": "2018-02-04T13:30:39.000Z",
        "createTime": "2017-12-06T13:30:39.000Z",
        "updateTime": "2017-12-06T13:32:12.000Z"
    }
}
```
###  1.13. 领取周卡奖励
 URL  : users/receiveWeekCardReward
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "add_coin": 25
}
```
###  1.14. 领取月卡卡奖励
 URL  : users/receiveMonthCardReward
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "add_coin": 25
}
```

###  1.15. 获取我的积分
 URL  : users/getPoint
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "point": 0
}
```

###  1.16. 获取我的积分变更记录
 URL  : users/getPointRecords
 
 输入  
```json 
{"pageindex":0,"pagecount":6}
```
 输出  
```json
{
    "errcode": 0,
    "claw_records": [
        {
            "id": 1,
            "userId": 1,
            "point": 25,
            "text": "test add",
            "createTime": "2017-12-03T20:21:23.000Z",
            "updateTime": "2017-12-03T20:21:24.000Z"
        }
    ],
    "count": 1
}
```

###  1.17. 获取我的抓娃娃记录
 URL  : users/getClawRecords
 
 输入  
```json 
{"pageindex":0,"pagecount":6}
```
 输出  
```json
{
    "errcode": 0,
    "claw_records": [
        {
            "id": 1,
            "remoteGameId": "0",
            "userId": 1,
            "clawerId": 1,
            "spendCoin": 1,
            "dollTypeId": 1,
            "result": null,
            "video": null,
            "startTime": "2017-11-10T16:33:24.000Z",
            "endTime": null,
            "createTime": "2017-11-10T16:33:24.000Z",
            "updateTime": "2017-11-10T16:33:24.000Z",
            "user_id": 1
        },
        {
            "id": 2,
            "remoteGameId": "0",
            "userId": 1,
            "clawerId": 1,
            "spendCoin": 1,
            "dollTypeId": 1,
            "result": null,
            "video": null,
            "startTime": "2017-11-10T16:34:39.000Z",
            "endTime": null,
            "createTime": "2017-11-10T16:34:39.000Z",
            "updateTime": "2017-11-10T16:34:39.000Z",
            "user_id": 1
        },
        {
            "id": 3,
            "remoteGameId": "0",
            "userId": 1,
            "clawerId": 1,
            "spendCoin": 1,
            "dollTypeId": 1,
            "result": 1,
            "video": null,
            "startTime": "2017-11-15T13:15:06.000Z",
            "endTime": "2017-11-15T13:15:40.000Z",
            "createTime": "2017-11-15T13:15:06.000Z",
            "updateTime": "2017-11-15T13:15:40.000Z",
            "user_id": 1
        },
        {
            "id": 4,
            "remoteGameId": "0",
            "userId": 1,
            "clawerId": 1,
            "spendCoin": 1,
            "dollTypeId": 1,
            "result": 1,
            "video": null,
            "startTime": "2017-11-15T13:29:47.000Z",
            "endTime": "2017-11-15T13:30:21.000Z",
            "createTime": "2017-11-15T13:29:47.000Z",
            "updateTime": "2017-11-15T13:30:21.000Z",
            "user_id": 1
        },
        {
            "id": 5,
            "remoteGameId": "0",
            "userId": 1,
            "clawerId": 1,
            "spendCoin": 1,
            "dollTypeId": 1,
            "result": 0,
            "video": null,
            "startTime": "2017-11-15T13:32:19.000Z",
            "endTime": "2017-11-15T13:32:41.000Z",
            "createTime": "2017-11-15T13:32:19.000Z",
            "updateTime": "2017-11-15T13:32:41.000Z",
            "user_id": 1
        },
        {
            "id": 6,
            "remoteGameId": "0",
            "userId": 1,
            "clawerId": 1,
            "spendCoin": 1,
            "dollTypeId": 1,
            "result": 0,
            "video": null,
            "startTime": "2017-11-15T13:33:34.000Z",
            "endTime": "2017-11-15T13:33:49.000Z",
            "createTime": "2017-11-15T13:33:34.000Z",
            "updateTime": "2017-11-15T13:33:49.000Z",
            "user_id": 1
        }
    ],
    "count": 261
}
```
###  1.18. 获取我的全部地址
 URL  : users/getAddresses
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "addresses": [
        {
            "id": 6,
            "userId": 2,
            "contact": "user2",
            "phoneNumber": "1234567",
            "province": "北京市",
            "municipality": "北京市",
            "county": "朝阳区",
            "address": "XX小区X号楼212",
            "createTime": "2017-11-20T13:11:37.000Z",
            "updateTime": "2017-11-20T13:11:37.000Z"
        }
    ]
}
```

###  1.19. 获取我的邀请码信息
 URL  : users/getInvitationCodeUsedInfo
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "total_reward_conis": 360,
    "use_count": 5
}
```

###  1.20. 获取公告
 URL  : users/getBulletins
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "bulletins": [
        {
            "id": 1,
            "title": "1234",
            "content": "content",
            "startTime": "2018-01-22T12:00:00.000Z",
            "endTime": "2018-01-29T12:00:00.000Z",
            "enable": 1,
            "createTime": "2018-01-21T16:09:17.000Z",
            "updateTime": "2018-01-22T02:59:56.000Z"
        },
        {
            "id": 2,
            "title": "1234",
            "content": "content",
            "startTime": "2018-01-22T12:00:00.000Z",
            "endTime": "2018-01-29T12:00:00.000Z",
            "enable": 1,
            "createTime": "2018-01-22T02:48:55.000Z",
            "updateTime": "2018-01-22T02:48:55.000Z"
        }
    ]
}
```
###  1.21. 获取每日登录奖励配置
 URL  : users/getLoginRewards
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
    "loginRewards": [
        {
            "id": 1,
            "type": 0,
            "value": 10,
            "index": 0,
            "imgUrl": " ",
            "createTime": "2018-01-24T16:21:56.000Z",
            "updateTime": "2018-01-24T16:21:57.000Z"
        },
        {
            "id": 2,
            "type": 1,
            "value": 10,
            "index": 1,
            "imgUrl": " ",
            "createTime": "2018-01-24T16:21:56.000Z",
            "updateTime": "2018-01-24T16:21:57.000Z"
        },
        {
            "id": 3,
            "type": 0,
            "value": 20,
            "index": 2,
            "imgUrl": " ",
            "createTime": "2018-01-24T16:21:56.000Z",
            "updateTime": "2018-01-24T16:21:57.000Z"
        },
        {
            "id": 4,
            "type": 1,
            "value": 20,
            "index": 3,
            "imgUrl": " ",
            "createTime": "2018-01-24T16:21:56.000Z",
            "updateTime": "2018-01-24T16:21:57.000Z"
        },
        {
            "id": 5,
            "type": 0,
            "value": 30,
            "index": 4,
            "imgUrl": " ",
            "createTime": "2018-01-24T16:21:56.000Z",
            "updateTime": "2018-01-24T16:21:57.000Z"
        },
        {
            "id": 6,
            "type": 1,
            "value": 30,
            "index": 5,
            "imgUrl": " ",
            "createTime": "2018-01-24T16:21:56.000Z",
            "updateTime": "2018-01-24T16:21:57.000Z"
        },
        {
            "id": 7,
            "type": 0,
            "value": 40,
            "index": 6,
            "imgUrl": " ",
            "createTime": "2018-01-24T16:21:56.000Z",
            "updateTime": "2018-01-24T16:21:57.000Z"
        }
    ]
}
```

  ###  1.22. 领取每日登录奖励
 URL  : users/receiveLoginReward
 
 输入  
```json 
{}
```
 输出  
```json
{
    "errcode": 0,
}
```
---

## 2.娃娃机相关
###  2.1.获取娃娃列表

 URL  : clawers/getDollTypesList    
 输入  
```json 
 {"pageindex":0,"pagecount":6,"tag":1}
```
 输出  
```json 
{
    "errcode": 0,
    "doll_types": [
        {
            "id": 1,
            "name": "doll1",
            "price": 1,
            "convertCoinCount": 10,
            "img": "images/item1.png",
            "description": "images/item1.png",
            "tags": [
                1,
                2,
                3
            ],
            "status": 0
        },
        {
            "id": 2,
            "name": "doll2",
            "price": 2,
            "convertCoinCount": 12,
            "img": "images/item2.png",
            "description": "images/item2.png",
            "tags": [
                1,
                2,
                3
            ],
            "status": 0
        },
        {
            "id": 3,
            "name": "doll3",
            "price": 3,
            "convertCoinCount": 13,
            "img": "images/item3.png",
            "description": "images/item3.png",
            "tags": [
                1,
                2,
                3
            ],
            "status": 0
        },
        {
            "id": 4,
            "name": "doll4",
            "price": 4,
            "convertCoinCount": 11,
            "img": "images/item3.png",
            "description": "images/item4.png",
            "tags": [
                1,
                2,
                3
            ],
            "status": 0
        },
        {
            "id": 9,
            "name": "doll9",
            "price": 9,
            "convertCoinCount": 33,
            "img": "images/item9.png",
            "description": "images/item9.png",
            "tags": [
                1,
                3
            ],
            "status": 0
        },
        {
            "id": 10,
            "name": "doll10",
            "price": 10,
            "convertCoinCount": 44,
            "img": "images/item10.png",
            "description": "images/item10.png",
            "tags": [
                1
            ],
            "status": 0
        }
    ]
}
```


###  2.2.获取娃娃机列表

 URL  : clawers/getClawersList    
 
 输入  
```json 
{"doll_type_id":1,"pageindex":0,"pagecount":6}    
```
 输出  
```json 
 {
    "errcode": 0,
    "clawers": [
        {
            "id": 1,
            "name": "c1",
            "dollTypeId": 1,
            "ip": "1",
            "camera1": "1",
            "camera2": "1",
            "status": 0,
            "dollType": {
                "id": 1,
                "name": "doll1",
                "price": 1,
                "img": "1",
                "description": "1",
                "convertCoinCount": 10,
                "createTime": "2017-11-09T16:40:31.000Z",
                "updateTime": "2017-11-09T16:40:32.000Z"
            },
            "currentUser": null,
            "currentClawRecord": null,
            "timerId": -1
        },
        {
            "id": 11,
            "name": "c11",
            "dollTypeId": 1,
            "ip": "1",
            "camera1": "1",
            "camera2": "1",
            "status": 0,
            "dollType": {
                "id": 1,
                "name": "doll1",
                "price": 1,
                "img": "1",
                "description": "1",
                "convertCoinCount": 10,
                "createTime": "2017-11-09T16:40:31.000Z",
                "updateTime": "2017-11-09T16:40:32.000Z"
            },
            "currentUser": null,
            "currentClawRecord": null,
            "timerId": -1
        }
    ]
}   
```


###  2.3.获取娃娃机详情

 URL  : clawers/getClawerDetail    

 输入  
```json 
 {"clawer_id":2}   
```
 输出  
```json 
 {
    "errcode": 0,
    "clawer": {
        "id": 2,
        "name": "c2",
        "dollTypeId": 2,
        "ip": "1",
        "camera1": "1",
        "camera2": "1",
        "status": 0,
        "dollType": {
            "id": 2,
            "name": "doll2",
            "price": 2,
            "img": "1",
            "description": "2",
            "convertCoinCount": 12,
            "createTime": "2017-11-09T16:40:31.000Z",
            "updateTime": "2017-11-09T16:40:32.000Z"
        },
        "currentUser": null,
        "currentClawRecord": null,
        "timerId": -1
    }
} 
```




###  2.4.获取娃娃机成功抓取记录

 URL  : clawers/getClawerSuccessRecord    

 输入  
```json 
{"clawer_id":1}
```
 输出  
```json 
{
    "errcode": 0,
    "records": [
        {
            "id": 50,
            "userId": 1,
            "clawerId": 2,
            "spendCoin": 2,
            "dollTypeId": 2,
            "result": 1,
            "video": null,
            "startTime": "2017-11-17T04:58:01.000Z",
            "endTime": "2017-11-17T04:58:34.000Z",
            "createTime": "2017-11-17T04:58:01.000Z",
            "updateTime": "2017-11-17T04:58:34.000Z",
            "user_id": 1,
            "user": {
                "id": 1,
                "wxOpenId": 0,
                "wxUnionId": 0,
                "name": "test",
                "headImgUrl": "0",
                "coin": 944,
                "createTime": "2017-11-09T15:33:42.000Z",
                "updateTime": "2017-11-17T12:26:53.000Z"
            }
        }
    ]
}
```


###  2.5.开始抓娃娃游戏

 URL  : clawers/start    

 输入  
```json 
{"clawer_id":1} 
```
 输出  
```json 
 {
    "errcode": 0,
    "claw_record_id": 6
}  
```


###  2.6.抓取娃娃

 URL  : clawers/grab    

 输入  
```json 
{"claw_record_id":6}
```
 输出  
```json 
{
    "errcode": 0
} 
```


###  2.7.获取游戏结果

抓取娃娃或者到达游戏结束时间后，调用此接口，可获取本次抓取娃娃的结果

 URL  : clawers/gameResult    

 输入  
```json 
{"claw_record_id":5}
```
 输出  
```json 
{
    "errcode": 0,
    "result": 0
}  
```

###  2.8.获取所有娃娃类型

 URL  : clawers/getAllDollType

 输入  
```json 
{}  
```
 输出  
```json 
{
    "errcode": 0,
    "doll_types": [
        {
            "id": 1,
            "name": "傲娇布朗熊",
            "price": 9,
            "convertCoinCount": 60,
            "img": "images/item1.png",
            "img70": "images/doll/70/傲娇布朗熊.jpg",
            "img250": "images/doll/250/傲娇布朗熊.jpg",
            "img300": "images/doll/300/傲娇布朗熊.jpg",
            "detailImages": [
                {
                    "width": 600,
                    "height": 810,
                    "url": "images/doll/detail/傲娇布朗熊1.jpg"
                },
                {
                    "width": 600,
                    "height": 1017,
                    "url": "images/doll/detail/傲娇布朗熊2.jpg"
                },
                {
                    "width": 600,
                    "height": 405,
                    "url": "images/doll/detail/傲娇布朗熊3.jpg"
                },
                {
                    "width": 600,
                    "height": 443,
                    "url": "images/doll/detail/傲娇布朗熊4.jpg"
                },
                {
                    "width": 600,
                    "height": 430,
                    "url": "images/doll/detail/傲娇布朗熊5.jpg"
                }
            ],
            "description": "images/item1.png",
            "tags": [
                1,
                2,
                3
            ]
        },
        {
            "id": 2,
            "name": "蠢萌泰迪",
            "price": 19,
            "convertCoinCount": 60,
            "img": "images/item2.png",
            "img70": "images/doll/70/蠢萌泰迪.jpg",
            "img250": "images/doll/250/蠢萌泰迪.jpg",
            "img300": "images/doll/300/蠢萌泰迪.jpg",
            "detailImages": [
                {
                    "width": 600,
                    "height": 810,
                    "url": "images/doll/detail/蠢萌泰迪1.jpg"
                },
                {
                    "width": 600,
                    "height": 638,
                    "url": "images/doll/detail/蠢萌泰迪2.jpg"
                },
                {
                    "width": 600,
                    "height": 436,
                    "url": "images/doll/detail/蠢萌泰迪3.jpg"
                },
                {
                    "width": 600,
                    "height": 442,
                    "url": "images/doll/detail/蠢萌泰迪4.jpg"
                }
            ],
            "description": "images/item2.png",
            "tags": [
                1,
                2,
                3
            ]
        }
    ]    
}
```

###  2.9.控制娃娃机移动
*方向键按下时，调用对应方向的移动接口，抬起时，调用stop接口。快速单击按键时调用对应的轻微移动接口，如（forwardLight、backwardLight，leftLight，rightLight）*

 URL  : clawers/forward  (backward,left,right,forwardLight,backwardLight,leftLight,rightLight,stop)    

 输入  
```json 
{"claw_record_id":6}
```
 输出  
```json 
{
    "errcode": 0
} 
```

###  2.10.获取所有娃娃类型标签
 URL  : clawers/getAllDollTypeTag    
 
 输入  
```json 
{}
```
 输出  
```json 
{
    "errcode": 0,
    "doll_type_tags": [
        {
            "id": 1,
            "name": "新品"
        },
        {
            "id": 2,
            "name": "特价"
        },
        {
            "id": 3,
            "name": "积分"
        }
    ]
}
```
###  2.11. 获取抓娃娃成功通知
 URL  : clawers/getClawSuccessNotices
 
 输入  
```json 
{}
```
 输出  
```json 
{
    "errcode": 0,
    "notices": [
		{ "userId": 1, "type": 1, "text": "用户A抓到了娃娃！", "time": "2017-11-15T13:54:20.000Z"},
		{ "userId": 2, "type": 2, "text": "用户B抓到了娃娃！", "time": "2017-11-15T13:54:20.000Z"},
	]
}
```
###  2.12. 领取分享奖励娃娃币
 URL  : clawers/receiveCoinsAfterShare
 
 输入  
```json 
{"claw_record_id":1}
```
 输出  
```json 
{
    "errcode": 0,
    "add_coin": 19
}
```
###  2.13. 提交申诉
 URL  : clawers/submitComplaint
 
 输入  
```json 
{"claw_record_id":1,"reason":"抓到了没奖励"}
```
 输出  
```json 
{
    "errcode": 0
}
```

###  2.14. 进入娃娃机直播间
 URL  : clawers/enterClawerLive
 
 输入  
```json 
{"clawer_id:1}
```
 输出  
```json 
{
    "errcode": 0
}
```
###  2.15. 离开娃娃机直播间
 URL  : clawers/leaveClawerLive
 
 输入  
```json 
{"clawer_id:1}
```
 输出  
```json 
{
    "errcode": 0
}
```
###  2.16. 获取娃娃机直播间所有用户信息
 URL  : clawers/getUsersInClawLive
 
 输入  
```json 
{"clawer_id":1}
```
 输出  
```json 
{
    "errcode": 0,
    "users": [
        {
            "id": 2,
            "name": "hc421078278",
            "headImgUrl": ""
        },
        {
            "id": 5,
            "name": "彭昆",
            "headImgUrl": "http://wx.qlogo.cn/mmopen/vi_32/DYAIOgq83ep94v8hrFeC8bo89kevu6X1iaIQ70nTawxUp6diaC0husUdkPOxQ2HsnOU6CgibkXH9Su9oI5uvThibXA/0"
        }
    ],
    "count": 2
}
```
###  2.17. 获取娃娃类型的图片列表
 URL  : clawers/getDollTypeImages
 
 输入  
```json 
{"doll_type_id":1}
```
 输出  
```json 
{
    "errcode": 0,
    "images": [
        {
            "width": 128,
            "height": 128,
            "url": "images/item1.png"
        },
        {
            "width": 128,
            "height": 128,
            "url": "images/item2.png"
        },
        {
            "width": 128,
            "height": 128,
            "url": "images/item3.png"
        }
    ]
}
```
###  2.18. 获取娃娃机状态
 URL  : clawers/getClawerStatus
 
 输入  
```json 
{"clawer_id":1}
```
 输出  
```json 
{
    "errcode": 0,
    "status": 0,
    "current_user": null
}
```

---

## 3.代币相关
###  3.1.获取代币变更记录

 URL  : coins/getCoinRecords    

 输入  
```json 
{"pageindex":1,"pagecount":6}
```
 输出  
```json 
{
    "errcode": 0,
    "coin_records": [
        {
            "id": 7,
            "userId": 1,
            "coin": 10,
            "text": "convertPrize",
            "createTime": "2017-11-15T13:54:20.000Z",
            "updateTime": "2017-11-15T13:54:20.000Z"
        }
    ]
}  
```

###  3.2.获取充值项

 URL  : coins/getPayItems    

 输入  
```json 
{}
```
 输出  
```json 
{
    "errcode": 0,
    "pay_items": [
        {
            "id": 1,
            "name": "充值6元娃娃币",
            "amount": 6,
            "coins": 36,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 2,
            "name": "首次充值6元娃娃币",
            "amount": 6,
            "coins": 66,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 3,
            "name": "充值18元娃娃币",
            "amount": 18,
            "coins": 189,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 4,
            "name": "首次充值18元娃娃币",
            "amount": 18,
            "coins": 198,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 5,
            "name": "充值60元娃娃币",
            "amount": 60,
            "coins": 666,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 6,
            "name": "首次充值60元娃娃币",
            "amount": 60,
            "coins": 690,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 7,
            "name": "充值118元娃娃币",
            "amount": 118,
            "coins": 1357,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 8,
            "name": "首次充值118元娃娃币",
            "amount": 118,
            "coins": 1416,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 9,
            "name": "充值328元娃娃币",
            "amount": 328,
            "coins": 3872,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 10,
            "name": "首次充值328元娃娃币",
            "amount": 328,
            "coins": 4100,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 11,
            "name": "充值648元娃娃币",
            "amount": 648,
            "coins": 7846,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 12,
            "name": "首次充值648元娃娃币",
            "amount": 648,
            "coins": 8424,
            "description": "",
            "imgurl": ""
        },
        {
            "id": 13,
            "name": "周卡",
            "amount": 28,
            "coins": 0,
            "card": 1,
            "description": "连续7天点击领取，充值当天算第一天",
            "imgurl": ""
        },
        {
            "id": 14,
            "name": "月卡",
            "amount": 148,
            "coins": 0,
            "card": 2,
            "description": "连续30天点击领取，充值当天算第一天",
            "imgurl": ""
        },
        {
            "id": -1,
            "name": "充值0.01元娃娃币",
            "amount": 0.01,
            "coins": 100,
            "description": "",
            "imgurl": ""
        }
    ]
}
```
---

## 4.奖品相关
###  4.1.获取奖品信息

 URL  : prizes/getPrizes    

 输入  
```json 
{"pageindex":1,"pagecount":6}
```
 输出  
```json 
{
    "errcode": 0,
    "prizes": [
        {
            "id": 414,
            "userId": 32,
            "dollTypeId": 6,
            "clawRecordId": 729,
            "status": 0,
            "createTime": "2017-12-25T16:33:10.000Z",
            "updateTime": "2017-12-25T16:33:10.000Z",
            "statusText": "未处理",
            "remainDays": 5
        }
    ],
    "count": 1
}
```


###  4.2.将奖品转换为代币
URL  : prizes/convertConis    

输入  
```json 
{"prize_ids":[1]} 
```   
输出  
```json 
		 {
		    "errcode": 0,
		    "user_coin": 1014,
		    "add_coin": 10
		}
```
###  4.3. 通过奖品Id获取发货单信息
URL  : prizes/getInvoiceByPrizeId    

输入  
```json 
{"prize_id":1} 
```   
输出  
```json 
{
    "errcode": 0,
    "invoice": {
        "id": 1,
        "code": "123415",
        "status": 0,
        "contact": "张三",
        "phone_number": "123456",
        "address": "北京市朝阳区大悦城1133号",
        "comment": "快点发货"
    }
}
```
###  4.4. 奖品申请发货
URL  : prizes/sendPrizes 

输入  
```json 
{{"prize_ids":[98,99],"address_id":3, "comment": "快点发货"}}
```   
输出  
```json 
{
    "errcode": 0,
    "invoice_id": 3
}
```
###  4.5. 通过奖品状态获取奖品列表
奖品状态：   
 "0": "未处理",
    "1": "已兑换娃娃币",
    "2": "等待发货",
    "3": "发货中",
    "4": "已送达"

URL  : prizes/getPrizesByStatus 

输入  
```json 
{"pageindex":0,"pagecount":6,"status":0}
```   
输出  
```json 
{
    "errcode": 0,
    "prizes": [
        {
            "id": 414,
            "userId": 32,
            "dollTypeId": 6,
            "clawRecordId": 729,
            "status": 0,
            "createTime": "2017-12-25T16:33:10.000Z",
            "updateTime": "2017-12-25T16:33:10.000Z",
            "statusText": "未处理",
            "remainDays": 5
        }
    ],
    "count": 1
}
```
###  4.6. 通过id获取奖品信息

URL  : prizes/getPrizesByIds

输入  
```json 
{"prize_ids":[98,99]}
```   
输出  
```json 
{
    "errcode": 0,
    "prizes": [
        {
            "id": 414,
            "userId": 32,
            "dollTypeId": 6,
            "clawRecordId": 729,
            "status": 0,
            "createTime": "2017-12-25T16:33:10.000Z",
            "updateTime": "2017-12-25T16:33:10.000Z",
            "statusText": "未处理",
            "remainDays": 5
        }
    ],
    "count": 1
}
```

###  4.7. 通过发货单id获取快递信息

URL  : prizes/getExpressInfoByInvoiceId

输入  
```json 
{
	"invoice_id":1
}
```   
输出  
```json 
{
    "expressCompany": "顺丰",
    "expressNumber": "1234215",
    "traces": [
        {
            "AcceptTime": "2014/06/25 08:05:37",
            "AcceptStation": "正在派件..(派件人:邓裕富,电话:18718866310)[深圳 市]",
            "Remark": null
        },
        {
            "AcceptTime": "2014/06/25 04:01:28",
            "AcceptStation": "快件在 深圳集散中心 ,准备送往下一站 深圳 [深圳市]",
            "Remark": null
        },
        {
            "AcceptTime": "2014/06/25 01:41:06",
            "AcceptStation": "快件在 深圳集散中心 [深圳市]",
            "Remark": null
        },
        {
            "AcceptTime": "2014/06/24 20:18:58",
            "AcceptStation": "已收件[深圳市]",
            "Remark": null
        },
        {
            "AcceptTime": "2014/06/24 20:55:28",
            "AcceptStation": "快件在 深圳 ,准备送往下一站 深圳集散中心 [深圳市]",
            "Remark": null
        },
        {
            "AcceptTime": "2014/06/25 10:23:03",
            "AcceptStation": "派件已签收[深圳市]",
            "Remark": null
        },
        {
            "AcceptTime": "2014/06/25 10:23:03",
            "AcceptStation": "签收人是：已签收[深圳市]",
            "Remark": null
        }
    ]
}
```

---

## 5.其他
###  5.1.获取所有滚屏广告
 URL  : posters/getAllPosters    

 输入  
```json 
{}
```
 输出  
```json 
{
    {
    "errcode": 0,
    "posters": [
        {
            "id": 1,
            "name": "1",
            "img": "images/poster1.jpg",
            "url": "1",
            "order": 0,
            "createTime": "2017-11-20T21:15:33.000Z",
            "updateTime": "2017-11-20T21:15:34.000Z"
        },
        {
            "id": 2,
            "name": "2",
            "img": "images/poster2.jpg",
            "url": "1",
            "order": 4,
            "createTime": "2017-11-20T21:15:33.000Z",
            "updateTime": "2017-11-20T21:15:34.000Z"
        },
        {
            "id": 3,
            "name": "3",
            "img": "images/poster3.jpg",
            "url": "1",
            "order": 3,
            "createTime": "2017-11-20T21:15:33.000Z",
            "updateTime": "2017-11-20T21:15:34.000Z"
        },
        {
            "id": 4,
            "name": "4",
            "img": "images/poster4.jpg",
            "url": "1",
            "order": 2,
            "createTime": "2017-11-20T21:15:33.000Z",
            "updateTime": "2017-11-20T21:15:34.000Z"
        },
        {
            "id": 5,
            "name": "5",
            "img": "images/poster5.jpg",
            "url": "1",
            "order": 1,
            "createTime": "2017-11-20T21:15:33.000Z",
            "updateTime": "2017-11-20T21:15:34.000Z"
        }
    ]
}
```
###  5.2.获取版本信息
 URL  : autoUpdate/getVersionInfo

 输入  
```json 
{
	"QdCode":"wancms"
}
```
 输出  
```json 
{
    "errcode": 0,
    "versionInfo": {
        "versionCode": 1,
        "downloadUrl": "http://cdn.piupiuwan.com/data/package/android/wxfxwwj/mddwwj_wxfxwwj_1.apk"
    }
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY0NzM3MDkyXX0=
-->