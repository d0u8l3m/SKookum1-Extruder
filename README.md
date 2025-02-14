<img src="https://github.com/Twotrees3Dofficial/SK1Extruderkit-New-design-with-cutter-function-and-consumable-detection/blob/main/Image/preview.png" width="1000"/>

#  SK1 Extruder kit: New design with cutter function and consumable detection

>The SK1 Extrusion Head Kit is a high-performance extrusion system designed for 3D printers. It integrates the latest hardware and intelligent features to provide higher printing accuracy, ease of use and a flexible modular design. The kit is suitable for a variety of 3D printer users, especially those who need efficient, accurate and stable printing.

## Introduction

<img src="Image/cutter.png" width="500"/>

The SK1 extruder kit was inspired by the user's urgent need to improve printing efficiency and reduce clog. Most printer users will experience the problem of blocked extrusion heads, resulting in print interruptions and difficult maintenance, especially when replacing consumables, requiring manual handling of residual material filaments.To address these challenges SK1 By adopting a newly designed control scheme, SK1 can not only increase the extrusion flow rate and increase the extrusion speed, but also significantly improve the overall stability and accuracy of the printing. Most importantly, the new cutter function greatly simplifies the material return operation, effectively avoiding material residue in the printer and eliminating the problem of extrusion head clogging. A smarter and more reliable extrusion system for high-end users and those who need fast print speeds.

## Usage scenario

<img src="Image/extrusion.png" width="500"/>

- **High-speed printing users:**  The SK1 extruder head significantly increases the extrusion flow rate, and with the enhanced heating block, users can still maintain stable print quality at high-speed printing.
- **Users of flexible materials such as TPU:**  SK1's cutter function and flow compensation technology ensure that materials can be easily returned when handling flexible materials, ensuring smooth printing.
- **Multi-material switching needs users:**  The modular design of the quick disassembly function, so that users can easily maintain the extrusion head, especially when the need to frequently change different types of materials, greatly improving the efficiency of operation.

## Key Features

- **Increased extrusion flow and speed:**  The upgraded extrusion head allows users to print at higher flow rates, accepting up to 37.68mm3/s, while maintaining a stable material flow through a more efficient heating block design and intelligent control.
- **Cutter function:**  The cutter greatly simplifies the material return operation and reduces the blockage problem caused by the material staying in the heating block after tearing. This not only improves the life of the extruder head, but also speeds up the speed of material replacement.
- **Intelligent flow compensation:**  The built-in consumable detector can monitor the use of consumables in real time, and automatically compensate the extrusion flow to ensure that the extrusion is consistent during the printing process, even when the material width error will not affect the printing effect.
- **New PCB control scheme:**  GD32F303 controller: integrated lis2dw gyroscope, improved overall control accuracy, stability and extruder response speed.
- **Modular quick-remove design:**  The simple quick-remove feature allows users to quickly perform routine maintenance or replace modular parts, reducing downtime and significantly improving the user experience.

<img src="Image/detection.png" width="250"/><img src="Image/disassembly.png" width="250"/>

## Hardware Detailsi

<img src="Image/pin.png" width="500"/>

The STL is a model of the sk1 extruder kit, you can download slices from the Hardware/STL path to print them.

<img src="Image/STL.png" width="500"/>

 
## Compatibility

>The SK1 Extruder Kit is compatible with most 3D printers, particularly those using the CoreXY system. For non-CoreXY machines, some additional configurations may be necessary to optimize performance. The cutter and detection function can be adapted to older klipper versions and sk1's existing screen firmware

## How to Use

- **Filament Loading and Unloading:**  The SK1 system includes the filament cutter for quick and easy filament switching. Simply engage the cutter after the print job to cleanly cut the filament.
- **Flow Compensation Calibration:**  Ensure the filament detector is calibrated by running a few test prints. The system will automatically adjust the extrusion based on real-time filament data.
- **Maintenance:**  Use the quick-release feature to remove the extruder for cleaning or replacement of parts. This reduces downtime and allows for faster printer maintenance.

## Calibration
1.	 The offset value is mainly used to calibrate the error between the measured value and the actual value, and the user only needs to modify its configuration file
2.	 Formula converter, mainly used for users who have strong hands-on ability and are not satisfied with the existing calculation algorithm,(not recommended to modify) can use matlab online function to import measurement data into Firmware/Matlab_simulation/Fourier. M refit the function and convert the formula into python language to write the configuration file (can be compatible with math module)
<img src="Image/fourier.png" width="500"/>
3.	  Alpha-Beta filter is mainly used to suppress the mechanical error generated by the acquisition of consumable sensors, and it is a simplified version of a small computational load similar to Kalman filter. We built a pseudo-model that generates random data so that users can debug the appropriate Alpha and Beta values to adjust the sensitivity and noise resistance of the data
<img src="Image/filter.png" width="500"/>
