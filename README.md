<h1 align="center">💸 API CHUYỂN TIỀN VIETTELPAY & NGÂN HÀNG  💸</h1>
<p align="center"><b>Hỗ trợ đầy đủ các ngân hàng lớn · Dễ tích hợp · Giá rẻ cho sinh viên</b></p>

<p align="center">
  <img src="https://img.shields.io/badge/API%20Status-Online-brightgreen?style=for-the-badge&logo=datadog" />
  <img src="https://img.shields.io/badge/Giá-35k%2Ftháng-blueviolet?style=for-the-badge&logo=moneygram" />
  <a href="https://t.me/minhquan2006"><img src="https://img.shields.io/badge/Telegram-%40minhquan2006-2CA5E0?style=for-the-badge&logo=telegram" /></a>
</p>

---

## 🔥 TÍNH NĂNG NỔI BẬT

| ✅  | Tính năng          | Mô tả                                                           |
| -- | ------------------ | --------------------------------------------------------------- |
| 💸 | Chuyển tiền        | Gửi tiền từ **ViettelPay** hoặc ngân hàng bất kỳ                |
| 🏦 | Đa ngân hàng       | Hỗ trợ: VCB, MB, ACB, MSB, TPBank, BIDV, VPBank, Techcombank... |
| 🔐 | Token bảo mật      | Xác thực API bằng **token riêng**, hỗ trợ giới hạn IP           |
| 🧾 | Truy vấn giao dịch | Lọc theo trạng thái, thời gian, số tài khoản                    |
| 🔁 | Webhook realtime   | Nhận callback khi giao dịch thành công                          |

---

## 🏦 DANH SÁCH NGÂN HÀNG HỖ TRỢ

* ✅ **Vietcombank (VCB)**
* ✅ **MB Bank**
* ✅ **ACB - Á Châu**
* ✅ **MSB - Maritime**
* ✅ **TPBank**
* ✅ **BIDV**
* ✅ **Techcombank**
* ✅ **VPBank**
* ✅ **VietinBank**
* ✅ **SHB, VIB, OCB...**
* ✅ Và tất cả tài khoản liên kết qua **ViettelPay**

> 👉 Muốn tích hợp thêm ngân hàng khác? Liên hệ **[@minhquan2006](https://t.me/minhquan2006)**

---

## 🧪 CẤU TRÚC API MẪU

### 🔄 `POST /api/v1/transfer`

```json
{
  "bank": "VCB",
  "stk": "0123456789",
  "amount": 100000,
  "note": "Ung ho ban"
}
```

### 🔍 `GET /api/v1/transaction/:id`

```json
{
  "id": "TXN123456789",
  "status": "success",
  "bank": "VCB",
  "amount": 100000,
  "note": "Ung ho ban",
  "time": "2025-09-01T10:00:00Z"
}
```

### 🔔 Webhook callback mẫu

```json
{
  "event": "transaction.success",
  "id": "TXN123456789",
  "amount": 100000,
  "bank": "VCB",
  "time": "2025-09-01T10:00:05Z"
}
```

---

## 💳 BẢNG GIÁ

| Gói            | Mô tả                                   | Giá           |
| -------------- | --------------------------------------- | ------------- |
| **Student**    | API cơ bản (ViettelPay + bank phổ biến) | **35k/tháng** |
| **Pro**        | Hạn mức cao, hỗ trợ ưu tiên             | Liên hệ       |
| **Enterprise** | Tuỳ biến theo nhu cầu DN                | Liên hệ       |

---

## 📞 LIÊN HỆ & HỖ TRỢ

* 🌐 Website: **[SPAYMENT.NET](https://spayment.net)**
* 💬 Telegram: **[@minhquan2006](https://t.me/minhquan2006)**
* 🛠️ Nhận code **tool / web**, bán **API gốc**, tích hợp theo yêu cầu.

---

### ⚠️ Lưu ý pháp lý

API chỉ phục vụ cho **mục đích hợp pháp**. Người dùng chịu trách nhiệm khi sử dụng sai quy định pháp luật.

---

<div align="center">

🔗 [![Use SPAYMENT.NET](https://img.shields.io/badge/use-SPAYMENT.NET-blue?style=for-the-badge)](https://spayment.net)

</div>

---

### © 2025 · SPAYMENT.NET — Made for Developers
