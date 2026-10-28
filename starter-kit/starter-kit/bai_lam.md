# BÀI LÀM – HACKATHON 01

- **Mã đề:** 19
- **Họ tên:Lê Đặng Thanh Tú** 
- **Lớp:CNTT2** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):Windows** 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\Lich_Trinh.txt .\docs\
mv .\Logo_Du_Lich.PNG .\media\
cp .\media\logo_du_lich.PNG .\backup\
rm .\temp_274.tmp
cd .\logs\
Get-ChildItem
cd ..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026   1:40 PM                backup
d-----        10/28/2026   1:36 PM                data
d-----        10/28/2026   1:39 PM                docs
d-----        10/28/2026   1:39 PM                logs
d-----        10/28/2026   1:39 PM                media
------        10/27/2026   1:32 AM             66 .env
-a----        10/27/2026   1:32 AM           2224 bai_lam.md

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
gc .\logs\travel.log | sls "ERROR"
gc .\logs\travel.log | sls "ERROR" > .\logs\daily_report.txt
gc .\logs\daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-08-28 08:30:34 [ERROR] Khong tim thay trang /tour-he (404)
2026-08-28 08:36:34 [ERROR] Giu cho that bai

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] Heading 1: tên dự án
- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
.\auto_report.ps1

```

### Kết quả hiển thị

```text
Dang loc log...
Hoan thanh!

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
(gc .\logs\travel.log | sls "ERROR").count

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
"=== TONG HOP LOG ===" > .\logs\tong_hop.txt
gc .\logs\travel.log | sls "WARNING" >> .\logs\tong_hop.txt
(gc .\logs\travel.log | sls "ERROR").count >> .\logs\tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG ===

2026-08-28 08:33:34 [WARNING] Thoi gian tai trang cham
2026-08-28 08:45:34 [WARNING] Thoi gian tai trang cham
2026-08-28 09:15:34 [WARNING] Thoi gian tai trang cham


6

```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/dat_tour_thang_8.xlsx`, không cần ghi vào đây.
