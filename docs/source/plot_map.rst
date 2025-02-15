.. _plot_map:


***************
地图底图
***************

地图底图加载
=============================

.. function:: transbigdata.plot_map(plt,bounds,zoom,style=4,imgsavepath = r'/Users/yuqing/Nutstore Files/我的坚果云/python_new/',printlog = False,apikey = '',access_token = '',styleid = 'dark')

添加地图底图

**输入**

bounds : List
    底图的绘图边界，[lon1,lat1,lon2,lat2] (WGS84坐标系) 其中，lon1,lat1是左下角坐标，lon2,lat2是右上角坐标 
zoom : number
    底图的放大等级，越大越精细，加载的时间也就越久，一般单个城市大小的范围，这个参数选取12到16之间 
style : number
    地图底图的样式，可选1-5，或'light','dark'，style为4时为light，style为5时为dark      
imgsavepath : str
    瓦片地图储存路径，设置路径后，会把地图下载到本地的文件夹下，使用时也会优先搜索是否有已经下载的瓦片，默认的存放路径是...小旭学长自己电脑的路径！
printlog : bool
    是否显示日志                                                


::

    #设定显示范围
    bounds = [lon1,lat1,lon2,lat2]  
    tbd.plot_map(plt,bounds,zoom = 12,style = 4)  

指北针和比例尺
=============================

.. function:: transbigdata.plotscale(ax,bounds,textcolor = 'k',textsize = 8,compasssize = 1,accuracy = 'auto',rect=[0.1,0.1],unit = "KM",style = 1,**kwargs)

为底图添加指北针和比例尺

**输入**

bounds : List
    底图的绘图边界，[lon1,lat1,lon2,lat2] (WGS84坐标系) 其中，lon1,lat1是左下角坐标，lon2,lat2是右上角坐标 
textsize : number
    标注文字大小                                                 
compasssize : number
    标注的指北针大小                                             
accuracy : number
    标注比例尺的长度（米）                                         
unit : str
    'KM','km','M','m' 比例尺的单位                               
style : number
    1或2，比例尺样式                                             
rect : List
    比例尺在图中的大致位置，如[0.9,0.9]则在右上角                    


::

    tbd.plotscale(ax,bounds = bounds,textsize = 10,compasssize = 1,accuracy = 2000,rect = [0.06,0.03])  
