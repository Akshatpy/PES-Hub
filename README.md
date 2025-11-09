## Code repo is private as of now , but website is live and running <br> https://www.peshub.live/
# PESU Hub - Student Marketplace

A modern, secure marketplace platform built specifically for PES University students to buy, sell, and exchange items like textbooks, electronics, furniture, and more.

## Features

- 🔐 **Secure Authentication** - College API integration for student verification
- 🛍️ **Product Management** - List, search, and manage items for sale
- 📦 **Order System** - Complete order lifecycle management
- 💬 **Communication** - Built-in chat system for buyers and sellers
- 📱 **Responsive Design** - Modern UI that works on all devices
- 🎨 **Beautiful Interface** - Dark theme with smooth animations

## Tech Stack

- **Frontend**: Next.js 15, React 19, TypeScript
- **Styling**: Tailwind CSS, Framer Motion
- **Database**: Supabase (PostgreSQL)
- **Authentication**: Custom college API + Supabase
- **UI Components**: Radix UI, Lucide Icons

## Prerequisites

- Node.js 18+ 
- npm or yarn
- Supabase account
- Access to PES University authentication API


The application uses the following main tables:

- **users** - Student profiles and authentication
- **categories** - Product categories (Electronics, Books, etc.)
- **products** - Items listed for sale
- **orders** - Purchase transactions
- **messages** - Communication between users

## API Endpoints

### Products
- `GET /api/products` - List all products with filters
- `POST /api/products` - Create a new product
- `GET /api/products/[id]` - Get product details
- `PUT /api/products/[id]` - Update product
- `DELETE /api/products/[id]` - Delete product

### Orders
- `GET /api/orders` - Get user orders (buying/selling)
- `POST /api/orders` - Create a new order
- `GET /api/orders/[id]` - Get order details
- `PUT /api/orders/[id]` - Update order status

### Categories
- `GET /api/categories` - List all categories

### Users
- `POST /api/saveUser` - Save user profile
- `POST /api/login` - Authenticate user

## Usage Guide

### For Students

1. **Login**: Use your PES University credentials
2. **Browse**: Search and filter products by category, price, condition
3. **Buy**: Click on products to view details and place orders
4. **Sell**: List your items with photos and descriptions
5. **Track**: Monitor your orders and sales

### For Administrators

1. **Monitor**: Track marketplace activity and user behavior
2. **Moderate**: Review reported items and manage disputes
3. **Analytics**: View marketplace statistics and trends

## File Structure

```
pesxchange/
├── src/
│   ├── app/                    # Next.js app router pages
│   │   ├── api/               # API routes
│   │   ├── marketplace/       # Marketplace page
│   │   ├── orders/           # Orders management
│   │   ├── sell/             # Sell item form
│   │   └── product/[id]/     # Product detail page
│   ├── components/            # Reusable UI components
│   ├── lib/                   # Utilities and configurations
│   └── types/                 # TypeScript type definitions
├── public/                    # Static assets
├── database_schema.sql        # Database setup script
└── README.md                  # This file
```

## Security Features

- **Input Validation**: All user inputs are validated
- **SQL Injection Protection**: Supabase handles query sanitization
- **Authentication Guards**: Protected routes require valid sessions
- **Data Validation**: Server-side validation for all operations

## Deployment

## License

This project is licensed under the MIT License - see the LICENSE file for details.

**Built with ❤️ for PES University students**
- Akshat , Atharv , Adhithya
