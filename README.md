<!DOCTYPE html>
<html>
<head>
  <title>第五組商務網站設計</title>
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
  <style>
    #mapid { height: 400px; width: 100%; } /* 調整地圖寬度以適應頁面 */
    .landmark-icon {
      border-radius: 50%;
      width: 30px;
      height: 30px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      font-size: 14px;
      border: 2px solid black;
    }
    .five-star { background-color: gold; color: black; }
    .four-star { background-color: purple; }
    .three-star { background-color: blue; }
    .two-star { background-color: gray; }
  </style>
</head>
<body>
    
	<h1>組員名單</h1>
  <ul>
    <li>S11410108 歐凡瑩S11410107 王紹宇S10410335 許容禎S11410213 謝昊玲S11410141 王政元</li>
  </ul>
  <h2>第五組商務網站設計</h2>

  <p>台中市擁有豐富的觀光資源，吸引了來自各地的遊客。為了提供舒適的住宿體驗，台中市擁有各式各樣的旅館，其中不乏提供高品質服務的星級旅館。本頁面將展示部分台中市星級旅館的分布情況與基本資訊，希望能幫助您更好地了解台中市的住宿選擇。</p>

  <h2>台中市旅館分布地圖</h2>
  <div id="mapid"></div>
HTML

<!DOCTYPE html>
<html>
<head>
  <title>第五組商務網站設計</title>
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
  <style>
    #mapid { height: 600px; width: 100%; }
    .landmark-icon {
      border-radius: 50%;
      width: 30px;
      height: 30px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      font-size: 14px;
      border: 2px solid black;
    }
    .five-star { background-color: gold; color: black; }
    .four-star { background-color: purple; }
    .three-star { background-color: blue; }
    .two-star { background-color: gray; }

    h2 {
      text-align: center;
      color: #333;
      margin-bottom: 20px;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 20px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      font-size: 16px;
    }

    thead {
      background-color: #4CAF50; /* Green header */
      color: white;
      font-weight: bold;
    }

    th, td {
      padding: 12px 15px;
      text-align: left;
      border-bottom: 1px solid #ddd;
    }

    tbody tr:nth-child(even) {
      background-color: #f2f2f2;
    }

    tbody tr:hover {
      background-color: #e0f7fa;
    }

    td a {
      color: #007bff;
      text-decoration: none;
      transition: color 0.3s ease;
    }

    td a:hover {
      color: #0056b3;
      text-decoration: underline;
    }
  </style>
