# CCNA
#MÔ HÌNH OSI

##Giới thiệu về mô hình phân lớp
- Host: là một thực thể mà có khả năng truyền ứng dụng.
- Host-to-host: Để truyền thông từ một host đến 1 host cần các mô hình:
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
##Mô hình OSI (Open System Interconnection)- Liên kết nối caccs hệ thống mở
- Là mô hình phân lớp nổi tiếng
- Gồm 7 lớp:
  <ul>
  <li>Lớp 7: Appliation: Hỗ trợ các ứng dụng trên mạng
  <li>Lớp 6: Presentation: Đảm bảo 2 tầng application ở 2 đầu có thể giao tiếp với nhau
  <li>Lớp 5: Session: Truyền thông liên host interhost bằng cách thiết lập quản lí và giải phóng các session giữa ứng dụng
  <li>Lớp 4: Transport: Quản lí kết nối đầu cuối(End to End Connections)
     <ul>
     <li>Xử lý các vấn đề truyền dẫn giữa các host
     <li>Đảm bảo dữ liệu truyền tải một cách đáng tin cậy từ điểm này đến điểm ia trong mạng
     <li>Đảm bảo duy trì, thiết lập, kết thúc các đường mạng ảo
     <li>Cung cấp cơ chế sửa lỗi, dò lỗi bằng điều khiển luồng
     </ul>
  <li>Lớp 3: Network: Phân bố dữ liệu từ điểm này đến điểm kia một cách tối ưu nhất bằng cách định tuyến các gói dữ liệu để tìm ra đường đi tối ưu nhất để phân phối dữ liệu
     <ul>
     <li>Định tuyến
     <li>Địa chỉ logic cho hệ thống mạng: Là địa chỉ chuyên dùng cho định tuyến (Vd địa chỉ IP)
     </ul>
  <li>Lớp 2: Data Link (Liên kết dữ liệu): Cung cấp, điều khiển việc truy nhập vào đường truyền vật lí và thực hiện chức năng giao tiếp vs lớp mạng ở bên trên. Có chơ chế dò lỗi.
  <li>Lớp 1: Physical (Lớp vật lý): Xây dựng đường truyền vật lý cho các host:
      <ul>
      <li>Truyền 1 dòng bit qua 1 đường truyền vật lý cụ thể nào đó.
      <li>Quy định các đặc điểm của một đường truyền vật lý về cơ, điện, quang, các thủ tục chức năng để làm sao đó có thể truyền được 1 dòng bit nhị phân qua đường truyền vật lý.
      </ul>
##Cách hoạt động mô hình OSI
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

#MÔ HÌNH TCP/IP
#Cấu trúc
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
