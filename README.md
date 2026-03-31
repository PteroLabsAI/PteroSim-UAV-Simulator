<p align="center">
  <img src="docs/images/pterosim-banner.png" alt="PteroSim Banner" width="100%">
</p>

<h1 align="center">
  PteroSim — High-Fidelity UAV Simulator
</h1>

<p align="center">
  <b>JSBSim 6-DOF physics · PX4 & ArduPilot SITL · gRPC API · Unreal Engine 5</b>
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
</p>

<p align="center">
  <a href="https://www.youtube.com/@PteroLabsAI">Watch Demo</a> ·
  <a href="https://pterolabs.ai">Website</a> ·
  <a href="https://github.com/PteroLabsAI/PteroSim-UAV-Simulator/releases">Download</a>
</p>

---

<p align="center">
  <img src="docs/images/screenshot-flight.png" alt="Flight View" width="45%">
  &nbsp;&nbsp;
  <img src="docs/images/screenshot-cockpit.png" alt="Cockpit View" width="45%">
</p>

## What is PteroSim?

PteroSim is a **standalone UAV simulator** built on Unreal Engine 5 with **JSBSim 6-DOF flight dynamics**. It connects natively to **PX4** and **ArduPilot** autopilots via MAVLink, making it a powerful tool for drone development, testing, and research.

Unlike archived alternatives (AirSim), PteroSim is **actively developed** and ships with a full **gRPC API** for programmatic control — even in the Free tier.

### Key Features

- **JSBSim 6-DOF Physics** — accurate aerodynamic simulation with real flight dynamics models
- **PX4 SITL** — hardware-in-the-loop via MAVLink with lockstep synchronization
- **ArduPilot SITL** — native support, no middleware required
- **gRPC API** — full programmatic control: spawn drones, read sensors, send commands
- **Stock Airframes** — F450 quadcopter, AH-1 Cobra helicopter, DeltaQuad VTOL
- **Sensor Suite** — IMU, GPS, barometer, airspeed, camera
- **Beyond Real-time** — 6x–10x faster than real-time simulation
- **Multi-Instance** — run 100+ agents simultaneously with mixed fleets
- **Visual Weather** — dynamic sky, clouds, time-of-day
- **Unreal Engine 5** — photorealistic rendering with Lumen GI and Nanite

---

## Quick Start

### 1. Download

Grab the latest release from [GitHub Releases](https://github.com/PteroLabsAI/PteroSim-UAV-Simulator/releases).

### 2. Extract & Run

```bash
# Unzip the archive
unzip PteroSim-v0.1.0-Win64.zip

# Launch the simulator
PteroSim.exe
```

### 3. Connect Your Autopilot

**PX4:**
```bash
# Start PX4 SITL (in WSL or Linux)
cd PX4-Autopilot
make px4_sitl none_iris
# PteroSim connects automatically on TCP port 4560
```

**ArduPilot:**
```bash
# Start ArduPilot SITL
sim_vehicle.py -v ArduCopter -f json --console --map
# Configure connection to PteroSim's JSON endpoint
```

### 4. Use the API (Optional)

```python
import grpc
from pterosim import simulator_pb2, simulator_pb2_grpc

channel = grpc.insecure_channel('localhost:50051')
stub = simulator_pb2_grpc.SimulatorStub(channel)

# Spawn a drone
stub.SpawnDrone(simulator_pb2.SpawnRequest(airframe="F450"))
```

---

## System Requirements

| | Minimum | Recommended |
|---|---------|-------------|
| **OS** | Windows 10 64-bit | Windows 11 64-bit |
| **CPU** | 4 cores, 3.0 GHz | 8+ cores, 3.5+ GHz |
| **RAM** | 8 GB | 16+ GB |
| **GPU** | GTX 1060 / RX 580 | RTX 3070+ / RX 6800+ |
| **Storage** | 5 GB | 10 GB (SSD) |

---

## Documentation

Full documentation is available at [pterolabs.ai](https://pterolabs.ai).

<!-- TODO: Uncomment when docs pages are live
- [Getting Started Guide](https://pterolabs.ai/docs/getting-started)
- [gRPC API Reference](https://pterolabs.ai/docs/api)
- [Custom Airframes Guide](https://pterolabs.ai/docs/custom-airframes) *(Pro)*
- [PX4 Integration](https://pterolabs.ai/docs/px4)
- [ArduPilot Integration](https://pterolabs.ai/docs/ardupilot)
-->

---

## Community & Contact

- **Website** — [pterolabs.ai](https://pterolabs.ai)
- **YouTube** — [@PteroLabsAI](https://www.youtube.com/@PteroLabsAI) — demos, tutorials, and showcases
- **LinkedIn** — [PteroLabs](https://www.linkedin.com/company/pterolabs)
- **Email** — info@pterolabs.ai

---

## License

PteroSim is proprietary software developed by **PteroLabs AI**.

- **Free tier** — free for non-commercial, personal, and academic use
- **Edu tier** — licensed for educational institutions
- **Pro tier** — licensed for commercial use

See [LICENSE](LICENSE) for full terms.

---

<p align="center">
  <sub>Built with Unreal Engine 5 · JSBSim · PX4 · ArduPilot</sub><br>
  <sub>© 2026 PteroLabs AI. All rights reserved.</sub>
</p>
