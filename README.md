# 🍽️ MessMate - Your Digital Mess Companion

<div align="center">

![MessMate Logo](https://img.shields.io/badge/MessMate-🍽️-orange?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyIDJMMTMuMDkgOC4yNkwyMCA5TDEzLjA5IDE1Ljc0TDEyIDIyTDEwLjkxIDE1Ljc0TDQgOUwxMC45MSA4LjI2TDEyIDJaIiBmaWxsPSIjRkY2QjM1Ii8+Cjwvc3ZnPgo=)

**A Revolutionary Mess Hall Experience for SRM Students**

[![React](https://img.shields.io/badge/React-18.2.0-61DAFB?style=flat-square&logo=react)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-4.4.5-646CFF?style=flat-square&logo=vite)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.3.0-38B2AC?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)
[![Firebase](https://img.shields.io/badge/Firebase-Ready-FFCA28?style=flat-square&logo=firebase)](https://firebase.google.com/)
[![PWA](https://img.shields.io/badge/PWA-Enabled-5A0FC8?style=flat-square&logo=pwa)](https://web.dev/progressive-web-apps/)

[🚀 Live Demo](https://messmatesrm.vercel.app) • [📱 Install PWA](https://messmatesrm.vercel.app) • [🐛 Report Bug](https://github.com/gowthamrdyy/messmate/issues) • [💡 Request Feature](https://github.com/gowthamrdyy/messmate/issues)

</div>

---

## 🌟 What is MessMate?

MessMate is not just another menu app – it's a **revolutionary digital companion** that transforms how SRM students interact with their mess halls. Born from the frustration of never knowing what's for dinner and the joy of discovering your favorite dishes, MessMate brings the future of dining to your fingertips.

### 🎯 The Vision

Imagine walking into your mess hall knowing exactly what's being served, seeing community ratings for each dish, and never missing your favorite meal again. MessMate makes this a reality by combining **real-time menu tracking**, **community-driven ratings**, and **intelligent meal scheduling** into one seamless experience.

---

## ✨ Features That Make MessMate Special

### 🔥 **Quantum Menu Navigation**
- **Live Meal Tracking**: Always know what's being served right now
- **Smart Time Detection**: Automatically shows current or next meal
- **Seamless Navigation**: Swipe through meals and days effortlessly
- **Weekend Scheduling**: Different timings for weekends automatically handled

### 🌟 **Community Rating System**
- **Meal-Specific Ratings**: Rate Tuesday's dinner separately from Wednesday's lunch
- **Real-Time Updates**: See ratings from the entire SRM community
- **Smart Aggregation**: Ratings are contextual to specific meals and days
- **Firebase Integration**: All ratings sync across devices and users

### 💎 **Dual View Modes**

#### 🎮 **Quantum Mode** (Default)
- Futuristic card-based interface
- Live meal indicators with pulsing animations
- Smooth transitions and hover effects
- Perfect for discovering what's available now

#### 📅 **Compact Mode**
- Full day overview in one screen
- All meals (Breakfast, Lunch, Snacks, Dinner) visible
- Ideal for planning your entire day
- Quick meal comparison

### 🎨 **Intelligent Design System**

#### 🌙 **Adaptive Theming**
- **Dark Mode**: Easy on the eyes, perfect for late-night meal planning
- **Light Mode**: Clean and crisp for daytime use
- **System Sync**: Automatically matches your device preference
- **Persistent Choice**: Remembers your preference across sessions

#### 🍕 **Smart Food Emojis**
- **Context-Aware**: Each dish gets the perfect emoji representation
- **Extensive Database**: 100+ food items with custom emoji mapping
- **Visual Recognition**: Instantly identify dishes at a glance
- **Cultural Relevance**: Emojis chosen specifically for Indian cuisine

### 📱 **Progressive Web App (PWA)**
- **Install Anywhere**: Works on phones, tablets, and desktops
- **Offline Support**: Access cached menus even without internet
- **Native Feel**: App-like experience in your browser
- **Auto-Updates**: Always get the latest features seamlessly

### ⭐ **Smart Favorites System**
- **Intelligent Matching**: Finds similar dishes across different days
- **Visual Indicators**: Favorite items highlighted throughout the app
- **Quick Access**: See all your favorites in one dedicated section
- **Persistent Storage**: Never lose your favorite dishes

### 🔍 **Advanced Search & Discovery**
- **Global Search**: Find any dish across all menus instantly
- **Smart Suggestions**: Autocomplete with intelligent matching
- **Quick Stats**: See your dining patterns and preferences
- **Meal Timing Alerts**: Get notified about current meal times

---

## 🏗️ Technical Architecture

### 🚀 **Modern Tech Stack**

```
Frontend Framework: React 18.2.0 with Hooks & Context
Build Tool: Vite 4.4.5 (Lightning-fast development)
Styling: Tailwind CSS 3.3.0 (Utility-first CSS)
Animations: Framer Motion (Smooth, performant animations)
State Management: Zustand (Lightweight, powerful state)
Storage: LocalStorage + Firebase Firestore
PWA: Workbox (Service workers, caching, offline support)
Icons: Lucide React (Beautiful, consistent icons)
```

### 🎯 **Performance Optimizations**

- **Code Splitting**: Lazy-loaded sections for faster initial load
- **Memoization**: React.memo and useMemo for optimal re-renders
- **Virtual Scrolling**: Smooth performance with large menu lists
- **Image Optimization**: Efficient emoji and icon rendering
- **Bundle Analysis**: Optimized chunk sizes and dependencies

### 🔧 **State Management Architecture**

```javascript
// Zustand Store Structure
{
  // UI State
  theme: 'dark' | 'light',
  compactMode: boolean,
  currentTime: Date,
  
  // Navigation State
  selectedMess: 'sannasi' | 'mblock',
  mealNavigation: {
    dayOffset: number,
    mealIndex: number,
    isLive: boolean
  },
  
  // User Data
  favorites: string[],
  
  // Community Data (Firebase)
  ratings: {
    [mealKey]: {
      [itemName]: {
        rating: number,
        count: number,
        lastUpdated: string
      }
    }
  }
}
```

### 🔥 **Firebase Integration**

```javascript
// Rating System Structure
ratings: {
  "sannasi_tuesday_dinner": {
    "Chicken Gravy": {
      rating: 4.2,
      count: 156,
      lastUpdated: "2024-01-15T18:30:00Z"
    },
    "Paneer Butter Masala": {
      rating: 4.0,
      count: 89,
      lastUpdated: "2024-01-15T18:25:00Z"
    }
  }
}
```

---

## 🚀 Getting Started

### 📋 Prerequisites

```bash
Node.js >= 16.0.0
npm >= 8.0.0 or yarn >= 1.22.0
Git
```

### ⚡ Quick Setup

```bash
# Clone the repository
git clone https://github.com/gowthamrdyy/messmate.git
cd messmate

# Install dependencies
npm install

# Start development server
npm run dev

# Open your browser
# Navigate to http://localhost:5173
```

### 🔧 Environment Configuration

Create a `.env.local` file in the root directory:

```env
# Firebase Configuration (Optional - for real-time ratings)
VITE_FIREBASE_API_KEY=your_api_key_here
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=123456789
VITE_FIREBASE_APP_ID=1:123456789:web:abcdef123456

# App Configuration
VITE_APP_NAME=MessMate
VITE_APP_VERSION=2.0.0
VITE_APP_DESCRIPTION=Your Digital Mess Companion
```

### 🏗️ Build for Production

```bash
# Create optimized production build
npm run build

# Preview production build locally
npm run preview

# Deploy to your favorite hosting platform
# (Vercel, Netlify, Firebase Hosting, etc.)
```

---

## 📱 Installation Guide

### 🌐 **Web Browser**
1. Visit [MessMate](https://messmate-srm.vercel.app)
2. Click the install button in your browser's address bar
3. Enjoy the native app experience!

### 📱 **Mobile Devices**

#### iOS (Safari)
1. Open MessMate in Safari
2. Tap the Share button (📤)
3. Select "Add to Home Screen"
4. Tap "Add" to install

#### Android (Chrome)
1. Open MessMate in Chrome
2. Tap the menu (⋮) button
3. Select "Add to Home screen"
4. Tap "Add" to install

### 💻 **Desktop**

#### Chrome/Edge
1. Visit MessMate
2. Click the install icon (⊕) in the address bar
3. Click "Install" in the popup

#### Firefox
1. Visit MessMate
2. Look for the PWA install prompt
3. Click "Install" when prompted

---

## 🎮 User Guide

### 🏠 **Home Screen Navigation**

#### **Quantum Mode** (Default Experience)
```
┌─────────────────────────────────────┐
│  🌟 LIVE: Lunch - Tuesday          │
│  ⏰ 11:30 AM - 1:30 PM             │
├─────────────────────────────────────┤
│  🍛 Biryani              ⭐ 4.5    │
│  🍗 Chicken Gravy        ⭐ 4.2    │
│  🥗 Mixed Vegetables     ⭐ 3.8    │
│  🍚 Steamed Rice         ⭐ 3.9    │
└─────────────────────────────────────┘
   ← Previous    🔴 LIVE    Next →
```

#### **Compact Mode** (Full Day View)
```
┌─────────────────────────────────────┐
│  📅 Tuesday, January 16, 2024       │
├─────────────────────────────────────┤
│  🌅 Breakfast (7:00-9:30)          │
│  🍞 Bread & Butter  🥛 Milk        │
│                                     │
│  🌞 Lunch (11:30-13:30) 🔴 LIVE    │
│  🍛 Biryani ⭐4.5  🍗 Chicken ⭐4.2 │
│                                     │
│  🍪 Snacks (16:30-17:30)           │
│  🫖 Tea & Biscuits                 │
│                                     │
│  🌙 Dinner (19:30-21:00)           │
│  🍝 Pasta  🥗 Salad  🍞 Garlic Bread│
└─────────────────────────────────────┘
```

### ⭐ **Rating System**

#### **How to Rate**
1. Go to Settings → Rate Food
2. Select items from current meal context
3. Rate 1-5 stars ⭐⭐⭐⭐⭐
4. Ratings are instantly shared with community

#### **Understanding Ratings**
- **⭐ 4.5 (156)**: 4.5 stars from 156 community ratings
- **Context-Specific**: Tuesday Dinner ratings ≠ Wednesday Lunch ratings
- **Real-Time**: See updated ratings immediately
- **Community-Driven**: All SRM students contribute

### 💖 **Favorites Management**

#### **Adding Favorites**
- Tap the ❤️ icon next to any dish
- Favorites are highlighted with blue ★ badges
- Access all favorites in the dedicated section

#### **Smart Matching**
- "Chicken Gravy" matches "Chicken Curry"
- Prevents duplicate favorites
- Intelligent dish recognition

### 🔍 **Search & Discovery**

#### **Global Search**
```
Search: "biryani" 
Results:
📅 Tuesday Lunch: Veg Biryani ⭐ 4.2
📅 Friday Lunch: Chicken Biryani ⭐ 4.6
📅 Sunday Lunch: Mutton Biryani ⭐ 4.8
```

#### **Quick Stats**
- Total favorites: 12 items
- Most rated meal: Friday Dinner
- Average community rating: 4.1 ⭐

---

## 🎨 Customization

### 🎭 **Themes**

#### **Dark Mode** (Default)
- Deep blacks and grays
- Orange and blue accents
- Easy on the eyes
- Perfect for evening use

#### **Light Mode**
- Clean whites and light grays
- Vibrant color accents
- High contrast
- Great for daytime

### 🎯 **Personalization**

#### **Mess Selection**
- **Sannasi Mess**: Main campus dining
- **M-Block Mess**: Engineering block dining
- Automatic menu switching
- Separate ratings per mess

#### **View Preferences**
- **Quantum Mode**: Card-based, animated
- **Compact Mode**: Dense, informative
- **Auto-Save**: Preferences persist

---

## 🔧 Development

### 📁 **Project Structure**

```
messmate/
├── public/                 # Static assets
│   ├── manifest.json      # PWA manifest
│   └── icons/             # App icons
├── src/
│   ├── components/        # React components
│   │   ├── ui/           # Reusable UI components
│   │   └── sections/     # Page sections
│   ├── hooks/            # Custom React hooks
│   ├── services/         # API and business logic
│   ├── store/            # State management
│   ├── utils/            # Helper functions
│   └── styles/           # CSS and styling
├── docs/                 # Documentation
└── tests/                # Test files
```

### 🧩 **Key Components**

#### **MealCard.jsx**
```javascript
// Quantum mode meal display
// Features: Live indicators, ratings, favorites
// Animations: Framer Motion transitions
// Performance: Memoized rendering
```

#### **CompactMealView.jsx**
```javascript
// Full day meal overview
// Features: All meals visible, quick navigation
// Layout: Grid-based responsive design
// Optimization: Virtual scrolling for large lists
```

#### **RateFoodModal.jsx**
```javascript
// Community rating interface
// Features: Search, rate, real-time updates
// Backend: Firebase Firestore integration
// UX: Smooth animations, instant feedback
```

### 🔄 **State Management**

#### **Zustand Store Pattern**
```javascript
// Lightweight, TypeScript-friendly
// No boilerplate, direct mutations
// Persistent storage integration
// DevTools support
```

#### **Custom Hooks**
```javascript
// useRating: Async rating operations
// useTheme: Theme management
// useOfflineData: PWA offline support
// useBottomNavigation: Mobile navigation
```

### 🎨 **Styling Architecture**

#### **Tailwind CSS Utilities**
```css
/* Responsive design */
.meal-card {
  @apply bg-white dark:bg-gray-800 
         rounded-xl shadow-lg 
         hover:shadow-xl transition-all
         p-6 m-4;
}

/* Custom animations */
.pulse-live {
  @apply animate-pulse bg-green-500;
}
```

#### **CSS Custom Properties**
```css
:root {
  --color-primary: #ff6b35;
  --color-secondary: #4f46e5;
  --color-success: #10b981;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
}
```

---

## 🚀 Deployment

### 🌐 **Vercel (Recommended)**

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Custom domain
vercel --prod --domain messmate-srm.com
```

### 🔥 **Firebase Hosting**

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login and initialize
firebase login
firebase init hosting

# Build and deploy
npm run build
firebase deploy
```

---

## 🤝 Contributing

### 🎯 **How to Contribute**

1. **Fork the Repository**
   ```bash
   git clone https://github.com/yourusername/messmate.git
   ```

2. **Create a Feature Branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Make Your Changes**
   - Follow the existing code style
   - Add tests for new features
   - Update documentation

4. **Commit Your Changes**
   ```bash
   git commit -m "Add amazing feature"
   ```

5. **Push and Create PR**
   ```bash
   git push origin feature/amazing-feature
   ```

### 📝 **Contribution Guidelines**

#### **Code Style**
- Use ESLint and Prettier configurations
- Follow React best practices
- Write meaningful commit messages
- Add JSDoc comments for functions

#### **Feature Requests**
- Open an issue with detailed description
- Include mockups or wireframes if applicable
- Explain the use case and benefits

#### **Bug Reports**
- Use the bug report template
- Include steps to reproduce
- Provide screenshots if relevant
- Mention browser and device information

---

## 🐛 Troubleshooting

### ❓ **Common Issues**

#### **PWA Installation Problems**
```
Problem: Install button not showing
Solution: 
1. Ensure HTTPS connection
2. Check manifest.json validity
3. Verify service worker registration
4. Clear browser cache and reload
```

#### **Rating System Not Working**
```
Problem: Ratings not saving/loading
Solution:
1. Check Firebase configuration
2. Verify internet connection
3. Clear localStorage data
4. Check browser console for errors
```

#### **Menu Not Loading**
```
Problem: Blank menu or loading forever
Solution:
1. Check network connection
2. Verify menu data structure
3. Clear app cache
4. Try different browser
```

#### **Performance Issues**
```
Problem: App running slowly
Solution:
1. Close other browser tabs
2. Clear browser cache
3. Disable browser extensions
4. Check device memory usage
```

### 🔧 **Debug Mode**

Enable debug mode by adding to localStorage:
```javascript
localStorage.setItem('messmate_debug', 'true');
```

This enables:
- Console logging
- Performance monitoring
- State change tracking
- Error boundary details

---

## 📊 Analytics & Insights

### 📈 **Usage Statistics**

MessMate tracks anonymous usage data to improve the experience:

- **Popular Meals**: Which meals get the most views
- **Rating Trends**: How community ratings change over time
- **Feature Usage**: Which features are most/least used
- **Performance Metrics**: Load times, error rates

### 🎯 **Community Insights**

- **Most Rated Dishes**: Biryani, Chicken Gravy, Paneer Butter Masala
- **Highest Rated Meal**: Sunday Lunch (4.6 ⭐ average)
- **Peak Usage Times**: 11:30 AM, 7:30 PM
- **Favorite Features**: Live meal tracking, Rating system

