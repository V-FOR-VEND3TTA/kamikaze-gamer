# kamikaze-gamer
Kamikaze Gamer is a world-class Django-based ecommerce platform exclusively for gamers. It offers both physical gaming products (peripherals, consoles, accessories) and digital products (game keys, DLCs, software licenses).

This project integrates **subscription-based game keys**, allowing users to purchase a subscription and receive **automatically assigned** digital game keys.  

---

## **🚀 Features**  

### **🛒 Ecommerce Functionalities**  
- **Supports Physical & Digital Products** (gaming gear + downloadable content).  
- **Advanced Product Filtering** (filter by platform, accessories, and genres).  

### **🔑 Subscription-Based Game Key System**  
- **Automated game key assignment** on successful subscription payment.  
- **Secure key delivery** via user dashboard.  
- **Auto-revocation** when the subscription expires (via Celery tasks).  

### **💳 Secure Checkout & Payments**  
- **Stripe & PayPal integration** (subscriptions & one-time purchases).  
- **Crypto payments support** (via CoinPayments API).  
- **Automatic tax & shipping cost calculations** based on user location.  

### **📊 Admin Panel & Analytics**  
- **Custom Django Admin Dashboard** for **orders & inventory** management.  
- **Sales reports & data visualizations** using Chart.js & Django ORM queries.  

### **🎨 UI/UX**  
- **Responsive Bootstrap UI** optimized for **mobile & desktop**.  
- **Dark Mode Support** (toggle via user settings).  

### **🔐 Security & Performance**  
- **CSRF & XSS protection, secure sessions**.  
- **Optimized database queries** for high-traffic handling.  
- **Caching (Redis, Memcached) for fast performance**.  

---

## **🛠️ Tech Stack**  

| Layer       | Technology |
|-------------|------------|
| **Backend** | Django, Django REST Framework |
| **Frontend** | Bootstrap, JavaScript (Alpine.js for interactivity) |
| **Database** | PostgreSQL (supports scaling) |
| **Caching** | Redis, Memcached |
| **Task Queue** | Celery (handles subscription expirations, key assignments) |
| **Payments** | Stripe, PayPal, Crypto (CoinPayments) |
| **Deployment** | Docker, Nginx, Gunicorn |

---

## **📂 Project Setup**  

### **🔧 Installation**  

1️⃣ **Clone the Repository**  
```bash
git clone https://github.com/yourusername/gamers-haven.git
cd gamers-haven
```
  
2️⃣ **Create & Activate a Virtual Environment**  
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

3️⃣ **Install Dependencies**  
```bash
pip install -r requirements.txt
```

4️⃣ **Set Up the Database**  
```bash
python manage.py migrate
```

5️⃣ **Create a Superuser** (for admin access)  
```bash
python manage.py createsuperuser
```

6️⃣ **Run the Development Server**  
```bash
python manage.py runserver
```

🎉 **Visit:** `http://127.0.0.1:8000/`  

---

## **📜 API Endpoints**  

| **Endpoint** | **Method** | **Description** |
|-------------|------------|----------------|
| `/api/products/` | GET | Get all gaming products |
| `/api/subscriptions/` | POST | Subscribe to a plan |
| `/api/game-keys/` | GET | Get assigned game keys |
| `/api/orders/` | GET | View order history |

---

## **🔑 Subscription-Based Game Key Flow**  

1️⃣ **User purchases a subscription** via Stripe/PayPal.  
2️⃣ **System assigns a unique game key** from the database.  
3️⃣ **User accesses their keys** via the **dashboard**.  
4️⃣ **Celery automatically revokes keys** after subscription expiry.  

---

## **📦 Deployment (Docker + Nginx + Gunicorn)**  

1️⃣ **Build & Run Containers**  
```bash
docker-compose up --build -d
```

2️⃣ **Migrate Database**  
```bash
docker-compose exec web python manage.py migrate
```

3️⃣ **Create Superuser**  
```bash
docker-compose exec web python manage.py createsuperuser
```

🎉 Your site is now live on **`http://yourdomain.com`**!  

---

## **🚀 Future Enhancements**  
✅ **Discount & Promotions System** (for loyal subscribers)  
✅ **In-App Game Activation** (Steam, Epic API integration)  
✅ **Multi-Tier Subscription Plans** (Basic, Pro, VIP)  

---

## **🛠 Contributing**  
Want to contribute? Fork the repo and submit a PR!  

1. **Fork the project**  
2. **Create a new branch** (`feature/new-feature`)  
3. **Commit your changes** (`git commit -m "Added new feature"`)  
4. **Push to branch** (`git push origin feature/new-feature`)  
5. **Open a Pull Request**  

---

## **📧 Support & Contact**  
For questions, open an **issue** or email: **support@gamershaven.com**.  

---

### **🎮 Level Up Your Gaming Store Today! 🚀**  
