# Apache JMeter

## Giới thiệu

Apache JMeter là công cụ mã nguồn mở được phát triển bởi **Apache Software Foundation**, được sử dụng để kiểm thử hiệu năng (**Performance Testing**), kiểm thử tải (**Load Testing**) và kiểm thử áp lực (**Stress Testing**) cho các ứng dụng Web, API và hệ thống mạng.

Trong dự án này, Apache JMeter được sử dụng để đánh giá khả năng xử lý của hệ thống khi có nhiều người dùng truy cập đồng thời, từ đó xác định hiệu năng và độ ổn định của ứng dụng.

## Mục đích sử dụng

* Kiểm thử hiệu năng của hệ thống.
* Mô phỏng nhiều người dùng truy cập đồng thời.
* Đo thời gian phản hồi (Response Time).
* Theo dõi tỷ lệ lỗi (Error Rate).
* Đánh giá khả năng chịu tải của ứng dụng trước khi triển khai.

## Cấu trúc Test Plan

Test Plan của dự án được xây dựng với các thành phần chính sau:

### Thread Group

* Cấu hình số lượng người dùng ảo (Virtual Users).
* Thiết lập thời gian Ramp-Up.
* Xác định số lần lặp (Loop Count).

### HTTP Request

* Gửi các request đến API của hệ thống.
* Kiểm thử các chức năng chính.

### HTTP Header Manager

* Khai báo các Header cần thiết:

  * `Content-Type`
  * `Authorization`
  * `Accept`

### Assertions

* Kiểm tra mã trạng thái HTTP.
* Xác nhận dữ liệu trả về đúng mong đợi.

### Listeners

* View Results Tree
* Summary Report
* Aggregate Report
* Graph Results

## Chỉ số đánh giá

| Chỉ số             | Ý nghĩa                                           |
| ------------------ | ------------------------------------------------- |
| Response Time      | Thời gian phản hồi của request                    |
| Throughput         | Số lượng request xử lý trong một đơn vị thời gian |
| Error Rate         | Tỷ lệ request bị lỗi                              |
| Average            | Thời gian phản hồi trung bình                     |
| Min / Max          | Thời gian phản hồi nhỏ nhất và lớn nhất           |
| Standard Deviation | Mức độ dao động của thời gian phản hồi            |

## Kết quả kiểm thử

Kết quả kiểm thử được thu thập thông qua các Listener của JMeter như:

* Summary Report
* Aggregate Report
* View Results Tree
* Graph Results

Các báo cáo này giúp đánh giá:

* Hiệu năng tổng thể của hệ thống.
* Khả năng đáp ứng khi số lượng người dùng tăng.
* Xác định các điểm nghẽn (Bottleneck) trong quá trình xử lý.
* Đánh giá độ ổn định của ứng dụng dưới tải.

## Công nghệ sử dụng

* Apache JMeter
* HTTP/HTTPS Protocol
* CSV Data Set Config *(nếu có)*
* JSON Extractor *(nếu có)*
* Assertions
* Listeners

## Kết luận

Apache JMeter được sử dụng trong dự án nhằm đánh giá hiệu năng và khả năng chịu tải của hệ thống thông qua việc mô phỏng nhiều người dùng truy cập đồng thời. Kết quả kiểm thử là cơ sở để phân tích hiệu suất, phát hiện các điểm nghẽn và hỗ trợ tối ưu hóa hệ thống trước khi đưa vào vận hành thực tế.
