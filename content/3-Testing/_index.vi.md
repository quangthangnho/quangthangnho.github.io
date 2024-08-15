---
title : "Kiểm tra"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

1. Kiểm tra Healthy
  + Di chuyển qua màn hình **Target group**
  + Click **LAB-TARGET-GROUP** và kiểm tra phần healthy

![test](/images/2.prerequisite/createTest-01.png)

{{% notice info %}}
Như kết quả từ ảnh trên có nghĩa là ALB của chúng ta đã có thể kết nối vào 2 instance
{{% /notice %}}

2. Kiểm tra bằng trình duyệt
  + Di chuyển qua màn hình **Load balancers**
  + Click **LAB-ALB** và kiểm tra DNS name ( Chúng ta sẽ sử dụng DNS này để truy cập. )

![test](/images/2.prerequisite/createTest-02.png)

  + Khi truy cập vào DNS trên bằng trình duyệt chúng ta sẽ nhận kết quả như hình dưới
  + Bạn có thể kiểm tra sự thay đổi bằng cách refresh trình duyệt.

![test](/images/2.prerequisite/createTest-03.png)

![test](/images/2.prerequisite/createTest-04.png)

  + Và đó là cách mà ALB giúp chúng ta cân bằng tải những request kết nối vào instance
