# ĐỒ ÁN CHALLENGE 4: BUILD A DECENTRALIZED EXCHANGE (DEX)

## Introduction

Dự án này là lời giải cho **Challenge 4: Build a DEX** thuộc hệ sinh thái **SpeedRunEthereum**.  
Bài tập tập trung vào việc xây dựng một **sàn giao dịch phi tập trung (Decentralized Exchange)** cho phép người dùng **swap giữa ETH và ERC20 Token** mà không cần bên trung gian.

DEX hoạt động dựa trên cơ chế **pool thanh khoản (Liquidity Pool)**, trong đó Smart Contract nắm giữ dự trữ ETH và Token để xác định giá giao dịch.

### Các tính năng đã hoàn thành
- **Add Liquidity:** Cho phép người dùng gửi ETH và Token vào pool để cung cấp thanh khoản.
- **Remove Liquidity:** Cho phép người dùng rút lại tài sản dựa trên tỷ lệ đóng góp.
- **Swap ETH → Token:** Người dùng có thể đổi ETH lấy Token theo công thức định giá của pool.
- **Swap Token → ETH:** Người dùng có thể đổi Token lấy ETH.
- **Liquidity Token:** Phát hành token đại diện cho phần sở hữu của người cung cấp thanh khoản.
- **Cơ chế định giá tự động:** Giá token thay đổi dựa trên tỷ lệ dự trữ trong pool.

---


## Yêu cầu môi trường 

Để chạy dự án, máy tính cần cài đặt:
- **NodeJS** (v16.x hoặc mới hơn)
- **Yarn** (khuyến nghị)
- **Git**
- **Trình duyệt Chrome**
- **Ví MetaMask**

---

## Hướng dẫn chạy 

Mở **3 cửa sổ Terminal riêng biệt** và chạy các lệnh sau theo đúng thứ tự.

### Bước 1: Cài đặt thư viện và chạy Blockchain cục bộ (Hardhat Node)
```bash
yarn install
yarn chain
```
### Bước 3: Triển khai Smart Contract lên Localhost
```bash
yarn deploy
```
### Bước 4: Khởi chạy giao diện người dùng (Frontend)
```bash
yarn start
```
### Bước 5: Truy cập: http://localhost:3000 để tương tác.

## ⚙️ Cấu hình mạng & Triển khai (Deployment)

---

### Môi trường (Local)

- Dự án được cấu hình mặc định chạy trên **Hardhat local blockchain**.
- Cấu hình này nằm trong file `scaffold.config.ts`:

```ts
targetNetworks: [chains.hardhat]




