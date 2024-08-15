---
title : "Phần ôn tập kiến thức"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

>Xin chúc mừng bạn đã xuất sắc hoàn thành workshop này! Đây là một cột mốc quan trọng trong hành trình học tập của bạn. Để củng cố và kiểm tra lại những kiến thức mà bạn đã tiếp thu, chúng ta sẽ cùng tham gia vào một trò chơi nhỏ. Trò chơi bao gồm 20 #### Câu hỏi, và việc trả lời đúng sẽ giúp bạn xác nhận sự hiểu biết sâu sắc của mình. Chúc bạn thật nhiều may mắn và thành công!


![ConnectPrivate](/images/ALB1.drawio.png)

{{% notice info %}}
Click vào chữ **Hiển thị đáp án** để hiển thị kết quả 
{{% /notice %}}

#### Câu hỏi 1: Mục đích của một Internet Gateway (IGW) trong sơ đồ là gì?
-  A) Kết nối VPC với các mạng nội bộ khác.
-  B) Kết nối VPC với internet.
-  C) Định tuyến lưu lượng giữa các subnets.
-  D) Quản lý lưu lượng truy cập đến NAT Gateway.
{{< showanswer >}}
-  B) Kết nối VPC với internet. <br/>
Giải thích: IGW cho phép các instance trong VPC có thể truy cập internet và ngược lại.
{{< /showanswer >}}

#### Câu hỏi 2: Route table cho public subnet trong sơ đồ có mục đích gì?
-  A) Định tuyến lưu lượng tới các mạng nội bộ khác.
-  B) Định tuyến lưu lượng tới internet thông qua IGW.
-  C) Định tuyến lưu lượng tới các subnet khác thông qua NAT Gateway.
-  D) Định tuyến lưu lượng tới các EC2 instances khác.
{{< showanswer >}}
-  B) Định tuyến lưu lượng tới internet thông qua IGW. <br/>
Giải thích: Public route table định tuyến lưu lượng từ public subnet tới internet thông qua IGW.
{{< /showanswer >}}

#### Câu hỏi 3: Mục đích của NAT Gateway trong sơ đồ là gì?
-  A) Kết nối EC2 instances trong private subnet với internet mà không công khai IP.
-  B) Kết nối tất cả các subnet với internet.
-  C) Định tuyến lưu lượng tới các subnet khác.
-  D) Kết nối các subnets với nhau.
{{< showanswer >}}
-  A) Kết nối EC2 instances trong private subnet với internet mà không công khai IP. <br/>
Giải thích: NAT Gateway cho phép các instance trong private subnet kết nối ra ngoài internet mà không cần gán IP công khai.
{{< /showanswer >}}

#### Câu hỏi 4: Trong sơ đồ, các EC2 instances ở private subnet có thể truy cập internet bằng cách nào?
-  A) Thông qua Internet Gateway trực tiếp.
-  B) Thông qua NAT Gateway.
-  C) Thông qua Direct Connect.
-  D) Không thể truy cập internet từ private subnet.
{{< showanswer >}}
-  B) Thông qua NAT Gateway. <br/>
Giải thích: Các EC2 instances trong private subnet sử dụng NAT Gateway để truy cập internet.
{{< /showanswer >}}

#### Câu hỏi 5: Private target group trong sơ đồ dùng để làm gì?
-  A) Định tuyến lưu lượng tới các EC2 instances công khai.
-  B) Định tuyến lưu lượng tới các EC2 instances trong private subnet.
-  C) Định tuyến lưu lượng tới các dịch vụ bên ngoài VPC.
-  D) Định tuyến lưu lượng giữa các subnets.
{{< showanswer >}}
-  B) Định tuyến lưu lượng tới các EC2 instances trong private subnet. <br/>
Giải thích: Private target group là một tập hợp các EC2 instances trong private subnet, dùng cho mục đích cân bằng tải.
{{< /showanswer >}}

#### Câu hỏi 6: Public subnet trong sơ đồ chứa gì?
-  A) Các EC2 instances private.
-  B) Các NAT Gateway và Load Balancer.
-  C) Các EC2 instances public và private.
-  D) Chỉ có Load Balancer.
{{< showanswer >}}
-  B) Các NAT Gateway và Load Balancer. <br/>
Giải thích: Public subnet chứa các thành phần cần kết nối trực tiếp với internet, như NAT Gateway và Load Balancer.
{{< /showanswer >}}

