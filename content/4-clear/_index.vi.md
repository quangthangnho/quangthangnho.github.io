---
title : "Dọn dẹp resources"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

1. Xoá ALB
  + Di chuyển qua màn hình **Load balancers**
  + Click **LAB-ALB**
  + Click **Actions**
  + Click **Delete load balancer**

![test](/images/2.prerequisite/createClear-01.png)

2. Xoá Target group
  + Di chuyển qua màn hình **Target groups**
  + Click **LAB-TARGET-GROUP**
  + Click **Actions**
  + Click **Delete**

![test](/images/2.prerequisite/createClear-02.png)


3. Xoá Instances
  + Di chuyển qua màn hình **Instances**
  + Click **LAB-EC2-PRIVATE-01** và **LAB-EC2-PRIVATE-02**
  + Click **instance state**
  + Click **Terminate instance**

![test](/images/2.prerequisite/createClear-03.png)

4. Xoá Security group
  + Di chuyển qua màn hình **Instances**
  + Click **LAB-INSTANCE-SG** và **LAB-ALB-SG**
  + Click **Actions**
  + Click **Delete security group**

![test](/images/2.prerequisite/createClear-04.png)

5. Xoá NAT gateways
  + Di chuyển qua màn hình **NAT gateways**
  + Click **LAB-NAT-GATEWAY**
  + Click **Actions**
  + Click **Delete NAT gateway**

![test](/images/2.prerequisite/createClear-06.png)

6. Xoá Elastic IPs
  + Di chuyển qua màn hình **Elastic IP addresses**
  + Chọn IP mà chúng ta đã tạo
  + Click **Actions**
  + Click **Release Elastic IP addresses**

![test](/images/2.prerequisite/createClear-07.png)

6. Xoá Internet gateways
  + Di chuyển qua màn hình **Internet gateways**
  + Click **LAB-IGW**
  + Click **Actions**
  + Click **Detach from VPC**

![test](/images/2.prerequisite/createClear-05.png)

  + Click **LAB-IGW**
  + Click **Actions**
  + Click **Delete internet gateway**

![test](/images/2.prerequisite/createClear-08.png)

6. Xoá VPC
  + Di chuyển qua màn hình **Your VPCs**
  + Click **LAB-VPC**
  + Click **Actions**
  + Click **Delete VPC**

![test](/images/2.prerequisite/createClear-09.png)