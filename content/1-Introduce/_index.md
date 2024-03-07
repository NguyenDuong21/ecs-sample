---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**VPC Endpoint (Virtual Private Cloud Endpoint)** là một dịch vụ trong Amazon Web Services (AWS) được thiết kế để kết nối giữa các tài nguyên trong một Virtual Private Cloud (VPC) của bạn và các dịch vụ AWS công cộng như Amazon S3, DynamoDB, SNS, SQS, ECR, CloudWatch và nhiều dịch vụ khác mà không cần thông qua Internet.

Truy cập trực tiếp từ VPC đến các dịch vụ công cộng của AWS thông qua VPC Endpoint có nhiều lợi ích như:

- Bảo mật: Dữ liệu không cần phải truy cập Internet, giảm nguy cơ bị tấn công từ bên ngoài.
- Hiệu suất: Truy cập trực tiếp đến các dịch vụ, giảm độ trễ so với việc truy cập thông qua Internet.
- Giảm chi phí: Không cần sử dụng gateway hoặc kết nối Direct Connect để truy cập dịch vụ AWS.
Có hai loại VPC Endpoint:

- Gateway Endpoint: Dùng cho các dịch vụ S3 và DynamoDB. Nó cho phép truy cập từ VPC đến các dịch vụ này thông qua một gateway được quản lý bởi AWS.
- Interface Endpoint: Dùng cho hầu hết các dịch vụ AWS khác (ví dụ như SNS, SQS, Kinesis). Nó tạo ra một interface network trong VPC của bạn, giúp tạo kết nối trực tiếp với dịch vụ AWS.
VPC Endpoint là một công cụ hữu ích trong việc tạo ra các mô hình kiến trúc cloud có hiệu suất cao và bảo mật.

Trong bài lab này, chúng ta cùng sử dụng **VPC Endpoint** để kết khởi chạy ECS cluster kết nối với các dịch vụ ECR, CLoudWatch để tăng cường bảo mật và giảm chi phí.