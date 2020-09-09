# R 함수 정리

## 함수

* [`as.character(x)`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EB%B3%80%ED%99%98)
* `is.character(x)`
* [`seq()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#3-%EB%B3%80%EC%88%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%B6%9C%EB%A0%A5)
* [`rep()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#3-%EB%B3%80%EC%88%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%B6%9C%EB%A0%A5)
* [`rev()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#3-%EB%B3%80%EC%88%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%B6%9C%EB%A0%A5)
* [`class()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#3-%EB%B3%80%EC%88%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%B6%9C%EB%A0%A5)
* [`names()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#3-%EB%B3%80%EC%88%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%B6%9C%EB%A0%A5)
* [`ls()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#%EC%83%9D%EC%84%B1%EB%90%9C-%EB%B3%80%EC%88%98-%ED%99%95%EC%9D%B8)
* `rm()`
  * [1일차](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#%EB%B3%80%EC%88%98-%EC%82%AD%EC%A0%9C)
  * [2일차 - 변수 전부 지우기](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EB%B3%80%EC%88%98%EB%A5%BC-%ED%8C%8C%EC%9D%BC%EB%A1%9C-%EC%A0%80%EC%9E%A5-%EB%B0%8F-%EB%A1%9C%EB%93%9C)
* `summay()`
  * [1일차](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#6-%EA%B8%B0%EB%B3%B8-%ED%86%B5%EA%B3%84-%ED%95%A8%EC%88%98)
  * [2일차 - 매트릭스](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_2.md#%EA%B8%B0%ED%83%80-%ED%95%A8%EC%88%98)
  * [3일차 - 데이터프레임](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EA%B8%B0%ED%83%80-%ED%95%A8%EC%88%98)
* [`which()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#which)
* [`which.max(x)`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#which)
* [`which.max(x)`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#which)
* [`paste()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#paste)
  * [`print()`]  vs.  [`cat()`]  vs.  [`paste`]
* [`sample()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#sample)
* [`help()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#document-%EC%B0%B8%EC%A1%B0)

<br>

* [`matrix()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_2.md#%EC%83%9D%EC%84%B1)
* `rbind()` & `cbind()`
  * [매트릭스](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_2.md#%EC%83%9D%EC%84%B1)
  * [데이터프레임](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EB%B3%80%ED%99%98)
* [`apply()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_2.md#%EA%B8%B0%ED%83%80-%ED%95%A8%EC%88%98)
* [`array()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_2.md#%EC%83%9D%EC%84%B1-1)

<br>

* [`factor()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EC%83%9D%EC%84%B1)
* [`plot()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EC%B0%B8%EA%B3%A0-plot)
* [`data.frame()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EC%83%9D%EC%84%B1-1)
* [`sort()` & `order()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EC%A0%95%EB%A0%AC) 
  * [`order() - 1일차`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#3-%EB%B3%80%EC%88%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%B6%9C%EB%A0%A5)
* [`str()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EA%B8%B0%ED%83%80-%ED%95%A8%EC%88%98)
* [`table()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EA%B8%B0%ED%83%80-%ED%95%A8%EC%88%98)
* [`subset()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EA%B8%B0%ED%83%80-%ED%95%A8%EC%88%98)
* [`is.na()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EA%B8%B0%ED%83%80-%ED%95%A8%EC%88%98)
* [`dim()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EA%B8%B0%ED%83%80-%ED%95%A8%EC%88%98)
* [`read.csv()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#csv-%ED%8C%8C%EC%9D%BC-%EC%9D%BD%EC%96%B4%EC%98%A4%EA%B8%B0)
* [`file.choose()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#csv-%ED%8C%8C%EC%9D%BC-%EC%9D%BD%EC%96%B4%EC%98%A4%EA%B8%B0)
* [`write.csv()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#csv-%ED%8C%8C%EC%9D%BC-%EC%9D%BD%EC%96%B4%EC%98%A4%EA%B8%B0)
* [`save()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EB%B3%80%EC%88%98%EB%A5%BC-%ED%8C%8C%EC%9D%BC%EB%A1%9C-%EC%A0%80%EC%9E%A5-%EB%B0%8F-%EB%A1%9C%EB%93%9C)
* [`load()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EB%B3%80%EC%88%98%EB%A5%BC-%ED%8C%8C%EC%9D%BC%EB%A1%9C-%EC%A0%80%EC%9E%A5-%EB%B0%8F-%EB%A1%9C%EB%93%9C)
* [`scan()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EB%8D%B0%EC%9D%B4%ED%84%B0-%ED%8C%8C%EC%9D%BC-%EB%A1%9C%EB%93%9C)
* [`readLines()`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_3.md#%EB%8D%B0%EC%9D%B4%ED%84%B0-%ED%8C%8C%EC%9D%BC-%EB%A1%9C%EB%93%9C)
* [`read.table()`]

<br>

* [`list()`]
* [`unlist()`]
* [`ifelse()`]
* [`switch()`]
* [`print()`]  vs.  [`cat()`]  vs.  [`paste`]

<br>

## 제어문

* [`if`]
* [`ifelse()`]
* [`switch()`]
* [`for`]
* [`while`]

<br>

## 내장변수

* [`LETTERS`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#3-%EB%B3%80%EC%88%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%B6%9C%EB%A0%A5)
* [`letters`](https://github.com/lsGee/TIL/blob/master/06.R/R%EA%B8%B0%EC%B4%88_1.md/#3-%EB%B3%80%EC%88%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%B6%9C%EB%A0%A5)