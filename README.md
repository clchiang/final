## 前端程式設計108-1期末報告

### 主題簡介
<p>我的網頁主題是測年齡的小遊戲，使用者選出自己熟悉的歌曲、明星、服裝、遊戲、日用品、食物和流行語之後，可以知道大約是哪個年代的人。</p>

### 如何使用
<p>1. 一開始會進到轉盤的畫面，點按開始後會開始轉，停下後會指著其中一個項目並跳出提示框。</p>
<p>2. 提示框按確定後，點選指到項目的圖片進入測驗（要稍微移動滑鼠，游標出現才能點選）。</p>
<p>3. 進到網頁後按開始，並依照經驗選取答案。</p>
<p>4. 作答完畢按確定鍵，網頁會跳出測驗結果；接受結果按確定，不接受則按取消。</p>
<p>5. 完成後可到Menu選擇下一項測驗。</p>

### 技術說明
#### 轉盤頁面
<p>1. Template來源：http://www.jq22.com/yanshi22646 </p>
<p>2. 用小畫家將中間按鈕改成繁體字。</p>
<p>3. 到https://icons8.com/icons 下載適合的icon，取代模板原來的圖片，並加入超連結。</p>

#### 測驗頁面
<p>1. Template來源：https://startbootstrap.com/themes/agency/ </p>
<p>2. 引用思源黑體字型。</p>
<p>3. button:用css改變底色和字體顏色。</p>
<p>4. 加入選項按鈕（參考https://www.wibibi.com/info.php?tid=190 ）。</p>
<p>5. 插入音樂。</p>
<p>6. 插入圖片，設定大小（300px*300px）。</p>
<p>7. 按確定後跳出測驗結果（jQuery）：</p> 
<p>   原本想依照使用者的回答得到相對應的年代，但做不出來所以改用隨機給出結果。先設定a為隨機選取某範圍數字，不同數字可讓不同對話框出現；對話框按確定則在確定鍵下方顯示"我覺得很準！"，按取消則顯示"再來一次！"</p>

                var txt;
                var a = Math.floor(Math.random() * 3);
                if (a == 0) {
                    var r = confirm("你是90年代的人");
                    if (r == true) {
                        txt = "我覺得很準！";
                    } else {
                        txt = "再來一次！";
                    }
                    document.getElementById("demo").innerHTML = txt;

                } else if (a == 1) {
                    var r = confirm("你是00後的年輕人");
                    if (r == true) {
                        txt = "我覺得很準！";
                    } else {
                        txt = "再來一次！";
                    }
                    document.getElementById("demo").innerHTML = txt;
                } else {
                    var r = confirm("你非常跟得上潮流！");
                    if (r == true) {
                        txt = "我覺得很準！";
                    } else {
                        txt = "再來一次！";
                    }
                    document.getElementById("demo").innerHTML = txt;
                }
            }
        
