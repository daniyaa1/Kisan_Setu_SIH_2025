# KisanSetu - Smart Farming Companion 🌾

KisanSetu is an intelligent agricultural mobile application designed to support farmers with AI-powered farming guidance, real-time weather insights, pest detection, soil health analysis, and market price tracking.


## Demo Video Link : https://youtube.com/shorts/UDDsZLbjiGw

## Features 🚀

### 🎤 Voice Assistant
- **Multilingual Support**: English, Hindi, and Punjabi
- **AI-Powered Responses**: Integration with Gemini API for intelligent farming advice
- **Text-to-Speech & Speech-to-Text**: Accessible for low-literate users
- **Contextual Guidance**: Farming-specific responses optimized for rural users

### 🌱 Soil Health Module
- **Soil Parameter Input**: pH, organic matter, and nutrient levels (N, P, K)
- **AI-Based Recommendations**: Personalized fertilizer guidance
- **Application Methods**: Step-by-step application instructions
- **Fertilizer Types**: Urea, Superphosphate, Potassium Chloride recommendations

### 🌤️ Weather Insights
- **Real-time Weather**: Current conditions and forecasts
- **Location-based**: Automatic location detection or manual input
- **Weather Alerts**: Push notifications for severe weather
- **Agricultural Advice**: Weather-specific farming recommendations

### 🐛 Pest & Disease Detection
- **Image Upload**: Camera and gallery support
- **AI Analysis**: Gemini Vision API for pest identification
- **Treatment Recommendations**: Preventive measures and remedies
- **Offline Fallback**: Local knowledge base for common issues

### 📈 Market Prices
- **Real-time Prices**: Live crop market data
- **Trending Crops**: Rice, Wheat, Corn, Soybeans, Cotton
- **Price Indicators**: Up/down trends with percentage changes
- **Market Analysis**: Daily insights and recommendations

### 📊 Advisory Dashboard
- **Personalized Insights**: Location and crop-specific advice
- **Integrated Recommendations**: Combines soil, weather, and market data
- **Priority Alerts**: High, medium, and low priority farming tasks
- **Daily Tips**: Farming best practices and seasonal advice

## Technology Stack 💻

### Frontend
- **Framework**: React Native with Expo
- **Language**: TypeScript
- **Styling**: Tailwind CSS with NativeWind
- **Navigation**: Expo Router with bottom tabs

### State Management
- **Query Management**: TanStack React Query
- **Local State**: Zustand
- **Persistence**: AsyncStorage for offline data

### APIs & Services
- **AI**: Google Gemini API (text + vision)
- **Weather**: OpenWeather API
- **Notifications**: Expo Notifications
- **Location**: Expo Location
- **Camera**: Expo Camera & Image Picker

### Development Tools
- **Bundler**: Metro (Expo)
- **Linting**: ESLint with Expo config
- **Type Checking**: TypeScript
- **Code Formatting**: Prettier

## Installation & Setup 🔧

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Expo CLI (`npm install -g @expo/cli`)
- Android Studio or Xcode for device testing

### 1. Clone the Repository
```bash
git clone https://github.com/Tarif-dev/Kisan_Setu_SIH_2025.git
cd SIH2025
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Environment Configuration
```bash
# Copy environment template
cp .env.example .env

# Edit .env file with your API keys
EXPO_PUBLIC_GEMINI_API_KEY=your_gemini_api_key
EXPO_PUBLIC_OPENWEATHER_API_KEY=your_openweather_api_key
```

### 4. Start Development Server
```bash
# Start Expo development server
npm start

