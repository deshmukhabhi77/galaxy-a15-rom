# Custom Android ROM & Recovery for Samsung Galaxy A15 5G

This project contains a **custom Android ROM and custom recovery** built for the **Samsung Galaxy A15 5G**, focused on **performance, efficiency, and system stability**.  

## ✨ Features
- **Performance Optimizations**: Kernel and system tweaks for smoother multitasking and faster responsiveness.  
- **Custom Recovery**: Flash firmware, perform backups, and restore your device safely.  
- **Resource Efficiency**: Optimized background processes and memory usage for better device longevity.  
- **Reproducible Builds**: Automated build pipeline with Linux shell scripts and Git.  

## 🛠️ Technical Highlights
- Based on **AOSP (Android Open Source Project)** with device-specific modifications.  
- Kernel compilation and device tree customization for Samsung Galaxy A15 5G.  
- Debugging and optimization using profiling and benchmarking tools.  
- Partition and boot image management.  

## 📥 Downloads

- **Recovery (TWRP 3.7.1_12)**: [twrp-3.7.1_12-a15x.tar](https://drive.google.com/file/d/1sMhe4FjR95fkDkZNaZwVXUgeLwJJxN3l/view?usp=sharing)
- **VBMeta**: [vbmeta.img](./vbmeta.img)
- **ROM**: [Download ROM from Google Drive](https://drive.google.com/file/d/1ZE5LAfxngbJp6IZ3JcKTV9mVyHiXMyqT/view?usp=sharing)

---

## 🔓 Unlock Bootloader & Flash TWRP on Samsung Galaxy A15 5G (Using Odin)

**⚠️ Warning:** Unlocking the bootloader will **erase all data** on your device. Back up your data before proceeding. Flashing custom recovery may void your warranty. Proceed at your own risk.

---

### **1. Prerequisites**
- A Windows PC
- Samsung USB drivers installed: [Download here](https://developer.samsung.com/mobile/android-usb-driver.html)
- Odin tool (latest version): [Download here](https://odindownload.com/)
- USB cable
- TWRP recovery `.tar` file for Galaxy A15 5G
- Fully charged phone (≥50%)

---

### **2. Enable Developer Options**
1. Go to **Settings → About Phone → Software Information**  
2. Tap **Build Number** 7 times until you see “Developer mode enabled”.  
3. Go back to **Settings → Developer Options**.  
4. Enable:
   - **OEM Unlocking**
   - **USB Debugging**

---

### **3. Unlock Bootloader**
1. Power off your phone.  
2. Boot into **Download Mode**:
   - Press and hold **Volume Up + Volume Down** simultaneously.  
   - Connect your phone to the PC via USB.  
   - Press **Volume Up** to confirm unlocking the bootloader.  
3. Your phone will erase all data and reboot once unlocking is complete.

---

### **4. Flash TWRP via Odin**
1. Boot your phone into **Download Mode**:
   - Power off → Press **Volume Down + Power** (or Volume Down + Volume Up depending on model).  
   - Press **Volume Up** to continue.  
2. Open **Odin** on your PC.  
3. Connect your phone via USB. Odin should detect your device (ID:COM will turn blue).  
4. Click **AP** in Odin and select the `twrp-3.7.1_12-a15x.tar` file.  
5. Make sure **F. Reset Time** is checked and **Re-Partition** is **unchecked**.  
6. Click **Start** to flash TWRP.  
7. Once completed, Odin will show **PASS!**, and your device will reboot.

---

### **5. Boot into TWRP**
1. Immediately after flashing, boot into TWRP recovery to prevent stock recovery from overwriting it:  
   - Power off → Press **Volume Up + Power** simultaneously.  
2. You are now in TWRP recovery. From here, you can flash VBMeta and your ROM.

---

### **6. Notes**
- Always boot into TWRP first after flashing.  
- Do **not** boot into the system before flashing VBMeta or ROM, as it may overwrite TWRP.  
- Use the **Backup** option in TWRP to create a Nandroid backup before flashing the ROM.


## 🚀 Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/galaxy-a15-rom.git
