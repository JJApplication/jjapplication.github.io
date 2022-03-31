## Welcome to Project JJ Pages
一个微服务群组(building)

### 服务定界
#### 管理服务
- Apollo 以上帝视角管理全局服务，包括但不限于服务部署安装启停，流量控制信息，缓存配置，文件服务器，容器管理，CICD（这些由中间件提供，总成到本服务）
- Athena 顶层数据层，管理数据库，NoSql，缓存
- Hermes 消息通知（不同于消息处理的中间件）负责服务与服务之间的通信，协议基于UDS和http

#### 业务服务
包含所有的功能型服务，包括博客，主页，网站，项目介绍
#### 中间件
- octopusTree  灵感来源于The World's Tree用于联通所有服务， 一个基于ast的消息自定义配置工具， 会在每个服务下生成.octopus目录保持服务元数据和通信数据（如服务间鉴权配置）
- dirichlet 一个命令行终端，用于以UDS和阿波罗服务通信
- Sandwich 路由控制中间件，一个基于go的反向代理服务，api网关后期希望实现的效果（鉴权，限流，流量监控转发），在以域名转发的基础上增加全局的api网关，能够自由转发流量到服务上
- jjmail现在更名为Dove， 用于处理邮件和短信通知
- jjgo全局的api管理，现在废弃，以模块化地代理转发服务sandwich替代，做到轻量
- plnack（plnack-gen） 自定义的通信协议，基于Go服务以http协议为基础，定制header和body体以符合服务间通信数据的传递，配合Hermes
- Noengine 基于nginx和lua的自定义nginx，更好的处理nginx代理和高级配置功能
- Truck 微服务服务备份还原服务
- And more...

### Support or Contact