#### Câu hỏi 7: Route table cho private subnet trong sơ đồ sẽ định tuyến lưu lượng tới đâu?
-  A) Trực tiếp tới Internet Gateway.
-  B) Trực tiếp tới NAT Gateway.
-  C) Trực tiếp tới public subnet.
-  D) Trực tiếp tới các EC2 instances khác.
{{< showanswer >}}
-  B) Trực tiếp tới NAT Gateway. <br/>
Giải thích: Route table của private subnet định tuyến lưu lượng từ private subnet tới internet thông qua NAT Gateway.
{{< /showanswer >}}

#### Câu hỏi 8: Tại sao lại có nhiều Availability Zone trong sơ đồ?
-  A) Để tối ưu hóa chi phí triển khai.
-  B) Để tăng cường tính khả dụng và dự phòng.
-  C) Để tăng tốc độ truy cập mạng nội bộ.
-  D) Để giảm bớt việc quản lý subnet.
{{< showanswer >}}
-  B) Để tăng cường tính khả dụng và dự phòng. <br/>
Giải thích: Sử dụng nhiều Availability Zone giúp tăng tính khả dụng của hệ thống trong trường hợp một Zone gặp sự cố.
{{< /showanswer >}}

#### Câu hỏi 9: Mục đích chính của Load Balancer trong sơ đồ là gì?
-  A) Định tuyến lưu lượng giữa các VPC khác nhau.
-  B) Phân phối lưu lượng đến các EC2 instances trong public subnet.
-  C) Phân phối lưu lượng đến các EC2 instances trong private subnet.
-  D) Quản lý lưu lượng truy cập đến các dịch vụ AWS khác.
{{< showanswer >}}
-  C) Phân phối lưu lượng đến các EC2 instances trong private subnet. <br/>
Giải thích: Load Balancer giúp phân phối lưu lượng đến các EC2 instances trong private subnet để đảm bảo cân bằng tải.
{{< /showanswer >}}

#### Câu hỏi 10: Mạng con nào trong sơ đồ có thể trực tiếp truy cập internet mà không cần thông qua NAT Gateway?
-  A) Private subnet 10.10.2.0/24.
-  B) Private subnet 10.10.4.0/24.
-  C) Public subnet 10.10.1.0/24.
-  D) Không mạng con nào có thể truy cập internet trực tiếp.
{{< showanswer >}}
-  C) Public subnet 10.10.1.0/24. <br/>
Giải thích: Chỉ các mạng con công khai (public subnets) có thể truy cập internet trực tiếp thông qua IGW.
{{< /showanswer >}}

#### Câu hỏi 11: Cấu trúc VPC trong sơ đồ thuộc loại nào?
-  A) VPC đơn giản với một Availability Zone.
-  B) VPC với nhiều Availability Zone.
-  C) VPC không có subnet công khai.
-  D) VPC không có NAT Gateway.
{{< showanswer >}}
-  B) VPC với nhiều Availability Zone. <br/>
Giải thích: VPC này được thiết kế với nhiều Availability Zone để tăng tính khả dụng và dự phòng.
{{< /showanswer >}}

#### Câu hỏi 12: Các subnet trong sơ đồ này có phải thuộc cùng một Availability Zone không?
-  A) Đúng, tất cả đều thuộc cùng một Availability Zone.
-  B) Sai, các subnet thuộc các Availability Zone khác nhau.
-  C) Một số thuộc cùng một Availability Zone, số còn lại thuộc Zone khác.
-  D) Không có thông tin về Availability Zone.
{{< showanswer >}}
-  B) Sai, các subnet thuộc các Availability Zone khác nhau. <br/>
Giải thích: Các subnet trong sơ đồ được phân bố trên nhiều Availability Zone để tăng tính khả dụng.
{{< /showanswer >}}

#### Câu hỏi 13: Mạng con nào trong sơ đồ này sẽ chứa các EC2 instances không có IP công khai?
-  A) Public subnet 10.10.1.0/24.
-  B) Public subnet 10.10.3.0/24.
-  C) Private subnet 10.10.2.0/24.
-  D) Không có mạng con nào chứa các EC2 instances như vậy.
{{< showanswer >}}
-  C) Private subnet 10.10.2.0/24. <br/>
Giải thích: Các EC2 instances không có IP công khai thường được triển khai trong private subnet.
{{< /showanswer >}}

