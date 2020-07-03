# Fun-in-R
This repository contains some fun data plotting using ggplot2 package in R. Inspired and taken help from this blog (https://fronkonstin.com/)  (work going on)

This will be the end result for now (more things later)
![Image](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Img.png)



```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)

```
```{r}
library(ggplot2)
```
Starting simple
Let's Start with a spiral image
```{r}


angle<-13*pi/180
a<-seq(1,1000)*angle #plottting 1000 points
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point() + theme(text=element_blank(),rect=element_blank()) #adding plot layers
```
