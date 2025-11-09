## Code repo is private as of now , but website is live and running
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

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd pesxchange
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Variables

Create a `.env.local` file in the root directory:

```env
# Supabase Configuration
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key

# College API (if needed)
COLLEGE_API_URL=your_college_api_url
COLLEGE_API_KEY=your_college_api_key
```

### 4. Database Setup

1. Go to your Supabase dashboard
2. Navigate to the SQL Editor
3. Run the SQL commands from `database_schema.sql` to create the necessary tables

```sql
-- Run the contents of database_schema.sql in your Supabase SQL editor
```

### 5. Run the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Database Schema

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

## Key Features Explained

### Authentication Flow
1. Student logs in with college credentials
2. User profile is saved to Supabase
3. JWT token is generated for session management
4. Protected routes check authentication status

### Product Management
- **Listing**: Students can create detailed product listings
- **Search**: Advanced filtering by category, price, condition
- **Images**: Support for multiple product images
- **Status**: Products can be active, sold, or inactive

### Order System
- **Buying**: Students can purchase items directly
- **Selling**: Automatic order creation when items are sold
- **Tracking**: Real-time order status updates
- **Communication**: Built-in messaging between parties

## Security Features

- **Input Validation**: All user inputs are validated
- **SQL Injection Protection**: Supabase handles query sanitization
- **Authentication Guards**: Protected routes require valid sessions
- **Data Validation**: Server-side validation for all operations

## Deployment

### Vercel (Recommended)

1. Connect your GitHub repository to Vercel
2. Set environment variables in Vercel dashboard
3. Deploy automatically on push to main branch

### Other Platforms

The app can be deployed to any platform that supports Next.js:
- Netlify
- Railway
- DigitalOcean App Platform
- AWS Amplify

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## Support

For support or questions:
- Create an issue in the GitHub repository
- Contact the development team
- Check the FAQ page in the application

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- PES University for providing the authentication API
- Supabase for the excellent database platform
- Next.js team for the amazing framework
- All contributors and beta testers

---

**Built with ❤️ for PES University students**
