T1F Games - Digital Game Store Platform
<div align="center"> <h3>🎮 Professional Game Marketplace built with Laravel & Vue.js</h3> <p>A modern, full-featured digital game store platform inspired by Steam</p> </div>
🌟 Features
User Features
✅ User Authentication - Register, Login, Profile Management
🎮 Game Catalog - Browse games with advanced search & filters
🛒 Shopping Cart - Add games to cart and manage purchases
💳 Checkout System - Simulated payment gateway integration
📚 Game Library - Access purchased games with unique keys
⭐ Review & Rating System - Rate and review games
❤️ Wishlist - Save games for later
🏷️ Genre & Tag Filtering - Find games by categories
Admin Features
📊 Dashboard - Overview of sales, games, and statistics
🎯 Game Management - Create, update, delete games
📦 Order Management - View and manage customer orders
💬 Review Moderation - Approve or reject user reviews
🏷️ Genre & Tag Management - Organize game categories
Technical Features
🎨 Modern UI - Dark theme with blue/black color palette
📱 Responsive Design - Works on all devices
⚡ Fast Performance - Optimized Vue.js SPA
🔒 Secure Authentication - Laravel Sanctum API tokens
🗄️ RESTful API - Clean API architecture
📝 Code Organization - MVC pattern, clean code structure
🛠️ Tech Stack
Backend
Laravel 10+ - PHP Framework
MySQL - Database
Laravel Sanctum - API Authentication
Eloquent ORM - Database Management
Frontend
Vue.js 3 - JavaScript Framework
Vue Router - Routing
Pinia - State Management
Axios - HTTP Client
Tailwind CSS - Styling
📋 Prerequisites
Before installation, make sure you have:

PHP >= 8.1
Composer
Node.js >= 16.x
npm or yarn
MySQL >= 5.7
🚀 Installation
1. Clone the Repository
bash
git clone https://github.com/yourusername/t1f-games.git
cd t1f-games
2. Install PHP Dependencies
bash
composer install
3. Install Node Dependencies
bash
npm install
4. Environment Setup
bash
cp .env.example .env
php artisan key:generate
5. Configure Database
Edit .env file with your database credentials:

env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=t1f_games
DB_USERNAME=root
DB_PASSWORD=your_password
6. Run Migrations & Seed Database
bash
php artisan migrate --seed
This will create:

All necessary tables
Admin user: admin@t1f.com / admin123
Regular user: user@t1f.com / user123
Sample games with genres and tags
7. Create Storage Link
bash
php artisan storage:link
8. Build Frontend Assets
bash
npm run build
For development with hot reload:

bash
npm run dev
9. Start Laravel Server
bash
php artisan serve
The application will be available at: http://localhost:8000

🎯 Quick Start
Access the Application
Homepage: http://localhost:8000
Store: http://localhost:8000/store
Login: http://localhost:8000/login
Admin Panel: http://localhost:8000/admin
Demo Credentials
Regular User:

Email: user@t1f.com
Password: user123
Admin User:

Email: admin@t1f.com
Password: admin123
📂 Project Structure
t1f-games/
├── app/
│   ├── Http/Controllers/
│   │   └── Api/
│   │       ├── AuthController.php
│   │       ├── GameController.php
│   │       ├── CartController.php
│   │       ├── OrderController.php
│   │       ├── ReviewController.php
│   │       └── Admin/
│   │           ├── GameManagementController.php
│   │           ├── OrderManagementController.php
│   │           └── ReviewManagementController.php
│   └── Models/
│       ├── User.php
│       ├── Game.php
│       ├── Genre.php
│       ├── Tag.php
│       ├── Cart.php
│       ├── Order.php
│       ├── OrderItem.php
│       └── Review.php
├── database/
│   ├── migrations/
│   └── seeders/
│       └── DatabaseSeeder.php
├── resources/
│   └── js/
│       ├── app.js
│       ├── App.vue
│       ├── components/
│       │   ├── Navbar.vue
│       │   ├── Footer.vue
│       │   └── GameCard.vue
│       ├── pages/
│       │   ├── HomePage.vue
│       │   ├── StorePage.vue
│       │   ├── GameDetailPage.vue
│       │   ├── CartPage.vue
│       │   ├── CheckoutPage.vue
│       │   ├── LibraryPage.vue
│       │   ├── WishlistPage.vue
│       │   ├── LoginPage.vue
│       │   ├── RegisterPage.vue
│       │   └── admin/
│       │       ├── AdminDashboard.vue
│       │       ├── AdminGames.vue
│       │       ├── AdminOrders.vue
│       │       └── AdminReviews.vue
│       └── stores/
│           ├── auth.js
│           ├── cart.js
│           └── wishlist.js
└── routes/
    └── api.php
