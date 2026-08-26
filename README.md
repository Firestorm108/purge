# purge
**Purge** is a fully open source wireless inductively coupled plasma cleaner consisting of three isolated PCBs and a vacuum chamber: the external user-control board, STM32 based motherboard, and the spark generator/ICP driver.

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
