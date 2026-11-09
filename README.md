# BakeryShopManagement
Dưới đây là file `README.md` chuẩn, chuyên nghiệp, mô tả đúng kiến trúc MVC 3 tầng thuần Java và phân công công việc của nhóm 3 người theo đúng yêu cầu đề bài.

Bạn chỉ cần tạo một file tên là `README.md` nằm ngay ở thư mục gốc (root) của dự án trên GitHub và dán nội dung này vào:

```markdown
# 🥐 Bakery Management System (Hệ Thống Quản Lý Tiệm Bánh)

Hệ thống quản lý tiệm bánh theo mô hình kiến trúc MVC 3-tier (3 tầng) được lập trình bằng ngôn ngữ Java và cơ sở dữ liệu PostgreSQL. Dự án không sử dụng các ORM framework (như Hibernate/JPA) hay Spring Boot ở tầng Controller & Database.

---

## 📌 Kiến Trúc Hệ Thống (3-Tier MVC Architecture)

Hệ thống được thiết kế và chia làm 3 tầng rõ ràng:

1. **Database Layer (DAO - Data Access Object):** 
   - Quản lý kết nối PostgreSQL bằng JDBC.
   - Viết các câu lệnh SQL trực tiếp (PreparedStatement) để thực hiện các thao tác CRUD.
2. **Controller Layer (Business Logic):** 
   - Xử lý các quy tắc nghiệp vụ (tính lương, giảm giá, tính tổng tiền đơn hàng, kiểm tra tồn kho).
   - Tiếp nhận dữ liệu từ UI và tương tác với tầng Database.
3. **GUI / UI Layer (View):** 
   - Giao diện người dùng tương tác hiển thị dữ liệu và tiếp nhận yêu cầu từ phía người dùng.

---

## 👥 Phân Công Nhiệm Vụ Trong Nhóm (Group Members)

| Họ và tên | Vai trò | Trách nhiệm chính |
| :--- | :--- | :--- |
| **Thành viên 1** *(Nhóm trưởng)* | **Database Engine** | Thiết kế DB Schema, viết script PostgreSQL, xây dựng kết nối JDBC (`DatabaseConnection`), viết tất cả các lớp DAO (`ProductDAO`, `OrderDAO`, `StaffDAO`,...). |
| **Thành viên 2** | **Controller Layer** | Xây dựng các lớp xử lý nghiệp vụ (`AuthController`, `OrderController`, `InventoryController`, `PayrollController`, `CustomerController`). |
| **Thành viên 3** | **UI/UX (GUI Layer)** | Thiết kế giao diện người dùng (Màn hình đăng nhập, Bảng điều khiển chính, Quản lý đơn hàng, Quản lý kho, Quản lý nhân sự). |

---

## 📁 Cấu Trúc Thư Mục Dự Án (Project Structure)

```text
BakeryManagementSystem/
├── .gitignore
├── README.md
├── database_script.sql          # Script tạo bảng & chèn dữ liệu PostgreSQL
└── src/
    └── main/
        ├── java/
        │   └── com/bakery/
        │       ├── database/    # Tầng Database (DAO, JDBC Connection)
        │       ├── model/       # Tầng Model / Entities (Person, Product, Order,...)
        │       ├── controller/  # Tầng Controller (Business Logic)
        │       └── view/        # Tầng GUI / UI
        └── resources/           # File cấu hình (db.properties, icons, images)

```

---

## 🛠️ Công Nghệ Sử Dụng (Tech Stack)

* **Ngôn ngữ:** Java (JDK 17+)
* **Cơ sở dữ liệu:** PostgreSQL
* **Kết nối DB:** Java Database Connectivity (JDBC)
* **Giao diện:** Swing / JavaFX / Web
* **Công cụ quản lý mã nguồn:** Git & GitHub

---

## 🚀 Hướng Dẫn Cài Đặt & Chạy Dự Án (Setup Instructions)

### 1. Yêu cầu môi trường

* Cài đặt Java Development Kit (JDK 17 trở lên).
* Cài đặt hệ quản trị CSDL PostgreSQL và pgAdmin.

### 2. Thiết lập Database

1. Mở **pgAdmin** hoặc PostgreSQL CLI.
2. Tạo một cơ sở dữ liệu mới tên là `bakery_db`.
3. Chạy file `database_script.sql` ở thư mục gốc để khởi tạo các bảng và dữ liệu mẫu.

### 3. Cấu hình kết nối Java

Chỉnh sửa thông tin `URL`, `USER`, `PASSWORD` trong file:
`src/main/java/com/bakery/database/DatabaseConnection.java` phù hợp với tài khoản PostgreSQL local của bạn.

### 4. Chạy ứng dụng

Mở dự án trên IDE (IntelliJ IDEA / Eclipse / NetBeans) và khởi chạy file:
`src/main/java/com/bakery/view/MainDashboard.java` (hoặc `LoginFrame.java`).

---

## 🌿 Quy Trình Làm Việc Với Git (Git Workflow)

1. Không push code trực tiếp lên nhánh `main`.
2. Mỗi tính năng mới tạo một nhánh riêng từ `main`:
```bash
git checkout main
git pull origin main
git checkout -b feature/ten-tinh-nang

```


3. Sau khi hoàn thành, tạo **Pull Request (PR)** trên GitHub để Trưởng nhóm review và merge vào `main`.

```

```
