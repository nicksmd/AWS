##### Overview
- VPC-peering cho phép kết nối 2 VPC thuộc cùng 1 region bằng Private IP.
Sau khi được kết nối, chúng có thể giao tiếp với nhau y hệt như trong
cùng 1 network.
- VPC-peering có thể kết nối VPC trong cùng 1 account hoặc VPC của các account
khác nhau nhưng nằm trong cùng 1 region
- VPC-peering ko thể kết nối 2 VPC có giải CIDR giao nhau

![](https://i2.wp.com/jayendrapatil.com/wp-content/uploads/2016/03/Screen-Shot-2016-06-15-at-12.33.00-PM.png?resize=768%2C166)

- VPC-peering không hỗ trợ kết nối kiểu bắc cầu

![](https://i2.wp.com/jayendrapatil.com/wp-content/uploads/2016/03/Screen-Shot-2016-06-15-at-12.33.07-PM.png?resize=768%2C252_)


![](https://i0.wp.com/jayendrapatil.com/wp-content/uploads/2016/03/Screen-Shot-2016-06-15-at-12.35.38-PM.png?resize=768%2C224)

- Chỉ có một VPC-peering được tạo ra giữa 2 VPC tại 1 thời điểm
-

##### Kiến trúc VPC-peering

![](https://i2.wp.com/jayendrapatil.com/wp-content/uploads/2016/03/Screen-Shot-2016-11-12-at-3.20.55-PM.png?resize=768%2C512)

- tác dụng làm giảm số lượng VPN

