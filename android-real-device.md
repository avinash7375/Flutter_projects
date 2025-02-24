**real Android device** for running Flutter apps instead of an emulator. This is **faster** and avoids performance issues. Here's how to do it:

---

## **1️⃣ Enable Developer Mode on Your Phone**
1. Open **Settings** on your Android phone.
2. Go to **About phone**.
3. Find **Build number** (usually inside **Software Information**).
4. Tap **Build number** **7 times** to enable **Developer Mode**.
5. You’ll see a message like **"You are now a developer!"**.

---

## **2️⃣ Enable USB Debugging**
1. Go to **Settings** → **System** → **Developer options**.
2. Scroll down and find **USB Debugging**.
3. Turn it **ON**.

---

## **3️⃣ Install ADB (Android Debug Bridge) on Your PC**
ADB (Android Debug Bridge) is needed to communicate with the device.

### **Windows:**
1. Install **Android SDK Platform-Tools** from:
   👉 [https://developer.android.com/studio/releases/platform-tools](https://developer.android.com/studio/releases/platform-tools)
2. Extract the ZIP file (e.g., `C:\platform-tools`).
3. Open **Command Prompt** and navigate to the folder:
   ```sh
   cd C:\platform-tools
   ```
4. Run:
   ```sh
   adb devices
   ```
   If your device appears, you're good to go!

### **Linux (Arch):**
1. Install ADB:
   ```sh
   sudo pacman -S android-tools
   ```
2. Check if your device is detected:
   ```sh
   adb devices
   ```

---

## **4️⃣ Connect Your Device to PC via USB**
1. Plug in your phone using a **USB cable**.
2. On your phone, you might see a **popup**:  
   ➝ **"Allow USB Debugging?"**  
   ➝ Tap **"Allow"**.
3. Run:
   ```sh
   adb devices
   ```
   You should see your phone listed.

---

## **5️⃣ Run Your Flutter App on Your Phone**
1. Open your Flutter project:
   ```sh
   cd my_app
   ```
2. Check available devices:
   ```sh
   flutter devices
   ```
   Your phone should appear in the list.
3. Run the app:
   ```sh
   flutter run
   ```
4. Your app will now open **on your real device**!

---

## **6️⃣ Enable Wireless Debugging (Optional)**
If you don’t want to use a USB cable every time, you can connect wirelessly:

1. Connect your phone and PC to the **same WiFi network**.
2. Enable **Developer Options** → **Wireless Debugging**.
3. Run:
   ```sh
   adb tcpip 5555
   adb connect <device_ip>:5555
   ```
   (Replace `<device_ip>` with your phone’s IP address from Settings → WiFi → Advanced).

Now you can **run and debug wirelessly**!

---

### ✅ **Done! Now you can test your Flutter app on a real phone.**
Need help with anything specific? 🚀
