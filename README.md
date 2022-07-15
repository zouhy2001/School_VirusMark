[toc]
# 使用方法
### 更新日志
2022.7.15 针对系统接口更新,脚本也更新支持新版接口打卡 唯一不同的是需要抓包获取auth_token 使用门槛大大提高
![](https://s3.bmp.ovh/imgs/2022/07/15/a3a5dc57d9da7362.png)
![](https://s3.bmp.ovh/imgs/2022/07/15/5e9ef3b459753ca9.png)
~~2022.1.26 新增批量查询学生签到情况,QQ机器人班级群提醒 具体见文档~~

2021.12.12 新增老师打卡支持,使用teacher.py 原学号处填工号 即可,感谢 [@xcf13363175](https://github.com/xcf13363175) 老师的issue
### 1.天才第一步
给本项目点个star😋

### 2.请完整阅读免责声明

<p align="center">免责声明</p>

脚本默认上报周围无疫情情况，当周围身边确无疫情发生时，可以使用此脚本，如有疫情，请停止立即使用此脚本，如实上报情况。一切开发旨在学习，请勿用于非法用途，所有不当使用与本人无关。

### 3.把main.py中的几大参数正确填好即可

![](https://i.bmp.ovh/imgs/2022/07/15/95d676540a2ca6f8.png)

**参数1**	为学校代码，我爬取了大部分江西高校的学校代码，可在下方自行查询

**参数2**	为个人学号，自填

**参数3 4** 	分别为经纬信息，查询方法为在[高德坐标拾取器(传送门click)](https://lbs.amap.com/tools/picker)中输入地址获取打卡位置的经纬坐标

**auth_token** 需要自己抓包 在 https://xyfyapi.jx.edu.cn/ali-pay/login 这个请求的请求体里 如更新日志图


![](https://z3.ax1x.com/2021/06/03/21MHZ8.png)

**后面几个参数按照你Alipay里历史打卡记录看着填就行。**

### 4.将脚本使用云函数执行，or使用服务器定时执行，即可

**注意！！！腾讯云函数的执行方法要填为 index.main**

[无服务器，腾讯云函数使用方法](https://blog.csdn.net/weixin_46486156/article/details/113555818?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-5.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-5.control)

[有服务器，linux下使用crontab定时执行py脚本](https://blog.csdn.net/libaominshouzhang/article/details/91597848)



## 说唱学校代码

唱跳rap篮球+F （Search学校名） 即Ctrl+F

|            学校名            |  学校代码  |
| :--------------------------: | :--------: |
|           南昌大学           | 4136010403 |
|         华东交通大学         | 4136010404 |
|         东华理工大学         | 4136010405 |
|         南昌航空大学         | 4136010406 |
|         江西理工大学         | 4136010407 |
|        景德镇陶瓷大学        | 4136010408 |
|         江西农业大学         | 4136010410 |
|        江西中医药大学        | 4136010412 |
|          赣南医学院          | 4136010413 |
|         江西师范大学         | 4136010414 |
|         上饶师范学院         | 4136010416 |
|           宜春学院           | 4136010417 |
|         赣南师范大学         | 4136010418 |
|          井冈山大学          | 4136010419 |
|         江西财经大学         | 4136010421 |
|         江西科技学院         | 4136010846 |
|          景德镇学院          | 4136010894 |
|           萍乡学院           | 4136010895 |
|       江西科技师范大学       | 4136011318 |
|         南昌工程学院         | 4136011319 |
|         江西警察学院         | 4136011504 |
|           新余学院           | 4136011508 |
|           九江学院           | 4136011843 |
|         江西工程学院         | 4136012766 |
|         南昌理工学院         | 4136012795 |
|       江西应用科技学院       | 4136012938 |
|         江西服装学院         | 4136013418 |
|         南昌职业大学         | 4136013420 |
|          南昌工学院          | 4136013421 |
|     南昌大学科学技术学院     | 4136013429 |
|       南昌大学共青学院       | 4136013430 |
|     华东交通大学理工学院     | 4136013431 |
|     东华理工大学长江学院     | 4136013432 |
|     南昌航空大学科技学院     | 4136013433 |
|   江西理工大学应用科学学院   | 4136013434 |
|  景德镇陶瓷大学科技艺术学院  | 4136013435 |
|    江西农业大学南昌商学院    | 4136013436 |
|    江西中医药大学科技学院    | 4136013437 |
|   江西师范大学科学技术学院   | 4136013438 |
|     赣南师范大学科技学院     | 4136013439 |
|   江西科技师范大学理工学院   | 4136013440 |
| 江西财经大学现代经济管理学院 | 4136013441 |
|         豫章师范学院         | 4136013774 |
|     江西软件职业技术大学     | 4136013776 |
|         南昌师范学院         | 4136014437 |
|   上饶幼儿师范高等专科学校   | 3636000312 |
|   抚州幼儿师范高等专科学校   | 3636000519 |
|     江西工业职业技术学院     | 4136010839 |
|     江西医学高等专科学校     | 4136010888 |
|         九江职业大学         | 4136011505 |
|       九江职业技术学院       | 4136011785 |
|     江西司法警官职业学院     | 4136012929 |
| 江西陶瓷工艺美术职业技术学院 | 4136012930 |
|     江西旅游商贸职业学院     | 4136012932 |
|     江西电力职业技术学院     | 4136012933 |
|     江西环境工程职业学院     | 4136012934 |
|       江西艺术职业学院       | 4136012936 |
|       鹰潭职业技术学院       | 4136012937 |
|   江西信息应用职业技术学院   | 4136012939 |
|     江西交通职业技术学院     | 4136012940 |
|       江西财经职业学院       | 4136012941 |
|     江西应用技术职业学院     | 4136012942 |
|     江西现代职业技术学院     | 4136012943 |
|   江西工业工程职业技术学院   | 4136012944 |
|     江西机电职业技术学院     | 4136012976 |
|       江西科技职业学院       | 4136013419 |
|     江西外语外贸职业学院     | 4136013422 |
|   江西工业贸易职业技术学院   | 4136013423 |
|       宜春职业技术学院       | 4136013424 |
|     江西应用工程职业学院     | 4136013425 |
|     江西生物科技职业学院     | 4136013426 |
|     江西建设职业技术学院     | 4136013427 |
|       抚州职业技术学院       | 4136013428 |
|    江西中医药高等专科学校    | 4136013775 |
|     江西经济管理职业学院     | 4136013866 |
|     江西制造职业技术学院     | 4136013867 |
|       江西工程职业学院       | 4136013868 |
|       江西青年职业学院       | 4136013869 |
|       上饶职业技术学院       | 4136013870 |
|     江西航空职业技术学院     | 4136013871 |
|     江西农业工程职业学院     | 4136013872 |
|       赣西科技职业学院       | 4136013873 |
|       江西卫生职业学院       | 4136013965 |
|    江西新能源科技职业学院    | 4136014166 |
|   江西枫林涉外经贸职业学院   | 4136014167 |
|     江西泰豪动漫职业学院     | 4136014168 |
|     江西冶金职业技术学院     | 4136014241 |
|       江西管理职业学院       | 4136014249 |
|       江西传媒职业学院       | 4136014250 |
|     江西工商职业技术学院     | 4136014321 |
|    景德镇陶瓷职业技术学院    | 4136014402 |
|       共青科技职业学院       | 4136014403 |
|     赣州师范高等专科学校     | 4136014465 |
|       江西水利职业学院       | 4136014476 |
|   宜春幼儿师范高等专科学校   | 4136014494 |
|       吉安职业技术学院       | 4136014504 |
|       江西洪州职业学院       | 4136014505 |
|     江西师范高等专科学校     | 4136014537 |
|     南昌影视传播职业学院     | 4136014544 |
|     赣南卫生健康职业学院     | 4136014569 |
|       萍乡卫生职业学院       | 4136014656 |
|     江西婺源茶业职业学院     | 4136014657 |
|       赣州职业技术学院       | 4136014665 |
