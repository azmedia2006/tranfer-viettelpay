<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SPAYMENT.NET - API Chuyển Tiền ViettelPay & Ngân Hàng</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #6a11cb;
            --secondary: #2575fc;
            --accent: #00c9ff;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #28a745;
            --danger: #dc3545;
            --warning: #ffc107;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            margin-bottom: 20px;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
            margin: 20px 0;
        }
        
        .badge {
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 15px;
            border-radius: 50px;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 5px;
        }
        
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }
        
        .feature-card {
            background: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        .feature-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .banks-section {
            background: white;
            border-radius: 15px;
            padding: 30px;
            margin: 40px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 30px;
            color: var(--primary);
            font-size: 1.8rem;
        }
        
        .banks-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 20px;
        }
        
        .bank-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 15px;
            border-radius: 10px;
            background: var(--light);
            transition: all 0.3s ease;
        }
        
        .bank-item:hover {
            background: #e9ecef;
            transform: scale(1.05);
        }
        
        .bank-icon {
            font-size: 2rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .api-demo {
            background: white;
            border-radius: 15px;
            padding: 30px;
            margin: 40px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }
        
        .code-block {
            background: #2d2d2d;
            color: #f8f8f2;
            padding: 20px;
            border-radius: 8px;
            overflow-x: auto;
            margin: 20px 0;
            font-family: 'Fira Code', monospace;
        }
        
        .code-key {
            color: #ff79c6;
        }
        
        .code-string {
            color: #f1fa8c;
        }
        
        .code-number {
            color: #bd93f9;
        }
        
        .code-comment {
            color: #6272a4;
        }
        
        .cta {
            text-align: center;
            padding: 50px 20px;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            border-radius: 15px;
            margin: 40px 0;
        }
        
        .cta-title {
            font-size: 2rem;
            margin-bottom: 20px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--accent);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s ease;
            margin: 10px;
        }
        
        .btn:hover {
            background: #0099cc;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        footer {
            text-align: center;
            padding: 30px 0;
            color: #6c757d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .features {
                grid-template-columns: 1fr;
            }
            
            .banks-grid {
                grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>💸 API CHUYỂN TIỀN VIETTELPAY & NGÂN HÀNG</h1>
            <p class="subtitle">Hỗ trợ đầy đủ các ngân hàng lớn - Dễ tích hợp - Giá rẻ cho sinh viên</p>
            
            <div class="badges">
                <div class="badge">
                    <i class="fas fa-circle-check"></i> API Online
                </div>
                <div class="badge">
                    <i class="fas fa-tag"></i> Chỉ 35k/tháng
                </div>
                <div class="badge">
                    <i class="fab fa-telegram"></i> Telegram: @minhquan2006
                </div>
            </div>
        </header>
        
        <div class="features">
            <div class="feature-card">
                <div class="feature-icon">💸</div>
                <h3 class="feature-title">Chuyển Tiền</h3>
                <p>Gửi tiền từ ViettelPay hoặc ngân hàng bất kỳ một cách nhanh chóng và an toàn.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🏦</div>
                <h3 class="feature-title">Đa Ngân Hàng</h3>
                <p>Hỗ trợ hầu hết các ngân hàng lớn tại Việt Nam với tỷ lệ thành công cao.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🔐</div>
                <h3 class="feature-title">Bảo Mật</h3>
                <p>Xác thực API bằng token riêng, hỗ trợ giới hạn IP để bảo vệ tài khoản của bạn.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🧾</div>
                <h3 class="feature-title">Truy Vấn GD</h3>
                <p>Dễ dàng lọc giao dịch theo trạng thái, thời gian, số tài khoản và nhiều tiêu chí khác.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">🔁</div>
                <h3 class="feature-title">Webhook</h3>
                <p>Tự động nhận kết quả khi giao dịch thành công thông qua webhook URL của bạn.</p>
            </div>
            
            <div class="feature-card">
                <div class="feature-icon">📚</div>
                <h3 class="feature-title">Tài Liệu</h3>
                <p>Tài liệu API chi tiết, dễ hiểu với các ví dụ code cho nhiều ngôn ngữ lập trình.</p>
            </div>
        </div>
        
        <div class="banks-section">
            <h2 class="section-title">🏦 DANH SÁCH NGÂN HÀNG HỖ TRỢ</h2>
            
            <div class="banks-grid">
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>Vietcombank</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>MB Bank</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>ACB</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>MSB</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>TPBank</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>BIDV</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>Techcombank</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>VPBank</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>VietinBank</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>SHB</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>VIB</span>
                </div>
                
                <div class="bank-item">
                    <div class="bank-icon"><i class="fas fa-building-columns"></i></div>
                    <span>OCB</span>
                </div>
            </div>
            
            <p style="text-align: center; margin-top: 20px;">
                <strong>Và tất cả tài khoản liên kết qua ViettelPay</strong>
            </p>
            
            <p style="text-align: center; margin-top: 10px; font-style: italic;">
                👉 Gửi yêu cầu tích hợp thêm ngân hàng khác qua Telegram @minhquan2006
            </p>
        </div>
        
        <div class="api-demo">
            <h2 class="section-title">🧪 CẤU TRÚC API MẪU</h2>
            
            <h3>🔄 POST <code>/api/v1/transfer</code></h3>
            
            <div class="code-block">
                <pre><code>{
  "<span class="code-key">bank</span>": "<span class="code-string">VCB</span>",
  "<span class="code-key">stk</span>": "<span class="code-string">0123456789</span>",
  "<span class="code-key">amount</span>": <span class="code-number">100000</span>,
  "<span class="code-key">note</span>": "<span class="code-string">Ung ho ban</span>"
}</code></pre>
            </div>
            
            <h3>📨 POST <code>/api/v1/transaction/query</code></h3>
            
            <div class="code-block">
                <pre><code>{
  "<span class="code-key">from_date</span>": "<span class="code-string">2023-01-01</span>",
  "<span class="code-key">to_date</span>": "<span class="code-string">2023-12-31</span>",
  "<span class="code-key">status</span>": "<span class="code-string">success</span>",
  "<span class="code-key">stk</span>": "<span class="code-string">0123456789</span>"
}</code></pre>
            </div>
            
            <h3>✅ Response Mẫu</h3>
            
            <div class="code-block">
                <pre><code>{
  "<span class="code-key">success</span>": <span class="code-number">true</span>,
  "<span class="code-key">message</span>": "<span class="code-string">Chuyển tiền thành công</span>",
  "<span class="code-key">transaction_id</span>": "<span class="code-string">TX123456789</span>",
  "<span class="code-key">amount</span>": <span class="code-number">100000</span>,
  "<span class="code-key">fee</span>": <span class="code-number">1100</span>
}</code></pre>
            </div>
        </div>
        
        <div class="cta">
            <h2 class="cta-title">Bắt Đầu Tích Hợp Ngay Hôm Nay!</h2>
            <p>Giá chỉ 35.000đ/tháng - Hỗ trợ sinh viên và dự án nhỏ</p>
            
            <a href="https://t.me/minhquan2006" class="btn">
                <i class="fab fa-telegram"></i> Liên hệ qua Telegram
            </a>
            
            <a href="#" class="btn" style="background: var(--success);">
                <i class="fas fa-book"></i> Xem tài liệu API
            </a>
        </div>
        
        <footer>
            <p>© 2023 SPAYMENT.NET - Dịch vụ API chuyển tiền ViettelPay & Ngân hàng</p>
            <p>Liên hệ: <a href="https://t.me/minhquan2006" style="color: #6c757d;">@minhquan2006</a></p>
        </footer>
    </div>
</body>
</html>
