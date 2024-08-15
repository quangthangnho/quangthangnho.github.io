---
title : "Tạo EC2"
date :  "`r Sys.Date()`" 
weight : 7
chapter : true
pre : " <b> 2.7 </b> "
---

#### Nội dung

>EC2 (Elastic Compute Cloud) là dịch vụ cung cấp máy chủ ảo trên AWS, cho phép bạn chạy các ứng dụng và dịch vụ với tài nguyên tính toán có thể tùy chỉnh theo nhu cầu. EC2 giúp bạn triển khai, quản lý, và mở rộng hệ thống dễ dàng mà không cần đầu tư vào phần cứng vật lý.


{{% notice info %}}
Ở bài lab này chúng ta sẽ tạo 2 EC2 nằm ở 2 AZ khác nhau.
{{% /notice %}}

1. Tạo EC2
  + Nhập từ khoá **ec2** vào thanh tìm kiếm và chọn dịch vụ **EC2**

![ec2](/images/2.prerequisite/createEC2-01.png)

2. Khởi chạy instance
  + Click **Instances**.
  + Click **Launch instances**.

![ec2](/images/2.prerequisite/createEC2-02.png)

3. Tại trang **Launch an instance**.
  + Tại mục **Name** nhập **LAB-EC2-PRIVATE-01**.
  + Tại mục **Application and OS Images (Amazon Machine Image)** chọn **Amazon Linux 2023 AMI**.
  
![ec2](/images/2.prerequisite/createEC2-03.png)

  + Tại mục **Instance type** chọn **t2.micro**.
  + Tại mục **Key pair (login)** chọn **Proceed without a key pair (Not recommended)** (Ở bài lab này mình không có ssh vào instance nên không cần khởi tạo key pair).
  
![ec2](/images/2.prerequisite/createEC2-04.png)

  + Tại mục **Network settings** chọn **Edit**. 
  + Tại mục **VPC** chọn **LAB-VPC**. 
  + Tại mục **Subnet** chọn **Lab-Private-Subnet-01**. 
  + Tại mục **Auto-assign public IP** chọn **Disabled**.
  + Tại mục **Firewall (security groups)** chọn **Select existing security group**. 
  + Tại mục **Common security groups** chọn **LAB-INSTANCE-SG**.

![ec2](/images/2.prerequisite/createEC2-05.png)

{{% notice info %}}
Ở bước tiếp theo chúng ta sẽ tạo một trang web đơn giản chạy trên instance.
{{% /notice %}}

  + Tại mục **Advanced details** click vào và cuộn xuống cuối trang

![ec2](/images/2.prerequisite/createEC2-06.png)

  + Tại mục **User data - optional** sao chép và dán đoạn script bên dưới vào.

![ec2](/images/2.prerequisite/createEC2-07.png)

  ```
  #!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
```


4. Tạo instance thứ hai tương tự instance thứ nhất ( các mục cần thay đổi).
   + Tại mục **Name** nhập **LAB-EC2-PRIVATE-02**.

![ec2](/images/2.prerequisite/createEC2-08.png)

  + Tại mục **Subnet** chọn **Lab-Private-Subnet-02**. 

![ec2](/images/2.prerequisite/createEC2-09.png)

5. Kết quả

![ec2](/images/2.prerequisite/createEC2-10.png)