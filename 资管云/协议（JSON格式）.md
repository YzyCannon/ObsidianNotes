hand-held terminal HHT
Intelligent cloud cabinet ICC
Borrowing and returning counter BTC
# 盘点机
开启主题号：682265633886208
### 连接
##### 接收：
{"cmd":"ConnectOK"}
##### 回复：
{"cmd":"Connect"}
### 单次读卡
##### 接收：
{"cmd": "ReadSingle","cardId":"E220212223242526272829FF"}
##### 回复：
{
"cmd": "ReadSingle",
"info":{"rfid":"002202304110021","name":" 实验室电脑桌1","xh":" 带主机式","gg":"L*750*800mm","warehouse":"实验室415"}
}

### 盘点
#### 步骤1（仓库查询）
##### 接收{"cmd": "Check1"}
##### 回复
{
"cmd": "Check1" ,
"info":[
{"wid":"1613339169554305024","title":"实验室415"},
{"wid":"1613339201049333760","title":"实验室515"}]
}
#### 步骤2（资产查询） 新增wid
##### 接收
{ "cmd": "Check2" ,"wid":"1674612739588362240"}
##### 回复
{"cmd":"Check2",
"info":[{"cardId":"E220212223242526272829FF","classify":"办公电脑","name":" 实验室电脑桌1","xh":" 带主机式","gg":"L*750*800mm","warehouse":"实验室415"},{"cardId":"E200010203040506070809FF","classify":"办公电脑","name":" 实验室电脑桌2","xh":" 带主机式","gg":"L*750*800mm","warehouse":"实验室415"}
]}
#### 步骤3 状态0未盘，1已盘，2其他（盘点结果）status为int类型
##### 接收
{
"cmd": "Check3",
"wid":"1674612739588362240", 
"info":[
{"cardId":"E220212223242526272829FF","status":1},
{"cardId":"E210111213141516171819FF","status":2},
{"cardId":"E200010203040506","status":3}，
{"cardId":"E240414243444546474849FF","status":3},
{"cardId":"E200010203040506070809FF","status":3}
]
}
{"cmd":"Check3","wid":"1674612739588362240","info":[{"cardId":"E210111213141516171819FF","status":1},{"cardId":"E200010203040506070809FF","status":3},{"cardId":"E220212223242526272829FF","status":1},{"cardId":"E240414243444546474849FF","status":3},{"cardId":"E200010203040506","status":2}]}
##### 回复
{
"cmd": "Check3"，
"records":"ok"
}

### 固定资产入库
##### 接收
{
"cmd":"AssetsInware",
"Records":[
"002202304110021",
"002202304110022"，
"002202304110023"
]
}
##### 回复
{
"cmd":"Inware"，
"records":"ok"
}
# 智能云柜
### 智能云柜初始化
##### 接收
{"cmd":"CabinetInit","id":"ICC202306200050"}
##### 回复
{"cmd":"CabinetInit","info":[
{"id":"0","name":"4环南孚电池","weight":"24","jldw":"个","classify":"5号电池","gg":"5号","xh":"电池","number":"0"},
{"id":"1","name":"挂钩","weight":"28","jldw":"件","classify":"收纳器","gg":"小件","xh":"挂钩","number":"0"}]
}
##### 接收
{
"cmd":"CabinetInit"，
"records":"ok"
}
### 耗材入库
##### 接收
{"cmd":"ConsumableInware",
"info":
[{"id":"0","number":5},
{"id":"1","number":5}
]}
##### 回复
{
"cmd":"ConsumableInware"，
"records":"ok"
}
### 智能云柜开锁
##### 发送
{"cmd":"Unlock"}
接收:{"cmd":"Unlock"}
##### 回复
{
"cmd":"Unlock"，
"records":"ok"
}
### 智能云柜上锁
##### 回复
{"cmd":"Lock",
"info":[
{"id":0,"number":3},
{"id":1,"number":3}
]
}
##### 接收
{"cmd":"Lock","records":"ok"}





