To install **Wine** from the official Wine repository, follow these steps. This guide works for **Ubuntu/Debian-based systems**. If you're using a different distro, let me know.  

---

### **Step 1: Enable 32-bit Architecture (if using a 64-bit system)**  
```bash
sudo dpkg --add-architecture i386
```

---

### **Step 2: Add the Wine Repository Key**  
```bash
sudo mkdir -pm755 /etc/apt/keyrings
sudo wget -O /etc/apt/keyrings/winehq-archive.key https://dl.winehq.org/wine-builds/winehq.key
```

---

### **Step 3: Add the Wine Repository**  
For **Ubuntu-based systems** (replace `$(lsb_release -sc)` with your Ubuntu version if needed):  
```bash
sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/$(lsb_release -sc)/winehq-$(lsb_release -sc).sources
```

For **Debian-based systems** (replace `bookworm` with your Debian version if needed):  
```bash
sudo wget -O /etc/apt/sources.list.d/winehq.sources https://dl.winehq.org/wine-builds/debian/dists/bookworm/winehq-bookworm.sources
```

---

### **Step 4: Update and Install Wine**  
```bash
sudo apt update
sudo apt install --install-recommends winehq-stable -y
```

---

### **Step 5: Verify Installation**  
```bash
wine --version
```

---

### **Step 6: Configure Wine (First Time Use)**  
```bash
winecfg
```
This will create the `.wine` directory and install some required packages.

---

### **Step 7: Install Winetricks (Optional, but Recommended)**  
```bash
sudo apt install winetricks -y
```
Winetricks allows installing missing DLLs, fonts, and other Windows components.

---

Now, **Wine** should be fully installed and ready to use. Let me know if you need a version-specific guide or extra details.
