# 3分鐘弄懂R程式語言！教學6與心得分享read.csv as.data.frame write.csv (2020) Introduction of R programming ep6!
![f1](https://github.com/HCH1/blog/blob/master/fig/r5.JPG)

## 前言
現今的社會與科技進度飛快，也造成的大量的資訊爆炸性的釋出。諸如前幾年常掛在嘴邊的大數據和人工智慧等等。以前的學習或者上班模式，大多是仰賴於紙本與部分的電腦輸入。而如今，可能excel or powerpoint變成人人必備的辦公技能之一。不光是這些偏向專業或辦公的軟體，就算你要當網紅，你也要會基本的app能力，例如: IG FB 修圖軟體等等。總言之，這些軟體是讓你的生活變得更輕鬆，更有趣才是。

你也知道，當你要跨入一個新知識領域，是痛苦且漫長的學習曲線。熟練之前更是一段不歸路，靠的只是一股腦的傻勁與熱誠。順道一提的是，或許你曾經有過此經驗，在學習某事情的當下，時光飛逝，彷彿進入的**心流**。筆者在學習**程式語言R**的時候，就有類似的經驗，故希望寫下一些經驗談與分享，能夠幫助到某些人，也算是樂趣之一。

### 只要你:
1. 有使用rstudio cloud。
1. 有用過excel整理數據甚至會用vlookup。
這樣你讀這篇會省力。然後我會把一些好用的網路資源或者SOP跟你說，讓你學習曲線可以快速點!


![f1](https://github.com/HCH1/blog/blob/master/fig/r5b.JPG)

## read.csv讀檔案 write.csv()存檔案
網路或blog常常教你如何慢慢刻寫出矩陣或者技巧很五花八門，但我後來發現，真實生活常遇到的案例常常是，有一個excel檔案給你，你要分析該怎辦?
但這邊所分享的，大多是程式碼前幾行的範本，千篇一律，基本功。

以下範本: 若計算的package很特別那一開始就要先呼叫該懶人包library()。

再來就是任何你的數據，你就先存成excel CSV，然後讓R去讀取，使用read.csv()，header代表第一row你要不要當表格的標題?

再來就是先轉成好矩陣as.data.frame(in1)，最好給他取外號讓他變成其他，好處是: 才不會影響到原始數據。原始數據有時候也會給別人使用。

中間就是一連串的計算，最常見動作就是儲存檔案write.csv()，x=代表數據來源，file=代表檔案名稱。

R語言，工作文件夾的位置很重要，你要在對的位置，才能讀取檔案，存檔案也是會被放在那。
四格介面，一些地方提醒你: 
1. 右下畫面上邊有按鈕upload可上傳檔案。
1. more > set as working 可把工作位置變成當下。這些是常做必要的。檔案要下載就用export。
1. 將範例貼在左下畫面按enter，跑完之後會在右上畫面有數據。上邊有data(藍圈白三角)，
1. 點選其中一個data左上畫面，左下畫面會有View(in1)，左上畫面會預覽表格數據，類似excel。這功能很方便階段性思考數據結構，處理後的檢查和找錯。

```
library(plotly)
in1 = read.csv("ask1.csv", header = TRUE)
in2 <- as.data.frame(in1)
a=1
b=1.1
c="red"
d=TRUE
ans1 <- in2
write.csv(x = ans1, row.names = FALSE, file = "ask2.csv")
```

![f1](https://github.com/HCH1/blog/blob/master/fig/r5c.JPG)

## 最後介紹常用語法，用來檢查對象數據:
```
dir() #工作位置當下有哪些檔案?
setwd("/cloud/project") #設定工作環境。也可用右下畫面按鈕設定
getwd() #工作位置是?

str() #診斷對象或數據型態
class() #速診對象或數據型態
dim() #算矩陣維度
length() #算向量長度
head() #列出數據前十項
as.data.frame() #轉換成好矩陣
as.character() #轉換成字
```

```
class(a)
[1] "numeric"
class(b)
[1] "numeric"
class(c)
[1] "character"
class(d)
[1] "logical"
class(in1)
[1] "data.frame"
```
## 總結
讀檔案，計算，存檔案。有不懂得就去官網查語法，除非天天用，不然一定忘。
其實範本代表規律常做的事情，接觸R語言一段時間後，你也會有自己的範本。這裡先給你懶人包，比較貼近真實案例。


## 若喜歡請按讚加分享：）
因為接觸和使用R一年了，故寫下多篇希望能幫到大家！

## End
