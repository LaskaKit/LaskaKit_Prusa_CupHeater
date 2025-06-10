Project Průša Cup Heater – A Simple Cup Heater for Schools and Enthusiasts
----------------------------------------------------------------------

The **Průša Cup Heater** project is designed primarily for schools, hobby clubs, and groups, but it is also suitable for adult makers and electronics hobbyists. The aim is to create a simple, easy-to-use heater for coffee or tea that utilizes readily available components and is therefore suitable even for beginners.

Basic Components and Their Functions
------------------------------------

*   **3D-printed enclosure** – serves as the base for assembling the project (recommended materials: PETG, ASA, ABS, PC-ABS, or similar).
    
*   **Heatbed tile** – a heating pad originally intended for Průša XL 3D printers.
    
*   **microESPswitch board with ESP32-C3** – a small board with powerful transistors for switching up to four loads (such as the heating pad) using GPIO pins (CH0 to CH3, e.g., GPIO0, GPIO1, GPIO4, GPIO5).
    
*   **DS18B20 temperature sensor** – a digital sensor for measuring temperature, connected via GPIO3.
    
*   **OLED display** – shows the current temperature and system status, connected via the I2C bus (SDA – GPIO18, SCL – GPIO19).
    
*   **Power supply** – thanks to the USB PD chip, the system can be powered at 15V or 20V via a USB-C connector.
    

How the Project Works
---------------------

The **microESPswitch** board allows easy control of up to four loads thanks to its powerful transistors. For connecting peripherals (such as the OLED display), an uŠup connector is available for I2C and SPI communication. The DS18B20 temperature sensor is attached to the heating pad, and the heating pad is connected to channel CH3 (controlled by GPIO5).

The sample code uses the **WiFiManager** library, which creates its own WiFi hotspot after startup. The user connects with a mobile phone and easily sets the desired pad temperature via the browser. The system maintains the temperature within the set range (e.g., 55–65°C) and automatically regulates power according to the current temperature.

LED Indication and Control
--------------------------

*   **White LED** – device is not connected to WiFi.
    
*   **Green LED** – device is connected to WiFi and ready to use.
    
*   **Blue LED** – heater is off.
    
*   **Red LED** – heater is on.
    

The OLED display shows the current temperature, heater status, and other useful information. All functions can be controlled via the web interface or directly on the board.

Assembly and Modifications
--------------------------

The project requires soldering from a USB adapter that supports 15V or 20V and assembly according to the included instructions. The finished program is available on GitHub and can be freely modified according to the user's needs.

> **Tip:** If you want to use the project at school or in a club, we recommend following the instructions and using the prepared sample code, which is optimized for easy operation and simple modifications.

**Sources and Links:**

*   **Code on GitHub:** [LaskaKit/LaskaKit\_Prusa\_CupHeater](https://github.com/LaskaKit/LaskaKit_Prusa_CupHeater)
    
*   **Manual (PDF):** [Tutorial\_CupHeater.pdf](https://github.com/LaskaKit/LaskaKit_Prusa_CupHeater/blob/main/Tutorial_CupHeater.pdf)
    
*   **Original idea:** @KutilDomaci and @Martin\_Velisek on X/Twitter
    

The **Průša Cup Heater** project is an ideal choice for teaching electronics, programming, and automation in schools and clubs, as well as for home enthusiasts who want to experiment with modern technologies.
