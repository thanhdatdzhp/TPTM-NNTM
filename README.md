# Hệ thống theo dõi và thông báo vị trí xe buýt theo thời gian thực

## Thông tin sinh viên

* **Sinh viên thực hiện:** Ngô Thành Đạt
* **Mã sinh viên:** 1671020081
* **Đề tài:** Hệ thống theo dõi và thông báo vị trí xe buýt theo thời gian thực
* **Giảng viên hướng dẫn:** Nguyễn Văn Nhân
* **Hướng đề tài:** Thành phố thông minh, IoT, GPS, ESP32, giao thông thông minh, Web Dashboard

## 1. Giới thiệu đề tài

Trong bối cảnh các đô thị ngày càng phát triển, nhu cầu sử dụng phương tiện giao thông công cộng ngày càng tăng cao. Tuy nhiên, hành khách thường gặp khó khăn trong việc xác định vị trí hiện tại của xe buýt cũng như thời gian xe đến trạm dừng. Điều này làm tăng thời gian chờ đợi và gây bất tiện trong quá trình di chuyển.

Đề tài xây dựng một hệ thống theo dõi vị trí xe buýt theo thời gian thực sử dụng ESP32 kết hợp GPS và nền tảng Web Dashboard. Hệ thống cho phép thu thập dữ liệu vị trí từ xe buýt, gửi lên máy chủ thông qua mạng WiFi và hiển thị trực quan trên bản đồ số. Người dùng có thể theo dõi vị trí hiện tại của xe, xem lộ trình di chuyển, dự đoán thời gian đến các trạm và tra cứu lịch sử hành trình.

Hệ thống là một mô hình ứng dụng của Internet of Things (IoT) trong lĩnh vực giao thông thông minh và thành phố thông minh, góp phần nâng cao chất lượng dịch vụ giao thông công cộng.

## 2. Mục tiêu của hệ thống

* Thu thập dữ liệu vị trí từ GPS.
* Truyền dữ liệu từ ESP32 đến máy chủ Flask.
* Hiển thị vị trí xe buýt trên bản đồ theo thời gian thực.
* Hiển thị danh sách các trạm dừng.
* Dự đoán thời gian xe đến từng trạm.
* Theo dõi chiều chạy lượt đi và lượt về.
* Lưu lịch sử hành trình của xe.
* Lưu lịch sử thời gian đến các trạm.
* Hỗ trợ người dùng theo dõi lộ trình xe buýt thuận tiện hơn.

## 3. Công nghệ sử dụng

| Nhóm công nghệ     | Công nghệ                       |
| ------------------ | ------------------------------- |
| Vi điều khiển      | ESP32                           |
| Định vị            | GPS NEO-6M                      |
| Ngôn ngữ lập trình | Python                          |
| Backend            | Flask                           |
| Frontend           | HTML, CSS, JavaScript           |
| Bản đồ             | Leaflet.js                      |
| Dữ liệu bản đồ     | OpenStreetMap                   |
| Giao tiếp          | HTTP REST API                   |
| IDE                | Arduino IDE, Visual Studio Code |
| Mạng truyền thông  | WiFi                            |

## 4. Chức năng chính

### 4.1. Theo dõi vị trí xe buýt

* Hiển thị vị trí hiện tại của xe trên bản đồ.
* Cập nhật dữ liệu theo thời gian thực.
* Hiển thị tốc độ xe.
* Hiển thị trạng thái hoạt động.

### 4.2. Quản lý tuyến đường

* Hiển thị tuyến xe buýt trên bản đồ.
* Hiển thị danh sách các trạm dừng.
* Hỗ trợ theo dõi lượt đi và lượt về.
* Hiển thị tiến trình di chuyển trên tuyến.

### 4.3. Dự đoán thời gian đến trạm

* Tính khoảng cách từ xe đến từng trạm.
* Dự đoán thời gian xe đến trạm dựa trên tốc độ hiện tại.
* Cập nhật ETA theo thời gian thực.

### 4.4. Lịch sử hành trình

* Lưu lịch sử các vị trí đã đi qua.
* Ghi nhận thời gian xe đến từng trạm.
* Hiển thị chiều chạy tương ứng.
* Hỗ trợ tra cứu lịch sử hoạt động.

### 4.5. Dashboard quản lý

* Hiển thị bản đồ thời gian thực.
* Hiển thị thông tin xe buýt.
* Hiển thị thống kê hành trình.
* Hiển thị trạng thái hoạt động của hệ thống.

## 5. Ý nghĩa trong thành phố thông minh

Hệ thống là một ứng dụng điển hình của Internet of Things (IoT) trong lĩnh vực giao thông thông minh. Thiết bị GPS đóng vai trò thu thập dữ liệu vị trí, ESP32 thực hiện truyền dữ liệu, Flask Server xử lý dữ liệu thời gian thực và Dashboard Web hỗ trợ người dùng giám sát hoạt động của xe buýt.

Mô hình có thể được mở rộng trong tương lai để:

* Quản lý nhiều xe buýt cùng lúc.
* Kết nối với GPS thực tế trên các phương tiện.
* Xây dựng ứng dụng Android và iOS.
* Tích hợp Firebase hoặc MySQL.
* Gửi thông báo khi xe sắp đến trạm.
* Kết nối với hệ thống giao thông thông minh của thành phố.
* Ứng dụng AI để dự đoán thời gian đến trạm chính xác hơn.

## 6. Tác giả

**Ngô Thành Đạt**  
**MSV:** 1671020081  
**Khoa Công nghệ Thông tin - Trường Đại học Đại Nam**
