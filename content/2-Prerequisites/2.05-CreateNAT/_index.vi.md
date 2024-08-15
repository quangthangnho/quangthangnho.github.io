---
title : "Tạo NAT Gateway"
date :  "`r Sys.Date()`" 
weight : 5
chapter : true
pre : " <b> 2.5 </b> "
---

#### Nội dung

>NAT Gateway trong AWS là công cụ giúp các máy chủ trong private subnet có thể truy cập internet mà vẫn giữ an toàn, không bị truy cập từ bên ngoài. Nó hoạt động như một cầu nối, cho phép các máy chủ này tải về các bản cập nhật hoặc liên lạc với các dịch vụ khác trên internet, nhưng không để lộ địa chỉ IP của chúng ra ngoài.


{{% notice info %}}
Để có thể tạo và sử dụng được NAT gateway chúng ta sẽ cần tạo Elastic IP trước.
{{% /notice %}}

1. Tạo Elastic IP

>Elastic IP trong AWS là một địa chỉ IP tĩnh mà bạn có thể gán cho các tài nguyên như máy chủ EC2. Điều này giúp đảm bảo rằng địa chỉ IP của bạn không thay đổi, ngay cả khi bạn khởi động lại hoặc thay đổi phiên bản máy chủ. Elastic IP rất hữu ích khi bạn cần duy trì một địa chỉ IP cố định để các ứng dụng hoặc người dùng có thể dễ dàng truy cập, ngay cả khi hạ tầng bên dưới có thay đổi.

  + Click **Elastic IPs**.
  + Click **Allocate Elastic IP address**.

![nat](/images/2.prerequisite/createNAT-01.png)

2. Tại trang **Allocate Elastic IP address**.
  + Để cấu hình mặc định và có thể thêm tag nếu muốn.
  + Click **Allocate**

![nat](/images/2.prerequisite/createNAT-02.png)

3. Tạo NAT Gateway
  + Click **NAT gateways**.
  + Click **Create NAT gateway**

![nat](/images/2.prerequisite/createNAT-03.png)

4. Tại trang **Create NAT gateway**.
  + Tại mục **Name** nhập **LAB-NAT-GATEWAY**.
  + Tại mục **Subnet** chọn **Lab-Public-Subnet-02**.
  + Tại mục **Elastic IP allocation ID** chọn **Elastic IP** mà ta vừa khởi tạo.
  + Click **Create NAT gateway**

![nat](/images/2.prerequisite/createNAT-04.png)

{{% notice info %}}
NAT gateway sẽ cần mất một khoảng thời gian để khởi tạo và có thể sử dụng. kiểm tra cột State để biết kết quả.
{{% /notice %}}

![nat](/images/2.prerequisite/createNAT-05.png)

![nat](/images/2.prerequisite/createNAT-06.png)

5. Cập nhập NAT Gateway cho route table private.
  + Chọn route table **LAB-Private-RouteTable**.
  + Click **actions**.
  + Click **Edit routes**

![nat](/images/2.prerequisite/createNAT-07.png)

6. Tại trang **Edit routes**.
  + Click **Add route**
  + Tại mục **Destination** điền **0.0.0.0/0**.
  + Tại mục **Target** chọn NAT gateway vừa khởi tạo.
  + Click **Save changes**

![nat](/images/2.prerequisite/createNAT-08.png)

{{% notice info %}}
Cấu hình NAT Gateway vào Private Route Table cho phép các tài nguyên trong private subnet truy cập internet mà không bị truy cập từ bên ngoài.
{{% /notice %}}