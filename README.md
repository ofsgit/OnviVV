# OnviVV

> **Turning cloud cameras into local cameras.**

OnviVV is an open-source project being developed to transform compatible **cloud-dependent cameras into fully local IP cameras**.

The project is currently in the **development/build stage**. There is **no public build available yet**.

Right now, the focus is on creating the **base system**, researching compatible camera hardware, and developing the core components that OnviVV will eventually use.

## 🚧 Development Status

**Status: 🏗️ Building the Base**

OnviVV is **not ready for installation or general testing yet**.

There is currently:

* No public firmware release
* No public installer
* No stable Web Configuration Interface
* No ready-to-flash image
* No guaranteed hardware compatibility
* No production release

The project is currently focused on building the foundation.

## 🎯 What OnviVV Is

Many inexpensive cameras are designed around a manufacturer's cloud service and mobile application.

OnviVV aims to change that.

```text
        CLOUD CAMERA
             │
             ▼
     Manufacturer Cloud
             │
             ▼
         Mobile App
```

becomes:

```text
          OnviVV
             │
       Local Network
             │
    ┌────────┼─────────┐
    ▼        ▼         ▼
   RTSP    ONVIF     Web UI
    │        │         │
    ▼        ▼         ▼
   NVR     VMS     Configuration
```

The long-term goal is to make the camera function like a **normal local IP camera**.

---

# SoC Support

OnviVV is being developed with support for multiple embedded camera SoC platforms in mind.

| SoC / Platform | Camera Ecosystem          | OnviVV Status  |
| -------------- | ------------------------- | -------------- |
| **Fullhan**    | Various CCTV / IP cameras | **Main Build** |
| **ANKYA**      | V380                      | Planned        |
| **RealTek**    | YooSEE                    | Planned        |
| **Grain**      | YooSEE                    | Planned        |
| **Ingenic**    | Older "Net Cam" cameras   | Planned        |

### Fullhan

**Fullhan** is the primary development platform for OnviVV.

The main OnviVV build will initially focus on compatible Fullhan-based camera hardware, allowing the core system and tooling to be developed around a known target platform.

### ANKYA

**ANKYA** is planned as a target for cameras using the **V380** ecosystem.

### RealTek

**RealTek** is planned for compatible cameras using the **YooSEE** ecosystem.

### Grain

**Grain** is also planned for compatible **YooSEE** cameras.

### Ingenic

**Ingenic** support is planned for older **"Net Cam"** devices and legacy camera hardware.

> **Note:** SoC support does not automatically mean every camera using that SoC will be compatible. Board design, sensor, RAM, flash, bootloader, peripheral hardware, and existing firmware can all affect compatibility. so im focusing of making a very generic image first as the "port".

---

# 🏗️ Current Development

The current development effort is focused on establishing the OnviVV base.

### Base System

* Camera hardware detection
* SoC detection
* System information
* Network initialization
* Camera sensor detection
* Basic service framework
* Configuration system
* Logging system

### Local Camera Services

* RTSP foundation
* ONVIF foundation
* Local HTTP server
* Local authentication
* Network configuration
* Camera configuration

### Web Configuration Interface v2

The **Web Configuration Interface v2** will eventually become the main administration interface.

Planned sections include:

* Dashboard
* Camera settings
* Video settings
* Stream settings
* Network settings
* ONVIF settings
* Storage settings
* User management
* System settings
* **About This Camera**

However, **Web Configuration Interface v2 is still being developed and is not currently available as a finished build.**

---

# 🔎 About This Camera

One planned feature is a detailed **About This Camera** page.

It will eventually expose information such as:

```text
OnviVV - About This Camera

Device
--------------------------------
Model:
Board:
SoC:
CPU:
RAM:
Flash:

Camera
--------------------------------
Sensor:
Resolution:
FPS:
Codec:

Network
--------------------------------
MAC:
IP:
Interface:

Software
--------------------------------
OnviVV:
Kernel:
Firmware:

Protocols
--------------------------------
RTSP:
ONVIF:
HTTP:
```

The exact information will depend on what can be detected from the camera hardware.

---

# 🔧 Hardware Research

Before OnviVV can support a camera, its hardware needs to be understood.

Development may involve identifying:

* SoC
* RAM
* Flash
* Camera sensor
* Ethernet/Wi-Fi chipset
* GPIO
* Storage
* Bootloader
* Linux kernel
* Existing services
* Existing streaming protocols
* Firmware structure

Different cameras may use completely different hardware even when they look almost identical.

---

# 📦 Firmware Adaptation

A future OnviVV release may provide hardware-specific adaptation tools.

The intended concept is:

```text
Original Camera Dump
        │
        ▼
 Hardware Analysis
        │
        ▼
 OnviVV Build/Adapter
        │
        ▼
 Adapted Camera System
        │
        ├── RTSP
        ├── ONVIF
        ├── Web UI
        └── Local Configuration
```

This is **not currently available as a finished automated system**.

Firmware work is still part of the development process.

---

# 🧪 Development / Testing

At this stage, OnviVV is primarily for development and research.

If you are interested in contributing hardware information or testing development builds, useful information includes:

```text
Camera model:
Board revision:
SoC:
RAM:
Flash:
Sensor:
Network chipset:
Original firmware:
Bootloader:
Kernel:
```

A complete backup of the original firmware should always be kept before experimenting with firmware modifications.

---

# 🗺️ Roadmap

## Phase 0: Build the Base

**Current phase**

* Project structure
* Build system
* Hardware detection
* Basic system services
* Configuration framework
* Logging
* Networking foundation

## Phase 1: Make It a Camera

* RTSP
* ONVIF
* Local HTTP server
* Camera configuration
* Basic authentication

## Phase 2: Web Configuration Interface v2

* Dashboard
* Camera settings
* Stream settings
* Network settings
* ONVIF settings
* Storage settings
* User management
* System settings
* About This Camera

## Phase 3: Hardware Support

* Hardware-specific builds
* Firmware adapters
* Automatic hardware detection
* Multiple SoC platforms
* Recovery tooling

## Phase 4: Public Release

* Public development builds
* Documentation
* Hardware compatibility list
* Stable release
* Developer tools

---

# 🚫 No Public Build Yet

**OnviVV does not currently have a public ready-to-use build.**

If you found this repository expecting a `.bin`, firmware image, installer, or ready-to-flash package, you're a little early. 🏗️

The project is currently **building the base**.

When usable development builds become available, they will be published here along with the required hardware information and installation instructions.

---

# 🤝 Contributing

Contributions and hardware research are welcome.

At this stage, useful contributions include:

* Hardware identification
* Firmware analysis
* SoC research
* Reverse engineering
* RTSP development
* ONVIF development
* Web UI development
* Testing
* Documentation

---

# ⭐ Vision

OnviVV is being built around one simple idea:

**A cloud camera should be able to work as a local camera.**

The project is not finished yet.

The base is being built first.

**OnviVV**
*Cloud camera → Local camera.*
