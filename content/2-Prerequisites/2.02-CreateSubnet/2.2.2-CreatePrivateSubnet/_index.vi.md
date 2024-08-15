---
title : "Tạo Private subnet"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2.1 </b> "
---

#### Tạo Private subnet

Theo mô hình thì chúng ta sẽ tạo 2 private subnet trên 2 AZ khác nhau.

1. Click **Subnets**.
  + Click **Create subnet**.

![PublicSubnet](/images/2.prerequisite/createPublicsubnet-01.png)

2. Tại trang **Create subnet**.
  + Tại mục **VPC ID** click chọn **Lab VPC**.
  + Tại mục **Subnet name** điền **Lab-Private-Subnet-01**.
  + Tại mục **Availability Zone** chọn Asia Pacific (Singapore) / ap-southeast-1a.
  + Tại mục **IPv4 CIRD block** điền **10.10.2.0/24**.

![PublicSubnet](/images/2.prerequisite/createPrivatesubnet-01.png)

3. Kéo xuống cuối trang , click **Add new subnet**.
  + Tại mục **Subnet name** điền **Lab-Private-Subnet-02**.
  + Tại mục **Availability Zone** chọn Asia Pacific (Singapore) / ap-southeast-1b.
  + Tại mục **IPv4 CIRD block** điền **10.10.4.0/24**.
  + Click **Create subnet**
  
![PublicSubnet](/images/2.prerequisite/createPrivatesubnet-02.png)

4. Kết quả
![PublicSubnet](/images/2.prerequisite/createPrivatesubnet-03.png)