---
title : "Tạo Application Load Balancer"
date :  "`r Sys.Date()`" 
weight : 9
chapter : true
pre : " <b> 2.9 </b> "
---

#### Nội dung

1. Tạo Application Load Balancer (ALB)
  + Click **Load Balancers**.
  + Click **Create load balancer**.

![alb](/images/2.prerequisite/createALB-01.png)

2. Tại trang **Compare and select load balancer type**.
  + Click **Create** tại phần **Application Load Balancer**

![alb](/images/2.prerequisite/createALB-02.png)

  + Tại trang **Create Application Load Balancer**.
  + Tại mục **Load balancer name** nhập **LAB-ALB**
  
![alb](/images/2.prerequisite/createALB-03.png)

  + Tại mục **VPC** nhập **LAB-VPC**
  + Tại mục **Availability Zones** chọn **Lab-Public-Subnet-01** và **Lab-Public-Subnet-02**
  + Tại mục **Security groups** chọn **LAB-ALB-SG**

![alb](/images/2.prerequisite/createALB-04.png)

  + Tại mục **Listeners and routing** cấu hình **forward to** sang **target group** mà chúng ta vừa tạo.
  + Click **Create load balancer**

![alb](/images/2.prerequisite/createALB-05.png)

3. Kết quả
  + Kiểm tra cột Status để xem trạng thái của ALB

![alb](/images/2.prerequisite/createALB-06.png)


![alb](/images/2.prerequisite/createALB-07.png)
