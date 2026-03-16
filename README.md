
# 🌱 Hệ Thống Phát Hiện Bệnh Trên Cây Trồng

Đây là một ứng dụng phát hiện bệnh trên cây trồng hiện đại, sẵn sàng cho môi trường production, sử dụng **deep learning** để nhận diện bệnh từ hình ảnh lá cây.
Hệ thống được xây dựng với **backend FastAPI** và **frontend React TypeScript**, có khả năng phát hiện bệnh trên nhiều loại cây như **Táo, Ngô, Nho, Khoai tây, Cà chua, Xoài, Cam quýt và Lúa**.

---

# ✨ Tính năng

- 🎯 Nhận diện bằng AI: Mô hình deep learning được huấn luyện với hơn **30 loại bệnh cây trồng**
- 🖼️ Upload ảnh dễ dàng: Hỗ trợ kéo‑thả ảnh lá cây
- ⚡ Dự đoán nhanh theo thời gian thực kèm **độ tin cậy (confidence score)**
- 🔄 Hỗ trợ nhiều framework ML: TensorFlow, PyTorch và ONNX
- 🌐 Giao diện web hiện đại với React + TypeScript
- 🚀 Backend FastAPI sẵn sàng triển khai production
- ☁️ Hỗ trợ deploy cloud (Render cho backend, Vercel cho frontend)
- 🔒 Bảo mật: rate limiting, CORS protection và validation dữ liệu

---

# 🏗️ Cấu trúc dự án

Plant Disease Detection/
├── PlantDiseaseDetection.ipynb    # Notebook huấn luyện model
├── backend/                       # Backend FastAPI
│   ├── app/                       # Source code backend
│   ├── models/                    # Model ML đã train
│   └── tests/                     # Test backend
├── frontend/                      # Frontend React TypeScript
│   ├── src/                       # Source code frontend
│   └── public/                    # Static assets
├── ML_Model/                      # Model artifacts và ảnh test
└── scripts/                       # Script tiện ích

---

# 🎯 Các bệnh cây trồng có thể phát hiện

Model có thể nhận diện **30+ bệnh** trên nhiều loại cây:

## 🍎 Táo
- Apple Scab
- Black Rot
- Cedar Apple Rust
- Healthy

## 🌽 Ngô
- Cercospora Leaf Spot
- Common Rust
- Northern Leaf Blight
- Healthy

## 🍇 Nho
- Black Rot
- Esca (Black Measles)
- Leaf Blight
- Healthy

## 🥔 Khoai tây
- Early Blight
- Late Blight
- Healthy

## 🍅 Cà chua
- Bacterial Spot
- Early Blight
- Late Blight
- Leaf Mold
- Septoria Leaf Spot
- Spider Mites
- Target Spot
- Yellow Leaf Curl Virus
- Mosaic Virus
- Healthy

## 🥭 Các cây khác
- Mango Anthracnose
- Citrus Canker
- Rice Blast

---

# 🛠️ Công nghệ sử dụng

## Frontend
- React 18 + TypeScript
- Vite
- Tailwind CSS
- React Router
- TanStack Query
- React Dropzone
- Lucide Icons

## Backend
- FastAPI
- Pydantic
- Uvicorn / Gunicorn
- Redis
- Pillow
- TensorFlow / PyTorch / ONNX

---

# 🚀 Hướng dẫn chạy nhanh

## Yêu cầu
- Python 3.11+
- Node.js 18+
- Git
- RAM tối thiểu 4GB (khuyến nghị 8GB)


## 1. Thiết lập Backend

cd backend
python -m venv venv

# Windows
venv\Scripts\activate

# Linux/Mac
source venv/bin/activate

pip install -r requirements.txt

uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

## 2. Thiết lập Frontend

cd frontend
npm install
npm run dev

## 3. Truy cập ứng dụng

Frontend: http://localhost:5173  
Backend API: http://localhost:8000  
API Docs: http://localhost:8000/docs

---

# 📊 Huấn luyện mô hình

Chạy notebook training:

pip install jupyter notebook
jupyter notebook PlantDiseaseDetection.ipynb

Notebook bao gồm:
- Tiền xử lý dữ liệu và augmentation
- Kiến trúc CNN + transfer learning
- Training và validation
- Export model
- Đánh giá hiệu suất

---

# ☁️ Triển khai Cloud

## Backend (Render)
1. Fork repository
2. Kết nối GitHub với Render
3. Tạo Web Service
4. Deploy bằng render.yaml

## Frontend (Vercel)

npm install -g vercel
cd frontend
vercel --prod

---

# 🔐 Bảo mật

- Kiểm tra loại file
- Giới hạn kích thước file
- Validation dữ liệu đầu vào
- CORS protection
- Rate limiting

---

# 🧪 Testing

Backend:
cd backend
pytest

Frontend:
cd frontend
npm test

---

# 📄 License

Dự án sử dụng **MIT License**.

---

❤️ Made for plant health monitoring.
