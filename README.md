# MakeAI SEB

**Ứng dụng trình duyệt thi an toàn dành cho các bài kiểm tra trên [MakeAI](https://edu.makeai.vn).**

MakeAI SEB giúp mở bài thi trong môi trường được kiểm soát, hạn chế truy cập các ứng dụng và tài nguyên không được phép
trong thời gian làm bài. MakeAI SEB được phát triển dựa trên nền tảng [Safe Exam Browser](https://safeexambrowser.org) (SEB)
và được tùy chỉnh cho hệ thống thi của MakeAI.

Phiên bản mới nhất: **1.0.3** · Trang tải chính thức: https://github.com/duytrinhmakeai/seb/releases

---

## 01 · Tải ứng dụng

Chọn bộ cài đặt Windows phù hợp:

| Bộ cài | Dành cho | Tải về |
|---|---|---|
| **MakeAI SEB** | Máy thi của sinh viên: chỉ có ứng dụng thi | [setup.zip (196 MB)](https://github.com/duytrinhmakeai/seb/releases/download/v1.0.3/MakeAISEB-1.0.3.0-x64-setup.zip) · [.msi (197 MB)](https://github.com/duytrinhmakeai/seb/releases/download/v1.0.3/MakeAISEB-1.0.3.0-x64.msi) |
| **MakeAI SEB Full** | Giáo viên, kỹ thuật viên: thêm công cụ cấu hình và công cụ khôi phục | [setup.zip (197 MB)](https://github.com/duytrinhmakeai/seb/releases/download/v1.0.3/MakeAISEB-1.0.3.0-x64-Full-setup.zip) · [.msi (198 MB)](https://github.com/duytrinhmakeai/seb/releases/download/v1.0.3/MakeAISEB-1.0.3.0-x64-Full.msi) |

Tài liệu đi kèm: [Hướng dẫn cài đặt](https://github.com/duytrinhmakeai/seb/releases/download/v1.0.3/HUONG-DAN-CAI-DAT.txt) ·
[Hướng dẫn cài đặt (bản Full)](https://github.com/duytrinhmakeai/seb/releases/download/v1.0.3/HUONG-DAN-CAI-DAT-Full.txt) ·
[Thay đổi trong phiên bản](https://github.com/duytrinhmakeai/seb/releases/download/v1.0.3/THAY-DOI.txt) ·
[SHA256SUMS.txt](https://github.com/duytrinhmakeai/seb/releases/download/v1.0.3/SHA256SUMS.txt)

## 02 · Cài đặt

1. Tải file `.msi`, hoặc tải file `.zip` rồi giải nén.
2. Mở file `MakeAISEB-1.0.3.0-x64.msi` (hoặc `MakeAISEB-1.0.3.0-x64-Full.msi`).
3. Đồng ý điều khoản, chọn **Install** và xác nhận quyền quản trị.
4. Khởi động lại máy nếu hệ điều hành yêu cầu.

> Nếu Windows hiển thị cảnh báo SmartScreen, chọn **More info** rồi **Run anyway**: bộ cài hiện chưa được ký số.
> Cài bản mới đè lên bản cũ sẽ tự nâng cấp, không cần gỡ trước. Cài bộ thường đè lên bộ Full (hoặc ngược lại) sẽ tự thay thế.

Cài hàng loạt (quản trị mạng, quyền Administrator): `msiexec /i MakeAISEB-1.0.3.0-x64.msi /qn`

## 03 · Bắt đầu bài thi

1. Đăng nhập MakeAI và mở bài thi được yêu cầu dùng SEB.
2. Nhấn **Chạy MakeAI SEB** trên trang hướng dẫn của bài thi, hoặc mở file cấu hình `.seb` do giáo viên gửi.
3. Cho phép trình duyệt mở ứng dụng MakeAI SEB khi được hỏi.

---

## Tính năng

| | |
|---|---|
| **Chế độ thi tập trung** | Giới hạn việc chuyển sang ứng dụng và tài nguyên khác theo cấu hình của kỳ thi. |
| **Mở bài thi nhanh** | Khởi động bài thi bằng file cấu hình hoặc nút Chạy MakeAI SEB trên Moodle. |
| **Hỗ trợ giám sát** | Hỗ trợ camera và màn hình khi kỳ thi được cấu hình yêu cầu giám sát. |
| **Dịch vụ bảo mật** | Dịch vụ MakeAI SEB tự đưa máy về trạng thái bình thường sau khi thi; bản Full có thêm công cụ khôi phục. |
| **Tiếng Việt** | Giao diện tiếng Việt mặc định; công cụ cấu hình và công cụ khôi phục có thêm tiếng Anh. |

## Yêu cầu máy tính

- Windows 10 phiên bản 1903 trở lên hoặc Windows 11, 64-bit.
- [Microsoft Visual C++ Redistributable 2015–2022 (x64)](https://aka.ms/vs/17/release/vc_redist.x64.exe).
- Webcam nếu kỳ thi yêu cầu giám sát camera.
- Nên chỉ sử dụng một màn hình trong thời gian làm bài.

## Kiểm tra toàn vẹn (SHA-256)

Đối chiếu mã dưới đây sau khi tải file để kiểm tra file không bị thay đổi
(PowerShell: `Get-FileHash <tên file> -Algorithm SHA256`).

| Tệp | SHA-256 |
|---|---|
| `MakeAISEB-1.0.3.0-x64-setup.zip` | `c043362ba39a2fd5222491e669d9c122eef01916369747c6c6af810d4cd84b9c` |
| `MakeAISEB-1.0.3.0-x64.msi` | `f7f0ad4afa4bd3269ee84425ca5862c902c2b6e26822f640e2f5be4356df0e78` |
| `MakeAISEB-1.0.3.0-x64-Full-setup.zip` | `b28e6deff2e8e7b334789e4fac27eddcb43a4aee3117ea22a71e4c6128023a06` |
| `MakeAISEB-1.0.3.0-x64-Full.msi` | `dc65d17c63a337794b60657be2b1cdd9292bcaa20b9477a866865c4121d95259` |

## Lưu ý trước khi thi

- Hãy cài MakeAI SEB trước giờ thi và kiểm tra ứng dụng trên đúng máy sẽ làm bài.
- Đóng các ứng dụng khác trước khi bắt đầu bài thi (điều khiển từ xa, chat, quay màn hình…).
- Nếu ứng dụng báo thiếu dịch vụ bảo mật hoặc không thể khởi động, hãy liên hệ quản trị viên.

---

**MakeAI Education** · *Learn AI today. Make AI tomorrow.* · [edu.makeai.vn](https://edu.makeai.vn) ·
[Facebook](https://www.facebook.com/AIhubacademy)

Safe Exam Browser © ETH Zürich, IT Services, phát hành theo [Mozilla Public License 2.0](https://mozilla.org/MPL/2.0/).
