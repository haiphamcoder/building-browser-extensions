# Hướng dẫn Đóng góp

Cảm ơn bạn đã quan tâm đến việc đóng góp cho dự án này! Tài liệu này sẽ hướng dẫn bạn cách đóng góp một cách hiệu quả.

## Tổng quan

Dự án này tuân theo các chuẩn sau:

- **[Conventional Commits](https://www.conventionalcommits.org/)** - Định dạng commit message chuẩn
- **[Semantic Versioning](https://semver.org/)** - Quản lý phiên bản theo ngữ nghĩa
- **[Conventional Branch](https://conventional-branch.github.io/)** - Quy ước đặt tên branch

## Conventional Commits

### Ngôn ngữ

**Tất cả commit message phải được viết bằng tiếng Anh.**

### Định dạng Commit Message

Mỗi commit message phải tuân theo định dạng sau:

```text
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Các loại Type

- `feat`: Thêm tính năng mới
- `fix`: Sửa lỗi
- `docs`: Thay đổi tài liệu
- `style`: Thay đổi định dạng (không ảnh hưởng đến logic)
- `refactor`: Refactor code (không thêm tính năng mới, không sửa lỗi)
- `perf`: Cải thiện hiệu suất
- `test`: Thêm hoặc sửa test
- `build`: Thay đổi hệ thống build hoặc dependencies
- `ci`: Thay đổi CI/CD configuration
- `chore`: Các thay đổi khác (không ảnh hưởng đến code)
- `revert`: Revert một commit trước đó

### Ví dụ

```bash
feat(extension): add automatic bookmark saving feature

fix(popup): fix empty list display issue

docs: update installation guide

refactor(background): optimize message passing handling
```

### Scope (Tùy chọn)

Scope mô tả phần nào của codebase bị ảnh hưởng. Ví dụ:

- `extension`, `popup`, `background`, `content`, `options`
- Tên module hoặc component cụ thể

### Breaking Changes

Nếu commit có breaking change, thêm `!` sau type và scope, và mô tả trong footer:

```text
feat(api)!: change response structure

BREAKING CHANGE: Response format changed from object to array
```

## Semantic Versioning

Dự án sử dụng [Semantic Versioning](https://semver.org/) với định dạng: `MAJOR.MINOR.PATCH`

### Quy tắc Versioning

- **MAJOR**: Tăng khi có breaking changes
- **MINOR**: Tăng khi thêm tính năng mới (backward compatible)
- **PATCH**: Tăng khi sửa lỗi (backward compatible)

### Ví dụ về Versioning

- `1.0.0` → `1.0.1`: Sửa lỗi nhỏ
- `1.0.1` → `1.1.0`: Thêm tính năng mới
- `1.1.0` → `2.0.0`: Breaking change

### Mapping với Conventional Commits

- `feat`: Tăng MINOR version
- `fix`: Tăng PATCH version
- `BREAKING CHANGE`: Tăng MAJOR version

## Conventional Branch

### Định dạng Branch Name

```text
<type>/<description>
```

### Các loại Branch Type

- `feature`: Tính năng mới
- `fix`: Sửa lỗi
- `hotfix`: Sửa lỗi khẩn cấp (từ production)
- `docs`: Cập nhật tài liệu
- `refactor`: Refactor code
- `test`: Thêm hoặc cải thiện test
- `chore`: Các thay đổi khác

### Ví dụ về Branch Name

```bash
feature/add-bookmark-sync
fix/popup-display-issue
docs/update-installation-guide
refactor/background-script
hotfix/critical-security-patch
```

### Quy tắc về Branch

- Sử dụng kebab-case (chữ thường, dấu gạch ngang)
- Mô tả ngắn gọn, rõ ràng
- Tránh ký tự đặc biệt và khoảng trắng

## Quy trình Đóng góp

### 1. Fork và Clone

```bash
# Fork repository trên GitHub
# Sau đó clone về máy
git clone https://github.com/your-username/building-browser-extensions.git
cd building-browser-extensions
```

### 2. Tạo Branch

```bash
# Tạo branch mới từ main/master
git checkout -b feature/your-feature-name
# hoặc
git checkout -b fix/your-bug-fix
```

### 3. Thực hiện Thay đổi

- Viết code rõ ràng, dễ đọc
- Thêm comment khi cần thiết
- Tuân theo coding style của dự án
- Viết test cho tính năng mới hoặc sửa lỗi

### 4. Commit Changes

```bash
# Stage các file đã thay đổi
git add .

# Commit với message theo Conventional Commits (phải viết bằng tiếng Anh)
git commit -m "feat(extension): add new feature"
```

### 5. Push và Tạo Pull Request

```bash
# Push branch lên remote
git push origin feature/your-feature-name
```

Sau đó tạo Pull Request trên GitHub với:

- Tiêu đề mô tả rõ ràng thay đổi
- Mô tả chi tiết về những gì đã thay đổi và lý do
- Liên kết đến issue liên quan (nếu có)

### 6. Review Process

- Maintainer sẽ review code của bạn
- Có thể yêu cầu thay đổi hoặc cải thiện
- Sau khi được approve, code sẽ được merge vào main branch

## Code Style

- Tuân theo coding conventions của ngôn ngữ được sử dụng
- Giữ code đơn giản và dễ hiểu
- Thêm comment cho logic phức tạp
- Đảm bảo code đã được test trước khi commit

## Testing

- Viết test cho mọi tính năng mới
- Đảm bảo tất cả test đều pass trước khi tạo PR
- Test trên các trình duyệt khác nhau (nếu là browser extension)

## Câu hỏi?

Nếu bạn có bất kỳ câu hỏi nào, vui lòng:

- Mở một issue trên GitHub
- Liên hệ với maintainer

Cảm ơn bạn đã đóng góp! 🎉
