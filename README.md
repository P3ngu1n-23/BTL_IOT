﻿

# BTL_IOT

## Giới thiệu

Dự án này là máy chủ backend cho hệ thống IoT, cung cấp các API để tương tác với các thiết bị như Đèn LED, Quạt, Loa và Cảm biến. Máy chủ được xây dựng bằng Node.js và Express, giao tiếp với cơ sở dữ liệu MySQL và sử dụng MQTT để trao đổi dữ liệu với các thiết bị.

## Yêu cầu

- Node.js và npm đã được cài đặt
- Cơ sở dữ liệu MySQL
- MQTT broker

## Cài đặt

1. Clone repository:

```
$ gitclone https://github.com/P3ngu1n-23/BTL_IOT
```

2. Cài đặt các phụ thuộc:

```
npm install
```

Cấu hình kết nối cơ sở dữ liệu trong config/db/mysql.js nếu cần thiết.

Thiết lập cơ sở dữ liệu bằng cách chạy file createDB.sql trong thư mục config/db/.

3. Sử dụng
Khởi động máy chủ:

```
node server.js
```

Máy chủ sẽ lắng nghe trên cổng 3000.

4. API Endpoints

 Người dùng
- POST /user/signup - Đăng ký người dùng mới
- POST /user/login - Đăng nhập

 Thiết bị
- GET /device - Lấy danh sách tất cả thiết bị
- GET /device/:id - Lấy thông tin thiết bị theo ID

 Đèn LED
- GET /led - Lấy danh sách tất cả Đèn LED
- PUT /led/on/:id - Bật Đèn LED
- PUT /led/off/:id - Tắt Đèn LED

 Quạt
- GET /fan - Lấy danh sách tất cả Quạt
- PUT /fan/on/:id - Bật Quạt
- PUT /fan/off/:id - Tắt Quạt

 Loa
- GET /speaker - Lấy danh sách tất cả Loa
- PUT /speaker/on/:id - Bật Loa
- PUT /speaker/off/:id - Tắt Loa

 Cảm biến
- GET /sensor - Lấy danh sách tất cả Cảm biến
- GET /sensor/newest/:id: Lấy data mới nhất của cảm biến
- GET /sensor/history/:id: Lấy toàn bộ data đã đo được của cảm biến
- PUT /sensor/on/:id - Bật Cảm biến
- PUT /sensor/off/:id - Tắt Cảm biến
