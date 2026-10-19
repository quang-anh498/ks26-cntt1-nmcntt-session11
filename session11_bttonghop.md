# Phần 1 : Hoàn thiện SRS bằng Heading Styles và Auto TOC.
## 1 và 2. Mở rộng khung tiêu đề & Gán cấp độ Heading.

### 1. Giới thiệu dự án [Heading 1]
- 1.1. Mục tiêu [Heading 2]
- 1.2. Đối tượng sử dụng [Heading 2]
### 2. Chức năng hệ thống [Heading 1]
- 2.1. Quản lý mượn sách [Heading 2]
- 2.2. Luồng mượn sách qua thẻ sinh viên [Heading 3]
- 2.3. Quản lý trả sách [Heading 2]
 ### 3. Yêu cầu bảo mật [Heading 1]
 ## 3. Viết nội dung mô tả
 - Dưới mục 2. Chức năng hệ thống.
 - Dưới mục 3. Yêu cầu bảo mật.

## 4. Thao tác chèn Auto TOC và  Cập nhật số trang.
- Chèn mục lục: 
```
References → Table of Contents → Chọn mẫu Automatic Table.
```
- Cập nhật số trang: Sau khi thêm 1 đoạn văn bản đẩy mục **3** sang trang mới 
 ```
 bấm Update Field → Chọn Update entire table.
 ```
 # Phần 2 : Chuẩn hóa dữ liệu và AutoFilter
 ## 1. Bảng chỉ ra 3 lỗi vi phạm 5 Quy tắc Vàng
 |  Lỗi |  Vị trí (hàng) | Quy tắc bị vi phạm |
 | :---: | :---: | :---| 
 | 1 | hàng 1 | Vi phạm quy tắc Merge Cells |
 | 2 | hàng 5 | Vi phạm quy tắc Hàng/Cột trốn
 | 3 | hàng 6 |Vi phạm quy tắc đặt dữ liệu tính toán
##  2. Viết lại bảng đã sửa đúng chuẩn.
| MSSV | Họ Tên |  Mã Sách | Ngày Mượn |  Tình Trạng |
| :---: | :---: | :---: | :---: | :---| 
| SV1 | Mai Ngọc Đức Hải | S01 | 15/10/2026 | Đang mượn
| SV2 | Lê Quang Hào| S02 | 15/10/2026 | Quá hạn
| SV3 | Tô Mạnh hào | S03 | 15/10/2026 | Đang mượn
| SV4 | Đặng Quang Anh | S099 | 15/10/2026 | Đã trả
## 3. Xác định Record và Field
- Field : Là tập hợp các thông tin cùng loại dọc theo cột.
- Record : Là tập hợp toàn bộ thông tin chi tiết về một đối tượng cụ thể nằm trên một hàng ngang.
## 4. Thao tác bật AutoFilter và lọc dữ liệu.
- Bật AutoFilter : Ctrl + Shift + L 
- Lọc trạng thái "Quá hạn" : chọn vào mũi tên lọc ở cột tình trạng , tích chọn "Quá hạn"  --> bấm OK.

# Phần 3 – Nối dữ liệu bằng VLOOKUP.
## 1. Công thức VLOOKUP cơ bản.
```
 =VLOOKUP(C2, DanhMucSach!$A$2:$C$100, 2)
 ```
 ## 2. Vấn đề với dòng Mã Sách S099 (Hàng 8).
 - Lỗi **#N/A**
 - Nguyên nhân: Mã sách **S099** không tồn tại trong  dữ liệu của **DanhMucSach**.
## 3. Công thức hoàn chỉnh bọc thêm IFERROR.
```
=IFERROR(VLOOKUP(C2, DanhMucSach!$A$2:$C$100, 2)
```
# Phần 4 – Slide báo cáo tiến độ.
## 1. Thiết kế nội dung Slide .
- Assertion Title : Chuẩn hóa  dữ liệu giúp tự động hóa 100% việc tra cứu tên sách và phát hiện những ai đang mượn, đã trả và chưa trả.
- Content AArea : 100% dữ liệu phiếu mượn được làm sạch và nối thành công, loại bỏ hoàn toàn lỗi cấu trúc thô.
## 2. Áp dụng Rule 10/20/30
- Quy tắc số lượng phải hoàn thành 10 slide và đầy đủ các phần trình bày gọn gàng, thuận mắt.
- Quy tắc thời gian trình bày 20 phút / 30pt font : Thời gian dành riêng để trình bày slide kết quả xử lý dữ liệu này dự kiến trong vòng 2 phút.
