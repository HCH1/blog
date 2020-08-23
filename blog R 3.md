# 三分鐘弄懂R程式語言！教學3與心得分享Variables Operators (2020) Introduction of R programming ep3!
![f1](https://github.com/HCH1/blog/blob/master/fig/r3.JPG)

## 前言
現今的社會與科技進度飛快，也造成的大量的資訊爆炸性的釋出。諸如前幾年常掛在嘴邊的大數據和人工智慧等等。以前的學習或者上班模式，大多是仰賴於紙本與部分的電腦輸入。而如今，可能excel or powerpoint變成人人必備的辦公技能之一。不光是這些偏向專業或辦公的軟體，就算你要當網紅，你也要會基本的app能力，例如: IG FB 修圖軟體等等。總言之，這些軟體是讓你的生活變得更輕鬆，更有趣才是。

你也知道，當你要跨入一個新知識領域，是痛苦且漫長的學習曲線。熟練之前更是一段不歸路，靠的只是一股腦的傻勁與熱誠。順道一提的是，或許你曾經有過此經驗，在學習某事情的當下，時光飛逝，彷彿進入的**心流**。筆者在學習**程式語言R**的時候，就有類似的經驗，故希望寫下一些經驗談與分享，能夠幫助到某些人，也算是樂趣之一。


### 只要你:
1. 有使用rstudio cloud。
1. 有用過excel整理數據甚至會用vlookup。
這樣你讀這篇會省力。然後我會把一些好用的網路資源或者SOP跟你說，讓你學習曲線可以快速點!


## Variables變數
我們很常遇到一種情況，例如將一個矩陣，取一個外號。好處是: 程式碼簡潔，也方便歸類和使用，也有一個頓點去做事。
例如: a <- 1 或 a = 1，這樣a就是整數了。當然你取外號可"對象object"或"數據data"來取都可。

然後外號，可取長一點但小心只用以下就好: nick_name，nick.name，nick1name，nickname之類的。一些特殊符號@#$%^就別去亂用當作外號。

### 取外號可用 _ . 123，但都盡量放在中間比較安全

```
# Assignment using equal operator.
var.1 = c(0,1,2,3)           
# Assignment using leftward operator.
var.2 <- c("learn","R")   
# Assignment using rightward operator.   
c(TRUE,1) -> var.3           
print(var.1)
print(var.2)
print(var.3)
```

## Operators算子
1. Arithmetic Operators 算術
1. Relational Operators 關係
1. Logical Operators 邏輯
1. Assignment Operators 賦予
1. Miscellaneous Operators 雜項

### [以google找圖當作範例來說明](https://www.google.com/search?q=R+Variables+Operators&tbm=isch&ved=2ahUKEwj-yrybmbPpAhVFFnIKHfa2DsEQ2-cCegQIABAA&oq=R+Variables+Operators&gs_lcp=CgNpbWcQAzoECAAQHjoGCAAQCBAeOgQIABAYOgYIABAKEBhQoWNY9mRgwmhoAHAAeACAAT6IAXuSAQEymAEAoAEBqgELZ3dzLXdpei1pbWc&sclient=img&ei=USS9Xr7eKMWsyAP27bqIDA&bih=937&biw=1920#imgrc=9ZUHUT2N6Jwm1M)

### Arithmetic Operators 算術
```
: 
+  
-  
*  
/  
%%  
%/%  
^ 
```

就是常見的 加 減 乘 除 指數等等，若常用excel這些都一樣不陌生。大多程式語言這部分都一樣。

```
v <- c( 2,5.5,6)
t <- c(8, 3, 4)
print(v/t)
print(v%%t)
print(v%/%t)
```

### Relational Operators 關係
```
>  
<  
==  
<=  
>=  
!=
```

基本上就是 大於 等於 小於 不等於 

```
v <- c(2,5.5,6,9)
t <- c(8,2.5,14,9)
print(v == t)
print(v!=t)
```

### Logical Operators 邏輯
```
&  
|  
!  
&&  
||
```
比較少用。

```
v <- c(3,1,TRUE,2+3i)
t <- c(4,1,FALSE,2+3i)
#
print(v&t)
[1]  TRUE  TRUE FALSE  TRUE

print(v|t)
[1]  TRUE FALSE  TRUE  TRUE

print(!v)
[1] FALSE  TRUE FALSE FALSE

print(v&&t)
[1] TRUE

print(v||t)
[1] FALSE
```

### Assignment Operators 賦予
就是前半部面講過的取外號。

### Miscellaneous Operators 雜項
```
%in% (滿常用的)    
%*%
:  
```

```
#檢查東西是否在向量vector裡面
v1 <- 8
v2 <- 12
t <- 1:10
print(v1 %in% t) 
print(v2 %in% t) 
```

```
#矩陣matrix的乘法運算。M_2x3 %*% N_3x2 會變成M_2x2
M = matrix( c(2,6,5,1,10,4), nrow = 2,ncol = 3,byrow = TRUE)
t = M %*% t(M)
print(t)
```

```
#給頭尾去生成vector
v <- 2:8
print(v)
```

## 總結
取外號 算數學 比大小邏輯 還有檢查是否在裡面 這些很常用


## 若喜歡請按讚加分享：）
因為接觸和使用R一年了，故寫下多篇希望能幫到大家！

## End
