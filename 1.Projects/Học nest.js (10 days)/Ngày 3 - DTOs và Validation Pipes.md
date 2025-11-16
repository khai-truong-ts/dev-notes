1. [x] Cài đặt `class-validator` và `class-transformer`. ✅ 2025-11-16
2. [x] Kích hoạt `ValidationPipe` toàn cục trong `main.ts`. ✅ 2025-11-16
3. [x] Tạo một file `dto/create-todo.dto.ts`. ✅ 2025-11-16
4. [x] Dùng `class-validator` decorators (ví dụ: `@IsString()`, `@IsNotEmpty()`) trong DTO. ✅ 2025-11-16
5. [x] Áp dụng DTO này vào `body` của route `@Post()` trong `TodosController` bằng decorator `@Body()`. ✅ 2025-11-16
6. [x] Thử gửi data sai từ Postman và xem Nest tự động báo lỗi 400. ✅ 2025-11-16
## Research thêm
- Param từ URL đa số là string nên cần nhớ phải parse sang number
- 204: Đã thực hiện xong và ko có gì để trả về
- Các Response trả về tương ứng với GET, POST, PUT, DELETE

|**Method**|**Ý nghĩa**|**Status Code (Thành công)**|**Nội dung (Body) trả về**|
|---|---|---|---|
|**`GET`**|Lấy dữ liệu|**`200 OK`**|Dữ liệu (ví dụ: `[...]` hoặc `{...}`)|
|**`POST`**|Tạo mới|**`201 Created`**|Đối tượng vừa được tạo (ví dụ: `{ "id": 3, ... }`)|
|**`PUT`/`PATCH`**|Cập nhật|**`200 OK`**|Đối tượng _sau khi_ đã cập nhật|
|**`DELETE`**|Xóa|**`204 No Content`**|**(Không có nội dung)**|

- Để customize 1 exception ta khai báo 1 Filter, gồm 2 steps
	- Step 1: implement Exception Filter
		- Chỗ này lưu ý là phải chỉ định rõ dòng này trong hàm catch() của interface ExceptionFilter `const ctx = host.switchToHttp();` để Nest.js biết mình đang muốn bắt những exception từ web nếu ko sẽ bị crash
	- Step 2: app.useGlobalFilters(new YourFilter()) 