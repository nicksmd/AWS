![](https://i0.wp.com/jayendrapatil.com/wp-content/uploads/2016/03/security-diagram.png?w=458)

##### 1. Security group
- hoạt động như firewall bảo vệ instance, kiểm soát traffic ra vào ở cấp độ instance
- mỗi ec2 có thể đc gán cho 5 security group khác nhau, mỗi SG với 50 rules.
- SG mặc định cho phép tất cả các traffic đi ra, và chỉ cho các traffic vào từ
các ec2 thuộc cùng SG
- SG custom chỉ cho phép tất cả traffic đi ra.
- SG chỉ có **Allow rules**, ko có Deny rules.

 ![](http://i.imgur.com/DksvkSg.png)

- SG có thể cho phép ec2 kêt nối đến 1 giải IP, 1 SG khác trong VPC hoặc peer VPC.
- SG có tính Stateful: response của 1 traffic đi ra sẽ được accept bất kể inbound rule có
cho phép hay ko, và ngược lại.
- Connection track: SG sử dụng connection track để track thông tin về traffic tới và rời ec2.
Không fai mọi loại traffic đều bị track: nếu traffic được chấp nhận ra vào tự do (all port, all source)
thì nó sẽ không bị track.
- Không thể dùng SG để block IP, vì mặc định mọi traffic đi vào EC2
đều bị block (và ko fai bằng SG). SG chỉ Allow traffic, ko có Deny traffic.
- Một SG rỗng (ko chứa rule nào cả) có thể dùng để cho phép các EC2 được assign với nó kết nối với nhau.

##### 2. NACLs
- hoạt động như firewall bảo vệ subnets, kiểm soát traffic ra vào ở cấp độ subnet
- ACL mặc định allow mọi inbound và outbound traffic
- ACL tạo mới deny mọi inbound và outbound traffic
- 1 subnet chỉ có thể gắn với 1 NACL, nếu ko đc gắn 1 cách có chủ ý thì nó
sẽ được ngầm định gắn với NACL mặc định.
- Mỗi rule có 1 index, các rule sẽ được áp dụng từ index thấp đến cao. Gặp 1 rule
thỏa mãn thì áp dụng luôn và dừng duyệt tiếp các rule còn lại.
- NACL thì **Stateless**
