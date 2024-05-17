#### 应用说明
该应用是AIotSdk_2.0版本 Flutter端Demo程序
AIotSdk2.1.1.3版本


#### 版本更新
1. 使用Flutter 封装SDK接口

#### 已知问题
1. Android版本在登录后进入首页，设备列表刷新有问题，可以前后台切换一下刷新；
2. iOS版本中首页(设备列表页)预览成功后，跳转到流管理界面，再次返回首页，不显示画面
2. iOS版本在流管理界面中，视频帧画面显示位置错乱

#### 功能列表

1. 设备管理: 在主界面可以浏览多个设备，并且收发消息

2. 流的操作: 可以对于任意一路订阅的流，进行预览、音放禁音、录像、截图操作

3. 流管理: 当连接上一个设备后，可以进入 "流管理" 界面，对该设备多路流进行操作

4. 文件传输: 进入全屏界面后，点击"开始传输"，可以进入设备的文件传输演示


#### APP使用说明
1. 项目配置：
   首次进入APP时，需要进行 appId;  authKey;  authSecret; 的配置操作 
   【特别注意】这三个参数一定要配置正确，如果配置错误，可以把应用数据清除后，重新进入APP配置
  
2. 设备管理：
   在首页设备列表界面，可以通过输入设备的NodeId可以进行设备添加；
   首页中，设备卡片界面显示的总是 BROADCAST_STREAM_1 这路流操作

3. 单个设备卡中的提示信息:
   设备没有连接："Disconnected"
   设备正在连接中: "Connecting..."
   设备已经连接，但是还没有订阅："Connected"
   设备已经连接，已经订阅播放视频："Subscribed"
   设备已经连接和订阅，正在录像："Recording..."


#### Device使用说明
1. 根据项目配置，使用HTTP工具软件（例如：PostMan）来发送一个HTTP请求激活设备，获得相应的信息

2. 将激活后服务端返回的data字段JSON拷贝出来，作为参数提供给设备运行，详见设备应用程序使用说明


#### Sample源码说明
1. APP端的sample源码在sample\aiot_flutter_sdk 目录下
   可以直接使用 Android Studio(Giraffe及以上版本) 或者 XCode(最低14.0) 直接打开这个工程目录，编译运行
   （前提：需要自己本地配置好 Flutter SDK）

2. 工程目录结构：
  （1）sample\aiot_flutter_sdk\example: 这个是Flutter APP的目录，里面细分android和ios两个目录
  （2）sample\aiot_flutter_sdk\lib: 这个是Dart语言实现的Flutter应用界面层
  （3）sample\aiot_flutter_sdk\android: 这是Android语言转换层，使用Java调用底层SDK转换成Dart消息
  （4）sample\aiot_flutter_sdk\ios: 这是iOS语言转换层，使用Swift调用底层SDK转换成Dart消息
