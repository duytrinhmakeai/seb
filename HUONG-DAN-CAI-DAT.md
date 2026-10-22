# Hướng dẫn cài đặt MakeAI SEB

MakeAI SEB là trình duyệt thi an toàn: khóa máy trong giờ thi, chỉ cho mở trang bài thi và, nếu kỳ thi yêu cầu,
chụp màn hình và ảnh webcam để giám sát.

[← Trang giới thiệu](README.md) · [Trang tải chính thức](https://github.com/duytrinhmakeai/seb/releases)

---

## 1. Chọn bộ cài

| Bộ cài | Dành cho | Trong Start Menu sẽ có |
|---|---|---|
| `MakeAISEB-<phiên bản>-x64.msi` | Máy thi của sinh viên | MakeAI SEB |
| `MakeAISEB-<phiên bản>-x64-Full.msi` | Giáo viên, kỹ thuật viên | MakeAI SEB, MakeAI SEB Configuration Tool (công cụ cấu hình), MakeAI SEB Reset Utility (công cụ khôi phục) |

Mỗi bộ có dạng `.msi` (chạy trực tiếp) hoặc `setup.zip` (giải nén ra được file `.msi`).
Cài bộ này đè lên bộ kia sẽ tự thay thế; cài bản mới đè lên bản cũ sẽ tự nâng cấp. Không cần gỡ trước.

## 2. Yêu cầu máy tính

- Windows 10 (bản 1903 trở lên) hoặc Windows 11, 64-bit.
- Microsoft Visual C++ Redistributable 2015–2022 (x64). Nếu máy chưa có, tải và cài từ trang của Microsoft:
  https://aka.ms/vs/17/release/vc_redist.x64.exe
- Webcam nếu kỳ thi có giám sát camera.
- Chỉ 1 màn hình: rút màn hình phụ hoặc máy chiếu trước khi thi.

## 3. Cài đặt

1. Tải bộ cài từ [trang tải chính thức](https://github.com/duytrinhmakeai/seb/releases) (nếu tải file `.zip` thì giải nén ra).
2. Nhấp đúp file `.msi`.
3. Đồng ý điều khoản, bấm **Install**. Windows hỏi quyền quản trị (UAC): chọn **Yes**.
   Cần tài khoản có quyền Administrator trên máy.
4. Cài xong, mở MakeAI SEB từ Start Menu hoặc bằng file cấu hình `.seb` của bài thi.

> Nếu Windows hiện **"Windows protected your PC"** (SmartScreen): bấm **More info** → **Run anyway**.
> Bộ cài hiện chưa được ký số, cảnh báo này là bình thường.

**Cài hàng loạt** (dành cho quản trị mạng), chạy với quyền Administrator:

```
msiexec /i MakeAISEB-1.0.3.0-x64.msi /qn
```

**Kiểm tra tính toàn vẹn** của file đã tải (PowerShell), rồi đối chiếu với `SHA256SUMS.txt` trong trang tải:

```
Get-FileHash .\MakeAISEB-1.0.3.0-x64.msi -Algorithm SHA256
```

## 4. Vào thi

**Cách 1 – File cấu hình `.seb`** (do giáo viên hoặc nhà trường gửi): nhấp đúp file `.seb`, MakeAI SEB tự mở và vào bài thi.

**Cách 2 – Từ trang bài thi trên MakeAI (Moodle):** đăng nhập, mở bài thi, bấm **Chạy MakeAI SEB** (hoặc
"Launch Safe Exam Browser" / "Download configuration" rồi nhấp đúp file vừa tải). Cho phép trình duyệt mở ứng dụng khi được hỏi.

**Trong giờ thi:**

- Máy chuyển sang màn hình thi riêng, không chuyển được sang ứng dụng khác.
- Nếu được hỏi đồng ý giám sát màn hình hoặc camera, bấm đồng ý để vào thi.
- Tắt trước các ứng dụng điều khiển từ xa, chat, quay màn hình (TeamViewer, UltraViewer, AnyDesk, Teams, Discord, OBS…).
  Nếu MakeAI SEB yêu cầu tắt, chọn đồng ý.
- Thoát: bấm nút thoát trên thanh tác vụ của MakeAI SEB (cần mật khẩu thoát do giám thị cung cấp)
  hoặc nộp bài theo hướng dẫn của bài thi.

## 5. Khi gặp sự cố

| Sự cố | Cách xử lý |
|---|---|
| Máy không trở lại bình thường sau khi thoát (mất Task Manager, không đăng xuất được…) | Khởi động lại máy hoặc đăng xuất rồi đăng nhập lại: dịch vụ MakeAI SEB tự khôi phục. Nếu vẫn chưa được: kỹ thuật viên cài bộ Full và chạy **MakeAI SEB Reset Utility** (Start Menu, quyền Administrator). |
| Báo lỗi "dịch vụ MakeAI SEB không chạy" | Cài lại bằng file `.msi`. |
| Báo lỗi màn hình | Rút màn hình phụ, tắt chế độ mở rộng (**Win + P** → **PC screen only**). |
| Cần gửi nhật ký lỗi cho bộ phận hỗ trợ | Nén thư mục `%LocalAppData%\SafeExamBrowser\Logs` (gõ đường dẫn này vào thanh địa chỉ của File Explorer). |

**Công cụ của bộ Full** (giao diện tiếng Việt mặc định, đổi sang tiếng Anh ở menu **Ngôn ngữ / Language**):

- **MakeAI SEB Configuration Tool:** tạo và sửa file cấu hình `.seb` (trang được mở, mật khẩu thoát, khóa phím, giám sát…).
- **MakeAI SEB Reset Utility:** đưa các thiết lập Windows mà MakeAI SEB đã thay đổi về trạng thái bình thường.

## 6. Gỡ cài đặt

**Settings** → **Apps** → **Installed apps** → **MakeAI SEB (x64)** hoặc **MakeAI SEB Full (x64)** → **Uninstall**.

---

**MakeAI Education** · [edu.makeai.vn](https://edu.makeai.vn)
