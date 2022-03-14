<!DOCTYPE HTML>
<html>
<head>
<meta charset=utf-8"/>
<title>hw</title>
<style type="text/css"> 
    html{height:100%} 
    body{height:100%;margin:0px;padding:0px} 
    #container{height:100%} 
    </style> 
</style> 
<script type="text/javascript" src="https://api.map.baidu.com/api?v=1.0&type=webgl&ak=v4KEbCG64O9zeSUyP6MFLX7xqOiR4IhU">
</script>
</head>


    
<body> 
    <div id="container"></div>
    <script type="text/javascript">
    var map = new BMapGL.Map("container");
    // 创建地图实例 
    var point = new BMapGL.Point(121.1, 28.35);
    // 创建点坐标 
    map.centerAndZoom(point, 12);
    
    var myicon = new BMapGL.Icon(
    　　　　　　　　'https://tse4-mm.cn.bing.net/th/id/OIP-C.DX5fBs0VPnO3GmLCZXsvsQHaE7?w=292&h=194&c=7&r=0&o=5&dpr=1.2&pid=1.7', 
    　　　　　　　　new BMapGL.Size(144,144), // 视窗大小
    　　　　　　　　{
    　　　　　　　　　　imageSize: new BMapGL.Size(144,92), // 引用图片实际大小
    　　　　　　　　　　imageOffset:new BMapGL.Size(0,0)  // 图片相对视窗的偏移
    　　　　　　　　}
    　　　　 );
            var marker = new BMapGL.Marker(point,{icon:myicon});
            map.addOverlay(marker);    
    
    
    var marker = new BMapGL.Marker(point);  // 创建标注
        map.addOverlay(marker);  // 将标注添加到地图中
        var opts = {
            width : 300,     // 信息窗口宽度
            height: 300,     // 信息窗口高度
            title : "雁荡山" , // 信息窗口标题
            message:"浙江温州。"
        }
        var infoWindow = new BMapGL.InfoWindow("雁荡山以山水奇秀闻名，素有“海上名山、寰中绝胜”之誉，史称中国“东南第一山”   ，主体位于浙江省温州市东北部海滨，小部在台州市温岭南境。雁荡山形成于1亿2000万年以前，是环太平洋大陆边缘火山带中一座白垩纪流纹质破火山 [2]  。雁荡山以瓯江自然断裂，分北雁荡山和南雁荡山。以景观区位分有北雁荡山、南雁荡山、西雁荡山、东雁荡山、中雁荡山之称。其开山凿胜始于南北朝，兴于唐，盛于宋。历代文人墨客纷至沓来，谢灵运、沈括、徐霞客、张大千、郭沫若、陈志岁等都留下了诗篇和墨迹。", opts);  // 创建信息窗口对象 
        marker.addEventListener("click", function(){          
            map.openInfoWindow(infoWindow, point); //开启信息窗口
        }); 
    
    </script> 
    </body> 

</html>
