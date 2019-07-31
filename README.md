# weChatToBaiDu
微信小程序   腾讯地图坐标 需转化成 百度坐标    向后台发送请求  （百度转腾讯）或（腾讯转百度）

在要转化的坐标的js中引入

    var coordinate = require('../../utils/WSCoordinate.js')//根据实际存放地址进行引入


      console.log('转化为百度度坐标')
      
      //fromLat:经度
      //fromLng:纬度
      
      var startPointBD = coordinate.transformFromGCJToBaidu(fromLat, fromLng);
      var fromLatbd = startPointBD.latitude;
      var fromLngbd = startPointBD.longitude;
      
      
     
    console.log('百度转化为腾讯')
      var startPointBD1 = coordinate.transformFromBaiduToGCJ(fromLatbd, fromLngbd);
      var  fromLatbd1 = startPointBD1.latitude;
      var  fromLngbd1 = startPointBD1.longitude;

      console.log(fromLatbd1)
      console.log(fromLngbd1)
