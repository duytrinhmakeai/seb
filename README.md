# MakeAI SEB

Trình duyệt thi an toàn của MakeAI (dựa trên Safe Exam Browser cho Windows): khóa máy trong giờ thi, chỉ cho mở trang
bài thi và, nếu kỳ thi yêu cầu, giám sát màn hình và webcam qua MakeAI SEB Server.

## Tải về

Xem mục [Releases](https://github.com/duytrinhmakeai/seb/releases). Có 2 bộ cài:

| Tệp | Dành cho |
|---|---|
| `MakeAISEB-<phiên bản>-x64-setup.zip` / `.msi` | Máy thi của sinh viên: chỉ có MakeAI SEB |
| `MakeAISEB-<phiên bản>-x64-Full-setup.zip` / `-Full.msi` | Giáo viên, kỹ thuật viên: thêm công cụ cấu hình và công cụ khôi phục |

Gói `setup.zip` gồm bộ cài `.msi`, hướng dẫn cài đặt và danh sách thay đổi. Kiểm tra tính toàn vẹn bằng `SHA256SUMS.txt`.
Cài bản mới đè lên bản cũ sẽ tự nâng cấp, không cần gỡ trước.

Trang tải chính thức: https://makeai.edu.vn/makeaiseb/

## Yêu cầu

- Windows 10 (1903 trở lên) hoặc Windows 11, 64-bit.
- Microsoft Visual C++ Redistributable 2015-2022 (x64): https://aka.ms/vs/17/release/vc_redist.x64.exe
- Bộ cài chưa được ký số: nếu Windows SmartScreen cảnh báo, chọn "More info" → "Run anyway".

## Giấy phép

Safe Exam Browser được phát hành theo Mozilla Public License 2.0 (© ETH Zürich, IT Services).
