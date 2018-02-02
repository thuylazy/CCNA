# **Bài 4: Chia địa chỉ IP**

1. **Một số kiến thức toán sử dụng trong việc tính toán địa chỉ IP**
- Chuyển đổi giữa hệ nhị phân và thập phân
- Một số giá trị lũy thừa 2 phải nhớ: 2^1 đến 2^12, 2^16
  Cho n bit nhị phân => 2^n số nhị phân n-bit chạy từ: 00..0 (n bit 0) đến 11..1(n bit 1) hay từ 0 đến 2^n - 1 (trong hệ thập phân)
- Bảng: 
  <ul>
  <li> Bảng 1:
      0000 0000 <-> 0
      1000 0000 <-> 128
      1100 0000 <-> 192
      1110 0000 <-> 224
      1111 0000 <-> 240
      1111 1000 <-> 248
      1111 1100 <-> 252
      1111 1110 <-> 254
      1111 1111 <-> 255
  <li> Bảng 2:
      Gọi n: số bit mượn => bước nhảy = 2^{8-n}
      |Số bit mượn|1|2|3|4|5|6|7|8|
      |----------------------------|
      |Bước nhảy|128|64|32|16|8|4|2|1|
  </ul>
