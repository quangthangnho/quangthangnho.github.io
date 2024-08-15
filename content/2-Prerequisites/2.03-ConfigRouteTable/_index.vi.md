---
title : "Cấu hình Route table"
date :  "`r Sys.Date()`" 
weight : 3
chapter : true
pre : " <b> 2.3 </b> "
---

#### Tạo Route table

1. Tạo public route table
  + Click **Route tables**.
  + Click **Create route table**.

![routetable](/images/2.prerequisite/createRouteTable-01.png)

2. Tại trang **Create route table**.
  + Tại mục **Name** điền **LAB-Public-RouteTable**.
  + Tại mục **VPC** click chọn **Lab-VPC**.
  + Click **Create route table**

![routetable](/images/2.prerequisite/createRouteTable-02.png)

3. Tạo private route table
  + Click **Route tables**.
  + Click **Create route table**.

![routetable](/images/2.prerequisite/createRouteTable-01.png)

4. Tại trang **Create route table**.
  + Tại mục **Name** điền **LAB-Private-RouteTable**.
  + Tại mục **VPC** click chọn **Lab-VPC**.
  + Click **Create route table**

![routetable](/images/2.prerequisite/createRouteTable-03.png)

5. Kết quả

![routetable](/images/2.prerequisite/createRouteTable-04.png)

6. Cập nhập subnet associations
  + Chọn **LAB-Public-RouteTable**.
  + Click **Actions**
  + Click **Edit subnet associations**
  + Chọn **Lab-Public-Subnet-01** và **Lab-Public-Subnet-02**
  + Click **Save associations**

![routetable](/images/2.prerequisite/createRouteTable-05.png)

![routetable](/images/2.prerequisite/createRouteTable-06.png)

6. Làm tương tự với **LAB-Private-RouteTable**

![routetable](/images/2.prerequisite/createRouteTable-07.png)