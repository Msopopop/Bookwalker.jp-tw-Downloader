# BookWalker 图源下载：支持起止页

[简体](#zh-cn) · [繁體](#zh-tw) · [English](#en)

这个脚本改自 Greasy Fork 上的「bookwalker图源下载」v0.7，主要补了结束页、图片格式，以及几处实际用起来很烦的问题。这里对应 v0.7.4。它不是 BOOK☆WALKER 官方工具。

<a id="zh-cn"></a>

## 简体中文

### 来源

原脚本是 [bookwalker图源下载](https://greasyfork.org/zh-CN/scripts/500575-bookwalker%E5%9B%BE%E6%BA%90%E4%B8%8B%E8%BD%BD)，作者 `summer`（Greasy Fork 页面显示「夏日」），参照的是 v0.7。

### 改了什么

原版只能设起始页。现在可以填结束页，结束页本身也会下载；留空就一直下到最后一页。进度里会同时写本次下载的第几页，以及它在书里的原页码。

不用手动数页也行。翻到想开始的页面，点「设为起始页」；结束页同理。遇到一次显示两页的情况，结束页会取后面那一页。

以前把结束页填得比起始页小，按下载后才会弹出错误窗口，而且关不掉，只能刷新。现在遇到这种范围，下载按钮直接变灰，设置里写出原因；改对了就能继续按。日志窗口也加了「关闭日志」。

图片默认存成 WebP，画质设为最高。想要完全无损，可以在下拉菜单里切到 PNG。两种格式都能逐页保存，也能勾选「打包下载」合成一个 ZIP。文件名里的特殊字符会处理掉，图片按原书页码编号。

网络出错时脚本会重试几次，不会一直转圈；下载中可以取消。打包时会等压缩包真正生成后再提示完成。导出格式和打包选项会记住。

### 怎么装、怎么用

1. 先装 Tampermonkey、Violentmonkey 之类的脚本管理器。
2. 把仓库里的 `bookwalker图源下载-起止页版.user.js` 导入，或新建脚本后把内容完整贴进去。
3. 打开 BOOK☆WALKER 日本站或台湾站的阅读器、试读页面。稍等几秒，右上角会出现「下载图源」。
4. 点旁边的箭头展开设置，填起止页，或直接用两个「设为…」按钮。选好 WebP / PNG，按需勾选打包。
5. 点「下载图源」，等它跑完。下载时别操作阅读器；日志可以关掉，也能按「取消下载」停下来。

单独下载的文件名类似 `书名 - 003.webp`，打包下载会得到 `书名.zip`。

### 用之前留意

原作者提醒过，这类脚本有封号风险。要不要用、用哪个账号试，自己决定。原版主要测过漫画和小说，部分书可能不支持，网站改版后也可能失效。

图片分辨率取决于网站提供的原始图源，可能比阅读器里看到的小。下载时不要同时开几个阅读器页面，很老的浏览器也可能无法打包。请只处理自己有权阅读的内容，不要把下载结果公开传播。

在 Edge 和 Firefox 里试过单页 WebP、ZIP、当前页按钮、无效范围提示和关闭日志。

---

<a id="zh-tw"></a>

## 繁體中文

### 來源

原腳本是 [bookwalker圖源下載](https://greasyfork.org/zh-CN/scripts/500575-bookwalker%E5%9B%BE%E6%BA%90%E4%B8%8B%E8%BD%BD)，作者 `summer`（Greasy Fork 頁面顯示「夏日」），參照的是 v0.7。

### 改了哪些地方

原版只能設起始頁。現在可以填結束頁，而且結束頁本身也會下載；留空就是下載到最後一頁。進度會同時顯示本次下載到第幾張，以及它在書裡原本的頁碼。

不想自己數頁也行。翻到想開始的地方，按「設為起始頁」；結束頁比照辦理。如果畫面一次顯示兩頁，結束頁會取後面那頁。

以前結束頁填得比起始頁小，按下載後才跳出錯誤視窗，偏偏又關不掉，只能重新整理。現在碰到這種範圍，下載按鈕會直接變灰，設定區寫明原因；改好就能繼續。日誌視窗也多了「關閉日誌」。

圖片預設存成 WebP，畫質設到最高。想要完全無損，就在下拉選單改選 PNG。兩種格式都能逐頁存檔，也能勾「打包下載」做成一個 ZIP。書名裡不適合當檔名的字元會自動處理，圖片依原書頁碼編號。

網路出錯會重試幾次，不會一直卡著；下載途中可以取消。打包時會等壓縮檔真的產生，才顯示完成。格式和打包選項會記住，下次打開還在。

### 怎麼裝、怎麼用

1. 先裝 Tampermonkey、Violentmonkey 之類的腳本管理器。
2. 把倉庫裡的 `bookwalker图源下载-起止页版.user.js` 匯入，或新增腳本後把內容完整貼上。
3. 打開 BOOK☆WALKER 日本站或臺灣站的閱讀器、試讀頁面。等幾秒，右上角會出現「下載圖源」。
4. 按旁邊的箭頭展開設定，填起止頁，或直接按兩個「設為…」按鈕。選好 WebP / PNG，需要的話再勾打包。
5. 按「下載圖源」，等它跑完。下載時不要操作閱讀器；日誌可以關掉，也能按「取消下載」停下來。

單張下載的檔名大概會是 `書名 - 003.webp`，打包則會得到 `書名.zip`。

### 使用前請留意

原作者提醒過，這類腳本可能有帳號風險。要不要用、用哪個帳號試，自己判斷。原版主要測過漫畫和小說，有些書可能不支援，網站改版後也可能失效。

圖片解析度取決於網站給的原始圖源，有可能比閱讀器畫面小。下載時不要一次開好幾個閱讀器頁面；太舊的瀏覽器也可能無法打包。請只處理自己有權閱讀的內容，不要把下載結果公開散播。

在 Edge 和 Firefox 裡試過單頁 WebP、ZIP、目前頁按鈕、無效範圍提示和關閉日誌。

---

<a id="en"></a>

## English

### Source

This is a modified copy of [bookwalker图源下载](https://greasyfork.org/zh-CN/scripts/500575-bookwalker%E5%9B%BE%E6%BA%90%E4%B8%8B%E8%BD%BD) v0.7 by `summer` (shown as 「夏日」 on Greasy Fork). 

### What changed

The original only had a start page. You can now set an end page too. That page is included; leave the field empty to go through the last page. Progress shows both the current item in your selection and its page number in the book.

If you don't want to count pages, just open the page you want and click "Set as start page" or "Set as end page". With a two-page spread, the end button uses the later page number.

The old popup was the annoying part. Enter an end page before the start page, click download, and the error window would sit there until you reloaded. Now the button turns gray right away and the menu tells you why. Fix the numbers and the button comes back. There is also a "Close log" button.

WebP is the default, at the highest quality setting. Switch to PNG if you want lossless files. Either format can be saved one page at a time or collected into one ZIP. Unsafe characters in book titles are cleaned up, and files are numbered by their original book page.

A failed page gets a few retries instead of spinning forever. You can cancel while it runs, and ZIP mode waits until the archive actually exists before reporting success. Format and ZIP choices are remembered.

### Install and use

1. Install a userscript manager such as Tampermonkey or Violentmonkey.
2. Import `bookwalker图源下载-起止页版.user.js` from this repository, or create a new userscript and paste the file into it.
3. Open a reader or preview page on BOOK☆WALKER's Japanese or Taiwan site. After a few seconds, "Download images" appears in the upper-right corner.
4. Click the arrow beside it. Enter your page range or use the two "Set as..." buttons, pick WebP or PNG, and turn on ZIP mode if you want one archive.
5. Click "Download images" and wait. Don't use the reader while it runs. You can close the log or stop with "Cancel download".

A single file looks like `Title - 003.webp`. ZIP mode gives you `Title.zip`.

### Before you start

The original author warned that scripts like this may put an account at risk. Decide for yourself whether to use it and which account to try. Comics and novels are what the original was mainly tested on. Some books may not work, and a site update can break the script.

Images keep the resolution supplied by the site, so they may look smaller than the viewer. Don't run several reader pages at once. Very old browsers may have trouble with ZIP mode. Only use content you are allowed to read, and don't share the files publicly.

Single-page WebP, ZIP, current-page buttons, invalid-range handling, and closing the log were tried in Edge and Firefox.
