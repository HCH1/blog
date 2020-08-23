ㄇ# 3分鐘弄懂R程式語言！教學1與心得分享rstudio cloud (2020) Introduction of R programming ep1!
![f1](https://github.com/HCH1/blog/blob/master/fig/r1.JPG)

#### [圖文好讀版]()

## 前言
現今的社會與科技進度飛快，也造成的大量的資訊爆炸性的釋出。諸如前幾年常掛在嘴邊的大數據和人工智慧等等。以前的學習或者上班模式，大多是仰賴於紙本與部分的電腦輸入。而如今，可能excel or powerpoint變成人人必備的辦公技能之一。不光是這些偏向專業或辦公的軟體，就算你要當網紅，你也要會基本的app能力，例如: IG FB 修圖軟體等等。總言之，這些軟體是讓你的生活變得更輕鬆，更有趣才是。

你也知道，當你要跨入一個新知識領域，是痛苦且漫長的學習曲線。熟練之前更是一段不歸路，靠的只是一股腦的傻勁與熱誠。順道一提的是，或許你曾經有過此經驗，在學習某事情的當下，時光飛逝，彷彿進入的**心流**。筆者在學習**程式語言R**的時候，就有類似的經驗，故希望寫下一些經驗談與分享，能夠幫助到某些人，也算是樂趣之一。

### (以下節錄自維基百科)
R語言，一種自由軟體程式語言與操作環境，主要用於統計分析、繪圖、數據挖掘。 R本來是由來自新西蘭奧克蘭大學的羅斯·伊哈卡和羅伯特·傑特曼開發（也因此稱為R），現在由“R開發核心團隊”負責開發。 R基於S語言的一個GNU計劃項目，所以也可以當作S語言的一種實現，通常用S語言編寫的代碼都可以不作修改的在R環境下運行。 R的語法是來自Scheme。

R的原始碼可自由下載使用，亦有已編譯的執行檔版本可以下載，可在多種平台下運行，包括UNIX（也包括FreeBSD和Linux）、Windows和MacOS。 R主要是以命令行操作，同時有人開發了幾種圖形用戶界面，其中RStudio是最為廣泛使用的整合開發環境。

### 只要你:
1. 有電腦，MAC or WIN10都可以。
1. 要有網路，有網頁例如chrome。因為隨後會介紹基於網路撰寫的R介面。
1. 會用excel or google excel，有用過vlookup等等的公式或邏輯運算。
這樣你讀這篇會省力。

然後我會把一些好用的網路資源或者SOP跟你說，讓你學習曲線可以快速點!


## [請先註冊rstudio cloud](https://rstudio.cloud/projects)
我不太懂為何很少blog提到這個，rstudio cloud，只要有網路網頁，不受限於地點或很多台電腦，就可以使用。

你要寫excel你就必須安裝office，不然就是用網路excel or google excel。R語言類似，你要不就安裝R語言在你的電腦裡，若你有三台電腦，你就要安裝三次然後三次維護更新。第二種方法就是使用網路R，但百家爭鳴，這裡我使用並推薦rstudio cloud。

rstudio cloud可直接用github登入，github也好用，或可考慮，一勞永逸。

### [或可考慮一起註冊github(擺放程式碼的地方)](https://github.com/)


![f1](https://github.com/HCH1/blog/blob/master/fig/r1c.JPG)

![f1](https://github.com/HCH1/blog/blob/master/fig/r1b.JPG)

## 左邊欄位的guide。Your Workspace > Projects
接下來介紹rstudio cloud操作介面UI。首先左邊欄位中間的guide，會教你如何建立專案。類似再google drive建立folder和excel。

左邊上面點選Your Workspace，畫面中上點選Projects，建立。過幾秒鐘後，畫面中間會出現Untitled Project。點選後會進去到rstudio cloud UI。

(我習慣把介面改成黑底，不傷眼。可去tools > optoins修改)

![f1](https://github.com/HCH1/blog/blob/master/fig/r1d.JPG)

畫面分成四個，田字。
1. 左上是撰寫code。
1. 左下是運算結果。
1. 右上會儲存數據，可以點開來看。
1. 右下類似於我的電腦，可看資料放哪，也可上傳 刪除 改名檔案，點選more，還可複製 輸出 設定R的工作位置。

首先新手可先玩玩看左上畫面，可上網找一下些簡單運算，然後點選run，即可運算。

或者直接把程式碼，貼到左下畫面，按下enter，即可運算。

範例:
```
# My first program in R Programming
myString <- "Hello, World!"
print ( myString)

# Create a matrix.
M = matrix( c('a','a','b','c','b','a'), nrow = 2, ncol = 3, byrow = TRUE)
print(M)

# Create a list.
list1 <- list(c(2,5,3),21.3,sin)

# Print the list.
print(list1)
```

## [cheat sheets](https://rstudio.cloud/learn/cheat-sheets)，要知道這裡可以查一些進階語法。
這很方便，有些常用熱門的package (類似懶人包)，或被整理成兩到三頁的總結，會有一個全面的概觀!

## 總結（若喜歡請按讚加分享：）
因為接觸和使用R一年了，故寫下多篇希望能幫到大家！

## End