#### Câu hỏi 14: Route table của public subnet có định tuyến trực tiếp tới NAT Gateway không?
-  A) Có.
-  B) Không.
-  C) Tùy thuộc vào cấu hình cụ thể.
-  D) Chỉ trong một số trường hợp.
{{< showanswer >}}
-  B) Không. <br/>
Giải thích: Public route table thường không cần định tuyến tới NAT Gateway, vì public subnet có thể trực tiếp truy cập internet qua IGW.
{{< /showanswer >}}

#### Câu hỏi 15: Các EC2 instances trong private subnet có thể bị truy cập trực tiếp từ internet không?
-  A) Có.
-  B) Không.
-  C) Chỉ trong một số trường hợp.
-  D) Tùy thuộc vào cấu hình bảo mật.
{{< showanswer >}}
-  B) Không. <br/>
Giải thích: Các EC2 instances trong private subnet không thể bị truy cập trực tiếp từ internet vì chúng không có IP công khai.
{{< /showanswer >}}

#### Câu hỏi 16: Lý do chính để sử dụng NAT Gateway thay vì chỉ sử dụng Internet Gateway là gì?
-  A) Để giảm chi phí kết nối.
-  B) Để tăng cường bảo mật cho các instances trong private subnet.
-  C) Để định tuyến lưu lượng nhanh hơn.
-  D) Để cung cấp địa chỉ IP công khai cho tất cả các instances.
{{< showanswer >}}
-  B) Để tăng cường bảo mật cho các instances trong private subnet. <br/>
Giải thích: NAT Gateway cho phép các instances trong private subnet truy cập internet mà vẫn giữ bảo mật cao.
{{< /showanswer >}}

#### Câu hỏi 17: Khi một EC2 instance trong private subnet gửi yêu cầu ra ngoài internet, địa chỉ IP nào sẽ được hiển thị với dịch vụ bên ngoài?
-  A) Địa chỉ IP công khai của EC2 instance.
-  B) Địa chỉ IP riêng của EC2 instance.
-  C) Địa chỉ IP của NAT Gateway.
-  D) Địa chỉ IP của Internet Gateway.
{{< showanswer >}}
-  C) Địa chỉ IP của NAT Gateway. <br/>
Giải thích: Khi truy cập internet thông qua NAT Gateway, IP công khai của NAT Gateway sẽ được hiển thị.
{{< /showanswer >}}

#### Câu hỏi 18: Load Balancer trong sơ đồ này thường được triển khai ở đâu?
-  A) Public subnet.
-  B) Private subnet.
-  C) Ngoài VPC.
-  D) Trong một mạng riêng biệt.
{{< showanswer >}}
-  A) Public subnet. <br/>
Giải thích: Load Balancer thường được triển khai trong public subnet để nhận lưu lượng từ internet trước khi phân phối đến các EC2 instances.
{{< /showanswer >}}

#### Câu hỏi 19: Route table nào sẽ được gán cho các EC2 instances trong private subnet?
-  A) Public route table.
-  B) Private route table.
-  C) Default route table.
-  D) Internet route table.
{{< showanswer >}}
-  B) Private route table. <br/>
Giải thích: Các EC2 instances trong private subnet sẽ sử dụng private route table để định tuyến lưu lượng qua NAT Gateway.
{{< /showanswer >}}

#### Câu hỏi 20: Mục đích chính của một VPC (Virtual Private Cloud) là gì?
-  A) Tạo ra một môi trường mạng công cộng cho các dịch vụ AWS.
-  B) Cung cấp một môi trường mạng riêng biệt trong AWS để triển khai các tài nguyên AWS.
-  C) Kết nối các mạng nội bộ của doanh nghiệp với AWS.
-  D) Định tuyến lưu lượng giữa các vùng địa lý khác nhau.
{{< showanswer >}}
-  B) Cung cấp một môi trường mạng riêng biệt trong AWS để triển khai các tài nguyên AWS. <br/>
Giải thích: VPC cho phép tạo ra một môi trường mạng riêng biệt, nơi bạn có thể triển khai và quản lý các tài nguyên AWS một cách an toàn.
{{< /showanswer >}}