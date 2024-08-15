---
title : "Tạo Internet Gateway"
date :  "`r Sys.Date()`" 
weight : 4
chapter : true
pre : " <b> 2.4 </b> "
---

#### Nội dung

>Internet Gateway trong AWS là cổng giúp kết nối mạng của bạn (VPC) với internet. Nó cho phép các tài nguyên trong mạng, như máy chủ, có thể truy cập internet và ngược lại. Nếu bạn muốn các máy chủ của mình có thể truy cập được từ bên ngoài, bạn cần phải gắn Internet Gateway vào VPC của mình. Đây là thành phần cần thiết để máy chủ trong public subnet có thể giao tiếp với internet.

1. Tạo Internet Gateway
  + Click **internet gateways**.
  + Click **Create internet gateway**.

![igw](/images/2.prerequisite/createIGW-01.png)

2. Tại trang **Create internet gateway**.
  + Tại mục **Name** điền **LAB-IGW**.
  + Click **Create internet gateway**

![igw](/images/2.prerequisite/createIGW-02.png)

3. Attach Internet Gateway vào VPC
  + Click **actions**.
  + Click **Attach to VPC**
  + Tại mục **Available VPCs** chọn **LAB-VPC**
  + Click **Attach internet gateway**

![igw](/images/2.prerequisite/createIGW-03.png)

![igw](/images/2.prerequisite/createIGW-04.png)

4. Kết quả

![igw](/images/2.prerequisite/createIGW-05.png)

5. Cập nhập Internet Gateway cho route table public.
  + Chọn route table **LAB-Public-RouteTable**.
  + Click **actions**.
  + Click **Edit routes**

![igw](/images/2.prerequisite/createIGW-06.png)

6. Tại trang **Edit routes**.
  + Click **Add route**
  + Tại mục **Destination** điền **0.0.0.0/0**.
  + Tại mục **Target** chọn internet gateway vừa khởi tạo.
  + Click **Save changes**

![igw](/images/2.prerequisite/createIGW-07.png)

{{% notice info %}}
Cấu hình IGW vào Public Route Table cho phép các tài nguyên trong public subnet kết nối và giao tiếp với internet.
{{% /notice %}}