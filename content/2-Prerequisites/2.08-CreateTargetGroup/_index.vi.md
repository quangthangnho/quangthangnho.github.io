---
title : "Tạo Target Group"
date :  "`r Sys.Date()`" 
weight : 8
chapter : true
pre : " <b> 2.8 </b> "
---

#### Nội dung

1. Tạo Target Group
  + Click **Target Groups**.
  + Click **Create target group**.

![ec2](/images/2.prerequisite/createTG-01.png)

2. Tại trang **Specify group details**.
  + Tại mục **Basic configuration** chọn **Instances**.
  + Tại mục **Target group name** nhập **LAB-TARGET-GROUP**.
  + Tại mục **Protocol : Port** nhập **HTTP** và cổng **80**
  + Tại mục **IP address type** chọn **IPv4**
  
![ec2](/images/2.prerequisite/createTG-02.png)

  + Tại mục **VPC** nhập **LAB-VPC**.
  + Tại mục **Protocol version** chọn **HTTP1**
  + Click **Next**
  
![ec2](/images/2.prerequisite/createTG-03.png)

3. Tại trang **Register targets**.
  + Tại mục **Available instances** chọn 2 instance chúng ta vừa khởi tạo
  + Click **Include as pending below**
  + Click **Create target group**
  
![ec2](/images/2.prerequisite/createTG-04.png)


4. Kết quả

![ec2](/images/2.prerequisite/createTG-05.png)