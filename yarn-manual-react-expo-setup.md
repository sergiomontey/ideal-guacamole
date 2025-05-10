# 🛠 React Expo TypeScript Setup on macOS (Yarn without Homebrew)

This guide walks you through manually setting up a macOS environment for developing React Native apps using **Expo with TypeScript**, using **Yarn (via npm)** and no Homebrew.

---

## 1. ✅ Install Node.js (Manually)

- Visit [https://nodejs.org](https://nodejs.org)
- Download the **LTS macOS Installer (.pkg file)**
- Open the file and follow the instructions to install

After installation, verify in Terminal:

```bash
node -v
npm -v
```

---

## 2. 🧶 Install Yarn (Using npm)

Install globally:

```bash
npm install -g yarn
```

Verify:

```bash
yarn -v
```

---

### ⚠️ Important Reminder

**Never run `npm install` or other npm commands with `sudo` unless absolutely necessary.**  
Doing so can create root-owned files that cause permission errors in the future.

---

## 3. 📦 Install Expo CLI (Optional Global Install)

Learn more at: [https://docs.expo.dev/more/expo-cli/](https://docs.expo.dev/more/expo-cli/)

📌 **Recommended:** Use `npx` directly without installing globally.

Start your app using:

```bash
npx expo start
```

If you still prefer a global installation (not recommended):

```bash
npm install -g expo-cli
```

---

## 4. 🧑‍💻 Install Xcode

- Open the **Mac App Store**
- Search for **Xcode** and install it
- Launch Xcode once and accept the license agreement

Install CLI tools:

```bash
xcode-select --install
```

---

## 5. 🤖 Install Android Studio

Download from: [https://developer.android.com/studio](https://developer.android.com/studio)

During setup, make sure to install:

- Android SDK  
- Android Emulator  
- Android SDK Command-line Tools

After install:

- Open Android Studio → Preferences → Appearance & Behavior → System Settings → Android SDK
- Note the SDK location (usually: `~/Library/Android/sdk`)

---

## 6. 🛠 Create `.zshrc` File and Set Android Emulator Path

a. Create the file (if it does not exist):

```bash
touch ~/.zshrc
```

b. Open it in a text editor:

```bash
open -a TextEdit ~/.zshrc
```

c. Add the following lines:

```bash
# Android SDK Path
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
```

d. Save and apply the changes:

```bash
source ~/.zshrc
```

---

## 7. 📱 Set Up Android Emulator

- Open Android Studio → Device Manager → Create Virtual Device
- Choose a device (e.g., Pixel 6)
- Download and install a system image (e.g., Android 13)
- Start the virtual device

Verify emulator is running:

```bash
adb devices
```

---

## 8. 🚀 Create and Run a Sample Expo App

```bash
npx create-expo-app myApp -t
cd myApp
npx expo start
```

Use:
- Press `i` to open iOS simulator (if Xcode installed)
- Press `a` to open Android emulator (if running)

---

🎥 For a full video walkthrough, check out the [MonteyCodes YouTube Channel](https://www.youtube.com/@MonteyCodes)