</head>
<body>

  <h2>台中市星級旅館資料表格</h2>
  <table>
    <thead>
      <tr>
        <th>星級</th>
        <th>旅館名稱</th>
        <th>地址</th>
        <th>連絡電話</th>
      </tr>
    </thead>
    <tbody id="hotel-table-body">
      <tr>
        <td>五星級</td>
        <td><a href="https://www.millenniumhotels.com/zh-tw/taichung/millennium-hotel-taichung/" target="_blank">日月千禧酒店</a></td>
        <td>臺中市西屯區市政路77號</td>
        <td>0437056000</td>
      </tr>
      <tr>
        <td>五星級</td>
        <td><a href="https://taichung.evergreen-hotels.com/tw/index.aspx" target="_blank">長榮桂冠酒店(台中)</a></td>
        <td>臺中市西屯區臺灣大道二段666號</td>
        <td>0423139988</td>
      </tr>
      <tr>
        <td>二星級</td>
        <td><a href="https://www.viphotel.com.tw/portfolio/chance-hotel/" target="_blank">巧合大飯店</a></td>
        <td>臺中市中區建國路163號</td>
        <td>0422297161</td>
      </tr>
      <tr>
        <td>三星級</td>
        <td><a href="https://www.zkhotel.com.tw/" target="_blank">中科大飯店</a></td>
        <td>臺中市北屯區旅順路2段7號1至19樓</td>
        <td>0422465599</td>
      </tr>
      <tr>
        <td>二星級</td>
        <td><a href="https://gorates-hotel.com/web/summary/58" target="_blank">創意時尚旅店</a></td>
        <td>臺中市北區五權路332、334號1至7樓</td>
        <td>0422022666</td>
      </tr>
      <tr>
        <td>三星級</td>
        <td><a href="http://www.parkcthotel.com/" target="_blank">成旅晶贊飯店</a></td>
        <td>臺中市中區民權路66號、繼光街25號1至9樓</td>
        <td>0422235678</td>
      </tr>
      <tr>
        <td>四星級</td>
        <td><a href="https://tchhotel.com/" target="_blank">台中港酒店</a></td>
        <td>臺中市梧棲區大智路二段388號</td>
        <td>0426568888</td>
      </tr>
      <tr>
        <td>五星級</td>
        <td><a href="https://www.freshfields.com.tw/" target="_blank">清新溫泉飯店</a></td>
        <td>臺中市烏日區溫泉路2號</td>
        <td>0423829888</td>
      </tr>
      <tr>
        <td>二星級</td>
        <td><a href="http://www.meijourneyhotel.com/" target="_blank">美之旅商務飯店</a></td>
        <td>臺中市西區美村路一段269號</td>
        <td>0423024330</td>
      </tr>
      <tr>
        <td>五星級</td>
        <td><a href="https://www.windsortaiwan.com/tw" target="_blank">裕元花園酒店</a></td>
        <td>臺中市西屯區台灣大道四段610號(台中港路3段78-3號)</td>
        <td>0424656555</td>
      </tr>
      <tr>
        <td>二星級</td>
        <td><a href="https://www.taiwantravelmap.com/hotel/1074-ch-index.html" target="_blank">墨鐵會館</a></td>
        <td>臺中市中區柳川西路三段19號1樓、4樓至12樓</td>
        <td>0422270088</td>
      </tr>
      <tr>
        <td>三星級</td>
        <td><a href="https://www.fushin-hotel.com.tw/taichung/tw/about/" target="_blank">台中富信大飯店</a></td>
        <td>臺中市中區市府路14號</td>
        <td>0422296999</td>
      </tr>
      <tr>
        <td>三星級</td>
        <td><a href="https://www.allurmotel.com/room.php?cid=8" target="_blank">歐遊國際精品旅館(台中館)</a></td>
        <td>臺中市南屯區文心南路98號</td>
        <td>0424727711</td>
      </tr>
      <tr>
        <td>二星級</td>
        <td><a href="https://www.ourseahotel.com/" target="_blank">梧棲行旅</a></td>
        <td>臺中市梧棲區大仁路2段291巷10號</td>
        <td>0426570857</td>
      </tr>
      <tr>
        <td>二星級</td>
        <td><a href="https://www.viphotel.com.tw/portfolio/palmer-hotel/" target="_blank">博奇大飯店</a></td>
        <td>臺中市中區雙十路一段5號</td>
        <td>0422296151</td>
      </tr>
      <tr>
        <td>三星級</td>
        <td><a href="http://taichung.villa-group.com.tw/" target="_blank">挪威森林文創休閒旅館</a></td>
        <td>臺中市南區正氣街36號</td>
        <td>0422873636</td>
      </tr>
      <tr>
        <td>三星級</td>
        <td><a href="http://tc.cloud-hotel.com.tw/zh-tw" target="_blank">雲端商務旅館</a></td>
        <td>臺中市中區公園路36號</td>
        <td>0422288168</td>
      </tr>
    </tbody>
  </table>

  <h2>台中市旅館分布推斷與未來規劃</h2>
  <p>根據目前台中市旅館的分布情況，我們可以觀察到大部分旅館旅館分布在台中火車站附近。</p>
  <p>未來，我們可以考慮因為市中心星級旅館的持續繁榮與升級。 隨著台中火車站周邊交通機能的提升（例如：捷運藍線的開通），以及都市更新計畫的推動，該區域的商業活動將更加蓬勃。五星級或更好的旅館可能會持續吸引高端商務旅客和觀光客，並為了維持競爭力而進行設施和服務的升級，甚至引進更具特色的主題或設計。</p>

  <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
  <script>
    var mymap = L.map('mapid').setView([24.15, 120.65], 12); // 設定地圖中心和縮放

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors'
    }).addTo(mymap);

    // 旅館資料陣列 (包含星級)
    var hotels = [
      { name: '台中日月千禧酒店', star: 5, lat: 24.1567302, lng: 120.6394838 },
      { name: '長榮桂冠酒店(台中)', star: 5, lat: 24.1589291, lng: 120.6545249 },
      { name: '巧合大飯店', star: 2, lat: 24.1382495, lng: 120.6827453 },
      { name: '中科大飯店', star: 3, lat: 24.1748009, lng: 120.6834606 },
      { name: '創意時尚旅店', star: 2, lat: 24.1521818, lng: 120.6778114 },
      { name: '成旅晶贊飯店', star: 3, lat: 24.1375375, lng: 120.680427 },
      { name: '台中港酒店', star: 4, lat: 24.2602639, lng: 120.5311567 },
      { name: '清新溫泉飯店', star: 5, lat: 24.1422381, lng: 120.6096036 },
      { name: '美之旅商務飯店', star: 2, lat: 24.1479955, lng: 120.6594073 },
      { name: '裕元花園酒店', star: 5, lat: 24.1799274, lng: 120.621489 },
      { name: '墨鐵會館', star: 2, lat: 24.1428135, lng: 120.6742112 },
      { name: '台中富信大飯店', star: 3, lat: 24.1391338, lng: 120.6772541 },
      { name: '歐遊國際精品旅館(台中館)', star: 3, lat: 24.1349799, lng: 120.6443397 },
      { name: '台中金典酒店', star: 5, lat: 24.1560646, lng: 120.6604982 },
      { name: '梧棲行旅', star: 2, lat: 24.2623909, lng: 120.5331495 },
      { name: '博奇大飯店', star: 2, lat: 24.1404251, lng: 120.683092 },
      { name: '挪威森林文創休閒旅館', star: 3, lat: 24.1300544, lng: 120.6797755 },
      { name: '雲端商務旅館', star: 3, lat: 24.1459917, lng: 120.677806 }
    ];

    hotels.forEach(function(hotel) {
      var starClass = '';
      if (hotel.star === 5) {
        starClass = 'five-star';
      } else if (hotel.star === 4) {
        starClass = 'four-star';
      } else if (hotel.star === 3) {
        starClass = 'three-star';
      } else if (hotel.star === 2) {
        starClass = 'two-star';
      }

      var icon = L.divIcon({
        className: 'landmark-icon ' + starClass,
        html: hotel.star // 顯示星級
      });

      L.marker([hotel.lat, hotel.lng], { icon: icon })
        .addTo(mymap)
        .bindPopup(`<strong>${hotel.name}</strong><br>星級：${hotel.star} 星`);
    });
  </script>

</body>
</html>
