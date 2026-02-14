# 🍽️ Food Bank Supply Chain Management Platform

## Designed by ANSH SHARMA

**AI-Powered Supply Chain Network for Food Recovery and Equitable Distribution**  
*Kozhikode, Kerala, India*

---

## 🌟 Project Overview

A comprehensive, full-stack web application featuring AI/ML-powered demand forecasting and route optimization for food bank operations in Kozhikode. This platform enables efficient food recovery from surplus events, ensures safe handling, and optimizes distribution to verified beneficiaries with minimal waste.

### Key Features

- **🤖 AI-Powered Demand Forecasting**: TensorFlow.js neural network predicting donation inflow and beneficiary outflow
- **🛣️ Route Optimization**: Advanced algorithms for last-mile delivery efficiency
- **📊 Real-time Dashboard**: Live monitoring of supply chain operations
- **📦 Inventory Management**: FEFO/FIFO tracking with spoilage prevention
- **📈 Analytics & Insights**: Comprehensive performance metrics and trend analysis
- **🎨 Beautiful UI**: Industrial supply chain themed interface with stunning visuals

---

## 🛠️ Technology Stack

### Backend
- **Node.js** with Express.js
- **TensorFlow.js** for machine learning models
- **In-memory data store** (production-ready for MongoDB/PostgreSQL integration)

### Frontend
- **Vanilla JavaScript** with Chart.js for visualizations
- **Custom CSS** with industrial supply chain aesthetics
- **Responsive Design** for all devices

### AI/ML Models
- **Demand Forecasting**: Neural network with 8 input features
- **Route Optimization**: K-means clustering + Nearest Neighbor algorithm
- **Location-Allocation**: Optimal hub placement using clustering

---

## 📁 Project Structure

```
foodbank-platform/
├── api/
│   ├── controllers/
│   │   └── apiController.js       # API request handlers
│   ├── models/
│   │   ├── demandForecasting.js   # ML forecasting model
│   │   └── routeOptimization.js   # Route optimization algorithms
│   ├── routes/
│   │   └── index.js               # API routes
│   ├── utils/
│   │   └── dataStore.js           # Data management
│   └── index.js                   # Express server
├── public/
│   ├── css/
│   │   └── styles.css             # Stunning UI styles
│   ├── js/
│   │   └── app.js                 # Frontend application
│   └── index.html                 # Main HTML file
├── package.json                   # Dependencies
├── vercel.json                    # Vercel configuration
└── README.md                      # This file
```

---

## 🚀 Quick Start

### Local Development

1. **Clone the repository**
```bash
git clone <your-repo-url>
cd foodbank-platform
```

2. **Install dependencies**
```bash
npm install
```

3. **Start the development server**
```bash
npm run dev
```

4. **Open your browser**
```
http://localhost:3000
```

---

## 🌐 Deploy to Vercel

### Method 1: GitHub Integration (Recommended)

1. **Push to GitHub**
```bash
git init
git add .
git commit -m "Initial commit - Food Bank Supply Chain Platform"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
```

2. **Deploy on Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Click "New Project"
   - Import your GitHub repository
   - Vercel will auto-detect settings
   - Click "Deploy"

### Method 2: Vercel CLI

1. **Install Vercel CLI**
```bash
npm install -g vercel
```

2. **Deploy**
```bash
vercel
```

3. **Follow the prompts**
   - Set up and deploy: Yes
   - Which scope: Select your account
   - Link to existing project: No
   - Project name: foodbank-platform
   - Directory: ./
   - Override settings: No

4. **Production deployment**
```bash
vercel --prod
```

---

## 🔧 Configuration

### Environment Variables

Create a `.env` file (optional for local development):

```env
PORT=3000
NODE_ENV=production
API_BASE_URL=/api
```

### Vercel Environment Variables

In Vercel dashboard, add:
- `NODE_ENV`: `production`

---

## 📊 API Endpoints

### Dashboard
- `GET /api/dashboard` - Get dashboard data with metrics, donations, and deliveries

### Forecasting
- `GET /api/forecast?days=7` - Get demand predictions for specified days
- `GET /api/model-status` - Get ML model training status

### Route Optimization
- `POST /api/optimize-route` - Generate optimized delivery route
- `GET /api/generate-hubs?numHubs=5` - Generate optimal hub locations

### Inventory
- `GET /api/inventory` - Get current inventory with expiry tracking

### Donations
- `GET /api/donations` - Get all donations
- `POST /api/donations` - Create new donation

### Deliveries
- `GET /api/deliveries` - Get all deliveries
- `POST /api/deliveries` - Schedule new delivery
- `PUT /api/deliveries/:id` - Update delivery status

