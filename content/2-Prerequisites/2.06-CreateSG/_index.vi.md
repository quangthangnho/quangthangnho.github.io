---
title : "Tạo Security Group"
date :  "`r Sys.Date()`" 
weight : 6
chapter : true
pre : " <b> 2.6 </b> "
---

#### Nội dung

>Security Group (SG) là một tường lửa ảo trong AWS, giúp kiểm soát và quản lý luồng lưu lượng đến và đi từ các tài nguyên như EC2 instances. Nó hoạt động dựa trên các quy tắc mà bạn định nghĩa, cho phép hoặc chặn lưu lượng dựa trên địa chỉ IP, giao thức, và cổng. Security Group giúp đảm bảo rằng chỉ những kết nối hợp lệ và an toàn mới được phép truy cập vào tài nguyên của bạn, tăng cường bảo mật hệ thống.


{{% notice info %}}
Ở bài lab này chúng ta sẽ tạo 2 Security Group . 1 Security Group dành cho Application Load Balancer và 1 Security Group dành cho các EC2.
{{% /notice %}}

1. Tạo Security Group cho ALB
  + Click **Security groups**.
  + Click **Create security group**.

![sg](/images/2.prerequisite/createSG-01.png)

2. Tại trang **Create security group**.
  + Tại mục **Security group name** nhập **LAB-ALB-SG**.
  + Tại mục **Description** nhập **allow http from internet**.
  + Tại mục **VPC** chọn **LAB-VPC**.
  + Tại mục **Inbound rules** chọn **Add rule**.
  + Cấu hình type **HTTP** và source **Anywhere-IPv4**
  + Click **Create security group**

![sg](/images/2.prerequisite/createSG-02.png)

3. Tạo Security Group cho EC2
  + Click **Security groups**.
  + Click **Create security group**.

![sg](/images/2.prerequisite/createSG-01.png)

4. Tại trang **Create security group**.
  + Tại mục **Security group name** nhập **LAB-INSTANCE-SG**.
  + Tại mục **Description** nhập **allow http connect from alb**.
  + Tại mục **VPC** chọn **LAB-VPC**.
  + Tại mục **Inbound rules** chọn **Add rule**.
  + Cấu hình type **HTTP** và source chọn SG của ALB vừa khởi tạo **LAB-ALB-SG**
  + Click **Create security group**

![sg](/images/2.prerequisite/createSG-03.png)

5. Kết quả

![sg](/images/2.prerequisite/createSG-04.png)