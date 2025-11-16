 ## Nhiệm vụ
1. [x] Trong `TodosController`, định nghĩa các route: `@Get()`, `@Post()`, `@Put(':id')`, `@Delete(':id')`. ✅ 2025-11-15
2. [x] Trong `TodosService`, tạo các phương thức (ví dụ: `getAll()`, `create()`) và trả về dữ liệu giả (một mảng). ✅ 2025-11-15
3. [x] **Quan trọng:** "Tiêm" (Inject) `TodosService` vào `TodosController` qua `constructor`. Hiểu rõ tại sao làm vậy (tách biệt logic). ✅ 2025-11-15
4. [x] Dùng **Rest Client VSCode Plugin** để gọi thử tất cả các API vừa tạo. ✅ 2025-11-15
## Research thêm
- Payload của 1 POST/PUT api phải dùng anotation `@Body`
- Http code có thể set từ `HttpStatus.CREATE` `HttpStatus.OK`: 200 (OK) là báo tác vụ đó đã thực hiện xong, 201 (CREATED) là báo đã tạo xong, 202 (ACCEPTED) là báo đã tiếp nhận và đang xử lý
  ```