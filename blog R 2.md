# 3分鐘弄懂R程式語言！教學2與心得分享 R - Data Types (2020) Introduction of R programming ep2!
![f1](https://github.com/HCH1/blog/blob/master/fig/r2.JPG)

#### [圖文好讀版]()

## 前言
現今的社會與科技進度飛快，也造成的大量的資訊爆炸性的釋出。諸如前幾年常掛在嘴邊的大數據和人工智慧等等。以前的學習或者上班模式，大多是仰賴於紙本與部分的電腦輸入。而如今，可能excel or powerpoint變成人人必備的辦公技能之一。不光是這些偏向專業或辦公的軟體，就算你要當網紅，你也要會基本的app能力，例如: IG FB 修圖軟體等等。總言之，這些軟體是讓你的生活變得更輕鬆，更有趣才是。

你也知道，當你要跨入一個新知識領域，是痛苦且漫長的學習曲線。熟練之前更是一段不歸路，靠的只是一股腦的傻勁與熱誠。順道一提的是，或許你曾經有過此經驗，在學習某事情的當下，時光飛逝，彷彿進入的**心流**。筆者在學習**程式語言R**的時候，就有類似的經驗，故希望寫下一些經驗談與分享，能夠幫助到某些人，也算是樂趣之一。

### (以下節錄自維基百科)
R語言，一種自由軟體程式語言與操作環境，主要用於統計分析、繪圖、數據挖掘。 R本來是由來自新西蘭奧克蘭大學的羅斯·伊哈卡和羅伯特·傑特曼開發（也因此稱為R），現在由“R開發核心團隊”負責開發。 R基於S語言的一個GNU計劃項目，所以也可以當作S語言的一種實現，通常用S語言編寫的代碼都可以不作修改的在R環境下運行。 R的語法是來自Scheme。

R的原始碼可自由下載使用，亦有已編譯的執行檔版本可以下載，可在多種平台下運行，包括UNIX（也包括FreeBSD和Linux）、Windows和MacOS。 R主要是以命令行操作，同時有人開發了幾種圖形用戶界面，其中RStudio是最為廣泛使用的整合開發環境。

### 只要你:
1. 有使用rstudio cloud。
1. 有用過excel整理數據甚至會用vlookup。
這樣你讀這篇會省力。然後我會把一些好用的網路資源或者SOP跟你說，讓你學習曲線可以快速點!


## R - Data Types
## 對象objects
導讀: 常用excel的人，大多數會把數據分成數字或文字，然後進行運算，重組，尋找等等。但程式語言會把這類的數據或變量，看得很細，越低階的語言(越靠近PC端)更是嚴謹，例如你可能有聽過有些blog在說: 字符，寬字符，整數，浮點數，雙浮點數，布林值等。

做任何事情之前，有"對象"是最重要的。。R語言的objects有六種:
1. Vectors
1. Lists
1. Matrices
1. Arrays
1. Factors
1. Data Frames

![f1](https://github.com/HCH1/blog/blob/master/fig/r2b.JPG)

[google關鍵字可以找到有人整理成圖片表示，淺顯易懂!](https://www.google.com/search?q=R+-+Data+Types&tbm=isch&ved=2ahUKEwi6j7jtwLLpAhUS5TgGHQk3Bk8Q2-cCegQIABAA&oq=R+-+Data+Types&gs_lcp=CgNpbWcQAzIECAAQHjIGCAAQCBAeMgYIABAIEB5Q2LfVA1jYt9UDYJy91QNoAHAAeACAASqIASqSAQExmAEAoAEBqgELZ3dzLXdpei1pbWc&sclient=img&ei=qse8XrqSMZLK4-EPie6Y-AQ&bih=937&biw=1920#imgrc=a8II-TxJPvFggM)

### Vectors向量
類似公車很多窗戶，數據住在裡面，一個"直排或橫排，類似數學矩陣的row or col。裡面只能塞同一種類型的數據型態!

### Matrices矩陣
由多個直排或橫排的Vectors組成。裡面只能塞同一種類型的數據型態!

### Data Frames好矩陣
或有人問，若是矩陣不同的直排我想塞入不同的數據型態，例如點名表，第一col放學號，第二col放人名之類。那請用Data Frames就對了。
我在使用R做矩陣處理時候，九成都是轉換成Data Frames，非常實用。

```
# Create the data frame.
BMI <- 	data.frame(
   gender = c("Male", "Male","Female"), 
   height = c(152, 171.5, 165), 
   weight = c(81,93, 78),
   Age = c(42,38,26)
)
print(BMI)
```

### Lists清單
類似捷運車廂，每個車廂可放入不同的對象objects!

### Arrays超矩陣
類似多維度的矩陣，不常用。

## 再來，每個對象objects身上可放數據Data Types。至少五種:
1. integer
1. numeric
1. character
1. logical
1. factor
1. missing

### integer整數
沒有小數點。例如: 1, 100, -9

### numeric數值
要多細有多細，小數點。例如: 0.1, -0.09, 234.567

### character字符
英文字或單字之類的。例如: “A”, “hello”, “welcome”

```
myname <- "nick"
class(myname)
```

### missing
例如excel有時候某欄位是空白的，那R讀取後會視為NA。

### logical邏輯
有人說布林值，代表真或假，二選一。例如: TRUE or FALSE

```
favourite.numeric <- as.numeric(8.8)
print(favourite.numeric)
favourite.numeric == 8.8
```

### factor因素
有意義的類別。例如捷運路線圖表，有一col列出顏色:紅線綠線藍線等等，這就是factor。

```
# Create a vector.
apple_colors <- c('green','green','yellow','red','red','red','green')

# Create a factor object.
factor_apple <- factor(apple_colors)

# Print the factor.
print(factor_apple)
print(nlevels(factor_apple))
```

### 總結: 
對象objects有"向量(vector)"公車 "清單(list)"捷運 矩陣(mx) 好矩陣(df) 超矩陣(array)。

### 然後對象身上的Data Types有: 
在國外搭捷運，付錢有是"整數或小數"，站名"中英(character)"文"二選一(logical)"，很多"顏色(factor)"路線。


## 總結（若喜歡請按讚加分享：）
因為接觸和使用R一年了，故寫下多篇希望能幫到大家！

## End
