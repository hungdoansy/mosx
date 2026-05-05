# Mosx

<p align="center">
  <img src="icon.png" width="64" height="64" alt="Mosx" />
</p>

Ứng dụng quản lý Messenger đa tài khoản (Multi-Account) cho macOS — xây dựng trên Electron + Chromium.

---

## Tính năng

- **Đa tài khoản** — Đăng nhập và sử dụng nhiều tài khoản Messenger cùng lúc, chuyển đổi 1 click qua Sidebar.
- **Cô lập dữ liệu** — Mỗi tài khoản chạy trên Session riêng biệt (Cookies, Cache, LocalStorage tách biệt hoàn toàn).
- **Bảo mật** — Chặn "Đã xem" (Read Receipts) và "Đang nhập" (Typing Indicator).
- **Thông báo & Badge** — Nhận thông báo và số tin nhắn chưa đọc cho từng tài khoản.
- **Auto-Fetch Avatar** — Tự động lấy ảnh đại diện từ Messenger.
- **Khóa ứng dụng (PIN)** — Bảo vệ ứng dụng bằng mã PIN.
- **Dark/Light mode** — Hỗ trợ chuyển đổi giao diện.

## Yêu cầu

- [Node.js](https://nodejs.org/) v24+
- [pnpm](https://pnpm.io/) v9.15+

## Cài đặt & Chạy

```bash
pnpm install
pnpm start
```

## Build (macOS)

```bash
# Tạo file .dmg
pnpm run build

# Hoặc chỉ build dmg
pnpm run build:dmg
```

File thành phẩm xuất hiện trong thư mục `dist/`.

## Cấu trúc dự án

| File               | Chức năng                                             |
| ------------------ | ----------------------------------------------------- |
| `main.js`          | Quản lý vòng đời App, Partitions, BrowserView, IPC.   |
| `renderer.js`      | Logic Sidebar đa tài khoản, Modal UI.                 |
| `index.html`       | Sidebar trái (nick) & Sidebar phải (công cụ) & Modal. |
| `preload.js`       | Cầu nối bảo mật giữa DOM và Backend.                  |
| `custom_style.css` | Giao diện Dark Glass và ẩn quảng cáo Facebook.        |

## License

MIT
