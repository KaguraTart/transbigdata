.. _getting_started:


******************************
安装、依赖与更新日志
******************************

安装
=============================

TransBigData依赖geopandas：https://geopandas.org/index.html
如果你已经安装了geopandas，则直接在命令提示符中运行下面代码即可安装::

  pip install -U transbigdata

在Python中运行下面代码::

  import transbigdata as tbd

依赖包
=============================
TransBigData依赖如下包

* pandas
* geopandas
* scipy
* matplotlib

可选依赖：

* networkx
* keplergl

版本更新
=============================

0.1.24 (2021-11-11)
------------------------
添加id_reindex_disgap方法对数据的ID列重新编号，如果相邻两条记录超过距离，则编号为新id
添加clean_traj方法轨迹数据清洗组合拳，能够有效解决轨迹漂移的问题

0.1.23 (2021-11-10)
------------------------
添加visualization_data方法,添加对keplergl的支持

0.1.22 (2021-11-10)
------------------------
添加visualization_od方法,添加对keplergl的支持

0.1.20 (2021-11-09)
------------------------
添加visualization_trip方法,添加对keplergl的支持

0.1.19 (2021-11-09)
------------------------
添加transform_shape方法,可以将GeoDataFrame整体做坐标转换

0.1.18 (2021-11-09)
------------------------
添加splitline_with_length方法,可以将长线段全部打断

0.1.17 (2021-11-08)
------------------------
添加geohash编码方法

0.1.16 (2021-11-05)
------------------------
添加getadmin方法，输入关键词抓取行政区划信息

0.1.15 (2021-11-04)
------------------------
添加metro_network方法，输入站点信息，输出网络信息

0.1.13 (2021-11-03)
------------------------
增加公交地铁线网拓扑建模的模块，添加split_subwayline方法，用公交/地铁站点对公交/地铁线进行切分，得到断面

0.1.12 (2021-11-02)
------------------------
增加爬虫模块，用getbusdata通过输入城市与关键词，获取公交线路的线型与站点，且不依赖于ak

0.1.11 (2021-11-01)
------------------------
公交GPS模块增加busgps_onewaytime函数，
输入到离站信息表arrive_info与站点信息表stop，计算单程耗时

0.1.10 (2021-10-31)
------------------------
增加公交GPS数据到离站信息识别的方法

0.1.9 (2021-10-28)
------------------------
改进id_reindex方法，sample支持所有模式，同时也添加了timegap和timecol参数

0.1.7 (2021-10-27)
------------------------
增加数据质量分析部分：

* sample_duration采样间隔

0.1.6 (2021-10-25)
------------------------
修正taxigps_traj_point的Bug

0.1.5 (2021-10-25)
------------------------
增加轨迹处理部分：

* taxigps_traj_point  输入出租车数据与OD数据，提取载客与空载的行驶路径点
* points_to_traj 输入轨迹点，生成轨迹线型的GeoDataFrame


0.1.4 (2021-10-24)
------------------------
增加栅格化的gridid_sjoin_shape方法，输入数据（带有栅格经纬度编号两列），矢量图形与栅格化参数，输出数据栅格并对应矢量图形。


0.1.3 (2021-10-23)
------------------------
增加预处理的clean_same,clean_drift,clean_taxi_status方法
为预处理的id_reindex方法加入sample参数

0.1.2 (2021-10-23)
------------------------
更新数据预处理的clean_outofshape方法
增加共享单车数据处理功能，bikedata_to_od提取骑行订单数据与停车数据

0.1.1 (2021-10-22)
------------------------
加入数据预处理的clean_outofbounds，dataagg，id_reindex方法

0.1.0 (2021-10-21)
------------------------
最初版本发布