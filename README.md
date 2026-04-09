<h1 align="center">
  PteroSim
</h1>

<p align="center">
  <b>High-fidelity UAV simulator built on Unreal Engine 5</b><br>
  <sub>PX4 & ArduPilot SITL · Programmable API · Multi-vehicle support</sub>
</p>

<p align="center">
  <a href="https://github.com/PteroLabsAI/PteroSim-UAV-Simulator/releases">
    <img src="https://img.shields.io/github/v/release/PteroLabsAI/PteroSim-UAV-Simulator?style=for-the-badge&color=blue" alt="Release">
  </a>
  <a href="#license">
    <img src="https://img.shields.io/badge/license-Proprietary-orange?style=for-the-badge" alt="License">
  </a>
  <a href="https://www.youtube.com/@PteroLabsAI">
    <img src="https://img.shields.io/badge/YouTube-Demos-red?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube">
  </a>
  <a href="https://www.linkedin.com/company/pterolabs">
    <img src="https://img.shields.io/badge/LinkedIn-PteroLabs-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=4QMwmZL_3O4">Watch Demo</a> ·
  <a href="https://pterolabs.ai">Website</a> ·
  <a href="https://github.com/PteroLabsAI/PteroSim-UAV-Simulator/releases">Download</a> ·
  <a href="#quick-start">Quick Start</a> ·
  <a href="mailto:info@pterolabs.ai">Contact</a>
</p>

---

<!-- TODO: Replace with actual screenshots/GIFs -->
<p align="center">
  <img src="docs/images/screenshot-hero.png" alt="PteroSim in action" width="90%">
</p>

## About

PteroSim is a standalone UAV flight simulator for drone development, testing, and research. Accurate 6-DOF flight dynamics, native **PX4** and **ArduPilot** SITL support, and a full programmatic API — free to use, no strings attached.

## Features

- **6-DOF flight dynamics** — up to 10x real-time, wind and turbulence
- **PX4 & ArduPilot SITL** — plug in your autopilot, fly immediately
- **Sensors** — IMU, GPS, barometer, airspeed, camera
- **Programmatic API** — spawn, control, and orchestrate multiple drones
- **Python SDK** — `pip install pterosim`, connect and automate in 3 lines

## Vehicle Types

<!-- TODO: Replace with screenshots or GIF showing all vehicle types -->
<p align="center">
  <img src="docs/images/vehicle-types.gif" alt="Multi-rotor, helicopter, VTOL, fixed-wing" width="90%">
</p>

<p align="center">
  <b>Multi-Rotor</b> · <b>Helicopter</b> · <b>VTOL</b> · <b>Fixed-Wing</b>
</p>

## Quick Start

**1. Download** the latest release from [GitHub Releases](https://github.com/PteroLabsAI/PteroSim-UAV-Simulator/releases).

**2. Extract and run** `PteroSim.exe`.

**3. Connect your autopilot:**

```bash
# PX4
cd PX4-Autopilot
make px4_sitl none_iris
# Connects automatically on TCP 4560

# ArduPilot
sim_vehicle.py -v ArduCopter -f json --console --map
```

**4. (Optional) Use the API:**

```python
from pterosim import PteroSimClient

client = PteroSimClient("localhost:50051")
client.spawn_drone(airframe="F450")
```

## System Requirements

| | Minimum | Recommended |
|---|---------|-------------|
| **OS** | Windows 10 64-bit / Ubuntu 22.04 | Windows 11 / Ubuntu 24.04 |
| **CPU** | Quad-core, 2.5 GHz | 6+ cores, 3.0+ GHz |
| **RAM** | 8 GB | 16 GB |
| **GPU** | GTX 770 / RX 570 | RTX 2070+ / RX 5700+ |
| **Storage** | 5 GB | 10 GB SSD |

## Documentation

Full documentation at [pterolabs.ai](https://pterolabs.ai).

<!-- TODO: Uncomment when docs pages are live
- [Getting Started](https://pterolabs.ai/docs/getting-started)
- [API Reference](https://pterolabs.ai/docs/api)
- [PX4 Integration](https://pterolabs.ai/docs/px4)
- [ArduPilot Integration](https://pterolabs.ai/docs/ardupilot)
- [Custom Airframes](https://pterolabs.ai/docs/custom-airframes)
-->

## License

PteroSim is proprietary software by [PteroLabs AI](https://pterolabs.ai).  
Free for non-commercial, personal, and academic use. See [LICENSE](LICENSE) for details.

---

<p align="center">
  <sub>Built with Unreal Engine 5</sub><br>
  <sub>&copy; 2026 PteroLabs AI</sub>
</p>
