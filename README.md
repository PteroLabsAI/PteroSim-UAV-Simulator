<h1 align="center">
  PteroSim
</h1>

<p align="center">
  <b>UAV Simulation platform</b><br>
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

<p align="center">
  <img src="pictures/PteroSimPoster.png" alt="PteroSim in action" width="90%">
</p>

## About

PteroSim is a UAV simulation platform for drone development, testing, and research. Accurate 6-DOF flight dynamics, native **PX4** and **ArduPilot** SITL support, and a full programmatic API.

## Features

- 6-DOF flight dynamics, up to 10x real-time
- Wind and turbulence modeling
- PX4 and ArduPilot SITL
- IMU, GPS, barometer, airspeed, camera
- Programmatic API for multi-drone orchestration
- Python SDK: `pip install pterosim`

## Vehicles

<table>
  <tr>
    <td align="center">
      <img src="pictures/Drone.png" width="100%"><br>
      <b>Quadcopter</b><br>
      PX4 · ArduPilot · Betaflight
    </td>
    <td align="center">
      <img src="pictures/Cobra.png" width="100%"><br>
      <b>Helicopter</b><br>
      PX4 · ArduPilot
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="pictures/Delta.png" width="100%"><br>
      <b>VTOL</b><br>
      PX4 · ArduPilot
    </td>
    <td align="center">
      <img src="pictures/Ingenuity.png" width="100%"><br>
      <b>Coaxial Helicopter</b><br>
      ArduPilot
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="pictures/Cessna.png" width="100%"><br>
      <b>Fixed-Wing</b><br>
      PX4 · ArduPilot
    </td>
    <td align="center">
      <img src="pictures/Tailsitter.png" width="100%"><br>
      <b>Tailsitter</b><br>
      PX4 · ArduPilot
    </td>
  </tr>
</table>

## Getting Started

Download the latest release from [GitHub Releases](https://github.com/PteroLabsAI/PteroSim-UAV-Simulator/releases), extract, and run `PteroSim.exe`. See the [documentation](https://pterosimdocs.readthedocs.io/en/latest/) for setup guides and API reference.

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
  <sub>&copy; 2026 PteroLabs AI</sub>
</p>
