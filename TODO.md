# 📋 Project To-Do List — Bitcoin Realtime Dashboard & AI Chatbot

## 🧱 1️⃣ Cấu trúc & môi trường ban đầu
- [ ] Tạo repo GitHub và khởi tạo README
- [ ] Thiết lập `.env.example` (API keys, DB URL)
- [ ] Cấu hình `docker-compose.yml` (backend, frontend, TimescaleDB, Redis)
- [ ] Khởi tạo dự án **FastAPI** (backend)
- [ ] Khởi tạo dự án **Next.js + Tailwind** (frontend)
- [ ] Tạo file `requirements.txt` và `package.json`

---

## 📡 2️⃣ Thu thập & xử lý dữ liệu (Data Layer)
- [ ] Kết nối API Binance & CoinGecko (OHLCV realtime)
- [ ] Tạo Celery task `collector_price`
- [ ] Tạo Celery task `collector_trends` (Google Trends mỗi 6h)
- [ ] Thêm NewsAPI / Reddit sentiment collector
- [ ] Viết script tính RSI, MACD, volatility
- [ ] Kiểm tra pipeline & log Celery (Flower / terminal)

---

## ⚙️ 3️⃣ API & WebSocket (Backend)
- [ ] Tạo `/api/chart-data` (GET) — JSON dữ liệu BTC
- [ ] Tạo `/api/forecast` (POST) — trả dự đoán mô hình
- [ ] Tạo `/api/chat` (POST) — gọi LLM (DeepSeek/Gemini)
- [ ] Tạo `/api/upload-image` (POST) — upload ảnh
- [ ] Tạo WebSocket `/ws/price` — stream realtime
- [ ] Thêm `/health` endpoint

---

## 💻 4️⃣ Frontend (Next.js + Tailwind + Recharts)
- [ ] Trang `/` (Dashboard tổng quan)
- [ ] Trang `/chart` (Candlestick + Line chart realtime)
- [ ] Trang `/chatbot` (Chatbot + Upload ảnh)
- [ ] Trang `/forecast` (Form chọn horizon, hiển thị kết quả)
- [ ] Component **ChartRealtime.tsx**
- [ ] Component **ChatbotPanel.tsx**
- [ ] Component **UploadImage.tsx**
- [ ] Responsive CSS cho mobile
- [ ] Dark/light theme toggle (optional)

---

## 🧠 5️⃣ Mô hình dự đoán (Model Layer)
- [ ] Chuẩn bị dữ liệu huấn luyện (CSV hoặc DB)
- [ ] Xây dựng baseline (Naïve, EWMA)
- [ ] Triển khai Prophet / ARIMA / SARIMAX (có exogenous)
- [ ] Huấn luyện LSTM / GRU (15m, 1h, 24h)
- [ ] Viết `train_model.py` (lưu trọng số & scaler)
- [ ] Endpoint `/api/forecast` đọc model và trả CI
- [ ] Đánh giá MAE / MAPE / RMSE (walk-forward)
- [ ] Lưu kết quả dự đoán vào DB

---

## 🤖 6️⃣ AI Chatbot & Vision
- [ ] Tích hợp **DeepSeek R1 (Ollama API)**
- [ ] Tích hợp **Gemini API** (Vision)
- [ ] Router `/api/chat` chọn provider
- [ ] Xử lý ảnh upload → OCR / pattern detect
- [ ] Hiển thị kết quả chatbot trong UI
- [ ] Giới hạn context và log chat

---

## 🚀 7️⃣ Deployment & Testing
- [ ] Viết Dockerfile cho backend & frontend
- [ ] Test `docker compose up` chạy toàn hệ
- [ ] Deploy lên **Railway** / **Fly.io** / VPS
- [ ] Kiểm tra build logs & WebSocket hoạt động
- [ ] Tạo file `Procfile` (Railway)
- [ ] Branch `production` riêng
- [ ] Cập nhật hướng dẫn deploy trong README

---

## 🧾 8️⃣ Báo cáo & Demo
- [ ] Viết báo cáo mô tả kiến trúc, quy trình
- [ ] Chuẩn bị slide demo (10–12 phút)
- [ ] Ghi video demo ngắn (optional)
- [ ] Tổng hợp kết quả, hướng mở rộng
- [ ] Hoàn thiện **Final Report Document**

---

## 🧰 9️⃣ Bảo trì & mở rộng (sau demo)
- [ ] Thêm nhiều crypto khác (ETH, SOL, BNB)
- [ ] Tích hợp login Google OAuth
- [ ] Lưu lịch sử chat trong DB
- [ ] Tạo API public key / throttling
- [ ] Tối ưu WebSocket broadcast
- [ ] Viết test unit + integration (pytest & Playwright)
- [ ] Dashboard admin (FastAPI Admin / Next Admin)

---

✅ *Mẹo:* Copy file này thành `TODO.md` trong repo để theo dõi tiến độ.  
Đánh dấu hoàn thành bằng cách đổi `[ ]` → `[x]` trong GitHub UI.
