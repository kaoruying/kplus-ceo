K PLUS CEO講堂｜GitHub Pages 前台網頁 + Google Sheet 後台報名資料

一、這包檔案內容
1. index.html
   手機優先的報名回覆網站。

2. google-apps-script.js
   Google Sheet 後台串接碼。

3. assets/
   網站使用的主視覺、Logo、講師照片。
   上傳 GitHub Pages 時，assets 資料夾一定要一起上傳。


二、Google Sheet 後台設定
1. 到 Google Drive 建立一份 Google 試算表。
   建議名稱：K PLUS CEO講堂報名資料

2. 打開試算表後，點選：
   擴充功能 → Apps Script

3. 將 google-apps-script.js 內的全部程式碼複製，貼到 Apps Script 編輯器。

4. 儲存專案。

5. 點選：
   部署 → 新增部署作業

6. 類型選擇：
   網頁應用程式

7. 執行身分選擇：
   我

8. 存取權選擇：
   任何人
   或
   知道連結的任何人

9. 按下部署後，複製 Web App URL。


三、將 Google Sheet 後台網址貼回網頁
1. 開啟 index.html。

2. 找到這一行：
   const SCRIPT_URL = "請貼上你的 Google Apps Script Web App URL";

3. 將引號中的文字換成剛剛複製的 Web App URL。

4. 儲存 index.html。


四、GitHub Pages 上傳方式
1. 建立一個新的 GitHub Repository。
   建議名稱：kplus-ceo-registration

2. 將以下內容一起上傳到 Repository 根目錄：
   index.html
   google-apps-script.js
   README.txt
   assets 資料夾

3. 到 GitHub Repository 的：
   Settings → Pages

4. Source 選擇：
   Deploy from a branch

5. Branch 選擇：
   main / root

6. 儲存後等待 GitHub Pages 產生網址。


五、後台資料欄位
Google Sheet 會自動產生以下欄位：
報名時間
所屬地區
對應場次
與會/參與學員
場次明細
通訊處名稱
姓名
出席回覆
其他需求


六、目前地區與場次判斷
北一、北二、桃竹 → 台北場
台北場(與會學員：北一、北二、桃竹處經理)
8/5(三)下午｜邱光隆｜逆境領導力｜台北金控大樓18樓
11/10(二)下午｜陳慧蓉｜教練引導力｜台北金控大樓18樓

中嘉、台南、高屏 → 高雄場
高雄場(參與學員：中嘉、台南、高屏處經理)
8/11(二）下午｜謝馨慧｜溝通影響力｜高雄明誠大樓12樓
11/11(三）下午｜陳慧蓉｜教練引導力｜高雄明誠大樓12樓


七、重要提醒
1. 如果網站照片讀不到，通常是 assets 資料夾沒有一起上傳。
2. 如果送出後 Google Sheet 沒有資料，請確認 index.html 裡的 SCRIPT_URL 是否已換成 Web App URL。
3. Apps Script 部署權限若不是「任何人」或「知道連結的任何人」，前台網頁可能無法寫入資料。
