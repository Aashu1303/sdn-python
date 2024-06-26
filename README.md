# SDN Implementation using OpenFlow

## Overview

This project demonstrates the implementation of Software-Defined Networking (SDN) using the OpenFlow protocol. The primary goal is to showcase how SDN can simplify network management by separating the control plane from the data plane, allowing centralized control of the network.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Network Topology](#network-topology)
- [OpenFlow Rules](#openflow-rules)
- [Testing and Monitoring](#testing-and-monitoring)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

```
SDN-OpenFlow-Implementation/
├── controller/
│   ├── README.md
│   └── scripts/
│       └── basic_flows.py
├── network/
│   ├── README.md
│   └── topology.py
├── docs/
│   ├── setup_guide.md
│   ├── architecture.md
│   └── troubleshooting.md
├── .gitignore
├── LICENSE
└── README.md
```

## Prerequisites

- Basic understanding of SDN and OpenFlow.
- Familiarity with Linux-based operating systems.
- Installed software:
  - Mininet
  - An SDN controller (OpenDaylight, Ryu, or Floodlight)
  - Wireshark or tcpdump for network monitoring
  - Python 3.x

## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/SDN-OpenFlow-Implementation.git
cd SDN-OpenFlow-Implementation
```

### 2. Install Mininet

Follow the [Mininet installation guide](http://mininet.org/download/) to set up Mininet on your system.

### 3. Install the SDN Controller

Choose and install one of the following SDN controllers:
- [OpenDaylight](https://www.opendaylight.org/)
- [Ryu](https://ryu-sdn.org/)
- [Floodlight](http://www.projectfloodlight.org/floodlight/)

Refer to the respective installation guides for setup instructions.

## Network Topology

Create a network topology using Mininet. For this project, we use a tree topology:

```bash
sudo mn --topo tree,depth=2 --controller remote
```

Refer to `network/topology.py` for the Mininet script used in this project.

## OpenFlow Rules

We use basic OpenFlow rules to manage network traffic. You can find the script for adding flow rules in `controller/scripts/basic_flows.py`.

### Running the Flow Rules Script

```bash
python3 controller/scripts/basic_flows.py
```

## Testing and Monitoring

- Use Wireshark or tcpdump to monitor network traffic.
- Check the controller logs for any issues or debugging information.

## Contributing

Contributions are welcome! Please fork this repository, make your changes, and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
Feel free to replace `yourusername` with your actual GitHub username in the repository URL.
