## Nhiệm vụ
1. [x] Ôn lại **TypeScript Decorators** (`@`) - đây là chìa khóa. ✅ 2025-11-15
2. [x] Cài đặt Nest CLI (`npm i -g @nestjs/cli`). ✅ 2025-11-15
3. [x] Khởi tạo dự án: `nest new my-api` ✅ 2025-11-15
4. [x] Phân tích luồng (flow): `main.ts` -> `AppModule` -> `AppController` -> `AppService`. ✅ 2025-11-15
5. [x] Tạo một `TodosModule` (bằng CLI: `nest g module todos`). ✅ 2025-11-15
6. [x] Tạo `TodosController` và `TodosService` ( `nest g controller todos`, `nest g service todos`). ✅ 2025-11-15
## Research thêm
- Understand AppModule, AppController, AppService
	- AppModule: Nơi khai báo các controllers, services, modules
	- AppController: Nơi tiếp nhận request và chuyển info cho Service sử lý (Service sẽ auto inject vào constructor của Controller)
	- AppService: Nơi sẽ trực tiếp làm các tác vụ liên quan tới business logic, DB
- Có thể lấy params Query từ `@Query`, headers từ `@Headers`, set header item bằng `@Header`
	- `@Query()`, `@Body()`, `@Param()`, `@Headers()` là các **Parameter Decorators** (Decorator cho Tham số).
	- `@Get()`, `@Post()`, `@UseGuards()`, `@Header()` là các **Method Decorators** (Decorator cho Phương thức).
- Methods của Controller ko cần nhất thiết phải là async, và nếu có là async thì nest.js có cơ chế tự handle promise
- Chúng ta có thể dùng `host` prop trong `@Controller` để làm host routing -> Tức là chỉ cho 1 số host name access our apis
- Chúng ta dùng 301 (có cache browser) và 302 để redirect từ Server giúp Google-bot đọc hiểu nhanh và đỡ tốn effort của SPA load bundle để redirect