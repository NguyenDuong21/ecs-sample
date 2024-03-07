---
title : "Tạo VPC endpoint"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---

Trong phần này, chúng ta sẽ cùng tạo VPC endpoint. Để  kết nối ECS cluster với ECR, CloudWatch chúng ta cần tạo các endpoin sau:
- com.amazonaws.region.ecr.dkr: Endpoint này được sử dụng cho Docker Registry APIs. Docker client như push và pull dùng endpoint này.
- com.amazonaws.region.ecr.api: Endpoint này dùng để  gọi đến Amazon ECR API.
- com.amazonaws.region.s3: ECR dùng s3 để lưu các layer vì vậy ta phải tạo s3 gateway endpoint thì ecs mới có thể pull các layer từ image của ECR.
- com.amazonaws.region.logs: Dùng cho cloud watch logs

Tạo Endpoint com.amazonaws.region.ecr.dkr chọn cả 2 private subnet của vpc:
![ECR](/images/image6.png) 

Tạo Endpoint om.amazonaws.region.ecr.api chọn cả 2 private subnet của vpc:
![ECR](/images/image7.png) 

Tạo Gateway Endpoint om.amazonaws.region.s3 chọn route tables của 2 private subnet:
![ECR](/images/image8.png) 

Tạo Endpoint om.amazonaws.region.logs chọn cả 2 private subnet của vpc:
![ECR](/images/image9.png) 
