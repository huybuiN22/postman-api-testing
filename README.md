                                                                          BÁO CÁO KIỂM THỬ API VỚI POSTMAN
                                                                          
1. Mục tiêu kiểm thử
Sử dụng công cụ Postman để thực hiện kiểm thử API thông qua các phương thức HTTP phổ biến.
Thông qua bài thực hành, sinh viên làm quen với việc tạo Collection, tạo Request, gửi yêu cầu đến API, kiểm tra kết quả trả về và sử dụng chức năng Test của Postman để tự động kiểm tra kết quả.
Các phương thức HTTP được thực hiện trong bài gồm GET, POST, PUT và DELETE.
2. Môi trường kiểm thử
Công cụ kiểm thử: Postman.
Nền tảng sử dụng: Postman Web.
API được sử dụng để kiểm thử: JSONPlaceholder.
Địa chỉ API: https://jsonplaceholder.typicode.com
Phương pháp kiểm thử: Kiểm thử thủ công kết hợp kiểm thử tự động bằng Postman Test Script.
3. Phương pháp kiểm thử
Trong quá trình thực hiện, tiến hành tạo một Collection có tên là Postman API Test.
Collection bao gồm bốn Request tương ứng với bốn phương thức HTTP là GET, POST, PUT và DELETE.
Sau khi gửi từng Request, tiến hành kiểm tra HTTP Status Code và dữ liệu Response trả về.
Ngoài việc kiểm tra thủ công, sử dụng chức năng Test của Postman để tự động kiểm tra kết quả của từng Request.
Cuối cùng sử dụng Collection Runner để chạy toàn bộ các Request và tổng hợp kết quả kiểm thử.
4. Kịch bản kiểm thử lần 1
Tên kịch bản
Kiểm thử lấy dữ liệu bằng phương thức GET.
Mục đích
Kiểm tra khả năng gửi yêu cầu GET đến API và nhận dữ liệu trả về.
Phương thức HTTP
GET.
URL
https://jsonplaceholder.typicode.com/posts/1
Kết quả mong đợi
Gửi yêu cầu thành công.
API trả về mã trạng thái HTTP 200 OK.
Response trả về dữ liệu ở định dạng JSON.
Response chứa thông tin của bài viết có ID bằng 1.
Kết quả thực tế
Request được gửi thành công.
API trả về mã trạng thái 200 OK.
Dữ liệu trả về đúng định dạng JSON và chứa thông tin bài viết có ID bằng 1.
Trạng thái
Thành công.
Kết quả sau khi kiểm thử

<img width="1920" height="1080" alt="get1" src="https://github.com/user-attachments/assets/ff4a9d79-4b58-4a1e-bb84-1e6555fd3d57" />

Kết quả kiểm thử chi tiết
<img width="1920" height="1080" alt="get2" src="https://github.com/user-attachments/assets/0dbe8f1d-23ee-4a95-b6af-71a64e42f0d5" />

Kết quả kiểm thử cho thấy các điều kiện kiểm tra đều đạt yêu cầu.
Kiểm tra Status Code 200: Thành công.
Kiểm tra Response có định dạng JSON: Thành công.
Kiểm tra Response có ID bằng 1: Thành công.
Tổng số Test Case: 3.
Số Test Case thành công: 3.
Số Test Case thất bại: 0.
Tỷ lệ thành công: 100%.
6. Kịch bản kiểm thử lần 2
Tên kịch bản
Kiểm thử tạo dữ liệu bằng phương thức POST.
Mục đích
Kiểm tra khả năng gửi dữ liệu mới đến API bằng phương thức POST.
Phương thức HTTP
POST.
URL
https://jsonplaceholder.typicode.com/posts
Dữ liệu gửi lên
Dữ liệu được gửi lên API gồm tiêu đề bài viết là “Postman Testing”, nội dung là “This is a test created with Postman” và userId bằng 1.
Kết quả mong đợi
Gửi yêu cầu thành công.
API trả về mã trạng thái HTTP 201 Created.
Response chứa trường title với giá trị “Postman Testing”.
Response chứa trường userId với giá trị 1.
Kết quả thực tế
Request được gửi thành công.
API trả về mã trạng thái 201 Created.
Các dữ liệu được kiểm tra trong Response đều đúng với kết quả mong đợi.
Trạng thái
Thành công.
Kết quả sau khi kiểm thử
<img width="1920" height="1080" alt="post1" src="https://github.com/user-attachments/assets/2d84291d-0a3d-4866-8923-b09b0af5c144" /><img width="1920" height="1080" alt="put" src="https://github.com/user-attachments/assets/04b39087-ae81-47f8-87f1-1502c5f08224" />
<img width="1920" height="1080" alt="put" src="https://github.com/user-attachments/assets/34f78501-cb8c-40ba-8500-9a617ed75fa6" />

