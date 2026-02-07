# 🚀 Quick Guide: Get Your APK in 5 Minutes

## Method 1: GitHub Actions (FREE - Recommended)

### Step 1: Create GitHub Account
- Go to https://github.com/signup
- Create a free account (takes 2 minutes)

### Step 2: Create New Repository
- Click the "+" icon → "New repository"
- Name it: `wifi-audit-poc`
- Make it Public
- Click "Create repository"

### Step 3: Upload Files
You can either:

**A) Use GitHub Web Interface:**
- Click "uploading an existing file"
- Drag and drop ALL files from this project folder
- Click "Commit changes"

**B) Use Git Commands (if you have Git installed):**
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/wifi-audit-poc.git
git push -u origin main
```

### Step 4: Wait for Build
- Go to "Actions" tab in your repository
- Wait 3-5 minutes for the build to complete
- You'll see a green checkmark when done

### Step 5: Download APK
- Click on the completed workflow
- Scroll down to "Artifacts"
- Download "app-debug.zip"
- Extract to get `app-debug.apk`

---

## Method 2: Install Android Studio (One-Time Setup)

### Step 1: Download Android Studio
- Go to: https://developer.android.com/studio
- Download for Windows (about 1GB)
- Install with default settings (takes 10-15 minutes)

### Step 2: Open Project
- Launch Android Studio
- Click "Open"
- Select this project folder
- Wait for Gradle sync (first time takes 5-10 minutes)

### Step 3: Build APK
- Click: **Build → Build Bundle(s) / APK(s) → Build APK(s)**
- Wait 2-3 minutes
- Click "locate" when build finishes
- APK is at: `app/build/outputs/apk/debug/app-debug.apk`

---

## Method 3: Use Online APK Builder (No Installation)

### Replit (Free, No Download)
1. Go to: https://replit.com
2. Sign up (free)
3. Create new Repl → Import from GitHub
4. Upload project files
5. Run build command
6. Download APK

### Appetize.io
1. Go to: https://appetize.io
2. Upload project as ZIP
3. Build online
4. Download APK

---

## 📱 Installing APK on Your Phone

### Step 1: Transfer APK
- Connect phone to PC via USB
- Copy `app-debug.apk` to phone's Download folder
- Or email it to yourself and download on phone

### Step 2: Enable Installation
- Go to: **Settings → Security**
- Enable: **Install from Unknown Sources**
- Or: **Settings → Apps → Special Access → Install Unknown Apps**
- Allow your file manager or browser

### Step 3: Install
- Open file manager on phone
- Navigate to Downloads
- Tap `app-debug.apk`
- Tap "Install"
- Tap "Open" when done

### Step 4: Grant Permissions
- When you open the app, it will ask for:
  - Location permission (required for WiFi scanning)
  - WiFi state permission
- Tap "Allow" for all permissions

---

## ⚡ Fastest Method Summary

**If you have 15 minutes:**
→ Install Android Studio (Method 2)

**If you want it now without installing anything:**
→ Use GitHub Actions (Method 1)

**If you're tech-savvy:**
→ Use command line with Android SDK

---

## 🆘 Need Help?

### Common Issues:

**"App not installed"**
- Enable "Install from Unknown Sources"
- Make sure you have Android 10 or higher

**"Parse error"**
- APK might be corrupted during transfer
- Re-download or re-transfer the file

**"App keeps crashing"**
- Make sure you granted all permissions
- Check if WiFi is enabled on your device

**"Can't find WiFi networks"**
- Grant Location permission (required for WiFi scanning)
- Enable Location services on your phone

---

## 📞 Quick Support

If you're stuck, the EASIEST method is:
1. Install Android Studio (15 minutes)
2. Open project
3. Click Build → Build APK
4. Done!

The APK will be ready for testing on your mobile device.
