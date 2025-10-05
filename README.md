# 🌟 GigGlobal - Freelance Marketplace Platform

<div align="center">
  <br/>
  <p><em>A comprehensive microservices-based freelance marketplace platform built with modern technologies</em></p>
</div>

## 🏗️ Architecture Overview

GigGlobal is a full-stack freelance marketplace application built using a microservices architecture pattern. The platform consists of multiple independent services that communicate with each other to provide a seamless user experience for both freelancers and clients.

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 18 with TypeScript
- **Styling**: Tailwind CSS + SCSS
- **State Management**: Redux Toolkit with Redux Persist
- **Build Tool**: Vite
- **UI Components**: Headless UI
- **Real-time Communication**: Socket.IO Client
- **Form Validation**: Yup
- **HTTP Client**: Axios
- **Routing**: React Router DOM v6
- **Icons**: React Icons
- **Rich Text Editor**: React Quill
- **PDF Generation**: React PDF Renderer
- **Payment Processing**: Stripe React
- **Monitoring**: Elastic APM RUM

### Backend Services
- **Language**: TypeScript/Node.js
- **Framework**: Express.js
- **Process Manager**: PM2
- **Authentication**: JWT + bcrypt
- **Real-time Communication**: Socket.IO
- **Message Queue**: RabbitMQ
- **API Gateway**: Custom Express Gateway
- **Logging**: Winston + Pino
- **Testing**: Jest
- **Code Quality**: ESLint + Prettier

### Databases
- **Authentication**: MySQL
- **User Data**: MongoDB
- **Reviews**: PostgreSQL
- **Caching**: Redis
- **Search & Analytics**: Elasticsearch

### DevOps & Infrastructure
- **Containerization**: Docker & Docker Compose
- **Monitoring**: Kibana Dashboard
- **Load Balancing**: Built-in with PM2
- **Development**: Hot reload with nodemon

## 🏛️ Microservices Architecture

The platform is divided into 8 core microservices, each handling specific business logic:

### 🔐 [Gateway Service](https://github.com/Sumaniac28/gigglobal-gateway)
**Language**: TypeScript
- API Gateway and request routing
- Authentication middleware
- Security and rate limiting
- WebSocket connections management

### 📧 [Notification Service](https://github.com/Sumaniac28/gigglobal-notification)
**Language**: EJS/TypeScript
- Email notifications
- Real-time notifications
- Notification templates
- Queue management

### 🔑 [Authentication Service](https://github.com/Sumaniac28/gigglobal-auth)
**Language**: TypeScript
- User registration and login
- Token management
- Password reset functionality
- OAuth integration

### 👥 [Users Service](https://github.com/Sumaniac28/gigglobal-users)
**Language**: TypeScript
- User profile management
- Seller/Buyer profiles
- Profile verification
- User statistics

### 💼 [Gig Service](https://github.com/Sumaniac28/gigglobal-gig)
**Language**: TypeScript
- Gig creation and management
- Category management
- Search and filtering
- Gig analytics

### 💬 [Chat Service](https://github.com/Sumaniac28/gigglobal-chat)
**Language**: TypeScript
- Real-time messaging
- Conversation management
- File sharing
- Message history

### 📦 [Order Service](https://github.com/Sumaniac28/gigglobal-order)
**Language**: TypeScript
- Order processing
- Payment integration
- Order tracking
- Delivery management

### ⭐ [Review Service](https://github.com/Sumaniac28/gigglobal-review)
**Language**: TypeScript
- Rating and review system
- Review moderation
- Seller reputation management
- Review analytics

## 🚀 Quick Start

### Prerequisites
- Node.js (v18+)
- Docker & Docker Compose
- Git

### 1. Clone the Repository
```bash
git clone https://github.com/Sumaniac28/gigglobal-client.git
cd gigglobal-client
```

### 2. Setup Infrastructure
```bash
cd volumes
docker-compose up -d
```

### 3. Start Client Application
```bash
cd client
npm install
npm run dev
```

### 4. Start Services
Each service needs to be cloned and started individually. Refer to individual service repositories for specific setup instructions.

## 🌐 Service Repository Links

| Service | Repository | Language | Description |
|---------|------------|----------|-------------|
| Gateway | [gigglobal-gateway](https://github.com/Sumaniac28/gigglobal-gateway) | TypeScript | API Gateway and routing |
| Notification | [gigglobal-notification](https://github.com/Sumaniac28/gigglobal-notification) | EJS | Email and real-time notifications |
| Authentication | [gigglobal-auth](https://github.com/Sumaniac28/gigglobal-auth) | TypeScript | User authentication |
| Users | [gigglobal-users](https://github.com/Sumaniac28/gigglobal-users) | TypeScript | User profile management |
| Gigs | [gigglobal-gig](https://github.com/Sumaniac28/gigglobal-gig) | TypeScript | Gig management |
| Chat | [gigglobal-chat](https://github.com/Sumaniac28/gigglobal-chat) | TypeScript | Real-time messaging |
| Orders | [gigglobal-order](https://github.com/Sumaniac28/gigglobal-order) | TypeScript | Order processing |
| Reviews | [gigglobal-review](https://github.com/Sumaniac28/gigglobal-review) | TypeScript | Rating and reviews |
| Client | [gigglobal-client](https://github.com/Sumaniac28/gigglobal-client) | TypeScript | Frontend application |

## 📊 Infrastructure Services

### Databases
- **Cache Storage**: Fast data access and session management
- **Document Database**: Flexible data storage for most services
- **Relational Database**: Structured data for authentication
- **Analytics Database**: Review and rating data storage

### Message Queue
- **Message Broker**: Inter-service communication and task queuing

### Search & Analytics
- **Search Engine**: Full-text search and data indexing
- **Analytics Dashboard**: System monitoring and data visualization

## 🔧 Development

### Code Quality
- **ESLint**: Linting for TypeScript/JavaScript
- **Prettier**: Code formatting
- **Jest**: Unit and integration testing

### Development Commands
```bash
# Client
npm run dev          # Start development server
npm run build        # Build for production
npm run lint:fix     # Fix linting issues
npm run prettier:fix # Format code

# Services
npm run dev          # Start with hot reload
npm run build        # Build TypeScript
npm run test         # Run tests
npm start           # Start with PM2
```

## 📁 Project Structure

```
GigGlobal/
├── client/                 # React frontend application
├── server/                 # Backend microservices
│   ├── 1-gateway-service/
│   ├── 2-notification-service/
│   ├── 3-auth-service/
│   ├── 4-users-service/
│   ├── 5-gig-service/
│   ├── 6-chat-service/
│   ├── 7-order-service/
│   ├── 8-review-service/
│   └── 9-gigglobal-helper/
├── volumes/               # Docker compose and configurations
└── apiCalls/             # API testing files
```

## 🚦 Service Communication

Services communicate through:
- **HTTP APIs**: RESTful endpoints for CRUD operations
- **WebSocket**: Real-time features (chat, notifications)
- **RabbitMQ**: Asynchronous message passing
- **Redis**: Shared session and cache storage

## � Monitoring & Logging

- **Application Performance Monitoring**: Real-time application health monitoring
- **Centralized Logging**: Structured logging across all services
- **Data Visualization**: Interactive dashboards for system metrics
- **Log Analysis**: Advanced search and filtering capabilities

## 📄 License

This project is private and proprietary.

## 👨‍💻 Developer

**Sumit Grover**
- GitHub: [@Sumaniac28](https://github.com/Sumaniac28)

---

<div align="center">
  <p>Built with ❤️ using modern web technologies</p>
</div>
