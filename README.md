<h1>用LIFFPY建立LIFF網頁</h1>
<p>此文章為如何透過liffpy套件在LINEBOT上面新增LIFF網頁的範本，主要程式碼如下：</p>

```

from liffpy import (
    LineFrontendFramework as LIFF,
    ErrorResponse
)

liff_api = LIFF("你的Channel AcessToken")

try:
    now_LIFF_APP_number = len(liff_api.get())
except:
    now_LIFF_APP_number = 0

target_LIFF_APP_number = 10
print(target_LIFF_APP_number,now_LIFF_APP_number)
if now_LIFF_APP_number < target_LIFF_APP_number:
    for i in range(target_LIFF_APP_number - now_LIFF_APP_number):
        liff_api.add(view_type="full",view_url="https://www.google.com")


```

將上述程式碼新增於LINEBOT主程式中，即可依target_LIFF_APP_number數量生成LIFF網頁

====================================
如果喜歡這個教學內容
歡迎訂閱Youtube頻道
[Maso的萬事屋](https://www.youtube.com/playlist?list=PLG4d6NSc7_l5-GjYiCdYa7H5Wsz0oQA7U)
或加LINE私下交流 LINE ID: mastermaso
![LOGO](https://yt3.ggpht.com/ytc/AKedOLR7I7tw_IxwJRgso1sT4paNu2s6_4hMw2goyDdrYQ=s88-c-k-c0x00ffffff-no-rj)

====================================
