# KiemThuPhanMem-Nhom24
Bài tập lớn môn Kiểm thử phần mềm - ĐH Đà Lạt

# Hướng dẫn cài đặt và chạy hệ thống (On-boarding Guide)
**Đề tài:** Phân tích nopCommerce (R04) & Model-Based Testing (K02)  
**Nhóm:** 24  
* Thành viên: Nguyễn Đức Hoàng (Leader), Nguyễn Trần Quỳnh Hương, Phanthamala Somsavath, Y Kina Niê

## 1. Phiên bản dự án (Pinned Version)
* **Tag:** `release-4.70.5`

## 2. Hướng dẫn cài đặt & Chạy hệ thống (Build & Run)
* **Cách nhanh nhất (Docker Compose):**
  1. Mở Terminal tại thư mục chứa mã nguồn.
  2. Chạy lệnh khởi chạy container (SQL Server + Web App):
     ```bash
     docker compose up -d
     ```
  3. Đợi các service khởi động hoàn tất.
* **Chạy bằng .NET SDK (Local):**
  1. Yêu cầu máy cài đặt .NET SDK (phiên bản tương thích nopCommerce v4.70) và SQL Server.
  2. Cấu hình Connection String trong file `appsettings.json`.
  3. Chạy lệnh: `dotnet run` tại thư mục project `Nop.Web`.

## 3. Truy cập và Demo 3 luồng nghiệp vụ
* Truy cập ứng dụng qua trình duyệt: `http://localhost:5000` (hoặc port đã cấu hình).
* **3 luồng demo chính:**
  1. Đăng ký tài khoản và đăng nhập khách hàng.
  2. Chọn sản phẩm, thêm vào giỏ hàng (Add to Cart) và hoàn tất Checkout đơn hàng.
  3. Đăng nhập trang Quản trị (`/admin`) để xem danh sách đơn hàng và chuyển đổi trạng thái đơn hàng (Order Lifecycle).
