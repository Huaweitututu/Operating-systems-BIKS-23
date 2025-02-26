# Опишіть набір базових дій в встановленому Вами гіпервізорі (Станіслав Рубель)

## Creating a new virtual machine (VM)
1. In the main VirtualBox window, click the "New" button.
 ![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_15-09-44.png)
2. Specify a name for the VM "linux", select the OS type Linux and the distribution Ubuntu.
 ![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_16-05-58.png)
3. Set the amount of RAM (2-4 GB is recommended for a basic configuration with a graphical shell).
 ![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_15-11-24.png)
4. Create a virtual hard disk:
5. Select the creation of a new disk.
6. Select the type (VDI), size (for example, 20 GB) and the allocation type (dynamic or fixed).
7. Click "Create".

## Вибір/додавання доступного для віртуальної машини обладнання
Select the VM, click "Settings." In "System," set CPU (e.g., 2 cores) and enable VT-x/AMD-V. In "Display," set 128 MB video memory and enable 3D acceleration. In "Storage," add an ISO (e.g., Ubuntu) to the virtual drive, then click "OK."

## Налаштування мережі та підключення до точок Wi-Fi
Go to "Settings," "Network," enable the adapter. Choose "NAT" for simple internet or "Bridged Adapter" for Wi-Fi, selecting the host’s Wi-Fi adapter (e.g., "Wi-Fi"). Click "OK," start the VM, and configure the guest OS network.

## Можливість роботи з зовнішніми носіями (flash-пам’ять)
Plug in a USB drive, start the VM, go to "Devices" > "USB," select the drive (e.g., "SanDisk USB 3.0"), and attach it. Access it in the guest OS (e.g., "/media/username/"). Detach via "Devices" > "USB" by unchecking it.

# Встановлення GNU/Linux із графічною оболонкою (Ubuntu 22.04 LTS) (Назар Видиборець)
1) Download the ISO from the official site.
![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_15-28-21.png)
2) Start the VM with the mounted Ubuntu ISO image.
3) In the bootloader, select "Install Ubuntu".
4) After the installation is complete, reboot the VM.

## Встановлення графічної оболонки GNOME
1) In the terminal:
![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_17-17-25.png)
2) Reboot the VM:
![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_17-17-49.png)
3) After rebooting, the GNOME GUI will appear.
![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_17-30-24.png)

## Встановлення другої графічної оболонки (наприклад, XFCE)
1) In the terminal:
![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_17-22-25.png)
2) Click "Log Out" in the top menu of GNOME.
3) On the GDM screen, select "XFCE" from the sessions menu.
4) Enter the password - and here you are in XFCE!
![alt text](https://github.com/Huaweitututu/Operating-systems-BIKS-23/blob/main/image_2025-02-26_17-31-18.png)

## Порівняння можливостей GNOME і XFCE (Святослав Чернуцький)
### GNOME:
- Сучасний, інтуїтивний інтерфейс із підтримкою жестів і розширень.
- Вимагає більше ресурсів (оперативна пам’ять ~1-2 ГБ).
- Підходить для повноцінних робочих станцій із акцентом на дизайн і зручність.
### XFCE:
- Легкий і швидкий (оперативна пам’ять ~500 МБ).
- Менш функціональний, але легко налаштовується.
- Ідеальний для старих машин або мінімалістичних систем.

## XFCE vs GNOME: Порівняння робочого середовища

| Feature             | XFCE                                      | GNOME                                      |
|---------------------|-----------------------------------------|-------------------------------------------|
| **Resource Usage**  | 200-500 MB RAM, low CPU load           | 800+ MB RAM, moderate CPU usage          |
| **Speed**          | Very fast, optimized for older PCs      | Moderate, better on modern hardware      |
| **User Interface**  | Traditional, Windows-like layout       | Modern, minimalist with Activities       |
| **Customization**   | Highly flexible (panels, themes)       | Limited (needs extensions for depth)     |
| **Functionality**   | Core features, extendable with tools   | Rich ecosystem, integrated apps          |
| **Wayland Support** | Limited (X11 primary)                 | Full native support                      |
| **Stability**       | Extremely stable, infrequent updates   | Mostly stable, occasional breakage       |
| **Learning Curve**  | Easy, intuitive for beginners         | Steeper, unique workflow                 |
| **Appearance**      | Simple, functional design             | Polished, visually appealing             |
| **Hardware Acceleration** | Basic support (optional)        | Strong support (3D, GPU-friendly)       |
| **Community Support** | Smaller, dedicated community        | Large, active community                 |
| **Best For**       | Low-spec systems, classic desktop fans | Modern setups, aesthetic-focused users   |

