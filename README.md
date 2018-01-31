# CCNA
#**BÀI 1: MÔ HÌNH OSI**

##**I.Giới thiệu về mô hình phân lớp**
- *Host:* là một thực thể mà có khả năng truyền ứng dụng.
- *Host-to-host:* Để truyền thông từ một host đến 1 host cần các mô hình:
  <ul>
  <li>Older: Truyền theo kiểu độc quyền (Bây giờ không sử dụng nữa).
  <li>Standards-based model: Cho phép một máy tính sử dụng nhiều sản phẩm của nhiều hãng phần mềm khác nhau. Mô hình chuẩn hóa này được xây dựng theo phương pháp phân lớp (Layered appoach).
  </ul>
- Mô hình phân lớp:
  <ul>
  <li>Giảm thiểu độ phức tạp.
  <li>Chuẩn hóa các giao diện.
  <li>Thúc đẩy kĩ thuật modun hóa (Có sự chuyên môn hóa trong kĩ thuật sản xuất).
  <li>Đảm bảo tương thích về công nghệ.
  </ul>
##**II.Mô hình OSI (Open System Interconnection)- Liên kết nối caccs hệ thống mở**
- Là mô hình phân lớp nổi tiếng
- Gồm 7 lớp:
  <ul>
  <li>Lớp 7: *Appliation:* Hỗ trợ các ứng dụng trên mạng
  <li>Lớp 6: *Presentation:* Đảm bảo 2 tầng application ở 2 đầu có thể giao tiếp với nhau
  <li>Lớp 5: *Session:* Truyền thông liên host interhost bằng cách thiết lập quản lí và giải phóng các session giữa ứng dụng
  <li>Lớp 4: *Transport:* Quản lí kết nối đầu cuối(End to End Connections)
     <ul>
     <li>Xử lý các vấn đề truyền dẫn giữa các host
     <li>Đảm bảo dữ liệu truyền tải một cách đáng tin cậy từ điểm này đến điểm ia trong mạng
     <li>Đảm bảo duy trì, thiết lập, kết thúc các đường mạng ảo
     <li>Cung cấp cơ chế sửa lỗi, dò lỗi bằng điều khiển luồng
     </ul>
  <li>Lớp 3: *Network:* Phân bố dữ liệu từ điểm này đến điểm kia một cách tối ưu nhất bằng cách định tuyến các gói dữ liệu để tìm ra đường đi tối ưu nhất để phân phối dữ liệu
     <ul>
     <li>Định tuyến
     <li>Địa chỉ logic cho hệ thống mạng: Là địa chỉ chuyên dùng cho định tuyến (Vd địa chỉ IP)
     </ul>
  <li>Lớp 2: *Data Link (Liên kết dữ liệu):* Cung cấp, điều khiển việc truy nhập vào đường truyền vật lí và thực hiện chức năng giao tiếp vs lớp mạng ở bên trên. Có chơ chế dò lỗi.
  <li>Lớp 1: *Physical (Lớp vật lý):* Xây dựng đường truyền vật lý cho các host:
      <ul>
      <li>Truyền 1 dòng bit qua 1 đường truyền vật lý cụ thể nào đó.
      <li>Quy định các đặc điểm của một đường truyền vật lý về cơ, điện, quang, các thủ tục chức năng để làm sao đó có thể truyền được 1 dòng bit nhị phân qua đường truyền vật lý.
      </ul>
##**III.Cách hoạt động mô hình OSI**
- Đi từ trên xuống dưới ( Từ lớp 7 xuống lớp 1).
- Header (HDR): Là thông tin quản lí của một gói tin.
- Toàn bộ gói tin lớp trên sẽ là phần dữ liệu của gói tin lớp dưới. Riêng ở lớp 2 có thêm phần kiểm tra lỗi FCS. Lớp vật lý: chuyển hóa thành một dòng bit nhị phân.
- Tiến trình ở phía đầu thu: Ngược lại, mỗi lần đi lên lại lược bỏ đi một HDR. Cuối cùng đến tay người dùng nó trả lại nguyên vẹn dữ liệu người dùng.
- Peer-to-Peer (Tiến trình truyền thông ngang hàng)
  <ul>
  <li>Transport: Segments
  <li>Network: Packets
  <li>Data Link: Frames
  <li>Physical: bit
  </ul>

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
