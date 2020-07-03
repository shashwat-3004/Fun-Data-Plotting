# Fun-in-R
This repository contains some fun data plotting using ggplot2 package in R. Inspired and taken help from this blog (https://fronkonstin.com/)  (work going on)

This will be the end result for now (more things later)
![Image](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Img.png)

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
![image1](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot.png)

let's look at the spiral path
```{r}
plot+ geom_path() + theme(text=element_blank(),rect=element_blank())
```
![image2](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot01.png)

Effect of changing angle
```{r}
angle<-2
a<-seq(1,1000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point() + theme(text=element_blank(),rect=element_blank())

angle<-4
a<-seq(1,1000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point() + theme(text=element_blank(),rect=element_blank())
```
![image3](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot02.png)
![image4](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot03.png)

Add colour

```{r}
angle<-13*pi/180
a<-seq(1,1000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point(color="darkgreen",alpha=0.8,aes(size=a)) + theme(text=element_blank(),rect=element_blank(),legend.position = "none")


angle<-pi*(3-sqrt(5)) #golden angle
a<-seq(1,1000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point(color="darkgreen",alpha=0.5,size=10) + theme(text=element_blank(),rect=element_blank(),legend.position = "none")

```
![image5](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot04.png)
![image6](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot05.png)

change Shape

```{r}
angle<-(3-sqrt(5))*pi
a<-seq(1,500)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point(color="darkgreen",shape=8,alpha=0.5,aes(size=a)) + theme(text=element_blank(),rect=element_blank(),legend.position = "none")
```
![image7](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot06.png)

The best part
```{r}
angle<-13*pi/180
a<-seq(1,2000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point(color="darkmagenta",shape=1,alpha=0.1,size=80) + theme(text=element_blank(),rect=element_blank(),legend.position = "none")
```
![image8](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot07.png)

```{r}
angle<-1.8
a<-seq(1,2000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point(color="darkmagenta",shape=1,alpha=0.1,size=80) + theme(text=element_blank(),rect=element_blank(),legend.position = "none")
```

![image9](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot08.png)
```{r}
angle<-2
a<-seq(1,2000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point(color="darkmagenta",shape=1,alpha=0.1,size=80) + theme(text=element_blank(),rect=element_blank(),legend.position = "none")

```
![image10](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot09.png)

```{r}
angle<-2.5
a<-seq(1,2000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point(color="darkblue",shape=1,alpha=0.1,size=80) + theme(text=element_blank(),rect=element_blank(),legend.position = "none")

```
![image11](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot10.png)

```{r}
angle<-1.3
a<-seq(1,2000)*angle 
x<-sin(a)
y<-cos(a)
df<-data.frame(x,y,a)
plot<-ggplot(data=df,aes(x*a,y*a))
plot+ geom_point(color="darkmagenta",shape=1,alpha=0.1,size=80) + theme(text=element_blank(),rect=element_blank(),legend.position = "none")
```

![image12](https://github.com/shashwat-3004/Fun-in-R-/blob/master/Plot/Rplot11.png)




