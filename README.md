# Khoa học dữ liệu - Đồ án cuối kỳ
## Nhóm 20:
* Thành viên:  
    * Trần Anh Hào      - 1612850
    * Nguyễn Quang Phú  - 1612508
* Đề tài: 
    * Câu hỏi: Dự đoán giá cho thuê chỗ ở trong 1 ngày.
    * Web thu thập dữ liệu: https://www.luxstay.com/
    * Trả lời được câu hỏi thì có lợi ích: đưa ra dự đoán giá cho một chỗ ở mới từ đó có thể lựa chọn, đánh giá xem chỗ ở mới giá có phù hợp không, xem xét có nên thuê hay không (đối với người thuê), xem xét giá người chủ nhà đề ra có hợp lý không để xem xét đưa vào chuỗi kinh doanh (đối với người chủ)
    * Nguồn gốc câu hỏi: cảm hứng lấy từ chương trình Shark tank Việt Nam
    * Dữ liệu hợp pháp: đã kiểm tra file robots.txt trên trang: https://www.luxstay.com/robots.txt
    * Thu thập dữ liệu: parse HTML.
    * Dữ liệu gồm ? dòng, ? cột.
    * Ý nghĩa từng cột: ?
    * Dữ liệu có giá trị thiếu hay không: ?
    * Vấn đề khác: ?

* Quá trình thu thập dữ liệu:
    * 19/11/2019:
        * Tìm hiểu về web API của luxstay tại: https://docs.luxstay.com/overview/
        * Tuy luxstay cung cấp đầy đủ API để lấy dữ liệu nhưng phải có liên kết với luxstay để cung cấp account. Vì vậy phải parse HTML.
        * Lấy trước các thông tin chung về chỗ ở gồm các thông tin: loại nhà, tên nhà, các loại phòng, giá, vị trí, số đánh giá của các địa điểm như Đà Lạt, Hà Nội, HCM, Vũng Tàu, Nha Trang, Quảng Ninh
    * 30/11/2019:
        * Lấy các thông tin chi tiết ở từng chỗ ở: diện tích, tiện ích.
        * Lúc lấy được lúc không được :(s

* Quá trình thực hiện:
    * 13/11/2019- 16/11/2019: Tìm kiếm ý tưởng và dữ liệu.
    * 17/11/2019- 18/11/2019: Thảo luận và thống nhất đề tài.
    * 19/11/2019- ?         : Bắt đầu thu thập dữ liệu.
