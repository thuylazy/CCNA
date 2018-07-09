# CHƯƠNG II: TCP/IP
## 2.1. Giao thức (protocol)
- Tập hợp các quy tắc cho phép các thiết bị có thể gaio tiếp, trao đổi thông tin với nhau.
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

