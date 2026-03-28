---
layout: default
title: Tensor USBDL Unbrick guide
nav_order: 1
has_children: false
---

---

# Pre requirements

Follow each step carefully.
Ensure you have the ADB/Fastboot drivers installed on your PC.
---
## Unbrick steps

~~~mermaid
flowchart TD
    A[Connect the device via USB while holding Power and Volume Down.] --> B["Pixel ROM Recovery/COM port visible in device manager."]
    B -->|Yes| C[Right click run.ps1 and run with Powershell]
    B -->|No| D[Disconnect and try again]
    D --> A
    C --> E{"Select your device:"}
    E -->|"Pixel 7 Series(Tensor G2)"| F[gs201]
    E -->|Pixel 8| G[gs301/shiba]
    E -->|Pixel 8 Pro| H[gs301/husky]
    F --> I[Wait until you see Acknowleged BL3B]
    G --> I 
    H --> I
    I --> M
    M{Device state: Error!} -->|yes| J["Wait patiently few hours(recommended to leave it for night) until you see fastboot screen"]
    M -->|No| N[Flash stock ROM]
    N --> P[Reboot and enjoy fixed device]
    J --> K[Disconnect device from PC and connect to charger for another few hours]
    K --> L[Reboot device]
    L --> A

~~~

---