### Analytics
- `GET /api/analytics?days=7` - Get analytics and trends

### Beneficiaries & Hubs
- `GET /api/beneficiaries` - Get all beneficiaries
- `GET /api/hubs` - Get all food bank hubs

---

## 🤖 AI/ML Models

### Demand Forecasting Model

**Architecture**:
- Input Layer: 8 features (day of week, events, historical demand, weather, etc.)
- Hidden Layers: 64 → 32 → 16 neurons with ReLU activation
- Dropout Layers: 20% dropout for regularization
- Output Layer: 2 neurons (donation inflow, beneficiary outflow)

**Features**:
- Day of week (0-7)
- Week of month (1-5)
- Month (1-12)
- Weekend indicator
- Event count
- Historical average demand
- Weather condition (0-5)
- Seasonal index

**Performance**:
- Training: 30 epochs on 1000 samples
- Validation: 200 samples
- Metrics: MSE loss, MAE
- Typical confidence: 85-90%

### Route Optimization Algorithm

**Method**: Nearest Neighbor with Capacity Constraints

**Features**:
- Vehicle capacity management (100 kg default)
- Haversine distance calculation
- Hub return when capacity exceeded
- Efficiency scoring

**Output**:
- Optimized delivery sequence
- Total distance (km)
- Estimated time (minutes)
- Efficiency score (0-100%)

### Hub Location Optimization

**Method**: K-means Clustering

**Features**:
- Optimal hub placement based on beneficiary density
- Service radius calculation (5 km default)
- Coverage analysis
- Convergence in 50 iterations max

---

## 🎨 Design System

### Color Palette
- **Primary**: #FF6B35 (Vibrant Orange)
- **Secondary**: #004E89 (Deep Blue)
- **Accent**: #F7B801 (Golden Yellow)
- **Success**: #2ECC71 (Green)
- **Warning**: #F39C12 (Orange)
- **Danger**: #E74C3C (Red)

### Typography
- **Display**: Archivo (900 weight for headers)
- **Monospace**: JetBrains Mono (for data and metrics)

### Theme
- Industrial Supply Chain Aesthetic
- Dark Mode with Grain Texture
- Gradient Accents
- Glassmorphism Effects

---

## 📱 Features & Functionality

### Dashboard
- Real-time key metrics
- Recent donation tracking
- Critical inventory alerts
- Scheduled delivery overview
- System status monitoring

### AI Forecast
- 7/14/30 day predictions
- Donation inflow forecasting
- Beneficiary demand prediction
- Confidence scores
- Interactive charts

### Route Optimizer
- Hub selection
- Optimized delivery sequence
- Distance and time calculations
- Efficiency metrics
- Hub location analysis

### Inventory Management
- FEFO/FIFO tracking
- Expiry date monitoring
- Status indicators (critical/warning/good)
- Real-time stock levels
- Spoilage prevention alerts

### Analytics
- Donation trends
- Delivery performance
- Supply vs demand analysis
- Top donors ranking
- Performance metrics

---

## 🔒 Security Considerations

- Input validation on all API endpoints
- CORS enabled for secure cross-origin requests
- Rate limiting ready for production
- Environment variable protection
- Secure data handling

---

## 🚧 Future Enhancements

- [ ] Database integration (MongoDB/PostgreSQL)
- [ ] User authentication & authorization
- [ ] Real-time notifications (WebSocket)
- [ ] Mobile app (React Native)
- [ ] Google Maps integration
- [ ] SMS/Email alerts
- [ ] Multi-language support
- [ ] Advanced ML models (LSTM, Prophet)
- [ ] Blockchain for supply chain transparency
- [ ] IoT sensor integration

---

## 📖 Value Chain Components

1. **Collection**: Surplus food from events, parties, restaurants
2. **Sorting**: Quality checks and categorization
3. **Safety Checks**: Temperature monitoring, contamination prevention
4. **Storage**: Cold chain management, FEFO/FIFO systems
5. **Dispatch**: AI-optimized routing and scheduling
6. **Last-Mile Delivery**: GPS tracking, proof of delivery
7. **Distribution**: Verified beneficiary delivery

---

## 👨‍💻 Developer

**ANSH SHARMA**

Built with ❤️ for Kozhikode's food security

---

## 📄 License

This project is developed for educational and social impact purposes.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

## 📞 Support

For issues and questions, please open an issue on GitHub.

---

## 🙏 Acknowledgments

- Anthropic Claude for AI assistance
- TensorFlow.js team
- Chart.js team
- Vercel for hosting
- Open source community

---

**Made with AI, Optimized for Impact** 🚀
