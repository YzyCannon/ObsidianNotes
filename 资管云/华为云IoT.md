设备ID 65699eb816c4bf77631a5831_test123
设备密钥 7aec8124212ffd6b4dbb607db7ff96d2
f69f0d7b68494561aa8ffa9137b17fcd
#### 设备开发资源

物联网平台支持设备通过MQTT协议、LWM2M/CoAP协议和HTTPS协议进行接入，也可以通过IoTEdge将Modbus、OPC-UA、OPC-DA这些协议的设备接入。设备可以通过调用接口或者集成SDK的方式接入到物联网平台。

#### 属性上报

属性上报是指*设备主动*向平台上报自己的属性（该示例代码已实现自动定时上报功能，可参考下一节在iot平台查看设备上报的数据内容）。
```
//上报json数据，注意serviceId要与产品模型中的定义对应
String jsonMsg = "{\"services\":[{\"service_id\":\"BasicData\",\"properties\":{\"luminance\":32},\"eventTime\":null}]}";
```
- 消息体jsonMsg组装格式为JSON，其中service_id要与产品模型中的定义对应，properties是设备的属性；
- luminance表示路灯亮度；
- event_time为可选项，为设备采集数据UTC时间，不填写默认使用系统时间。

设备或网关成功连接到物联网平台后，即可调用MqttAsyncClient的publish(String topic,MqttMessage message)方法向平台上报设备属性值。

#### 命令下发
can not get api debug endpoint, instanceId:c9197b44d4c94c9a8cb2ca30466a8cbe please check if the service is available

- service_id表示服务ID，例如：BasicData。
- command_name表示命令名称，例如：lightControl。
- paras表示下发参数，例如：{"switch":"ON"}。