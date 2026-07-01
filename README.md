# Illusionist

> *Control What the Network Believes Is Real.*

![Git](https://img.shields.io/badge/Git-F05032.svg?style=flat-square&logo=Git&logoColor=white)  ![GNU%20Bash](https://img.shields.io/badge/GNU%20Bash-4EAA25.svg?style=flat-square&logo=GNU-Bash&logoColor=white)  ![Gunicorn](https://img.shields.io/badge/Gunicorn-499848.svg?style=flat-square&logo=Gunicorn&logoColor=white)  ![Django](https://img.shields.io/badge/Django-092E20.svg?style=flat-square&logo=Django&logoColor=white)  ![Python](https://img.shields.io/badge/Python-3776AB.svg?style=flat-square&logo=Python&logoColor=white)

## Overview

Illusionist is a network manipulation toolkit built with Django. It performs ARP spoofing against local network targets, overrides DNS resolution for selected domains through a custom routing table, and applies ANSI-styled terminal output throughout for clear operational feedback.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)

---

## Features

|      | Component         | Details                                                                                                                                                                                                                                          |
| :--- | :---------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ⚙️  | **Architecture**  | <ul><li>Django-based web application backend</li><li>Static file serving via `dj-static` + `gunicorn` WSGI server</li><li>Network utility layer powered by `scapy` and `nmap`</li><li>DNS configuration managed via `dns.conf`</li></ul>         |
| 🔩  | **Code Quality**  | <ul><li>Python-based codebase with shell scripting support (`.sh`)</li><li>Dependency versions pinned in `requirements.txt` for reproducibility</li><li>Uses `colorama` for structured, color-coded CLI output</li></ul>                         |
| 📄  | **Documentation** | <ul><li>No dedicated docs directory detected</li><li>`LICENSE` file present — project is open-source</li><li>Minimal inline documentation inferred from project structure</li></ul>                                                              |
| 🔌  | **Integrations**  | <ul><li>`scapy` — low-level packet crafting & network sniffing</li><li>`nmap` — port scanning & host discovery</li><li>`requests` + `bs4` — HTTP client & HTML scraping</li><li>`tldextract` — domain parsing & URL decomposition</li></ul>     |
| 🧩  | **Modularity**    | <ul><li>Separation of network utilities from web layer</li><li>Shell scripts (`.sh`) handle OS-level automation tasks</li><li>`mac-vendor.txt` used as a static lookup resource for MAC address resolution</li></ul>                             |
| ⚡️  | **Performance**   | <ul><li>`gunicorn` enables multi-worker concurrent request handling</li><li>`scapy` provides high-performance raw socket packet processing</li><li>`nmap` leveraged for fast, parallel host/port scanning</li></ul>                              |
| 🛡️  | **Security**      | <ul><li>Network reconnaissance tooling — **intended for authorized use only**</li><li>MAC vendor lookup via `mac-vendor.txt` for device fingerprinting</li><li>DNS config (`dns.conf`) suggests custom resolver or DNS spoofing capability</li></ul> |

---

## Project Structure

```
└── Illusionist/
    ├── arp_spoof.py
    ├── colors.py
    ├── dns.conf
    ├── dns_spoof.py
    ├── install.sh
    ├── LICENSE
    ├── logo.png
    ├── mac-vendor.txt
    ├── README.md
    ├── requirements.txt
    └── runserver.sh
```

---

## Getting Started

### Prerequisites

- Python 3.10+ / Node.js 18+ *(depending on the stack above)*

### Installation

```sh
git clone "https://github.com/IlluzyonistCode/Illusionist
cd Illusionist"
pip install -r requirements.txt
```

### Usage

```sh
python manage.py runserver
```

---

## Contributing

- [Report Issues](https://github.com/IlluzyonistCode/Illusionist/issues)
- [Submit Pull Requests](https://github.com/IlluzyonistCode/Illusionist/pulls)
- [Discussions](https://github.com/IlluzyonistCode/Illusionist/discussions)

---

## License

Distributed under the [AGPL-3.0](LICENSE) license.
