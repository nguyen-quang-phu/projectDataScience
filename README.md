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
    * Dữ liệu thô gồm 7507 dòng, 8 cột.
    * Ý nghĩa từng cột: 
        * Link: chưa link dẫn đến trang.
        * Tên: tên nhà.
        * Loại nhà: nhà thuộc loại gì (biệt thự, căn hộ dịch vụ, căn hộ chung cư, nhà riêng, ...)
        * Diện tích:
        * Các loại phòng: chứa thông tin cho thuê (nguyên căn, phòng riêng,...) và số phòng của chỗ ở (bao nhiêu phòng khách, bao nhiêu phòng tắm, bao nhiêu phòng ngủ, bao nhiêu giường,...)
        * Giá: 
        * Vị trí: Đà lạt, HCM, Hà Nội, Quảng Ninh, Nha Trang, Vũng Tàu,...
        * Tiện ích: Máy lạnh, Máy giặt, Tủ lạnh,....
    * Dữ liệu có giá trị thiếu hay không: Tất cả các cột đều có giá trị thiếu
    * Vấn đề khác: 

* Chứng minh tính đúng đắn dữ liệu:
    * Theo thông tin trên https://www.luxstay.com/vi/about các chỗ ở trên luxstay đều được đội ngũ chuyên gia kiểm soát chất lượng, sàng lọc kỹ càng.
    * Theo Thoả Thuận Hợp Tác Với Chủ Nhà - Điều khoản và Điều kiện: mục A điều 3, mục A điều 8, mục B điều 2.1. Giá chỗ ở đều do đội ngũ chuyên gia của Luxstay đưa ra.
    ![Imgur](https://i.imgur.com/om0Q7hP.png)
    ![Imgur](https://i.imgur.com/Uy1hQ2c.png)
    ![Imgur](https://i.imgur.com/xM0R25u.png)

*   Thông tin dữ liệu sau khi thu thập:
<pre>
    * Link          : 7507 non-null object  
    * Tên           : 7489 non-null object
    * Loại nhà      : 7491 non-null object
    * Diện tích     : 7368 non-null object
    * Các loại phòng: 7489 non-null object
    * Giá           : 7488 non-null object
    * Vị trí        : 7487 non-null object
    * Tiện ích      : 7373 non-null object
</pre>
* Quá trình thu thập dữ liệu:
    * 19/11/2019:
        * Tìm hiểu về web API của luxstay tại: https://docs.luxstay.com/overview/
        * Tuy luxstay cung cấp đầy đủ API để lấy dữ liệu nhưng phải có liên kết với luxstay để cung cấp account. Vì vậy phải parse HTML.
        * Lấy trước các thông tin chung về chỗ ở gồm các thông tin: loại nhà, tên nhà, các loại phòng, giá, vị trí, số đánh giá của các địa điểm như Đà Lạt, Hà Nội, HCM, Vũng Tàu, Nha Trang, Quảng Ninh
    * 30/11/2019:
        * Lấy các thông tin chi tiết ở từng chỗ ở: diện tích, tiện ích.
        * Lúc lấy được lúc không được :(
    * 1/12/2019:
        * Lấy tất cả các phần thông tin còn lại
        * Trộn các file nhỏ lại thành 1 file chung
    * 6/12/2019:
        * Chạy lại các đoạn code lấy dữ liệu với hi vọng giảm được số dòng bị null.
        * Bổ sung một số đoạn lấy dữ liệu với hi vọng giảm được số dòng bị null.
    * 20/12/2019-21/12/2019:
        * Lấy giá cuối tuần sau khi được góp ý.
* Quá trình tiền xử lý dữ liệu:
    * 6/12/2019:
        * Đặt lại tên cột: "link", "name", "type", "area", "room_types", "price", "location" "other"
        * Chỉnh sửa dữ liệu vài thuộc tính
        * Xử lý giá trị thiếu vài thuộc tính
    * 1/1/2020:
        * Chuẩn hóa file về dạng có 1 output.
    * 2/1/2020:
        * Chuyển kiểu dữ liệu của mỗi cột về đúng dạng của nó.

* Quá trình thực hiện:
    * 13/11/2019- 16/11/2019: Tìm kiếm ý tưởng và dữ liệu.
    * 17/11/2019- 18/11/2019: Thảo luận và thống nhất đề tài.
    * 19/11/2019- 06/12/2019: Thu thập dữ liệu.
    * 06/12/2019- 13/12/2019: Tiền xử lý dữ liệu.
    * 02/01/2020- 09/01/2020: Thử các siêu tham số và tìm mô hình tốt nhất trong thời gian cho phép.
