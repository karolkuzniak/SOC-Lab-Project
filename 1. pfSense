## 🌐 **pfSense Setup**  

### **Download pfSense**  

1. **Visit the Official pfSense Website**:  
   Go to the official website and download the latest stable version of **pfSense Community Edition**.
   
![Zrzut ekranu 2025-01-24 190027](https://github.com/user-attachments/assets/14ae2f23-40f2-4bf4-8022-e42a7fffcf84)

---

### **Create the Virtual Machine**  

1. **Create a New Virtual Machine**:  
   - Open **VirtualBox** and create a new VM for pfSense.
   - In the **Network** settings, enable **3 Network Adapters** for different zones:
     - **RED Card**: External network (WAN).
     - **GREEN Card**: Internal network (LAN).
     - **ORANGE Card**: DMZ network.
    
![1](https://github.com/user-attachments/assets/edb9d3a9-cb9f-4dde-a6fe-1f8ca5b712a7)

   
2. **Note the MAC Addresses**:  
   - Make a note of the MAC addresses for each adapter as they will be useful for the configuration later.

---

### **Install pfSense**

1. **Start the VM**:  
   - After creating the virtual machine, start it up and **mount the pfSense ISO** image when prompted.
  
![2](https://github.com/user-attachments/assets/09b4f904-e856-466d-8445-a6fdc35d8193)

![3](https://github.com/user-attachments/assets/8d94036b-92bd-4e1f-b26e-bff1168d5830)


2. **Installation Process**:  
   - Accept the **Copyright and Trademark Notices**.
   - Select **Install** to begin the installation process.
   - Use the **default keymap** during installation.
   - For partitioning, use the **default options** (since this is a lab environment, no encryption or mirroring is necessary).
   - Allow the system to complete the installation and **reboot** once done.

![4](https://github.com/user-attachments/assets/bf9b4667-c0ec-4d7f-b287-467befbb48a2)

![7](https://github.com/user-attachments/assets/ce395c12-41b2-4a27-8a96-728d0d7f7d06)

![9](https://github.com/user-attachments/assets/509cc292-f2ef-473a-96d9-d9bc85d1b917)


3. **No Manual Configuration**:  
   - Skip manual configuration after installation. The system will automatically proceed.

---

### **Configure pfSense Interfaces**

1. **Interface Configuration**:  
   - Upon reboot, you’ll be presented with the pfSense interface configuration menu. Select **Option 1** to configure interfaces.

2. **Assign the Interfaces**:  
   - The system will display the MAC addresses of the network interfaces. Match the interfaces to the following:
     - **RED Interface (WAN)**: Select the first network adapter (external network).
     - **GREEN Interface (LAN)**: Select the second network adapter (internal network).
     - **ORANGE Interface (DMZ)**: Select the third network adapter (DMZ network).

3. **Confirm Configuration**:  
   - After selecting the interfaces, confirm the changes by pressing **Enter**.

---

### **Assign IP Addresses**

1. **Assign IP Addresses to Interfaces**:  
   - Select **Option 2** to configure the IP addresses.
   - **WAN (RED)**: Leave this as **DHCP** so it can automatically obtain an IP address from the external network.
   - **LAN (GREEN)**: Select **Option 2** to configure the LAN interface and assign a static IP and subnet mask (e.g., `192.168.1.1/24`).
   - **DMZ (ORANGE)**: Leave this without a gateway and assign an appropriate IP in a different subnet (e.g., `192.168.2.1/24`).

2. **Final Confirmation**:  
   - Once IP addresses are configured, confirm and **save** the changes.

---

### **Reboot and Test the Configuration**

1. **Reboot pfSense**:  
   After the interfaces are configured, the system may ask you to **reboot**. Ensure the configuration is saved and reboot the system.

2. **Access pfSense Web Interface**:  
   - You can access the pfSense web interface by typing the IP address of the **LAN interface** (`192.168.1.1` or whatever you set) in a browser.

---

### **Final Notes**:  
This pfSense setup will provide the core network firewall and routing functionality for the lab, allowing network segmentation between the WAN, LAN, and DMZ networks.
