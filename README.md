# purge
**Purge** is a fully open source wireless inductively coupled plasma cleaner consisting of three isolated PCBs; the external user-control board, STM32 based motherboard, spark generator/ICP driver, and a vaccum chamber.

# PCB & Assembly
<img width="402" height="432" alt="Screenshot 2026-08-26 at 1 35 50 PM" src="https://github.com/user-attachments/assets/ba371e15-7a31-40f3-8946-8c971e7ddf92" />
<img width="400" height="332" alt="Screenshot 2026-08-26 at 3 20 42 PM" src="https://github.com/user-attachments/assets/1ea39bca-b1df-4f6a-9ace-787dd37b65d8" />

<img width="400" height="612" alt="Screenshot 2026-08-26 at 2 14 10 PM" src="https://github.com/user-attachments/assets/d893ec3a-6273-4693-b3ea-e933ad8c33d5" />
<img width="400" height="565" alt="Screenshot 2026-08-26 at 3 26 43 PM" src="https://github.com/user-attachments/assets/84effc23-75ec-49e8-bae5-cf887f458ca7" />

# The Process

**Purge** is a specialized type of plasma cleaner. There are **zero** electrodes in the vacuum chamber, meaning the sterility levels are very high, atomically sterile even. There are three stages to the process.

<h3>Stage 1: Chamber Prep</h3>
A 4.5 CFM standard vacuum pump evacuates much of the air inside of the glass dome to 37.5 mTorr. This makes the plasma much easier to form, as there is a reduced gas density. 
The chamber is made up of a custom machined aluminum base and a cheap glass dome you can find on Amazon. There is a slight implosion risk, so it is important you wear proper PPE.

<h3>Stage 2: Plasma Formation</h3>
There are two parts to the plasma formation. Since inductively coupled plasma (ICP) is relatively harder to form than capacitively coupled plasma or direct discharges, simply running the RF through the primary coil may not form the plasma.
To form the plasma, we initiate a short high voltage spark with an external device. In this case, I'm using a high frequency solid state plasma flame generator, similar to the ICP circuit itself. It ionizes some of the gas in the chamber, making
ICP form much easier. The ICP driver powers on after this, and the chamber fills with plasma.

<h3>Stage 3: Adjustment & Control</h3>
You can change the plasma inside the chamber using the built in STM32 interrupter. It allows you to pulse the plasma at any desired frequency within the chip and MOSFETs limits. This can be useful if you are trying to 
do research using the device, or wish to adjust power levels based on the item you are sterilizing.

# Bill of Materials

| Item | Price | Link |
|---|---:|---|
| Control PCB | $10 | JLCPCB |
| Header Pins | $3 | [AliExpress](https://www.aliexpress.us/item/3256801327743339.html) |
| OLED Screen | $4 | [AliExpress](https://www.aliexpress.us/item/3256805954920554.html) |
| 10K Potentiometers | $4 | [AliExpress](https://www.aliexpress.us/item/3256809938132755.html) |
| Push Button | $4 | [AliExpress](https://www.aliexpress.us/item/3256808590713102.html) |
| 3mm Flat Top LEDs | $2 | [AliExpress](https://www.aliexpress.us/item/2251801539552759.html) |
| F-F Jumpers | $2 | [AliExpress](https://www.aliexpress.us/item/2255800018543465.html) |
| ICP Driver PCB + Assembly | $55 | JLCPCB |
| FQA18N50 MOSFETs | $10 | [AliExpress](https://www.aliexpress.us/item/3256811881586105.html) |
| 6kV 33pF Capacitors | $2 | [AliExpress](https://www.aliexpress.us/item/2251832494176278.html) |
| 12AWG Solid Core | $4 | [AliExpress](https://www.aliexpress.us/item/3256808900976117.html) |
| Massive Heatsink | $10 | [AliExpress](https://www.aliexpress.us/item/3256809168389115.html) |
| HFSSTC Module | $24 | [AliExpress](https://www.aliexpress.us/item/3256810369157220.html) |
| 24AWG Solid Core (Inductor Wire) | $7 | [Amazon](https://www.amazon.com/0-2mm%C2%B2-Electrical-Colors-Tinned-breadboard/dp/B09WMQZYXV/) |
| 6AWG Primary Copper | $24 | [Amazon](https://www.amazon.com/99-9-Copper-Diameter-Jewelry-Making/dp/B0CNRT19WB/) |
| Purge Motherboard PCB + Assembly | $80 | JLCPCB |
| 24V → 12V Isolation SMPS | $6 | [AliExpress](https://www.aliexpress.us/item/3256807230654430.html) |
| 24V 10A Power Supply | $30 | [Amazon](https://www.amazon.com/Power-Supply-Adapter-Transformers-Universal/dp/B0D5B33JCH) |
| JLCPCB Customs & Shipping | $91 | JLCPCB |
| 4" × 7" Glass Dome | $30 | [Amazon](https://www.amazon.com/Plymor-Brand-Glass-Display-Cloche/dp/B006XIQGX8/) |
| 4.5 CFM Vacuum Pump | $60 | [Amazon](https://www.amazon.com/VECOTOOLS-Foldable-Automotive-Household-Maintenance/dp/B0GZVLP3PL/) |
| Hosing & Gauge | $28 | [Amazon](https://www.amazon.com/R410A-Recharge-Manifold-Gauge-Set/dp/B0DZ6G6ZBT/) |
| SAE to NPT Adapter | $9 | [Amazon](https://www.amazon.com/uxcell-Fitting-Connector-Conditioner-Refrigeration/dp/B08MZ4TPMZ/) |
| NPT Tap | $7 | [Amazon](https://www.amazon.com/Drill-America-DWTPT1-Qualtech-Carbon/dp/B01DZD1SSQ/) |
| M5 × 100mm Threaded Rods | $10 | [Amazon](https://www.amazon.com/LWCUSNJ-Threaded-M5-0-8mm-Stainless-Threads/dp/B0FHB8P689/) |
| Silicone Caulk | $3 | [Amazon](https://www.amazon.com/White-Acrylic-Latex-Caulk-Silicone/dp/B00GVLHBDG/) |
| Custom Aluminum Base Plate | $50 | JLC CNC |
| Silicone Isolation Feet | $20 | [Amazon](https://www.amazon.com/Isolation-Feet-8Pack-Turntable-Subwoofer-Resonance/dp/B0FX8S3D77) |



**Total: $589**
