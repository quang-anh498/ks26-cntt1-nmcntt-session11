# Yêu cầu đề bài 
 ## Phần 1 
   1. Lookup_value nằm ở sheet **Don_Hang** mà bạn muốn tím kiếm thông tin. Đây là chìa khóa để tìm **VLOOKUP** trong bảng danh mục.
   2. Table-value là toàn bộ bảng dữ liệu bên Sheet ** Danh_muc** chứa cả cột Mã linh kiện , tên linh kiện và đơn giá. 
   3. col_index_num là số thứ tự của cột, chứa thông tin bạn muốn lấy về Sheet
   4. range_lookup là xác định hình thức tìm kiếm chính xác hay tương đối. Đảm bảo excel chỉ trả về đúng kết quả khi mã linh kiện khớp hoàn toàn 100%.

## Phần 2 : 
Viết công thức VLOOKUP hoàn chỉnh
 
=IFERROR(VLOOKUP(A2, Danh_Muc!$A$2:$C$100, 2, FALSE), "Không tìm thấy linh kiện")
