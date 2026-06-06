# README

# HỆ THỐNG THEO DÕI VÀ THÔNG BÁO VỊ TRÍ XE BUÝT THEO THỜI GIAN THỰC

## Thông tin sinh viên

* **Sinh viên thực hiện:** Ngô Thành Đạt
* **Mã sinh viên:** 1671020081
* **Giảng viên hướng dẫn:** Nguyễn Văn Nhân
* **Khoa:** Công nghệ Thông tin
* **Trường:** Đại học Đại Nam
* **Đề tài:** Hệ thống theo dõi và thông báo vị trí xe buýt theo thời gian thực
* **Lĩnh vực:** Thành phố thông minh (Smart City), IoT, GPS, Web Dashboard, Giao thông thông minh

---

# 1. Giới thiệu đề tài

Trong những năm gần đây, cùng với sự phát triển mạnh mẽ của đô thị hóa và sự gia tăng dân số tại các thành phố lớn, nhu cầu sử dụng phương tiện giao thông công cộng ngày càng tăng. Xe buýt là một trong những phương tiện giao thông được nhiều người lựa chọn nhờ chi phí thấp, tính an toàn cao và khả năng vận chuyển số lượng lớn hành khách.

Tuy nhiên, một trong những bất tiện lớn nhất đối với người sử dụng xe buýt là không thể biết chính xác vị trí hiện tại của xe cũng như thời gian xe sẽ đến trạm dừng. Điều này khiến hành khách phải chờ đợi lâu, khó chủ động sắp xếp thời gian và làm giảm hiệu quả sử dụng giao thông công cộng.

Với sự phát triển của Internet of Things (IoT), GPS và các nền tảng Web hiện đại, việc xây dựng các hệ thống theo dõi phương tiện theo thời gian thực đã trở nên dễ dàng và hiệu quả hơn. Các thiết bị định vị GPS có thể cung cấp dữ liệu vị trí chính xác, trong khi các nền tảng Web giúp hiển thị thông tin trực quan trên bản đồ số.

Xuất phát từ thực tế đó, đề tài "Hệ thống theo dõi và thông báo vị trí xe buýt theo thời gian thực" được xây dựng nhằm hỗ trợ hành khách theo dõi vị trí xe buýt trực tuyến thông qua Website. Hệ thống sử dụng ESP32 kết hợp GPS để thu thập dữ liệu vị trí, truyền dữ liệu lên máy chủ Flask thông qua WiFi và hiển thị trực quan trên bản đồ OpenStreetMap.

Ngoài chức năng theo dõi vị trí hiện tại, hệ thống còn hỗ trợ hiển thị tuyến đường, danh sách trạm dừng, dự đoán thời gian đến trạm, thống kê hành trình, lưu lịch sử hoạt động và phân biệt chiều chạy lượt đi - lượt về. Đây là một mô hình ứng dụng IoT trong giao thông thông minh và là nền tảng để phát triển các hệ thống quản lý vận tải công cộng trong tương lai.

---

# 2. Mục tiêu của hệ thống

Hệ thống được xây dựng nhằm đạt được các mục tiêu sau:

* Thu thập dữ liệu vị trí xe buýt theo thời gian thực bằng GPS.
* Truyền dữ liệu từ ESP32 đến máy chủ Flask thông qua WiFi.
* Hiển thị vị trí xe buýt trực tiếp trên bản đồ.
* Theo dõi tuyến đường và các trạm dừng.
* Dự đoán thời gian xe đến các trạm.
* Hiển thị chiều chạy lượt đi và lượt về.
* Lưu lịch sử hành trình của xe.
* Thống kê quãng đường đã di chuyển.
* Hỗ trợ hành khách giảm thời gian chờ đợi.
* Hỗ trợ đơn vị quản lý giám sát phương tiện.

---

# 3. Kiến trúc hệ thống

Hệ thống được xây dựng theo mô hình Client - Server.

```text
GPS Module
      │
      ▼
    ESP32
      │
      │ WiFi
      ▼
 Flask Server
      │
      ▼
 REST API
      │
      ▼
Website Dashboard
      │
      ▼
 Người dùng
```

Nguyên lý hoạt động:

1. GPS xác định vị trí hiện tại của xe buýt.
2. ESP32 đọc dữ liệu GPS.
3. ESP32 gửi dữ liệu lên Flask Server.
4. Flask xử lý dữ liệu vị trí.
5. Website lấy dữ liệu từ API.
6. Hiển thị vị trí xe trên bản đồ.
7. Tính toán thời gian đến trạm.
8. Lưu lịch sử hành trình.

---

# 4. Công nghệ sử dụng

| Nhóm công nghệ     | Công nghệ             |
| ------------------ | --------------------- |
| Vi điều khiển      | ESP32                 |
| Định vị            | GPS NEO-6M            |
| Ngôn ngữ lập trình | Python                |
| Backend            | Flask                 |
| Frontend           | HTML, CSS, JavaScript |
| Bản đồ             | Leaflet.js            |
| Nền bản đồ         | OpenStreetMap         |
| Giao tiếp          | HTTP REST API         |
| IDE                | Arduino IDE           |
| Soạn thảo mã nguồn | Visual Studio Code    |

