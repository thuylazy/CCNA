#**Bài 3: Ethernet LAN**

**LAN** (Local Area Network - Mạng nội bộ): Là một mạng có quy mô vừa hoặc nhỏ dùng trong một bệnh viện, một trường học,... có tốc độ cao và có nhiều kích thước khác nhau (có thể rất nhỏ hoặc rất lớn).
- Các thành phần cơ bản của mạng LAN:
  <ul>
  <li>Máy tính (Computer): có thể là PCs hay servers
  <li>Kết nối mạng (Interconnections)
      <ul>
      <li>NICs: card mạng
      <li>Media: phương tiện truyền dẫn (là đoạn dây cáp để đấu nối trong mạng)
      </ul>
  <li>Thiết bị mạng (Network devices): Hubs, Switches, Routers
  <li>Các giao thức (Protocols): Ethernet, IP, ARP, DHCP
  </ul>
- Chức năng: 
  <ul>
  <li>Chia sẻ dữ liệu, các ứng dụng, các tài nguyên
  <li>Cung cấp một đường kết nối đến một mạng khác
  </ul> 
- Kích thước mạng LAN:
  <ul>
  <li>Rất nhỏ: VD: SOHO LAN (Small Office Home Office)
  <li>Rất lớn: Enterprise (Mạng doanh nghiệp)
  </ul>
- Công nghệ mạng LAN phổ biến: Ethernet
- Chuẩn mạng LAN: Chủ yếu tập trung ở mô hình OSI 2 lớp: lớp Physical và lớp Data Link
- Giao thức CSMA/CD (Đa truy nhập cảm biến sóng mang dò được xung đột): giảm thiểu tối đa sự xung đột có thể xảy ra trên một hệ thống mạng
- Cấu trúc của các Ethernet Frame:
- Một số hình thức truyền thông trong mạng LAN:
  <ul>
  <li>Unicast: 1 host gửi dữ liệu cho 1 host
  <li>Broadcast: 1 host gửi dữ liệu cho tất cả các host còn lại trong hệ thống
  <li>Multicast: 1 host gửi cho một nhóm host trong hệ thống
  </ul>
- Địa chỉ MAC được sử dụng trong môi trường LAN:
  <ul>
  <li>MAC: địa chỉ vật lý của lớp 2
  <li>MAC: là 1 dãy nhị phân dài 48bit
  <li>Gồm 2 phần: 
      <ul>
      <li>OUI: định danh cho nhà sản xuất
      <li>Vendor Assigned: định danh cho từng thiết bị do nhà sản xuất đó sx ra
      </ul>
  </ul>