# For specific platforms
npm run android  # Android
npm run ios      # iOS
npm run web      # Web
```

## API Configuration 🔑

### Gemini AI API
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create a new API key
3. Add to `.env` file as `EXPO_PUBLIC_GEMINI_API_KEY`

### OpenWeather API
1. Visit [OpenWeather](https://openweathermap.org/api)
2. Sign up and get free API key
3. Add to `.env` file as `EXPO_PUBLIC_OPENWEATHER_API_KEY`

## Project Structure 📁

```
SIH2025/
├── app/                    # App routes and screens
│   ├── (tabs)/            # Tab navigation screens
│   │   ├── index.tsx      # Home/Dashboard
│   │   ├── advisory.tsx   # Advisory screen
│   │   ├── assistant.tsx  # Voice assistant
│   │   ├── market.tsx     # Market prices
│   │   └── settings.tsx   # Settings
│   ├── _layout.tsx        # Root layout
│   ├── soil-health.tsx    # Soil analysis screen
│   └── pest-detection.tsx # Pest detection screen
├── components/            # Reusable components
├── services/             # API services
│   ├── geminiService.ts  # Gemini AI integration
│   ├── weatherService.ts # Weather API
│   └── notificationService.ts # Push notifications
├── stores/               # State management
│   ├── weatherStore.ts   # Weather state
│   └── locationStore.ts  # Location state
├── assets/               # Images and static files
└── globals.css          # Global styles
```

## Features Implementation 🛠️

### Voice Assistant
- Integrated with Gemini AI for intelligent responses
- Supports farming-specific queries
- Text-to-speech for accessibility
- Multilingual support framework

### Soil Health Analysis
- Input validation for soil parameters
- AI-powered fertilizer recommendations
- Visual feedback and guidance
- Application method instructions

### Weather Integration
- Real-time weather data from OpenWeather
- Location-based forecasts
- Agricultural weather advisories
- Severe weather notifications

### Pest Detection
- Camera integration for image capture
- AI-powered pest identification
- Treatment recommendations
- Prevention strategies

### Market Tracking
- Real-time crop price monitoring
- Trend analysis and indicators
- Market insights and recommendations
- Price change notifications

## Deployment 🚀

### Expo Application Services (EAS)
```bash
# Install EAS CLI
npm install -g eas-cli

# Configure EAS
eas login
eas init

# Build for Android
eas build --platform android

# Build for iOS
eas build --platform ios
```

### Manual Build
```bash
# Android APK
npx expo export:embed
npx expo run:android

# iOS
npx expo run:ios
```

## Contributing 🤝

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Development Guidelines 📝

### Code Standards
- Use TypeScript for all new files
- Follow Expo and React Native best practices
- Use functional components with hooks
- Implement proper error handling
- Write farmer-friendly error messages

### Design Principles
- **Accessibility First**: Large buttons, clear icons, simple language
- **Offline Support**: Store data locally when possible
- **Performance**: Optimize for low-end devices
- **Farmer-Centric**: Design for rural users with varying tech literacy

### Testing
```bash
# Lint code
npm run lint

# Type checking
npx tsc --noEmit

# Run on device/simulator
npm start
```

## Troubleshooting 🔧

### Common Issues

**Metro bundler issues:**
```bash
npx expo start --clear
```

**iOS simulator not working:**
```bash
npx expo run:ios --device
```

**Android build errors:**
```bash
cd android && ./gradlew clean && cd .. && npx expo run:android
```

### API Issues
- Verify API keys in `.env` file
- Check internet connectivity
- Ensure API quotas are not exceeded
- Review API documentation for changes

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments 🙏

- **Smart India Hackathon 2025** for the opportunity
- **Google Gemini AI** for intelligent farming guidance
- **OpenWeather** for weather data services
- **Expo Team** for the excellent development platform
- **Farming Community** for valuable feedback and insights

## Contact 📧

- **Project Lead**: [Tarif-dev](https://github.com/Tarif-dev)
- **Repository**: [Kisan_Setu_SIH_2025](https://github.com/Tarif-dev/Kisan_Setu_SIH_2025)
- **Issues**: [GitHub Issues](https://github.com/Tarif-dev/Kisan_Setu_SIH_2025/issues)

---

**Made with ❤️ for farmers by Team SIH2025**