---

# 5. Chức năng chính

## 5.1 Theo dõi vị trí xe buýt

* Hiển thị vị trí xe theo thời gian thực.
* Cập nhật dữ liệu liên tục.
* Hiển thị tốc độ hiện tại.
* Hiển thị trạng thái xe.

## 5.2 Hiển thị tuyến đường

* Hiển thị toàn bộ tuyến xe buýt.
* Hiển thị các trạm dừng.
* Hiển thị chiều chạy.

## 5.3 Dự đoán thời gian đến trạm

* Tính khoảng cách đến trạm.
* Tính ETA.
* Cập nhật ETA theo thời gian thực.

## 5.4 Lưu lịch sử hành trình

* Lưu vị trí đã đi qua.
* Lưu thời gian đến từng trạm.
* Lưu chiều chạy.

## 5.5 Dashboard quản lý

* Bản đồ trực quan.
* Danh sách trạm.
* Thống kê hoạt động.
* Thông tin xe buýt.

---

# 6. Giao diện hệ thống

Hệ thống được thiết kế theo mô hình Dashboard hiện đại gồm:

### Bản đồ theo dõi

* Hiển thị xe buýt.
* Hiển thị tuyến đường.
* Hiển thị các trạm.

### Thông tin xe buýt

* Mã xe.
* Tốc độ.
* Trạng thái.
* Trạm hiện tại.
* Trạm tiếp theo.

### Danh sách trạm

* Tên trạm.
* ETA.
* Trạng thái đã đến.

### Lịch sử hành trình

* Thời gian đến trạm.
* Tên trạm.
* Lượt đi/lượt về.

### Thống kê

* Quãng đường đã đi.
* Số trạm đã qua.
* Tiến độ hành trình.

---

# 7. Cấu trúc thư mục dự án

```text
BusTrackingSystem/
│
├── app.py
│
├── templates/
│   └── index.html
│
├── static/
│   ├── css/
│   ├── js/
│   └── images/
│
├── esp32/
│   └── bus_tracker.ino
│
├── data/
│   └── route_data.json
│
├── requirements.txt
│
└── README.md
```

---

# 8. Cài đặt môi trường

## 8.1 Arduino IDE

Cài đặt:

* esp32 by Espressif Systems
* TinyGPSPlus
* ArduinoJson

Thư viện sử dụng:

```cpp
WiFi.h
HTTPClient.h
TinyGPS++.h
ArduinoJson.h
```

---

## 8.2 Python

Kiểm tra:

```bash
python --version
```

Cài Flask:

```bash
pip install flask
```

---

# 9. Chạy hệ thống

## Bước 1

Upload code ESP32:

```text
Arduino IDE → Upload
```

## Bước 2

Khởi động Flask:

```bash
python app.py
```

Kết quả:

```text
Running on http://127.0.0.1:5000
```

## Bước 3

Mở Website:

```text
http://localhost:5000
```

hoặc:

```text
http://IP_MAY_TINH:5000
```

---

# 10. Kết quả đạt được

Sau khi hoàn thành, hệ thống đã thực hiện được:

✔ Theo dõi vị trí xe buýt theo thời gian thực.

✔ Hiển thị tuyến đường trên bản đồ.

✔ Hiển thị danh sách các trạm dừng.

✔ Dự đoán thời gian đến trạm.

✔ Hiển thị chiều chạy lượt đi và lượt về.

✔ Lưu lịch sử đến trạm.

✔ Thống kê quãng đường di chuyển.

✔ Dashboard trực quan và dễ sử dụng.

---

# 11. Ý nghĩa trong thành phố thông minh

Hệ thống là một mô hình ứng dụng IoT trong lĩnh vực giao thông thông minh.

Các thành phần:

* GPS: thu thập dữ liệu vị trí.
* ESP32: truyền dữ liệu.
* Flask Server: xử lý dữ liệu.
* Web Dashboard: giám sát và quản lý.

Mô hình giúp:

* Nâng cao chất lượng giao thông công cộng.
* Giảm thời gian chờ đợi của hành khách.
* Hỗ trợ quản lý phương tiện hiệu quả.
* Hướng tới xây dựng thành phố thông minh.

---

# 12. Hướng phát triển

Trong tương lai hệ thống có thể mở rộng:

* Quản lý nhiều xe buýt cùng lúc.
* Kết nối GPS thực tế.
* Tích hợp Firebase Cloud.
* Xây dựng ứng dụng Android.
* Xây dựng ứng dụng iOS.
* Thông báo khi xe sắp đến trạm.
* Tích hợp AI dự đoán thời gian đến trạm.
* Kết nối trung tâm điều hành giao thông thông minh.

---

# 13. Tác giả

**Ngô Thành Đạt**
**MSV:** 1671020081
**Khoa Công nghệ Thông tin - Trường Đại học Đại Nam**

**Giảng viên hướng dẫn:** Nguyễn Văn Nhân
