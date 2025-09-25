# HomeDeetz Mobile Setup Guide

## Current Mobile Features

The HomeDeetz platform now includes enhanced mobile support with:

### Web Mobile Experience ✅
- **Responsive Design**: Optimized layouts for all screen sizes
- **Mobile Navigation**: Hamburger menu with slide-out drawer
- **Touch Gestures**: Swipe navigation in image carousels
- **Touch-Friendly Buttons**: 44px minimum touch targets
- **Mobile Optimizations**: Smooth scrolling, safe area support
- **Progressive Web App Ready**: Meta tags for mobile browsers

### Native Mobile App (Capacitor) ✅
- **Cross-Platform**: iOS and Android from single codebase
- **Native Performance**: WebView with native capabilities
- **Hot Reload**: Development server integration

## Setting Up Native Mobile Apps

### Prerequisites
- Node.js and npm installed
- For iOS: Mac with Xcode
- For Android: Android Studio

### Step 1: Transfer to GitHub
1. Click the "Export to GitHub" button in Lovable
2. Clone the repository to your local machine
3. Run `npm install` to install dependencies

### Step 2: Add Mobile Platforms
```bash
# Add iOS platform (Mac only)
npx cap add ios

# Add Android platform
npx cap add android
```

### Step 3: Build and Sync
```bash
# Build the web app
npm run build

# Sync with native platforms
npx cap sync
```

### Step 4: Run on Device/Emulator
```bash
# For iOS (requires Xcode)
npx cap run ios

# For Android (requires Android Studio)
npx cap run android
```

### Step 5: Development Workflow
After making changes to your code:
1. Git pull the latest changes
2. Run `npx cap sync` to update native platforms
3. The app will hot-reload from the Lovable development server

## Mobile Features Included

### Touch Interactions
- **Swipe Gestures**: Navigate image carousels with swipe
- **Touch Feedback**: Visual feedback on button presses
- **Smooth Scrolling**: Native-feeling scroll behavior

### Mobile Navigation
- **Hamburger Menu**: Collapsible side navigation
- **Bottom Sheet**: Mobile-friendly dialogs
- **Safe Area Support**: Respects device notches and home indicators

### Performance Optimizations
- **Touch Manipulation**: Optimized touch event handling
- **Lazy Loading**: Images load as needed
- **Responsive Images**: Automatic sizing for different screens

## Configuration Details

The Capacitor configuration (`capacitor.config.ts`) includes:
- **App ID**: `app.lovable.ce992053d96245b8829ac4ffc9c80dcc`
- **App Name**: `home-deetz-insight-hub`
- **Hot Reload**: Connected to Lovable development server
- **Splash Screen**: Branded with HomeDeetz colors

## Troubleshooting

### Common Issues
1. **Build Errors**: Ensure `npm run build` completes successfully
2. **Sync Issues**: Run `npx cap update ios` or `npx cap update android`
3. **Platform Not Found**: Re-run `npx cap add [platform]`

### iOS Specific
- Requires Mac with Xcode installed
- May need to configure signing certificates
- Test on physical device for best results

### Android Specific
- Requires Android Studio and SDK
- Enable Developer Options on test device
- USB debugging must be enabled

## Next Steps

For advanced mobile features, consider adding:
- Push notifications
- Camera integration
- Offline data sync
- App store optimization

Read more about mobile development: https://lovable.dev/blogs/TODO