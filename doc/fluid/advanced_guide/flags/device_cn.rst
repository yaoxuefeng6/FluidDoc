
设备管理
==================


FLAGS_paddle_num_threads
*******************************************
(始于0.15.0)

控制每个paddle实例的线程数。

取值范围
---------------
Int32型，缺省值为1。

示例
-------
FLAGS_paddle_num_threads=2 - 将每个实例的最大线程数设为2。


FLAGS_selected_gpus
*******************************************
(始于1.3)

设置用于训练或预测的GPU设备。

取值范围
---------------
以逗号分隔的设备ID列表，其中每个设备ID是一个非负整数，且应小于您的机器拥有的GPU设备总数。

示例
-------
FLAGS_selected_gpus=0,1,2,3,4,5,6,7 - 令0-7号GPU设备用于训练和预测。

注意
-------
使用该flag的原因是我们希望在GPU设备之间使用聚合通信，但通过CUDA_VISIBLE_DEVICES只能使用共享内存。