[English](README.md) | Tiếng Việt

# BankSystem - Luyện tập Unit Testing

Dự án C# minh họa quy trình unit testing chuyên nghiệp cho logic quản lý tài khoản ngân hàng.

## Công nghệ sử dụng

- **Ngôn ngữ:** C# (.NET Core)
- **Framework kiểm thử:** Microsoft Unit Test Framework (MSTest)
- **Công cụ:** Visual Studio Test Explorer

## Phương pháp kiểm thử

Dự án tập trung xác minh độ tin cậy của các giao dịch ghi nợ (debit) và ghi có (credit) thông qua quy trình kiểm thử lặp:

1. **Arrange-Act-Assert (AAA):** Mỗi test được cấu trúc theo 3 bước: chuẩn bị dữ liệu, thực hiện thao tác, và kiểm tra kết quả.
2. **Phát hiện lỗi (Bug Discovery):** Các unit test ban đầu được dùng để phát hiện và sửa lỗi logic trong việc tính toán số dư.
3. **Tái cấu trúc (Refactoring):** Cải thiện code sản xuất, sử dụng các hằng số (constants) mô tả rõ ràng cho thông báo lỗi sau khi các test ban đầu đã pass.

## Các kịch bản kiểm thử

- **Kiểm tra ghi nợ (Debit Validation):** Đảm bảo số tiền ghi nợ không được vượt quá số dư hiện tại.
- **Kiểm thử biên (Boundary Testing):** Kiểm thử với giá trị 0, số dương và số âm để đảm bảo tính ổn định của hệ thống.
- **Xử lý ngoại lệ (Exception Handling):** Xác minh `ArgumentOutOfRangeException` được ném ra kèm thông báo lỗi cụ thể khi đầu vào không hợp lệ.

## Cách chạy

1. Mở file `.sln` bằng **Visual Studio**.
2. Mở **Test Explorer** (`Test > Windows > Test Explorer`).
3. Nhấn **Run All** để chạy toàn bộ bộ test và xem kết quả xanh/đỏ (pass/fail).

---

*Dự án tuân theo các best practice của Microsoft trong việc viết và chạy unit test cho managed code.*
