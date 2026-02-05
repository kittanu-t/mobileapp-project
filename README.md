# Mobile Application Project

โปรเจกต์นี้เป็น Mobile Application ที่พัฒนาด้วย **Android (Kotlin)**  
เชื่อมต่อกับ **REST API (Node.js + Express)** และฐานข้อมูล **MySQL**  
โดยใช้ GitHub เป็นศูนย์กลางในการทำงานร่วมกันเป็นทีม

---

## 🧱 Technology Stack

### Frontend (Mobile)
- Android Studio
- Kotlin
- Retrofit (REST API)

### Backend
- Node.js
- Express.js
- MySQL (ผ่าน XAMPP)
- dotenv

### Tools
- Git & GitHub
- Postman
- XAMPP (MySQL)

---

## 📂 Project Structure

mobileapp-proj/
│
├── backend/ # Node.js REST API
│ ├── server.js
│ ├── package.json
│ ├── package-lock.json
│ └── node_modules/
│
├── android/ # Android Studio Project
│ ├── app/
│ ├── gradle/
│ └── build.gradle
│
├── .gitignore
└── README.md


---

## ⚙️ Backend Setup (Node.js)

### 1. ติดตั้ง dependencies
```
cd backend
npm install
```

2. สร้างไฟล์ .env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=mobileapp_proj
DB_PORT=3306
PORT=3000
⚠️ .env ไม่ถูก push ขึ้น GitHub

3. รัน server
node server.js
ถ้าเห็น:
Connected to MySQL
Server running on port 3000
แสดงว่า backend พร้อมใช้งาน

🗄️ Database Setup (MySQL)
CREATE DATABASE mobileapp_db;
USE mobileapp_db;

CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100)
);

📱 Android Setup
  1. เปิด Android Studio
  2. Open Project → เลือกโฟลเดอร์ android/
  3. Run บน Emulator

Base URL สำหรับ Emulator
.baseUrl("http://-----:3000/")

👥 Team Members




📌 Notes
- Backend และ Android แยกกันชัดเจน (Client–Server)
- ใช้ REST API เป็นตัวกลาง
- รองรับการทำงานเป็นทีมผ่าน GitHub

---

# Workflow งานกลุ่ม (เขียนใส่รายงาน / อาจารย์ถามตอบได้)

> :highlight[ห้าม push ตรง branch main โดยตรง]

## กฎการทำงานเป็นทีม

### 1. โครงสร้าง Branch
- `main` → branch หลัก (โค้ดที่เสถียร)
- `feature-android` → งานฝั่ง Android
- `feature-backend` → งานฝั่ง Backend
- (ถ้ามีหลาย feature สามารถแยกย่อยได้)

---

### 2. ขั้นตอนการทำงานของแต่ละคน

```
git checkout -b feature-ชื่องาน
```
