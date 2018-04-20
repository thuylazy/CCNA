# **Bài 4: Chia địa chỉ IP**

## **I.Một số kiến thức toán sử dụng trong việc tính toán địa chỉ IP**
- Chuyển đổi giữa hệ nhị phân và thập phân
- Một số giá trị lũy thừa 2 phải nhớ: 2^1 đến 2^12, 2^16
  <ul>
  <li>Cho n bit nhị phân => 2^n số nhị phân n-bit chạy từ: 00..0 (n bit 0) đến 11..1(n bit 1) hay từ 0 đến 2^n - 1 (trong hệ thập phân)
  </ul>
- Bảng: 
  <ul>
  <li> Bảng 1:
      <ul>
      <li>0000 0000 <-> 0
      <li>1000 0000 <-> 128
      <li>1100 0000 <-> 192
      <li>1110 0000 <-> 224
      <li>1111 0000 <-> 240
      <li>1111 1000 <-> 248
      <li>1111 1100 <-> 252
      <li>1111 1110 <-> 254
      <li>1111 1111 <-> 255
      </ul>
  <li> Bảng 2:
      <ul>
      <li>Gọi n: số bit mượn => bước nhảy = 2^{8-n}

           |Số bit mượn|1|2|3|4|5|6|7|8|
           |-----------|-|-|-|-|-|-|-|-|
           |Bước nhảy|128|64|32|16|8|4|2|1|

      </ul>
  </ul>

## **II.Cấu trúc địa chỉ IP**
- Địa chỉ IP là một dãy nhị phân dài tổng cộng 32 bits
- Gồm 2 phần:
  <ul>
  <li>Networks: định danh cho cả một mạng máy tính
  <li>Host: định danh cho từng host cụ thể trong mạng mt ấy
  </ul>
- Được viết thành từng cụm 8 bits, được gọi là một octet. Các octet được đổi ra số thập phân và được ngăn cách với nhau bằng dấu chấm.
  <ul>
  <li>VD: 10000000 01101100 01111010 11001100 --> 131.108.122.204
  </ul>
- Các bit phần mạng không được phép đồng thời bằng 0
- Nếu tất cả các bit phần host = 0 --> địa chỉ mạng
- Nếu tất cả các bit phần host = 1 --> địa chỉ quảng bá (broadcast)
  <ul>
  <li>Vd: Địa chỉ IP 192.168.1.1: Phần mạng: 192.168.1; Phần host 1
  <li>Gọi tên toàn bộ mạng 192.168.1: 192.168.1.0
  <li>Gọi tên toàn bộ host 192.168.1: 192.168.1.255
  </ul>
- Các lớp địa chỉ IP
  <ul>
  <li>Lớp A: 1 byte đầu là phần mạng, 3 byte sau là phần host
  <li>Lớp B: 2 byte đầu là phần mạng, 2 byte sau là phần host
  <li>Lớp B: 3 byte đầu là phần mạng, 1 byte sau là phần host
  </ul>

- LỚP A
  <ul>
  <li>Network : 8 bits
      <ul>
      <li>Bit đầu luôn bằng 0
      <li>7 bits sau định danh cho phần mạng
      <li>Địa chỉ mạng chạy từ  1.0.0.0 -> 127.0.0.0. Trong đó mạng 127.0.0.0 (loop network) khong dùng cho các host
      <li>->địa chỉ mạng sử dụng được: 1.0.0.0 -> 126.0.0.0 (2^{8} - 2 = 126 mạng)
      </ul>
  <li>Phần host: 24 bits: định danh cho phần host -> mỗi mạng lớp A có 2^{24} - 2 host
  <li> **Kết luận:** Khi nhìn 1 địa chỉ IP: octet đầu chạy từ 1 ->126 => địa chỉ IP thuộc lớp A
  </ul>

- LỚP B
  <ul>
  <li>Network: 16bit
      <ul>
      <li>2 bits đầu luôn là 1 0
      <li>14 bits sau: định danh cho phần mạng
      <li>Địa chỉ mạng chạy từ 128.0.0.0 -> 191.255.0.0
      <li>-> có tất cả 2^{14} mạng trog lớp B
      </ul>
  <li>Host: 16 bits -> có 2^{16} - 2 host
  <li> **Kết luận:** octet đầu từ 128 -> 191 => địa chỉ IP thuộc lớp B
  </ul>

