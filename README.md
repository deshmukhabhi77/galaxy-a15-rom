# galaxy-a15-rom
Custom Android ROM and Recovery for Samsung Galaxy A15 5G, optimized for improved performance, resource efficiency, and system stability. Includes a custom recovery for firmware flashing, backup, and system restore.

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

- **Recovery (TWRP 3.7.1_12)**: [twrp-3.7.1_12-a15x.tar](./twrp-3.7.1_12-a15x.tar)
- **VBMeta**: [vbmeta.img](./vbmeta.img)
- **ROM**: [Download ROM from Google Drive](https://drive.google.com/file/d/1ZE5LAfxngbJp6IZ3JcKTV9mVyHiXMyqT/view?usp=sharing)

---

## 🛠️ Installation Instructions

1. **Unlock Bootloader**:
   - Enable Developer Options: Settings > About phone > Tap "Build number" 7 times.
   - Enable OEM Unlocking and USB Debugging: Settings > Developer options.
   - Connect your device and run:
     ```bash
     adb reboot bootloader
     fastboot oem unlock
     ```

2. **Flash Custom Recovery**:
   ```bash
   fastboot flash recovery twrp-3.7.1_12-a15x.tar

   
## 🚀 Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/galaxy-a15-rom.git
