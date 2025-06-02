# Escape Room Communication Standard (ERCS)

[![Deploy Docs](https://github.com/proffalken/ercs/actions/workflows/mkdocs.yml/badge.svg)](https://github.com/proffalken/ercs/actions/workflows/mkdocs.yml)
[View on GitHub](https://github.com/proffalken/ercs)

---

Welcome to the official documentation for the **Escape Room Communication Standard (ERCS)** — a flexible, extensible messaging specification designed to enable smart, interactive components in escape rooms to communicate seamlessly, regardless of platform or transport layer.

This standard enables escape room developers to:

- Track player progress and puzzle states across multiple devices
- Monitor hardware health and environmental sensor data
- Build thematically rich, immersive experiences using a consistent interface
- Integrate embedded systems (ESP32, Arduino), web services, and control software with ease

---

## 🔧 Key Concepts

### 🧩 Puzzles
Each game is composed of multiple puzzles, each themed and tracked individually.

### 📡 Devices
Any interactive component (button, sensor, light, lock, etc.) that communicates via ERCS.

### 💬 Messages
JSON-based messages represent state changes, progress, heartbeat updates, and more.

### 📦 Capabilities
Devices advertise what they support — inputs, outputs, sensors, and more — at registration time.

---

## 🚀 Supported Transports

While ERCS defines the message structure in JSON, the actual transport layer may vary depending on the device or control system:

- USB Serial
- MQTT
- WebSockets
- HTTP(S)

---

## 🔄 Extensibility

The standard is designed to evolve. Unknown fields and new capabilities can be added without breaking existing systems using reserved areas like:

- `metadata` (for any future, non-critical information)
- `sensors[]` (for modular sensor data tracking)

---

## 🤝 Get Involved

ERCS is a collaborative effort. Contributions, suggestions, and extensions are welcome via GitHub Issues and Pull Requests.

> Made with ❤️ by escape room developers, for escape room developers.

