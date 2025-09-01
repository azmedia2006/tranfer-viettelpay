<!-- Banner -->
<p align="center">
  <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExMmZ2bGx0dDNtMHZoc3BkdmN3eTI5NjN6eTRjMGk5cHJ1dWJlZ2NseSZlcD12MV9naWZzX3NlYXJjaCZjdD1n/HUkOv6BNWc1HO/giphy.gif" width="100%" alt="Banner" />
</p>

<h1 align="center">💳 API CHUYỂN TIỀN VIETTELPAY & NGÂN HÀNG - SPAYMENT.NET 💸</h1>

<p align="center">
  <b>Giải pháp Banking API cho sinh viên, tool dev, web tài chính</b><br/>
  <b>Giá rẻ - Tốc độ - Bảo mật - Dễ tích hợp</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/API%20STATUS-ONLINE-brightgreen?style=for-the-badge&logo=datadog" />
  <img src="https://img.shields.io/badge/Giá%20API-35K%2Ftháng-blueviolet?style=for-the-badge&logo=moneygram" />
  <img src="https://img.shields.io/badge/Telegram%20Support-%40minhquan2006-2CA5E0?style=for-the-badge&logo=telegram" />
</p>

---

## 🔥 TÍNH NĂNG NỔI BẬT

| ✅ Tính năng         | 💡 Mô tả nhanh |
|---------------------|----------------|
| 💸 Chuyển tiền       | ViettelPay → VCB, MB, MSB, ACB... |
| 🛡️ Token bảo mật     | Token riêng, hỗ trợ IP whitelist |
| 🧾 Lịch sử giao dịch | API query theo thời gian, trạng thái |
| 🔔 Webhook           | Nhận callback realtime khi hoàn thành |
| 📥 Dễ tích hợp       | Hỗ trợ POSTMAN, cURL, Python, PHP, Node.js |

---

## 📂 CẤU TRÚC API

### ➕ Chuyển khoản đơn
```http
POST /api/v1/transfer
Host: spayment.net
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json

{
  "bank": "VCB",
  "stk": "0123456789",
  "amount": 50000,
  "note": "Ung ho ban be"
}
