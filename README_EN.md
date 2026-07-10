<p align="center">
  <img src="https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge" alt="Version">
  <img src="https://img.shields.io/badge/Protocol-MTProto%20Fake--TLS-purple?style=for-the-badge" alt="Protocol">
  <img src="https://img.shields.io/badge/Platform-Docker%20%2F%20Railway-orange?style=for-the-badge" alt="Platform">
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" alt="Status">
</p>

<div align="center">
  <h1>🚀 DX-Proxy Panel</h1>
  <p><strong>Next-Gen Telegram MTProto Proxy Management Panel</strong></p>
  <p>Modern • Fast • Self-Hosted • Zero Desync</p>

  [![GitHub stars](https://img.shields.io/github/stars/COD-DEXTER/DX-Proxy?style=social)](https://github.com/COD-DEXTER/DX-Proxy/stargazers)
  [![GitHub forks](https://img.shields.io/github/forks/COD-DEXTER/DX-Proxy?style=social)](https://github.com/COD-DEXTER/DX-Proxy/network/members)

  <p><a href="./README_fa.md">فارسی</a> | English</p>
</div>

---

## 📖 About the Project

**DX-Proxy** is an advanced, high-performance management system for deploying and controlling multi-secret Telegram MTProto proxies, built on the robust `mtg-multi` core.

The panel is architected around a single source of truth: the web dashboard and the terminal menu both read from and write to the same data layer, making desync between the CLI and the web UI impossible.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🎨 **Modern Glassmorphic UI** | Luxurious dark theme, live stat cards, and dynamic glow effects |
| ⚡ **Railway Auto-Detection** | Zero manual configuration — connection domains and details are pulled automatically from Railway env vars |
| 👥 **Smart User Management** | Create, instantly toggle, rotate secrets, and delete keys, with a built-in QR code generator |
| 🔄 **Zero-Desync Architecture** | Fully unified execution flow between the Web UI and the container terminal menu |
| 🔐 **First-Run Password Enforcement** | Forces an administrator credential change on first login |

---

## ⚙️ Ports and Network Configuration (Railway)

To ensure a successful deployment on **Railway**, configure your networking settings exactly as follows:

| Port Type | Internal Port | Railway Connection Type | Purpose |
|---|---|---|---|
| Telegram Proxy | `8080` | TCP Proxy | Telegram client connections |
| Web Management Panel | `2053` | Public Domain (HTTP) | Secure HTTPS dashboard access |

> 💡 Map internal port `8080` to a **TCP Proxy** — this exposes the public address your users connect to in Telegram.
> Map internal port `2053` to a **Public Domain** — this generates an SSL-secured HTTPS endpoint for your dashboard.

---

## 💻 Dual Management Interfaces

### Interface 1 — Web UI

Navigate to your generated Railway HTTPS domain (port `2053`) to access the responsive web dashboard.

> Default login credentials: `admin` / `admin`
> You'll be prompted to set new credentials immediately on first login.

### Interface 2 — Container CLI

Open the terminal console on Railway (or your local Docker container) and launch the `dx` management utility for an interactive text menu:

```bash
dx
```

Or run direct commands from the shell:

```bash
dx add-user client_name
dx remove-user client_name
dx status
```

---

## 🙏 Donation & Support

If you find this project useful, consider supporting the developer via the following cryptocurrency wallets:

| Network | Wallet Address |
|---|---|
| 🔺 TRON (TRX) | `TCViL7pRSiEhFBXE2h6jzB4KE5xtcKQ56x` |
| 💎 TON (GRAM) | `UQCAwbc2cibVwOKfgvpuN5zONxfnSfsylIged7XnUykL6OmJ` |
| 🟡 Binance Smart Chain (USDT BEP20) | `0xFa204Fe8d2FEBdf7D896F942861A9538382C5668` |

<div align="right">

[⬆ Back to top](#-dx-proxy-panel)

</div>