twgeojson
=========

行政區域疆界
county = 縣市, town = 鄉鎮市區, village = 村里
以下資料在 [Dropbox](https://www.dropbox.com/sh/w7yq1muzpkhr4lq/h9-AIV6OCh) 上也有放一份

村里界圖
--------
資料來源: [國土資訊圖資資訊中心 - 全國村里界圖（台澎金馬）-經緯度](http://tgos.nat.gov.tw/tgos/Web/Metadata/TGOS_MetaData_View.aspx?MID=36646&SHOW_BACK_BUTTON=false)

資料時間: 2012/11/13(已經升格五都)

檔案說明:

| 檔名                | 說明                         | 大小 |
|---------------------|------------------------------|------|
| twcounty2010.json   | 五都升格後村里圖(原始精度), 共8052村里 | 70M |
| twcounty2010.2.json | 精度 0.01 資料               | 5.8M  |
| twcounty2010.3.json | 精度 0.001 資料              | 8.2M |
| twcounty2010.4.json | 精度 0.0001 資料             | 17M |
| twcounty2010.5.json | 精度 0.00001 資料            | 39M |
| twcounty2010.6.json | 精度 0.000001 資料           | 59M |

鄉鎮市界圖/縣市界圖
-------------------
資料來源: [國土資訊系統社會經濟資料庫共通平台](http://segis.moi.gov.tw/STAT/Web/Platform/Product/STAT_ProductFreeList.aspx)

資料時間: 101年(已經升格五都), 98年(五都升格前)

| 檔名                | 說明                         | 大小 |
|---------------------|------------------------------|------|
| twcounty2010.json   | 五都升格後縣市界圖(原始精度), 共22縣市 | 9.9M |
| twcounty2010.2.json | 精度 0.01 資料               | 89K  |
| twcounty2010.3.json | 精度 0.001 資料              | 362K |
| twcounty2010.4.json | 精度 0.0001 資料             | 1.8M |
| twcounty2010.5.json | 精度 0.00001 資料            | 5.9M |
| twcounty2010.6.json | 精度 0.000001 資料           | 8.8M |

| 檔名                | 說明                         | 大小 |
|---------------------|------------------------------|------|
| twtown2010.json     | 五都升格後鄉鎮縣市界圖(原始精度), 共369鄉鎮 | 33M |
| twtown2010.2.json   | 精度 0.01 資料               | 264K  |
| twtown2010.3.json   | 精度 0.001 資料              | 1.1M |
| twtown2010.4.json   | 精度 0.0001 資料             | 4.7M |
| twtown2010.5.json   | 精度 0.00001 資料            | 16M |
| twtown2010.6.json   | 精度 0.000001 資料           | 28M |

| 檔名                | 說明                         | 大小 |
|---------------------|------------------------------|------|
| twcounty1984.json   | 五都升格前縣市界圖(原始精度), 共25縣市 | 9.4M |
| twcounty1984.2.json | 精度 0.01 資料               | 104K  |
| twcounty1984.3.json | 精度 0.001 資料              | 398K |
| twcounty1984.4.json | 精度 0.0001 資料             | 1.9M |
| twcounty1984.5.json | 精度 0.00001 資料            | 6.3M |
| twcounty1984.6.json | 精度 0.000001 資料           | 8.9M |

| 檔名                | 說明                         | 大小 |
|---------------------|------------------------------|------|
| twtown1984.json     | 五都升格前鄉鎮縣市界圖(原始精度), 共367鄉鎮 | 32M |
| twtown1984.2.json   | 精度 0.01 資料               | 283K  |
| twtown1984.3.json   | 精度 0.001 資料              | 1.1M |
| twtown1984.4.json   | 精度 0.0001 資料             | 4.7M |
| twtown1984.5.json   | 精度 0.00001 資料            | 16M |
| twtown1984.6.json   | 精度 0.000001 資料           | 28M |

其他
----
- parse.php 將 shp 處理成 geojson 的程式，需要有 shp2pgsql (要裝 postgis)
  只需要將 shp 檔抓下來，再用 parse.php xxx.shp 就會產生 output.json 和 output.sample.json 了
- scripts/simplify.php 可以降低精度，作法是 php scripts/simplify.php {old.json} 0.01 > {new.json}
- 如果想要五都升格前的資料，可以到 [https://github.com/g0v/twgeojson](https://github.com/g0v/twgeojson)

