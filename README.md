# 一个地铁让座项目
#### *当你乘坐地铁的时候，有没有是否该让座给对方的烦恼？*
#### *因为我们用二分法来区分对方是很危险的，`如果对方能主动告诉你`，那该有多好啊！* :smile:
---
## sharemseat具体是干啥的？
1.提供想让位置的用户知道谁想坐位置    
2.提供想坐位置的用户知道谁想让位置  
#### *对，你没看错，我们要实现的目标就是这么简单*  
---
## sharemseat的流程是怎么样的？
1.先发布需要让座需求(假设发布需求的人为A)<br />
2.由系统推送给附近相关人，以及可能相关的人(假设让座的人为B)<br />
```
假设可能性1:
A可能附近又多个站点并不确定那个站点可以等到位置 可以同时对多个站点发布座位需求，
需求条件可能为:
1.什么站上车(可以获取站点附近相关的人进行通知)
2.什么时间上车(可以计算出可能的车次)
3.去往什么方向或那一站下车(可以通知相关方向的车次)
```
3.B 看到后如果可以让座则进行需求回应（可能有多个B进行回应）<br />
4.A 看到回应则根据回应选择寻找最近方便的位置 <br />
5.A 完成需求后则需求结束 <br />
```
    完成需求条件：
    * A主动确定坐上位置或者主动取消 
    * 现实时间已经超过发布的时间
```
---
## sharemseat的架构是怎么样的？
方案1：
前端 h5 vue.js 
后端 springmvc

方案2：
h5 vue.js 

数据库-mysql
