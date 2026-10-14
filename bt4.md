**Phần1 :** 

&#x20;1. Lập bảng so sánh hai toán tử về:



|| Cơ chế hoạt động trong PowerShell.| Rủi ro mất dữ liệu.| Ngữ cảnh sử dụng thực tế.| Encoding file đầu ra.|
|-|-|-|-|-|
|>|Dấu ">" tương đương ( out-file -append ) nó cho cho phép người dùng ghi đè và xóa nội dung bên trong file đang có sẵn.|Nếu người dùng không để ý mà dùng ">" lên file đang chứa dữ liệu quan trọng thì sẽ dẫn đến dữ liệu bị xóa sạch khỏi file và ghi đè nội dung mới lên.|Phù hợp cho các kịch bản sinh báo cáo tổng hợp hằng ngày hoặc reset lại trạng thái từ đầu|Nếu mở bằng các công cụ hoặc trình soạn thảo không tương thích với UTF-16, file có thể bị lỗi font|
|>>|Dấu ">>" tương đương (app\_content) nó sẽ ghi nối tiếp lên nội dung bên trong file mà không xóa đi dữ liệu bên trong file.|Còn dùng ">>" thì sẽ không bị mất dữ liệu bên trong file cũ.|Phù hợp cho việc ghi hệ thống, thu thập lỗi phát sinh liên tục trong ngày mà không làm mất dữ liệu của các thời điểm trước đó.|Tương tự ">" thay vì sử dụng UTF-16 thì sử dụng UTF-8. |



**Phần2 :**

&#x20;Thay vì sử dụng thuật toán ">>" thuần túy có nguy cơ rủi do thì chúng ta hãy sử dụng :

&#x20;

&#x20; Get-Content .\\server.log | Select-String "ERROR" | Add-Content -Path daily\_report.txt -Encoding utf8

