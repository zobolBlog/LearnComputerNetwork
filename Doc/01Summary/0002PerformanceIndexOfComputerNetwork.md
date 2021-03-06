## 计算机网络的性能指标
在平常生活中，我们经常遇到：
* 办手机套餐的时候，经常会询问朋友，哪一家的通讯套餐目前速度更快，价格更实惠，更稳定？
* 在公司办公楼一般我们的信号都很好，但是到了偏远地区信号就会很慢。
* 很多时候，晚上7~9点一般是网速比较慢的时段，凌晨深夜的网速一般比较快。
* 去海上或者深山探险的人，往往会额外购买卫星通讯设备和账号


这就说明，**不同的计算机网络之间是存在一定差异**的。
对于不同需求的人群，提供不同的计算机网络，是通讯提供商必须要做的事情。
```
（1）不是网速越快越好，很多时候稳定，紧急时刻能确保信号连通更重要
（2）网速过快，也要考虑搭建成本，费用问题。比如5G的硬件费用居高不下
（3）搭建一个小公司的网络，没必要考虑太多所谓“高并发”问题
（4）系统的备份恢复有时候优先于效率
（5）系统的性能并不是一成不变的，它随着时段不同而变化
```

具体的评价指标一般分为：**速率/带宽、吞吐量、时延、时延带宽积、往返时间、利用率、丢包率**等。
```
看着指标有很多，其实总结就两点：速度和安全。即一秒钟传输多少数据/传输一单位数据要多久；信息的准确到达率。
```
### 速率
速率就是在信道上的**传输数据的速度**，被定义为该信道**一秒钟**传输的**比特**的数量。
```
比特就是 “二进制数字1、0”的音译。一般用小写b或bit表示
```
速率可以分为瞬时速率，平均速率、额定速率。
```
（1）瞬时速率就是当前的传输速率，一般在很多下载软件都能看到这种
（2）平均速率，一般最能反应网络的性能好坏。
（3）额定速率，一般就是厂家给你宣传的速率，不一定是最高速率，但一般达不到宣传那么高。
```
明确数据量bit、B、KB、MB、GB和速率b/s、Kb/s、Mb/s、Gb/s的区别.
```
（1）1 字节B = 8bit(这样定义主要是2^8=256足够表示英文中所有字母和标点符号)。
（2）数据量等级是二进制递增的，除首次外，每次递增2^10的指数差距（1B = 8 bit）。
（3）速率等级是十进制递增的，每次递增10^3的指数差距。
```

<p align="center"><img width="400" height="300" src="/LearnComputerNetwork/Photo/02.jpg"></p>


许多人分不清两者区别，做题习惯用口诀“**大B二进制，小b十进制**”,我认为这是不好的习惯。。



```
（1）速率选择十进制，是因为本质是一个物理量，除法得到，是给外行人士看的。使用十进制表示更直观，十进制适合除法表示。
同时速率必须选择比特bit作为数量基准，不可以使用字节B等。
（2）数据量选择二进制，选择字节作为基准，是因为计算机内部都是二进制存储的，字节也是大部分操作系统访问的最小单元，是给专业人士看的，
而且计算机涉及到内存的访问都是二进制的。
```
速率必须是比特bit为基准，数据量一般选择字节B。
```diff
- 许多硬盘厂家，采用用十进制表明硬盘存储量，然后用户拿回去发现不够，告知是因为计算机术语转换问题。
- 这其实是完全子虚乌有的，因为计算机用于存储数据，永远都是二进制，数据的真实存在必须是以二进制存在的。
- 存储数据使用十进制是毫无必要的。
```
<p align="center"><img width="800" height="220" src="/LearnComputerNetwork/Photo/03.jpg"></p>

常见题型：给出一块具体**数据的量**，某个信道的**速率**，**时间**中的任意两者
```diff
+ 因为速率的单位永远都是bit,所以我们把数据量也转为bit的数量，然后进行计算。
+ （注意数据量的K、M、G跟速率的K、M、B意思不一样。）
```

#### 带宽

<div><div ><pre><code style="display: block;background: #1e1e1e;line-height: 160%;border: 0;padding: 18px;color: #f4f4f4;">
（1）不是网速越快越好，很多时候稳定，紧急时刻能确保信号连通更重要
（2）网速过快，也要考虑搭建成本，费用问题。比如5G的硬件费用居高不下
（3）搭建一个小公司的网络，没必要考虑太多所谓“高并发”问题
（4）系统的备份恢复有时候优先于效率
（5）系统的性能并不是一成不变的，它随着时段不同而变化

</code></pre></div></div>


<div class="language-plaintext highlighter-rouge"><div class="highlight"><pre class="highlight"><code style="display: block;background: #1e1e1e;line-height: 160%;border: 0;padding: 18px;color: #f4f4f4;">
（1）不是网速越快越好，很多时候稳定，紧急时刻能确保信号连通更重要
（2）网速过快，也要考虑搭建成本，费用问题。比如5G的硬件费用居高不下
（3）搭建一个小公司的网络，没必要考虑太多所谓“高并发”问题
（4）系统的备份恢复有时候优先于效率
（5）系统的性能并不是一成不变的，它随着时段不同而变化
</code></pre></div></div>


