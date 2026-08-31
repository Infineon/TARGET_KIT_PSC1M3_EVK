# KIT_PSC1M3_EVK BSP

## Overview

 The PSOC™ Control C1M3 Kit (KIT_PSC1M3_EVK) is based on the PSOC™ Control family of devices. It enables the evaluation and development of applications for the PSOC™ Control C1M3 MCU.

**Note:**



Programming this kit requires installing [SEGGER J-Link software](https://www.segger.com/downloads/jlink/#J-LinkSoftwareAndDocumentationPack).




To use code from the BSP, simply include a reference to `cybsp.h`.

## Features


Kit Features:

- PSOC™ Control C1M3 (ARM® Cortex®-M0 based) Microcontroller in a VQFN48 package
- On board Debugger for downloading and debugging of application code
- Virtual COM port for UART communication with terminal program e.g. Hyperterminal
- 2x30 card edge connector for extension to application card e.g. Colour LED Card and White LED Card
- 4 User LEDs connected to GPIO P4.4, P4.5, P4.6, P4.7
- Variable resistor R122 connected to analog input P2.5
- All the pins of PSOC™ Control C1M3 are accessible via the connector JP101, JP103, JP104 and JP105
- CAN interface with CAN transceiver mounted


Kit Contents:

- KIT_PSC1M3_EVK evaluation board


## BSP Configuration

The BSP has a few hooks that allow its behavior to be configured. Some of these items are enabled by default while others must be explicitly enabled. Items enabled by default are specified in the KIT_PSC1M3_EVK.mk file. The items that are enabled can be changed by creating a custom BSP or by editing the application makefile.

Components:
* Device specific category reference (e.g.: CAT1) - This component, enabled by default, pulls in any device specific code for this board.

Defines:
* CYBSP_WIFI_CAPABLE - This define, disabled by default, causes the BSP to initialize the interface to an onboard wireless chip if it has one.
* CY_USING_HAL - This define, enabled by default in some BSPs, specifies that the HAL is intended to be used by the application. This will cause the BSP to include the applicable header file and to initialize the system level drivers.  Newer BSPs pull in the v3.x HAL, which enables itself via its own makefile, so CY_USING_HAL is not present.
* CYBSP_CUSTOM_SYSCLK_PM_CALLBACK - This define, disabled by default, causes the BSP to skip registering its default SysClk Power Management callback, if any, and instead to invoke the application-defined function `cybsp_register_custom_sysclk_pm_callback` to register an application-specific callback.



See the [BSP Setttings][settings] for additional board specific configuration settings.

## API Reference Manual

The KIT_PSC1M3_EVK Board Support Package provides a set of APIs to configure, initialize and use the board resources.

See the [BSP API Reference Manual][api] for the complete list of the provided interfaces.

## More information
* [KIT_PSC1M3_EVK BSP API Reference Manual][api]
* [KIT_PSC1M3_EVK Documentation](http://www.infineon.com/KIT_PSC1M3_EVK)
* [Infineon Technologies AG](https://www.infineon.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.infineon.com/modustoolbox)

[api]: https://infineon.github.io/TARGET_KIT_PSC1M3_EVK/html/modules.html
[settings]: https://infineon.github.io/TARGET_KIT_PSC1M3_EVK/html/md_bsp_settings.html

---
© 2026, Infineon Technologies AG, or an affiliate of Infineon Technologies AG.