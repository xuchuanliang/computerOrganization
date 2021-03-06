#系统总线
##总线的基本概念
- 总线是连接多个部件的信息传输线，是各部分共享的传输介质。
- 总线上信息的传达：串行、并行
##总线的分类
- 总线的分类：按数据的传输方式可分为并行传输总线和串行传输总线；按总线的使用范围分为计算机总线、测控总线、网络通信总线；按连接部件分为片内总线、系统总线、通信总线；
- 片内总线：片内总线是指芯片内部的总线
- 系统总线：系统总线是指CPU、I/O设备各大部件之间的信息传输线，又称为板级总线。
按系统总线传输信息不同分为数据总线、地址总线和控制总线；数据总线用来传输各功能部件之间的数据信息，它是双向传输总线；地址总线主要是用来指出数据总线上源数据和目的数据在主存单位的地址或I/O设备的地址；控制总线：由于数据总线、地址总线
都是被挂在总线上的所有部件共享的，如何使各部件能在不同时刻占有总线控制权，需依靠控制总线来完成，因此控制总线是用来发出各种控制信号的传输线。
常见的控制信号如下：
时钟：用来同步各种工作；
复位：初始化所有部件；
总线请求：表示某部件需获得总线使用权；
总线允许：标识需要获得总线使用权的部件已获得控制权；
中断请求：表示某部件提出中断请求；
中断响应：表示中断请求已经被接受；
存储器写：将数据总线的数据写至存储器的指定地址单元内；
存储器读：将指定存储单元中的数据读到数据总线上；
I/O读：从指定的I/O端口将数据读到数据总线中；
I/O写：将数据总线上的数据输出到指定的I/O端口中；
传输响应：表示数据已经被接收，或已将数据送至数据总线上。
- 通信总线：用于计算机系统之间或计算机系统与其他系统之间的通信。按传输方式可分为两种：串行传输和并行传输
##总线的特征和性能指标
- 总线特征：机械特征、电气特征、功能特征、时间特征
- 总线的性能指标：总线宽度、总线带宽、时钟同步/异步、总线复用、信号线数、总线控制方式、其他指标
##总线结构
- 分为单总线结构和多总线结构
- 多总线结构：包含主存总线和I/O总线
##总线控制
- 总线控制主要包含判优控制（又称仲裁逻辑）和通信控制
- 主设备（模块）--对总线有控制权；从设备（模块）--响应从主设备发来的总线命令
- 总线判优控制：集中式（包含链式查询、计数器定时查询、独立请求方式）和分布式
- 链式查询方式：BS：总线忙；BR：总线请求；BG：总线统一
- 总线通信控制目的解决通信双方协调配合问题
- 总线传输周期是指主设备和从设备之间完成一次完整的和可靠的通讯需要的时间
- 总线传输周期包含申请分配阶段【主模块申请，总线仲裁决定】、寻址阶段【主模块向从模块给出地址和命令】、传数阶段【主模块和从模块交换数据】、结束阶段【主模块撤销有关信息】
- 总线通信的四种方式：同步通信【由统一时标控制数据传送】、异步通信【采用应答方式，没有公共时钟标准】、半同步通信【同步、异步结合】、分离式通信【充分挖掘系统总线的每一瞬间潜力】
- 异步通信：不互锁、半互锁、全互锁
- 半同步通信（同步、异步结合）：同步--发送方用系统始终前沿发信号，接受方用系统始终后沿判断、识别；异步--允许不同速度的模块和谐工作，增加一条等待信号
- 分离式通信：一个总线的传输周期---子周期1：主模块申请占用总线，使用完后即放弃总线使用权；子周期2：从模块申请占用总线，将各种信息送至总线上
- 分离式通信特点：各模块有权申请占用总线；采用同步方式通信，不等对方回答；各模块准备数据时，不占用总线；总线被占用时，无空闲；



