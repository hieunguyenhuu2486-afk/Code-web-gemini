<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bánh Căn Bánh Xèo Bảy | Đặc sản Phan Thiết</title>
    
    <style>
        :root {
            --primary-color: #d84315;
            --secondary-color: #fbe9e7;
            --text-color: #3e2723;
            --shadow: 0 8px 16px rgba(0,0,0,0.1);
            --transition: all 0.3s ease;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        
        body { 
            background-color: #f5f5f5; 
            color: var(--text-color); 
            line-height: 1.6; 
            padding-bottom: 90px;
        }

        /* Nav */
        .top-nav { background: white; position: sticky; top: 0; z-index: 100; display: flex; justify-content: center; box-shadow: 0 2px 10px rgba(0,0,0,0.05); }
        .tab-btn { background: none; border: none; padding: 15px 30px; font-size: 1.1rem; font-weight: bold; color: #757575; cursor: pointer; transition: var(--transition); border-bottom: 3px solid transparent; }
        .tab-btn:hover { color: var(--primary-color); }
        .tab-btn.active { color: var(--primary-color); border-bottom: 3px solid var(--primary-color); }

        .container { max-width: 800px; margin: 20px auto; padding: 0 15px; }

        /* Hero Banner 3D */
        .hero-banner { background: linear-gradient(135deg, #ff7043, #d84315); color: white; text-align: center; padding: 40px 20px; border-radius: 15px; box-shadow: var(--shadow); margin-bottom: 30px; transition: var(--transition); }
        .hero-banner:hover { transform: translateY(-5px); }
        .hero-banner h1 { font-size: 2.2rem; margin-bottom: 10px; text-shadow: 2px 2px 4px rgba(0,0,0,0.2); }
        
        /* Box Thông tin */
        .info-card { background: white; border-radius: 12px; padding: 20px; margin-bottom: 25px; box-shadow: var(--shadow); border-left: 6px solid var(--primary-color); transition: var(--transition); }
        .info-card h3 { margin-bottom: 15px; color: var(--primary-color); }
        .info-card p { margin-bottom: 8px; font-size: 1.05rem; }

        /* Google Reviews - Fetch thực tế */
        .review-slider { display: flex; gap: 15px; overflow-x: auto; padding: 10px 0; scroll-behavior: smooth; }
        .review-card { background: #fff; padding: 15px; border-radius: 12px; min-width: 280px; box-shadow: 0 4px 10px rgba(0,0,0,0.05); border: 1px solid #f0f0f0; }
        .stars { color: #ffb300; font-size: 1.2rem; letter-spacing: 2px; }
        .reviewer { font-weight: bold; font-size: 0.95rem; margin-top: 5px; color: #111; }
        .review-text { font-size: 0.9rem; color: #555; font-style: italic; margin-top: 8px; }

        /* Thư viện hình ảnh thực tế */
        .gallery-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; }
        .gallery-img { width: 100%; height: 160px; object-fit: cover; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); transition: var(--transition); }
        .gallery-img:hover { transform: scale(1.03); }

        .tab-content { display: none; animation: fadeIn 0.5s; }
        .tab-content.active { display: block; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

        /* Thẻ Menu 3D */
        .menu-category { font-size: 1.4rem; color: var(--primary-color); margin: 30px 0 15px 0; font-weight: 700; text-align: center; position: relative; }
        .menu-category::after { content: ''; display: block; width: 50px; height: 3px; background: var(--primary-color); margin: 8px auto 0; border-radius: 2px; }
        .menu-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 20px; }
        .menu-card { background: white; border-radius: 12px; padding: 20px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); transition: var(--transition); border: 1px solid #f0f0f0; }
        .menu-card:hover { transform: translateY(-8px); box-shadow: 0 12px 24px rgba(0,0,0,0.15); border-color: var(--primary-color); }
        .menu-card h3 { font-size: 1.1rem; margin-bottom: 5px; color: #212121; }
        .menu-card .desc { font-size: 0.9rem; color: #757575; margin-bottom: 15px; }
        .menu-card .price { font-weight: bold; color: var(--primary-color); font-size: 1.2rem; background: var(--secondary-color); display: inline-block; padding: 5px 10px; border-radius: 20px; }

        /* Nút cố định Zalo/Maps */
        .bottom-actions { position: fixed; bottom: 0; left: 0; width: 100%; background: rgba(255, 255, 255, 0.95); backdrop-filter: blur(10px); display: flex; justify-content: center; padding: 15px 10px; box-shadow: 0 -4px 15px rgba(0,0,0,0.1); z-index: 100; gap: 15px; }
        .action-btn { flex: 1; max-width: 300px; padding: 12px 20px; border-radius: 30px; text-align: center; text-decoration: none; font-weight: bold; font-size: 1rem; color: white; transition: var(--transition); box-shadow: 0 4px 10px rgba(0,0,0,0.2); }
        .btn-zalo { background: linear-gradient(45deg, #0088cc, #00aaff); }
        .btn-maps { background: linear-gradient(45deg, #43a047, #66bb6a); }
        .action-btn:hover { transform: scale(1.05); box-shadow: 0 6px 15px rgba(0,0,0,0.3); }

        /* KHUNG CHATBOT TỰ ĐỘNG TƯ VẤN */
        .chat-widget { position: fixed; bottom: 85px; right: 15px; width: 320px; background: white; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.2); z-index: 999; display: flex; flex-direction: column; transition: var(--transition); border: 1px solid #eee; }
        .chat-header { background: linear-gradient(135deg, #ff7043, #d84315); color: white; padding: 12px 15px; font-weight: bold; cursor: pointer; display: flex; justify-content: space-between; align-items: center; border-radius: 12px 12px 0 0; }
        .chat-body { padding: 15px; height: 250px; overflow-y: auto; background: #fdfbf7; display: flex; flex-direction: column; gap: 12px; }
        .bot-msg { background: white; padding: 10px 12px; border-radius: 12px 12px 12px 0; box-shadow: 0 2px 5px rgba(0,0,0,0.05); font-size: 0.9rem; align-self: flex-start; border: 1px solid #e0e0e0; max-width: 85%; }
        .user-msg { background: var(--primary-color); color: white; padding: 10px 12px; border-radius: 12px 12px 0 12px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); font-size: 0.9rem; align-self: flex-end; max-width: 85%; }
        .chat-options { padding: 12px; background: white; border-top: 1px solid #eee; display: flex; flex-direction: column; gap: 8px; }
        .chat-options button { border: 1px solid var(--primary-color); background: white; color: var(--primary-color); padding: 8px 12px; border-radius: 20px; cursor: pointer; transition: 0.2s; font-size: 0.85rem; font-weight: bold; text-align: left; }
        .chat-options button:hover { background: var(--primary-color); color: white; }
        
        .chat-collapsed .chat-body, .chat-collapsed .chat-options { display: none; }
        .chat-collapsed .chat-header { border-radius: 12px; }
    </style>
</head>
<body>

    <!-- Thanh chuyển 2 mục -->
    <nav class="top-nav">
        <button class="tab-btn active" onclick="switchTab('trangchu')">Trang Chủ & Đánh Giá</button>
        <button class="tab-btn" onclick="switchTab('thucdon')">Menu Chọn Món</button>
    </nav>

    <div class="container">
        
        <!-- ================= MỤC 1: TRANG CHỦ & DOANH NGHIỆP ================= -->
        <div id="trangchu" class="tab-content active">
            
            <div class="hero-banner">
                <h1>BÁNH CĂN BÁNH XÈO BẢY</h1>
                <p>Đặc sản Phan Thiết - Ăn nóng tại lò</p>
            </div>

            <div class="info-card">
                <h3>📍 Thông tin liên hệ</h3>
                <p><strong>Địa chỉ:</strong> 110 Hà Huy Tập, Khu Phố 5, Phường Phan Thiết, Lâm Đồng (Bình Thuận cũ).</p>
                <p><strong>Giờ phục vụ:</strong> 11:00 - 21:00 (Hàng ngày)</p>
            </div>

            <!-- Hình ảnh thực tế từ Google Maps -->
            <div class="info-card">
                <h3>📸 Hình Ảnh Tại Quán</h3>
                <div class="gallery-grid">
                    <img src="https://lh3.googleusercontent.com/grass-cs/AABkmLcBlzpUVTWes1QyOYGp2kAEQByyph8iQNYldT9TRudceJMTMT3nYXm8P_IaAForQ8yiNozLHFVqxZxz7lnDL6sqBVPoCbKRGSl2ogSiCi8s5RUJP8lrAG8wcbwkS9-8Cz0s__h155pmf-mc=k-no" class="gallery-img" alt="Bánh căn Bảy">
                    <img src="https://lh3.googleusercontent.com/grass-cs/AABkmLdUWl666s0U320tulhgk-DU1p9mGuWLGBQkxY1ruBc8A8nYoj9RjEn8B_G8mUGNZlBkhvPnJlcFu5TNH1oHnfEv7d0IXa3mF48Kvpb0ndtSQbIzqHD0PE-N_7BCFqps-kxrBX4Tkt3VnEGl=k-no" class="gallery-img" alt="Bánh xèo Bảy">
                    <img src="https://lh3.googleusercontent.com/grass-cs/AABkmLdLb-s51nJmh0PR7pxwBgXecS7QTPb4RR4tEpSoDdbCGtjAwBAdw_yoAxzagAO2s9NKHTsNN7fee-KyWD1Qgxb8aBaJ-FdtLhxgICXFt9NSla4t70MvslcRq3SwJkAqPkjIlTe9UrfMfQ3a=k-no" class="gallery-img" alt="Hải sản">
                    <img src="https://lh3.googleusercontent.com/grass-cs/AABkmLchIY1lMZ12wDw31JqDzFAlOAKO2RETWhxMxNA_gv9vBxbm-gWsuQIRi_2tP1oITdzLSz6p9VVN48_6aKstP_orwsue1xhbGi3eaMw9t1nkU39K_Fe8-W2zn5lBn67LIv0EBa4g4OCxMPEk=k-no" class="gallery-img" alt="Thực đơn">
                </div>
            </div>

            <!-- Đánh giá thực tế từ Google Maps -->
            <div class="info-card">
                <h3>⭐ Khách Hàng Đánh Giá Quán</h3>
                <div class="review-slider">
                    <div class="review-card">
                        <div class="stars">★★★★★</div>
                        <div class="reviewer">Hồng phúc Bùi hoàng</div>
                        <div class="review-text">"Đồ ăn nóng ngon đặt biệt là cá kho ngon xuất sắc ..!!!"</div>
                    </div>
                    <div class="review-card">
                        <div class="stars">★★★★★</div>
                        <div class="reviewer">Thái Võ Dương Thành</div>
                        <div class="review-text">"Quán local, trong hẻm, khá hợp vị, quan trọng là giá cả rất dễ chịu."</div>
                    </div>
                    <div class="review-card">
                        <div class="stars">★★★★★</div>
                        <div class="reviewer">Nguyễn Bùi Bá Huy</div>
                        <div class="review-text">"Quán ăn ngon và anh chị chủ cũng rất dễ thương. Giá bình dân. Sẽ quay lại nhiều lần"</div>
                    </div>
                    <div class="review-card">
                        <div class="stars">★★★★★</div>
                        <div class="reviewer">Thùy Dương Cao</div>
                        <div class="review-text">"Bánh căn ngon, bánh xèo cũng ngon nè"</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ================= MỤC 2: THỰC ĐƠN ================= -->
        <div id="thucdon" class="tab-content">
            
            <h2 class="menu-category">Combo Bánh Căn Truyền Thống</h2>
            <div class="menu-grid">
                <div class="menu-card">
                    <h3>Combo Bánh Căn Truyền Thống</h3>
                    <p class="desc">5 cặp bánh kèm nước chấm (trứng, xíu mại, da heo, xoài).</p>
                    <div class="price">37.000đ</div>
                </div>
                <div class="menu-card">
                    <h3>Combo Bánh Căn Trứng</h3>
                    <p class="desc">5 cặp bánh trứng kèm nước chấm đầy đủ.</p>
                    <div class="price">42.000đ</div>
                </div>
            </div>

            <h2 class="menu-category">Bánh Căn Hải Sản</h2>
            <div class="menu-grid">
                <div class="menu-card">
                    <h3>Bánh căn Tôm, Mực, Trứng</h3>
                    <p class="desc">Phần 6 cái, nước chấm chưa kèm topping.</p>
                    <div class="price">32.000đ</div>
                </div>
                <div class="menu-card">
                    <h3>Bánh căn Tôm, Mực (hoặc Tôm/Mực)</h3>
                    <p class="desc">Phần 6 cái, nước chấm chưa kèm topping.</p>
                    <div class="price">37.000đ</div>
                </div>
            </div>

            <h2 class="menu-category">Bánh Xèo & Món Kèm</h2>
            <div class="menu-grid">
                <div class="menu-card">
                    <h3>Bánh Xèo Thập Cẩm</h3>
                    <p class="desc">Phần 3 cái (Tôm, mực, thịt). Giòn rụm miền Trung.</p>
                    <div class="price">40.000đ</div>
                </div>
                <div class="menu-card">
                    <h3>Cá Kho Rục Xương</h3>
                    <p class="desc">Đặc sản ăn kèm đậm đà.</p>
                    <div class="price">15k - 20k</div>
                </div>
            </div>
            
            <br><br><br>
        </div>
    </div>

    <!-- Thanh Buttons Zalo & Maps 3D -->
    <div class="bottom-actions">
        <a href="https://zalo.me/0918450223" target="_blank" class="action-btn btn-zalo">💬 Đặt Hàng Zalo</a>
        <a href="https://www.google.com/maps/search/?api=1&query=110+Hà+Huy+Tập,+Phường+Đức+Thắng,+Phan+Thiết,+Bình+Thuận" target="_blank" class="action-btn btn-maps">🗺️ Chỉ Đường Maps</a>
    </div>

    <!-- CHATBOT TỰ ĐỘNG -->
    <div class="chat-widget chat-collapsed" id="chatWidget">
        <div class="chat-header" onclick="toggleChat()">
            <span>🤖 Trợ Lý Quán Bảy</span>
            <span id="chatIcon">▲</span>
        </div>
        <div class="chat-body" id="chatBody">
            <div class="bot-msg">Dạ chào bạn! Mình là trợ lý ảo của Quán Bảy. Mình có thể giúp gì cho bạn ạ?</div>
        </div>
        <div class="chat-options">
            <button onclick="handleChat('time')">👉 Quán mở cửa lúc mấy giờ?</button>
            <button onclick="handleChat('menu')">👉 Tư vấn giá các món ăn</button>
            <button onclick="handleChat('order')">👉 Tôi muốn đặt giao hàng</button>
        </div>
    </div>

    <script>
        // Chuyển Tab
        function switchTab(tabId) {
            document.querySelectorAll('.tab-btn').forEach(btn => btn.classList.remove('active'));
            document.querySelectorAll('.tab-content').forEach(content => content.classList.remove('active'));
            event.target.classList.add('active');
            document.getElementById(tabId).classList.add('active');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Logic Chatbot Tự Động
        function toggleChat() {
            const widget = document.getElementById('chatWidget');
            const icon = document.getElementById('chatIcon');
            widget.classList.toggle('chat-collapsed');
            icon.innerText = widget.classList.contains('chat-collapsed') ? '▲' : '▼';
        }

        function handleChat(type) {
            const body = document.getElementById('chatBody');
            
            if(type === 'time') {
                body.innerHTML += `<div class="user-msg">Quán mở cửa lúc mấy giờ?</div>`;
                setTimeout(() => {
                    body.innerHTML += `<div class="bot-msg">Dạ, quán phục vụ từ 11:00 trưa đến 21:00 tối hàng ngày ạ.</div>`;
                    body.scrollTop = body.scrollHeight;
                }, 600);
            } 
            else if (type === 'menu') {
                body.innerHTML += `<div class="user-msg">Tư vấn giúp tôi giá các món nhé.</div>`;
                setTimeout(() => {
                    body.innerHTML += `<div class="bot-msg">Quán chuyên Bánh căn truyền thống (37k-42k), Bánh căn hải sản (32k-42k), Bánh xèo miền Trung (40k) và Cá kho rục xương rất ngon ạ! Bạn chuyển sang mục Menu Chọn Món để xem chi tiết nhé.</div>`;
                    body.scrollTop = body.scrollHeight;
                }, 800);
            } 
            else if (type === 'order') {
                body.innerHTML += `<div class="user-msg">Tôi muốn đặt giao hàng.</div>`;
                setTimeout(() => {
                    body.innerHTML += `<div class="bot-msg">Dạ, để chốt đơn nhanh nhất, bạn vui lòng nhấn vào nút <b>💬 Đặt Hàng Zalo</b> màu xanh ở dưới cùng màn hình để kết nối với nhân viên quán nhé!</div>`;
                    body.scrollTop = body.scrollHeight;
                }, 700);
            }
        }
    </script>

</body>
</html>