🔧 Configuration
API Endpoint
The frontend is configured to use the API at http://localhost:8000. To change this, update VITE_API_URL in your .env file:

env
VITE_API_URL=http://localhost:8000
Image Storage
Game cover images and screenshots should be stored in storage/app/public/games/. Make sure to run:

bash
php artisan storage:link
📱 API Endpoints
Public Endpoints
GET  /api/games              - List all games
GET  /api/games/{slug}       - Get game details
GET  /api/games/featured     - Get featured games
GET  /api/games/latest       - Get latest games
GET  /api/genres             - List all genres
GET  /api/tags               - List all tags
POST /api/login              - User login
POST /api/register           - User registration
Protected Endpoints (Requires Authentication)
GET    /api/user             - Get current user
POST   /api/logout           - User logout
GET    /api/cart             - Get cart items
POST   /api/cart             - Add to cart
DELETE /api/cart/{id}        - Remove from cart
GET    /api/wishlist         - Get wishlist
POST   /api/wishlist         - Add to wishlist
GET    /api/orders           - Get user orders
POST   /api/orders           - Create order
GET    /api/library          - Get owned games
POST   /api/reviews          - Submit review
Admin Endpoints (Requires Admin Role)
GET    /api/admin/games                - List games (admin)
POST   /api/admin/games                - Create game
PUT    /api/admin/games/{id}           - Update game
DELETE /api/admin/games/{id}           - Delete game
GET    /api/admin/games-statistics     - Get statistics
GET    /api/admin/orders               - List all orders
PUT    /api/admin/orders/{id}/status   - Update order status
GET    /api/admin/reviews              - List all reviews
PUT    /api/admin/reviews/{id}/approve - Approve review
DELETE /api/admin/reviews/{id}         - Delete review
🎨 Design System
Color Palette
css
/* Primary Colors */
Dark Navy: #0f172a (slate-950)
Deep Blue: #1e3a8a (blue-950)
Bright Blue: #2563eb (blue-600)

/* Accent Colors */
Success Green: #10b981 (green-500)
Warning Yellow: #f59e0b (yellow-500)
Danger Red: #ef4444 (red-500)

/* Text Colors */
White: #ffffff
Light Gray: #cbd5e1 (slate-300)
Dark Gray: #475569 (slate-600)
Typography
Font Family: Inter, system-ui, sans-serif
Headings: Bold, large sizes
Body: Regular weight, comfortable line height
🧪 Testing
Run PHP Tests
bash
php artisan test
Run JavaScript Tests
bash
npm run test
📦 Deployment
Production Build
bash
# Build frontend assets
npm run build

# Optimize Laravel
php artisan config:cache
php artisan route:cache
php artisan view:cache

# Set proper permissions
chmod -R 775 storage bootstrap/cache
Environment Variables for Production
env
APP_ENV=production
APP_DEBUG=false
APP_URL=https://yourdomain.com

# Update database credentials
DB_CONNECTION=mysql
DB_HOST=your_production_host
DB_DATABASE=your_production_db
DB_USERNAME=your_production_user
DB_PASSWORD=your_production_password
🤝 Contributing
Contributions are welcome! Please follow these steps:

Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request
📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

👨‍💻 Author
T1F Development Team

Website: https://t1f.com
Email: contact@t1f.com
🙏 Acknowledgments
Laravel Community
Vue.js Community
Tailwind CSS Team
All contributors and testers
📞 Support
For support, email support@t1f.com or join our Discord community.

<div align="center"> <p>Made with ❤️ by T1F Development Team</p> <p>⭐ Star this repo if you find it helpful!</p> </div>
