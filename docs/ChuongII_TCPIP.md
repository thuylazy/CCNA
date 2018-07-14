# CHƯƠNG II: TCP/IP
## 2.1. Giao thức (protocol)
- Tập hợp các quy tắc cho phép các thiết bị có thể giao tiếp, trao đổi thông tin với nhau.
- Các giao thức mạng phổ biến: 
   <ul>
   <li> TCP/IP
   <li> IPx/SPx
   <li> Appletalk
   <li> Netbios
   <li> OSI
   </ul>
## 2.2. TCP/IP là gì?
- TCP/IP là giao thức cơ bản được sử dụng giữa các máy vi tính và các thiết bị mạng truyền thông với nhau.
## 2.3. Địa chỉ TCP/IP
- Địa chỉ IP là địa chỉ Logical được cung cấp cho toàn bộ các thiết bị trong hệ thống mạng.
- Nằm trong tầng mạng- Networks (tầng 3 trong mô hình tham chiếu OSI)
- 2 phiên bản IP là: IPv4 và IPv6
## 2.4. Địa chỉ IPv4
- Biểu diễn dưới dạng nhị phân (bit 0 và 1)
- vd : Địa chỉ IP 192.168.1.2 ở dạng nhị phân (32 bit) là: 11000000.10101000.00000001.00000010
- 32bits đc chia làm 4 octet: 11000000 - octet thứ nhất......
- Địa chỉ IP ở dạng thập phân: 85.5.191.1
## 2.5. Bảng chuyển đổi từ hệ nhị phân sang hệ thập phân
## 2.6. Bảng chuyển đổi từ hệ thập phân sang hệ nhị phân
## 2.7. Gán một địa chỉ IP tĩnh cho máy tính
## 2.8. Gán địa chỉ IPv4 động cho 1 Host
- DHCP (Dynamic Host Configuration Protocol): là dịch vụ "được dùng" cho phép gán IPv4 một cách tự động cho các host trong hệ thống, giảm thiểu khối lượng công việc của các quản trị viên hoặc nhân viên hỗ trợ mạng và theo đó loại bỏ các lỗi kết nối không đáng có.
## 2.9. Phạm vi khả dụng cuả IPv4
- Từ 0.0.0.0 -> 255.255.255.255
## 2.10. Các lớp địa chỉ IP (IP Address Classification)
- Đc chia thành 5 lớp sau:
  <ul>
  <li> Lớp A: 0 -> 127
  <li> Lớp B: 128 -> 191
  <li> Lớp C: 192 -> 223
  <li> Lớp D: 224 -> 239 : Sử dụng cho các dịch vụ, giao thức Multicasting
  <li> Lớp E: 240 -> 255: Sd cho nghiên cứu và phát triển
  </ul>
## 2.11. Phần Mạng và Host
- Địa chỉ IP đc chia thành 2 phần là Network ID và Host ID
- Lớp A: N.H.H.H
- Lớp B: N.N.H.H
- Lớp C: N.N.N.H
- H: Host ID - địa chỉ của một thiết bị cụ thể trong hệ thống mạng
- N: Network ID - là địa chỉ cung cấp cho từng mạng riêng
## 2.12. Mạng và địa chỉ Broadcast
- Network ID:
  <ul>
  <li> Định danh cho một mạng.
  <li> Các bit trong phần Host ID đều là bit 0.
  </ul>
- Địa chỉ Broadcast: 
  <ul>
  <li> Là địa chỉ đại diện cho toàn bộ thiết bị trong một mạng
  <li> Là địa chỉ IP lớn nhất trong một dải mạng
  <li> Các bit trong phần Host ID đều là bit 1
  </ul>
- IP khả dụng trong 1 mạng:
  <ul>
  <li> Là những IP có thể sử dụng gán cho các Host
  </ul>
## 2.13. Subnet - mask
- subnet - mask là để phân biệt giữa phần Network và phần Host
- 1 là đại diện cho phần Network
- 0 là đại diện cho phần host
- Class A: **N**.H.H.H **255**.0.0.0
- Class B: **N.N**.H.H **255.255**.0.0
- Class C: **N.N.N**.H **255.255.255**.0
## 2.14. Địa chỉ riêng (Reserved Address)
- Class D và class E
- Gồm Network ID và Broadcast ID
- 0.x.x.x - không hợp lệ
- 127.x.x.x - dành cho địa chỉ Loopback 
## 2.15. 127.x.x.x - Địa chỉ Loopback 
- Địa chỉ được sử dụng để kiểm tra giao thức TCP/IP trên chính thiết bị đó
- Lệnh ktra: ping 127.0.0.1
## 2.16. Địa chỉ IP Private/IP Public
  |Private IP|Public IP|
  |----------|---------|
  |1. Đc sử dụng trong mạng LAN hoặc trong một tổ chức riêng.|1. Đc sd là địa chỉ công cộng trong internet|
  |2. K đc nhận diện Internet|2. Đc nhận diện trên Internet|
  |3. Cấp phát tự do bởi người quản trị hệ thống|3. Đc cung cấp bởi nhà cung cấp dịch vụ(từ IANA), việc cấp phát tuân thủ các quy trình quy định nghiên ngặt|
  |4. Là địa chỉ duy nhất trong một mạng hoặc một tổ chức| 4. Là địa chỉ duy nhất trên toàn cầu|
  |5. Miễn phí|5. Phải trả chi phí cho nhà cũng cấp dịch vụ ( hay IANA)
  |6. Không đc đăng kí chủ sở hữu|6. Dc đăng kí chủ sở hữu|
## 2.17. Địa chỉ cá nhân (Private IP Address)
- Là địa chỉ nhất định trong mỗi lớp địa chỉ IP đc các tổ chức sử dụng để cấp phát cho các thiết bị trong mạng nội bộ.
- Lớp A: **10**.0.0.0 đến **10**.255.255.255
- Lớp B: **172.16**.0.0 đến **172.31**.255.255
- Lớp C: **192.168.0**.0 đến **192.168.255**.255
## 2.18. Phân bổ địa chỉ IP
- Đăng kí Internet theo khu vực (REgional Internet Registries - RIRs)
- Đăng kí chính thức tại IANA.org 
## 2.19. Mạng con (subnetting)

