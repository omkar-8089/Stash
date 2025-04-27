
# 📱 Stash MVP

> React Native mobile application powered by **Expo**.  
> Ready to run on **Android** and **iOS** simulators or physical devices.

---

## 🚀 Project Setup

### 1. Install Node.js
- Install the latest **LTS version** of [Node.js](https://nodejs.org/).
- Recommended: Node.js `v18.x` or `v20.x`.

Check if installed:
```bash
node -v
```

---

### 2. Install Expo CLI
```bash
npm install -g expo-cli
```

Check if installed:
```bash
expo --version
```

---

### 3. Create Project (already done)
```bash
expo init Stash
```
Choose **blank** template.

Navigate into project:
```bash
cd Stash
```

---

### 4. Install Navigation Libraries
```bash
npm install @react-navigation/native
npm install react-native-screens react-native-safe-area-context react-native-gesture-handler react-native-reanimated
npm install @react-navigation/native-stack
```

Install Expo dependencies:
```bash
expo install react-native-screens react-native-safe-area-context react-native-gesture-handler react-native-reanimated
```

---

### 5. Update `babel.config.js`
Ensure your `babel.config.js` looks like:

```javascript
module.exports = function(api) {
  api.cache(true);
  return {
    presets: ['babel-preset-expo'],
    plugins: ['react-native-reanimated/plugin'],
  };
};
```

---

## 🖥️ Running the App

### Start the development server:
```bash
npm start
```
or
```bash
expo start
```

This will open the **Expo DevTools** in your browser.

---

### 📱 To Run on Android Emulator:
- Install **Android Studio** with **Android SDK**.
- Set environment variables:
  - `ANDROID_HOME`
  - Update `Path` with:
    - `%ANDROID_HOME%\platform-tools`
    - `%ANDROID_HOME%\emulator`
- Confirm by running:
  ```bash
  adb --version
  ```
- In Expo DevTools, press `a` to launch Android Emulator.

---

### 🍏 To Run on iOS Simulator (Mac Only):
- Install Xcode from App Store.
- Ensure Xcode command-line tools are installed.
- Press `i` in Expo DevTools to open iOS Simulator.

---

### 📱 To Run on Physical Device:
- Install **Expo Go** app on your phone.
- Scan the QR code shown in Expo DevTools.
- App will open directly on your device!

---

## ❗ Troubleshooting

- **os.availableParallelism is not a function**  
  → Update Node.js to version 18+.

- **Failed to resolve Android SDK path / adb not recognized**  
  → Install Android Studio and set environment variables properly.

- **Metro bundler stuck or slow**  
  → Press `r` to refresh or `shift + r` for hard reload in Expo DevTools.

---

## 📂 Project Structure

```
/Stash
  /assets             # images, fonts, etc.
  /screens            # app screens
  App.js              # main entry
  app.json            # Expo configuration
  babel.config.js     # babel config
  package.json        # npm dependencies
```

---

## 🔥 Tech Stack

- **React Native** (with Expo)
- **React Navigation** (Stack Navigation)
- **Expo DevTools** for development
- **Android/iOS Emulator** or **Expo Go**

---

# 🎯 Notes
- Use lightweight components wherever possible for faster load times.
- Follow responsive design practices for different device sizes.
- Focus initially on Android testing, then move to iOS polishing if needed.

---

# 📋 License
MIT
