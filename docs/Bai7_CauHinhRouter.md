#Bai7_Router
## **I.Các thành phần cơ bản**
- Tp bên trong (Internal components): Bao gồm CPU, ROM, FLASH, NVRAM, RAM.
- Tp bên ngoài (External components): Các cổng, các giao diện của Router
  <ul>
  <li>WAN
  <li>LAN
  <li>Console/AUX: dùng để cấu hình
  </ul>
### **1.Tp bên trong**
#### *a. CPU: Đơn vị xử lí trung tâm*
- Thực hiện các chỉ thị của HĐH
  <ul>
  <li>Khởi tạo hệ thống
  <li>Định tuyến
  <li>Điều khiển các card mạng
  </ul>
- Những con Router lớn có thể có nhiều CPU
##### *b. Bộ nhớ ROM*
- Gồm 3 tp chính:
  <ul>
  <li>Chương trình kiểm tra lỗi (power-on diagnostics)
  <li>Chương trình bootstrap
  <li>Phần mềm HĐH phụ
  </ul>
- Chức năng: Kiểm tra phần cứng trong khi Router khởi động lên và load IOS (HĐH chính của Router) từ flash vào RAM
- Bộ nhớ ROM không thể xóa được, chúng chỉ có thể nâng cấp bằng thay thế ROM chips hoặc sockets
#### *c. Bộ nhớ RAM *
- Chia ra bởi IOS (HĐH chính của Router)
- Chia thành 2 phần: Bộ nhớ chính (Main memory) và bộ nhớ chia sẻ (Shared memory)
- Bộ nhớ chính sử dụng các chức năng của Router như lưu file runing-config,...
- Bộ nhớ chia sẻ là buffer cho các tiến trình đang xử lí
- Bộ nhớ RAM có thể nâng cấp
#### *d. NVRAM*
- Dùng để chứa file đặc biệt: file starup configuration (file cấu hình)
- Trên PC k có
- K bị mất nội dung khi tắt Router đi
#### *e. Bộ nhớ Flash (Đặc biệt)*
- Tương đương với chức năng ổ cứng trên PC
- Chứa mọi tài nguyên của con Router: chưa HĐH chính của con Router (Full current version of IOS)
- Nén lại trong bộ nhớ Flash -> bung ra ở RAM
- Có thể xóa, sửa, ghi đè, không bị mất dữ liệu khi tắt
#### *f. Buses*
- Đấu giữa CPU với Interface: System Bus
- Đấu giữa CPU và Memory: CPU Bus

### **2.Các tp bên ngoài: Các cổng mạng của Router (Interface)**
- Các interface của router dùng để kết nối với môi trường bên ngoài
- 3 loại interface:
  <ul>
  <li>Local Area Networks: LANs
  <li>Wide Area Networks: WANs
  <li>Management Ports: Console/AUX
  </ul>

## *II.Tiến trình cấu hình  trên Router**

