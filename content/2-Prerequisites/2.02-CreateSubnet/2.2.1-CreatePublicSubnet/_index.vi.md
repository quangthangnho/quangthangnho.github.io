---
title : "Tạo Public subnet"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2.2 </b> "
---

#### Tạo Public subnet

Theo mô hình thì chúng ta sẽ tạo 2 public subnet trên 2 AZ khác nhau.

1. Click **Subnets**.
  + Click **Create subnet**.

![PublicSubnet](/images/2.prerequisite/createPublicsubnet-01.png)

2. Tại trang **Create subnet**.
  + Tại mục **VPC ID** click chọn **Lab VPC**.
  + Tại mục **Subnet name** điền **Lab-Public-Subnet-01**.
  + Tại mục **Availability Zone** chọn Asia Pacific (Singapore) / ap-southeast-1a.
  + Tại mục **IPv4 CIRD block** điền **10.10.1.0/24**.

![PublicSubnet](/images/2.prerequisite/createPublicsubnet-02.png)

3. Kéo xuống cuối trang , click **Add new subnet**.
  + Tại mục **Subnet name** điền **Lab-Public-Subnet-02**.
  + Tại mục **Availability Zone** chọn Asia Pacific (Singapore) / ap-southeast-1b.
  + Tại mục **IPv4 CIRD block** điền **10.10.3.0/24**.
  + Click **Create subnet**
  
![PublicSubnet](/images/2.prerequisite/createPublicsubnet-03.png)

4. Cấu hình Enable auto-assign public IPv4 address cho 2 public subnet
  + Click **Lab-Public-Subnet-01**
  + Click **Actions**.
  + Click **Edit subnet settings**.

![PublicSubnet](/images/2.prerequisite/createPublicsubnet-04.png)

5. Click chọn **Enable auto-assign public IPv4 address**.
  + Click **Save**.

![PublicSubnet](/images/2.prerequisite/createPublicsubnet-05.png)

6. Làm tương tự cho subnet **Lab-Public-Subnet-02**