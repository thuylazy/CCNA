#**BÀI 2.MÔ HÌNH TCP/IP**

##**I.Cấu trúc**
- Gồm 4 lớp:
  <ul>
  <li>Sử dụng các tên khác nhau từ lớp 1 đến lớp 3
  <li>Gom lớp 5,6,7 thành một lớp
  </ul>

|Application|
|-----------|
|Transport|
|Internet|
|Network Access|

- Các giao thức: 
  <ul>
  <li>Transport: có 2 giao thức là UDP và TCP
  <li>Internet: IP
  <li>Network Access: Ethernet
  </ul>

##**II.Tìm hiểu tầng transport**
- Tương đương tầng transport của mô hình OSI
- Có 2 giao thức nổi tiếng: UDP và TCP
- Dùng để:
  <ul>
  <li>Ghép các phiên truy nhập các ứng dụng (Session multiplexing)
  <li>Segmentation: phân mảnh dữ liệu
  <li>Flow control: Cơ chế điều khiển luồng
     <ul>
     <li>(UDP: không có; TCP: có)
     <li>Khi có yêu cầu mới được thực thi
     </ul>
  <li>Kiểu truyền connection-oriented (khi có yêu cầu): thiết lập xong kết nối thì mới thực hiện truyền dữ liệu vào kết nối ấy. Giao thức TCP sử dụng kiểu truyền này
     <ul>
     <li>Connectionless: truyền dữ liệu ngay vào đường truyền mà không cần thiết lập kết nối từ trước. Giao thức UDP sử dụng.
     </ul>
  <li>Kiểu truyền tin cậy (Reliability): khi có yêu cầu mới thi hành. Đảm bảo dữ liệu được truyền nhận một cách tin cậy từ điểm này đến điểm kia của hệ thống mạng.
  </ul>
- So sánh kiểu truyền tin cậy (Reliable) với kiểu truyền tổng lực (Best-Effort Comparison)

|    |Reliable|Best-Effort|
|----|--------|-----------|
|Kiểu kết nối|Connection-oriented|Connectionless|
|Loại giao thức|TCP|UDP|
|Cách đánh STT|Có|Không|
|Sử dụng|Sử dụng trong ứng dụng thiên hướng về truyền file như Gmail, File sharing, Downloading|Thiên hướng về thời gian thực: voice streaming, video streaming|

- Giao thức UDP (User Datagram Protocol):
  <ul>
  <li>Hoạt động ở tầng transport của mô hình OSI và TCP/IP
  <li>Là giao thức connectionless
  <li>Cho phép ứng dụng truy cập vào lớp mạng
  <li>Cung cấp cơ chế kiểm tra lỗi giới hạn do đó không đảm bảo độ tin cậy
  <li>Cung cấp cơ chế phân phối theo kiểu best-effort
  <li>Không có cơ chế phục hồi dữ liệu
  </ul>

- Giao thức TCP
  <ul>
  <li>Là giao thức connection-oriented
  <li>Kiểu truyền Full-duplex: có thể truyền và nhận tại 1 thời điểm
  <li>Có cơ chế báo nhận
  <li>Có cơ chế phục hồi dữ liệu
  </ul>
