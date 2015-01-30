

## OpenStack 版本演变

OpenStack 到目前为止发布了十个版本，每个版本都有一个代号，代号首字母从A开始递增，从第三版之后基本上保持了每年发布两个版本，分别在四月和十月发布，每次发布可能会增加一些开发成熟的组件，下表为 OpenStack 历史发布版本信息：

发布名称 | 发布日期    | 包含的组件
---------|-------------|------------------
Austin   | 2010.10.21  | Nova, Swift
Bexar    | 2011.2.3    | Nova, **Glance**, Swift
Cactus   | 2011.4.15   | Nova, Glance, Swift
Diablo   | 2011.9.22   | Nova, Glance, Swift
Essex    | 2012.4.5    | Nova, Glance, Swift, **Horizon, Keystone**
Folsom   | 2012.9.27   | Nova, Glance, Swift, Horizon, Keystone, **Quantum,** Cinder
Grizzly  | 2013.4.4    | Nova, Glance, Swift, Horizon, Keystone, Quantum, Cinder
Havana   | 2013.10.17  | Nova, Glance, Swift, Horizon, Keystone, ~~Quantum~~, **Neutron,** Cinder, **Heat, Ceilometer**
Icehouse | 2014.4.17   | Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, **Trove**
Juno     | 2014.10.16  | Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, **Sahara**
Kilo     | 2015.4（***待发布***） | Nova, Glance, Swift, Horizon, Keystone, Neutron, Cinder, Heat, Ceilometer, Trove, Sahara, **Ironic, Zaqar, Manila, Designate, Barbican**

## OpenStack 包含组件

OpenStack 是一种模块化松耦合架构，由最初的只有计算和存储两个组件，逐渐增加到 J 版的 11 个组件，而且还有很多组件在开发中，各个组件有其功能和代号：

组件代号 | 最早加入版本 | 功能  
---------|--------------|---------
Nova     | Austin       | Compute
Swift    | Austin       | Object Storage
Cinder   | Folsom       | Block Storage
Neutron  | Havana       | Networking
Horizon  | Essex        | Dashboard
Keystone | Essex        | Indentity Service
Glance   | Bexar        | Image Service
Ceilometer | Havana     | Telemetry
Heat     | Havana       | Orchestration
Trove    | Icehouse     | Database
Sahara   | Juno         | Elastic Map Reduce
