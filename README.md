# 🛒 E-Commerce Microservices Platform

A complete, working e-commerce application built with 8 microservices that demonstrates real-world microservices architecture.

## 🎯 What This Is

A fully functional e-commerce platform where users can:
- ✅ Register and login
- ✅ Browse products
- ✅ Add items to cart
- ✅ Place orders
- ✅ View order history
- ✅ Process payments (simulated)

## 🏗️ Architecture (8 Microservices)

1. **Auth Service** (Port 3001) - User authentication and JWT tokens
2. **User Service** (Port 3002) - User profiles and management
3. **Product Service** (Port 3003) - Product catalog and inventory
4. **Cart Service** (Port 3004) - Shopping cart management
5. **Order Service** (Port 3005) - Order processing and management
6. **Payment Service** (Port 3006) - Payment processing (simulated)
7. **Notification Service** (Port 3007) - Email/SMS notifications
8. **Frontend** (Port 3000) - React.js user interface

## 🚀 Quick Start

### Prerequisites
- Docker & Docker Compose

### Run the Platform

```bash
# Start everything
./start.sh

# Or manually:
docker-compose up --build -d
```

### Access the Application

1. **Frontend**: http://localhost:3000
2. **Register** a new account
3. **Browse products** and add to cart
4. **Place orders** and see the full workflow

### Stop the Platform

```bash
docker-compose down
```

## 🛠️ Technology Stack

- **Frontend**: React.js with React Router
- **Backend**: Node.js + Express.js
- **Database**: MongoDB
- **Authentication**: JWT tokens
- **API Communication**: REST APIs with Axios
- **Containerization**: Docker
- **Orchestration**: Docker Compose

## 📱 Features

### User Features
- User registration and authentication
- Product browsing with real data
- Shopping cart functionality
- Order placement and tracking
- Order history
- Responsive web interface

### Technical Features
- Microservices architecture
- Service-to-service communication
- JWT-based authentication
- RESTful APIs
- Docker containerization
- Database per service pattern
- Proper error handling
- CORS enabled for frontend-backend communication

## 🔧 Development

### Local Development (without Docker)

```bash
# Start MongoDB
mongod

# Start each service in separate terminals
cd services/auth-service && npm install && npm start
cd services/user-service && npm install && npm start
cd services/product-service && npm install && npm start
cd services/cart-service && npm install && npm start
cd services/order-service && npm install && npm start
cd services/payment-service && npm install && npm start
cd services/notification-service && npm install && npm start
cd services/frontend && npm install && npm start
```

### Testing the Services

```bash
# Test auth service
curl -X POST http://localhost:3001/register \
  -H "Content-Type: application/json" \
  -d '{"email":"test@example.com","password":"password","name":"Test User"}'

# Test product service
curl http://localhost:3003/products

# Test with authentication
curl -H "Authorization: Bearer YOUR_JWT_TOKEN" http://localhost:3002/profile
```

## 🏭 Production Deployment

This platform is ready for production deployment:

1. **Kubernetes**: Convert Docker Compose to Kubernetes manifests
2. **Cloud Deployment**: Deploy to AWS, Azure, or GCP
3. **Load Balancing**: Add nginx or cloud load balancers
4. **Monitoring**: Add Prometheus, Grafana, and logging
5. **CI/CD**: Integrate with GitHub Actions or similar

## 🎓 Learning Outcomes

This project demonstrates:
- Microservices architecture patterns
- Inter-service communication
- Authentication and authorization
- Database design for microservices
- Frontend-backend integration
- Docker containerization
- RESTful API design
- Error handling and validation

## 🤝 Perfect For

- DevOps portfolios
- Microservices learning
- Job interviews
- Production deployment practice
- Architecture demonstrations

## 🚨 Troubleshooting

### Common Issues

```bash
# Port conflicts
lsof -i :3000-3007

# Check Docker containers
docker-compose ps

# View logs
docker-compose logs -f [service-name]

# Reset everything
docker-compose down -v
docker-compose up --build -d
```

---

**🎉 You now have a complete, working e-commerce platform with 8 microservices!**

This demonstrates real-world microservices architecture and is perfect for your DevOps portfolio.