Kết quả kiểm thử chi tiết
Kiểm tra Status Code 201: Thành công.
Kiểm tra Response chứa title: Thành công.
Kiểm tra Response chứa userId: Thành công.
Tổng số Test Case: 3.
Số Test Case thành công: 3.
Số Test Case thất bại: 0.
Tỷ lệ thành công: 100%.
7. Kịch bản kiểm thử lần 3
Tên kịch bản
Kiểm thử cập nhật dữ liệu bằng phương thức PUT.
Mục đích
Kiểm tra khả năng cập nhật dữ liệu thông qua phương thức PUT.
Phương thức HTTP
PUT.
URL
https://jsonplaceholder.typicode.com/posts/1
Dữ liệu gửi lên
Dữ liệu cập nhật gồm ID bằng 1, tiêu đề mới là “Updated Post”, nội dung là “Updated using Postman” và userId bằng 1.
Kết quả mong đợi
Gửi yêu cầu thành công.
API trả về mã trạng thái HTTP 200 OK.
Response chứa dữ liệu đã được cập nhật.
Giá trị của trường title là “Updated Post”.
Kết quả thực tế
Request được gửi thành công.
API trả về kết quả sau khi cập nhật dữ liệu.
Trạng thái
Thành công.
Kết quả sau khi kiểm thử
<img width="1920" height="1080" alt="put" src="https://github.com/user-attachments/assets/f5fbfd5c-c029-400d-825c-ab0183f11767" />

Kết quả kiểm thử chi tiết
Kiểm tra Status Code 200: Thành công.
Kiểm tra dữ liệu title đã được cập nhật thành “Updated Post”: Thành công.
Tổng số Test Case: 2.
Số Test Case thành công: 2.
Số Test Case thất bại: 0.
Tỷ lệ thành công: 100%.
8. Kịch bản kiểm thử lần 4
Tên kịch bản
Kiểm thử xóa dữ liệu bằng phương thức DELETE.
Mục đích
Kiểm tra khả năng gửi yêu cầu DELETE đến API.
Phương thức HTTP
DELETE.
URL
https://jsonplaceholder.typicode.com/posts/1
Kết quả mong đợi
Gửi yêu cầu thành công.
API trả về mã trạng thái HTTP phù hợp.
Request được xử lý mà không xảy ra lỗi.
Kết quả thực tế
Request được gửi thành công và API trả về kết quả phù hợp.
Trạng thái
Thành công.
Kết quả sau khi kiểm thử
<img width="1920" height="1080" alt="delete" src="https://github.com/user-attachments/assets/ef5d2e9b-ec01-458d-9955-e9645fb7bcfc" />
Kết quả kiểm thử chi tiết
Kiểm tra Status Code: Thành công.
Tổng số Test Case: 1.
Số Test Case thành công: 1.
Số Test Case thất bại: 0.
Tỷ lệ thành công: 100%.
9. Kiểm thử Collection
Sau khi hoàn thành các kịch bản kiểm thử GET, POST, PUT và DELETE, tiến hành sử dụng chức năng Collection Runner của Postman để chạy toàn bộ Collection.
Collection gồm bốn Request là GET, POST, PUT và DELETE.
Kết quả cấu hình Collection Runner
<img width="1920" height="1080" alt="cauhinh" src="https://github.com/user-attachments/assets/5a804e5f-fe79-43d5-9c13-efbb36aa9255" />
Sau khi cấu hình, tiến hành chạy Collection bằng chức năng Start Run.
Kết quả chạy Collection
<img width="1920" height="1080" alt="runner" src="https://github.com/user-attachments/assets/1ca170e9-e6ea-46ca-9818-81291a493361" />

Kết quả kiểm thử được tổng hợp dựa trên số lượng Request và Test Case Passed hoặc Failed được hiển thị trên Postman.
10. Kết quả kiểm thử
Số lượng kịch bản đã kiểm thử: 4.
Số lần thành công: 4
Số lần thất bại: 0
Tỷ lệ thành công: 100%
11. Phát hiện lỗi
Trong quá trình thực hiện kiểm thử, các Request GET, POST, PUT và DELETE được gửi đến API để kiểm tra khả năng hoạt động.
Các kết quả được kiểm tra thông qua HTTP Status Code và dữ liệu Response trả về.
Nếu tất cả các kiểm thử đều thành công thì không phát hiện lỗi trong quá trình thực hiện.
ID lỗi: Không có.
Mô tả lỗi: Không phát hiện lỗi nghiêm trọng trong quá trình kiểm thử.
Mức độ ảnh hưởng: Không.
Ghi chú: Các Request được kiểm tra và cho kết quả phù hợp với yêu cầu đặt ra.
12. Nhận xét
Qua bài thực hành, em đã làm quen với công cụ Postman và hiểu được cách sử dụng Postman để kiểm thử API.
Em đã thực hiện được việc tạo Collection và tạo các Request với các phương thức GET, POST, PUT và DELETE.
Ngoài ra, em đã biết cách kiểm tra HTTP Status Code, kiểm tra dữ liệu Response và sử dụng Test Script để tự động kiểm tra kết quả.
Việc sử dụng Collection Runner giúp thực hiện nhiều Request liên tiếp và theo dõi kết quả kiểm thử một cách thuận tiện.
13. Kết luận
Sau khi hoàn thành bài thực hành, em đã có những kiến thức cơ bản về kiểm thử API bằng Postman.
Em đã biết cách gửi các HTTP Request, kiểm tra Response, kiểm tra Status Code và xây dựng các Test Case tự động.
Bài thực hành giúp em hiểu rõ hơn về quy trình kiểm thử REST API và cách sử dụng Postman trong kiểm thử phần mềm.
Thông qua việc thực hiện các phương thức GET, POST, PUT và DELETE, em hiểu rõ hơn cách các API xử lý những thao tác lấy, tạo, cập nhật và xóa dữ liệu.
