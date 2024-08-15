---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
Trong workshop này, bạn sẽ học cách triển khai và cấu hình một hệ thống sử dụng **Amazon Application Load Balancer** (ALB) để phân phối lưu lượng truy cập vào các ứng dụng web nằm trong các máy chủ EC2 riêng tư.
Bằng cách sử dụng ALB, bạn có thể đảm bảo rằng lưu lượng truy cập được phân phối đều giữa các máy chủ, giúp cải thiện hiệu suất và độ tin cậy của ứng dụng.

#### Chức năng của Load Balancer
**Load Balancer** đóng vai trò là điểm tiếp nhận duy nhất cho tất cả các yêu cầu từ người dùng. Nó sẽ phân phối các yêu cầu này đến các instance EC2 trong **target group** dựa trên các quy tắc được cấu hình. Điều này giúp cải thiện tính sẵn sàng của ứng dụng và tối ưu hóa việc sử dụng tài nguyên.

#### Chức năng của Application Load Balancer (ALB)
**Amazon Application Load Balancer (ALB)** chịu trách nhiệm phân phối lưu lượng truy cập từ người dùng đến các ứng dụng chạy trên các máy chủ EC2 nằm trong các subnet riêng tư trong VPC của bạn. ALB hoạt động ở lớp 7 của mô hình OSI (lớp ứng dụng), cho phép nó phân phối lưu lượng dựa trên nội dung yêu cầu HTTP/HTTPS, chẳng hạn như đường dẫn URL hoặc header.

#### Chức năng của Target Group
**Target Group** là một nhóm các tài nguyên (chẳng hạn như các instance EC2) mà ALB sẽ gửi lưu lượng truy cập đến. Trong mô hình này, các target group chứa các instance EC2 nằm trong các subnet riêng tư. ALB sẽ theo dõi tình trạng của các instance này và chỉ gửi lưu lượng đến những instance khỏe mạnh, đảm bảo tính sẵn sàng cao của ứng dụng.

![ConnectPrivate](/images/ALB1.drawio.png)