UPI Payment Gateway Integration

A production-ready implementation for integrating UPI (Unified Payments Interface) payments in web or mobile applications.

🔗 Live Demo (Deployed Link)

Paste your deployed URL here:

➡️ https://mini-project-2-3w1q.onrender.com/

✨ Features

Generate UPI payment requests (QR / Deep Link)

Support for Google Pay, PhonePe, Paytm, BHIM and other UPI apps

Transaction status verification via backend

Secure API integration with checksum & signatures

Webhook support for payment confirmation

Compatible with mobile (Android/iOS) and web apps

🧰 Tech Stack

Frontend: React / Next.js / Flutter / Android/iOS (any UI)

Backend: Node.js / Express / Django / Spring Boot

Payments: UPI Deep Link (upi://pay), NPCI APIs, Bank PSP APIs

Database: MongoDB / PostgreSQL / MySQL

🗺️ Architecture

Client (React/Android/iOS) ──▶ Backend API (Node/Django)
     │                                 │
     ▼                                 ▼
 UPI Intent / QR Code             UPI PSP / Bank API
     │                                 │
     ▼                                 ▼
   Payment App (GPay/Paytm)       Transaction Verification

🚀 Getting Started (Local)

1) Clone & install

git clone https://github.com/your-username/upi-payment-gateway.git
cd upi-payment-gateway
npm install

2) Environment variables

Create .env file:

PORT=3000
NODE_ENV=production
UPI_MERCHANT_VPA=merchant@upi
UPI_MERCHANT_NAME=YourMerchant
UPI_CALLBACK_URL=https://yourdomain.com/api/payment/callback
DB_URL=postgresql://user:pass@localhost:5432/upipay
SECRET_KEY=change_me

3) Run locally

npm run dev

Your app runs on http://localhost:3000

💳 Payment Flow

Frontend generates UPI deep link or QR:
upi://pay?pa=merchant@upi&pn=YourMerchant&mc=0000&tid=txn123&tr=order123&tn=Order+Payment&am=500&cu=INR&url=https://yourdomain.com/callback

User pays via UPI app (GPay/PhonePe/etc.)

Backend verifies transaction via PSP/Bank API or webhook callback.

Order marked success/failure in DB.

☁️ Deployment

Vercel / Netlify (Frontend)

Deploy frontend project

Paste backend API URL in .env

Update README with deployed link

Render / Railway / AWS / Azure (Backend)

Deploy backend as Web Service

Add environment variables

Ensure webhook callback URL is public (HTTPS)

📎 Where to paste deployed link

README (top of this file) under Live Demo section

GitHub → About → Website field

Frontend .env for API URL (e.g., NEXT_PUBLIC_API_URL=https://your-backend.com)

📦 Production Checklist



📸 Screenshots

Add your payment flow screenshots here:

/docs/screenshots/upi-qr.png
/docs/screenshots/payment-success.png

🤝 Contributing

PRs welcome! Please open an issue before big changes.

📄 License

MIT (or your choice)
