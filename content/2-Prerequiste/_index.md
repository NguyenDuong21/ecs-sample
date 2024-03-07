---
title : "Các bước chuẩn bị"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---

Tạo VPC với 2 private subnet theo hình sau:


- Chọn VPC and more nhập tên VPC, CIDR, và chọn 2 AZ

![VPC](/images/image.png) 

- Chọn 0 public subnet và 2 private subnet, chọn NAT gateways và S3 VPC endpoints là none

![VPC](/images/image2.png) 

- Tạo và đợi việc tạo VPC hoàn thành.