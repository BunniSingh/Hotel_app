# Real Estate Web Application

A modern, responsive real estate web application built with React.js and Firebase Authentication. This application allows users to browse property listings, authenticate, and manage their property searches.

## 🚀 Features

- **Home Page**: Hero section, What We Do cards, Featured Properties, Best Properties (Sale & Rent), Newsletter subscription, Footer
- **Property Listings**: Dynamic property listings fetched from API with filtering capabilities
- **Authentication**: Complete signup/login system with Firebase Authentication
- **Responsive Design**: Mobile-first design using TailwindCSS
- **API Integration**: Real property data from MockAPI
- **User Session Management**: Persistent login state using React Context

## 🛠️ Tech Stack

- **Frontend**: React.js (Functional Components + Hooks)
- **Routing**: React Router DOM
- **Styling**: TailwindCSS
- **Authentication**: Firebase Authentication
- **API**: Axios for HTTP requests
- **State Management**: React Context API
- **UI Components**: Custom components with shadcn/ui
- **Icons**: Lucide React

## 📋 Requirements Met

### Pages Implemented
✅ **Home Page**
- Hero section with banner
- "What We Do" section (4 cards)
- Featured Properties (API data)
- Properties available for sale and rent (API data)
- Newsletter subscription section
- Footer

✅ **Property Listing Page**
- Display list of properties fetched from API
- Filter by property type (sale/rent)
- Search functionality by location

✅ **Signup Page**
- Form with name, email, password, confirm password
- Firebase Authentication integration
- Redirect to login page on success

✅ **Login Page**
- Form with email + password
- Firebase Authentication
- Session storage with Context API
- Redirect to homepage on success

### API Integration
✅ Using required API: `https://68b826bcb715405043274639.mockapi.io/api/properties/PropertyListing`

### Technical Guidelines
✅ React.js with Functional Components + Hooks
✅ React Router for navigation
✅ Firebase Authentication
✅ TailwindCSS for styling
✅ Responsive design (desktop & mobile)
✅ User state management with Context API

## 🔧 Setup Instructions

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd real-estate-app
```

2. **Install dependencies**
```bash
npm install
# or
yarn install
```

3. **Firebase Setup**
   - Create a new Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Enable Authentication and choose Email/Password as sign-in method
   - Copy your Firebase configuration
   - Update `src/lib/firebase.ts` with your Firebase config:

```javascript
const firebaseConfig = {
  apiKey: "your-api-key",
  authDomain: "your-auth-domain",
  projectId: "your-project-id",
  storageBucket: "your-storage-bucket",
  messagingSenderId: "your-messaging-sender-id",
  appId: "your-app-id"
};
```

4. **Start the development server**
```bash
npm run dev
# or
yarn dev
```

5. **Open your browser**
Navigate to `http://localhost:5173` to view the application.

## 🏗️ Project Structure

```
src/
├── components/
│   ├── ui/                 # Reusable UI components (shadcn/ui)
│   ├── Hero.tsx           # Hero section component
│   ├── Navbar.tsx         # Navigation component
│   ├── Footer.tsx         # Footer component
│   ├── PropertyCard.tsx   # Property card component
│   ├── FeaturedProperties.tsx
│   ├── BestProperties.tsx
│   ├── WhatWeDo.tsx
│   ├── ValueProposition.tsx
│   ├── StartJourney.tsx
│   └── Newsletter.tsx
├── pages/
│   ├── Index.tsx          # Main page wrapper
│   ├── Home.tsx           # Home page
│   ├── Properties.tsx     # Property listings page
│   ├── Login.tsx          # Login page
│   ├── Signup.tsx         # Signup page
│   └── NotFound.tsx       # 404 page
├── contexts/
│   └── AuthContext.tsx    # Authentication context
├── lib/
│   ├── firebase.ts        # Firebase configuration
│   ├── api.ts            # API helper functions
│   └── utils.ts          # Utility functions
├── hooks/
│   └── use-toast.ts      # Toast hook
└── App.tsx               # Main App component
```

## 🔥 Firebase Configuration

### Authentication Setup
1. Go to Firebase Console
2. Navigate to Authentication > Sign-in method
3. Enable Email/Password authentication
4. Optionally enable Google, Facebook, or other providers

### Security Rules (Optional)
If using Firestore for additional data:
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

## 📱 Responsive Design

The application is fully responsive and optimized for:
- Desktop (1024px and above)
- Tablet (768px - 1023px)
- Mobile (below 768px)

## 🎨 Design System

- **Colors**: Primary blue theme with semantic color variables
- **Typography**: Inter font family with responsive text scaling
- **Components**: Consistent spacing, shadows, and hover effects
- **Layout**: Grid-based responsive layouts

## 🚀 Deployment

### Vercel (Recommended)
1. Connect your GitHub repository to Vercel
2. Configure build settings:
   - Build Command: `npm run build`
   - Output Directory: `dist`
3. Add environment variables for Firebase config
4. Deploy

### Netlify
1. Connect your GitHub repository to Netlify
2. Configure build settings:
   - Build Command: `npm run build`
   - Publish Directory: `dist`
3. Add environment variables for Firebase config
4. Deploy


## 🔍 API Documentation

### Property API Endpoint
```
GET https://68b826bcb715405043274639.mockapi.io/api/properties/PropertyListing
```

### Property Data Structure
```javascript
{
  "createdAt": "2025-09-02T19:04:31.145Z",
  "name": "Property Name",
  "buildingNumber": "764",
  "cardinalDirection": "South",
  "city": "City Name",
  "country": "Country",
  "countryCode": "HM",
  "latitude": -68.6896,
  "longitude": -9.4525,
  "state": "State",
  "timeZone": "America/Belize",
  "image": "https://picsum.photos/seed/rko0Qcmc/1736/389",
  "ownerName": "Owner Name",
  "contactNumber": "1-839-606-5135 x9492",
  "id": "1"
}
```

## 🧪 Features Overview

### Authentication Features
- User registration with email/password
- User login with email/password
- Password validation and confirmation
- Remember me functionality
- Session persistence
- Protected routes
- Auto-redirect after authentication

### Property Features
- Dynamic property listings from API
- Property search by location/name
- Filter by sale/rent type
- Property cards with images and details
- Contact information display
- Responsive property grid
- Loading states and error handling

### UI/UX Features
- Modern, clean design
- Smooth animations and transitions
- Mobile-responsive layout
- Toast notifications for user feedback
- Loading skeletons
- Hover effects and interactions
- Consistent color scheme and typography

## 📞 Support

For any questions or issues, please refer to the documentation or contact the development team.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

To connect a domain, navigate to Project > Settings > Domains and click Connect Domain.