- LỚP C
  <ul>
  <li>Network: 24 bits
      <ul>
      <li>3 bits đầu luôn là 1 1 0
      <li>21 bit sau: định dnah cho phần mạng
      <li>Địa chỉ mạng 192.0.0.0 -> 223.255.255.0 -> có tất cả 2^{21} mạng
      </ul>
  <li>Phần host: 8 bits -> có 2^{8} - 2 =254 host
  <li> **KL:** octet đầu 192->223: địa chỉ lớp C
  </ul>

- LỚP D
  <ul>
  <li>Địa chỉ: 224.0.0.0 -> 239.255.255.255
  <li>Địa chỉ multicast
  <li>VD:
      <ul>
      <li>224.0.0.5 dùng cho OSPF 
      <li>224.0.0.9 dùng cho RIPv2
      </ul>
  <li> **KL** octet đầu 224 -> 239: địa chỉ multicast lớp D
  </ul>


- LỚP E
  <ul>
  <li>Từ 240.0.0.0 trở đi
  <li>Dự phòng
  <li> **KL:** octet đầu từ 240 trở đi: Địa chỉ lớp E
  </ul>

 **TỔNG KẾT**

 |Octet đầu|Loại địa chỉ IP|
 |---------|--------------|
 |1 -> 126| Lớp A|
 |128 -> 191|Lớp B|
 |192 -> 223| Lớp C|
 |224 ->239| Lớp D|
 | 240 trở đi| Lớp E|

- ĐIẠ CHỈ BROADCAST
  <ul>
  <li>Có 2 loại: 
      <ul>
      <li>Direct broadcast: 192.168.1.255
      <li>Local broadcast: 255.255.255.255
      </ul>
  </ul>

## **III.Các loại địa chỉ IP**
-Có 2 loại địa chỉ IP: Private và Public
- Dải địa chỉ Private:
  <ul>
  <li>Lớp A: 10.x.x.x
  <li>Lớp B: 172.16.x.x -> 172.31.x.x
  <li>Lớp C: 192.168.x.x
  </ul>
- NAT: chuyển đổi private <-> public
- Ý nghĩa của địa chỉ private: bảo tồn địa chỉ IP public

## **IV.BÀI TẬP**
- Cho viết địa chỉ nào sau đây có thể dùng cho host:
  <ul>
  <li>A. 150.100.255.255 : địa chỉ lớp B, host =1 => địa chỉ broadcast => không dùng cho host
  <li>B. 175.100.255.18 : địa chỉ lớp B, có thể dùng cho host
  <li>C. 195.234.253.0 : địa chỉ lớp C, host =0 => địa chỉ mạng => không dùng cho host
  <li>D. 100.0.0.23 : địa chỉ lớp A, có thể dùng cho host
  <li>E. 188.258.221.176: k tồn tại địa chỉ này
  <li>F. 127.34.25.189: k thuộc lớp nào=> k dùng cho host
  <li>G. 224.156.217.73: địa chỉ lớp D(Multicast) => không dùng cho host
  </ul>

## **V.Cách máy tính xác định địa chỉ mạng:**

- Subnet-mark là một dãy nhị phân dài 32 bits được dùng để AND với địa chỉ IP để xác định địa chỉ mạng của địa chỉ IP ấy.
  <ul>
  <li>VD: Có địa chỉ IP: 192.168.1.1. Để xác định địa chỉ mảng của địa chỉ IP này ta AND với subnet -mark 255.255.255.0
  <li> 192.168.1.1  AND  255.255.255.0
  <li>-> 11000000.10101000.00000001.00000001  AND 11111111.11111111.11111111.00000000
  <li>KQ:11000000.10101000.00000001.00000000 <-> 192.168.1.0
  </ul>

- Khai báo một địa chỉ IP trên card mạng của máy tính bắt buộc phải khai báo một địa chỉ IP kèm với subnet-mark. 

  |Lớp|Subnet-mark|
  |----|----------|
  |A|255.0.0.0|
  |B|255.255.0.0|
  |C|255.255.255.0|

- Quy tắc viết địa chỉ IP: Sử dụng số Prefix, gọi là Prefix-length
  <ul>
  <li>   **A.B.C.D/n** với n: số bit mạng
  <li>VD: 
      <ul>
      <li>172.16.1.1
      <li>255.255.0.0
      <li>-> 172.16.1.1/16
      </ul>
  </ul>



