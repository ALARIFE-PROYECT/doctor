markdown# 🩺 Doctor - BigByte Framework

**Doctor** is a library from the **BigByte** ecosystem that acts as an intelligent Node.js script launcher. It provides a real-time monitoring environment for the launched process, facilitating performance and activity inspection, ideal for backend developers working with APIs or Node services.

## 🚀 Features

- Execute any Node.js script from CLI.
- Automatically launches a web monitoring interface.
- Real-time inspection of:
  - **CPU** and **memory** usage.
  - **Event loop** status.
  - **HTTP requests** information (for REST APIs).
- **PID-based** monitoring of the launched process.
- Configurable monitoring port (`--port`).

## 📦 Installation

```bash
npm install -g @bigbyte/doctor
```

## 🛠️ Basic usage

```bash
doctor ./my-script.js
```

This will execute `my-script.js` and launch a web interface at `http://localhost:8088` showing the process status.

### Change the monitor port

```bash
doctor ./my-script.js --port 3000
```

## 📊 Monitoring interface

Once the process is launched, access:

```
http://localhost:8088
```

(or the specified port)

### Visualize:

- Real-time CPU and memory charts.
- Event Loop status (delay, blocks).
- Request statistics (if it's a REST API):
  - Total number of requests.
  - Response time.
  - Routes and methods used.

## 📁 Project structure

```bash
my-project/
├── script.js      # Script to execute
└── ...
```

## 🧩 Integration

Doctor is part of the **BigByte** framework and can be used as a launcher in development, testing, or benchmarking environments.

## 📜 License

This project is licensed under the terms of the [Apache License 2.0](./LICENSE).