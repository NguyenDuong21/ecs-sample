---
title : "Tạo ECR private"
date :  "`r Sys.Date()`" 
weight : 3 
chapter : false
pre : " <b> 3. </b> "
---

**Chú ý:** VPC Endpoin không hỗ trợ ECR public

Trong bước này, chúng ta sẽ thực hiện tạo ECR private và push docker image lên ECR này

- Tại ECR console, nhấn Create repository. Tại option Visibility settings chọn Private và Repository name

![ECR](/images/image3.png) 

- Tải source code mẫu và build image

- Chọn vào repo và nhấn vào nút View push commands

![ECR2](/images/image4.png)


- Tag image vừa build và push lên ECR theo hướng dẫn

![ECR3](/images/image5.png)
