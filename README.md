# Proxy Tester

A fast, lightweight desktop application for testing and benchmarking HTTP(S) proxies using real-world TLS and HTTP validation.

Built as a small internal tool for friends, with a focus on realistic proxy performance rather than just “alive or dead” checks.

---

## 👋 Why I Built This

A few of my friends are deep into botting Pokémon cards (and yes — they bot for me too so I can actually grab stuff at MSRP 😄).

Lately, they kept running into issues where **proxy quality was the deciding factor** between a successful checkout and a failed task. One thing that came up repeatedly was that “good” proxies weren’t just about being alive — they needed to be able to **connect to, negotiate with, and communicate reliably with specific retail sites**.

Instead of guessing or relying solely on third-party tools, I decided to build a **super quick, lightweight proxy tester** that focuses on what actually matters:  
how well a proxy can establish a real HTTPS connection and talk to the target host.

The initial focus is on the sites they struggle with most:
- **Walmart.ca**
- **Costco.ca**

The project is intentionally designed to be **extensible**, so adding support for additional websites or different testing strategies in the future is straightforward.

This tool isn’t meant to replace full bot frameworks — it’s meant to make **proxy selection smarter, faster, and more transparent**.

---

## 🎥 Demo Video

Watch a short walkthrough of the app here:

👉 **Demo:**  
(Watch here)[https://drive.google.com/file/d/1nLyy_LZtHxogT_euDdF2UstxhaNpktHG/view?usp=drive_link]

The demo shows:
- Adding proxies
- Testing proxies in bulk
- Realistic latency results
- Comparing proxy quality visually

---

## ✨ Features

- ⚡ **Fast, realistic proxy testing**
  - TCP connect
  - HTTP `CONNECT` tunnel
  - TLS handshake
  - Minimal HTTPS request for real-world timing

- 📊 **Latency measurements comparable to bot tools**
  - Timings closely resemble tools like Stellar
  - Measures actual encrypted data flow, not just socket availability

- 🧠 **Clean, minimal UI**
  - Easy-to-scan results
  - Status and speed combined into a single “Result” column

- 🖥 **Packaged desktop app**
  - Distributed as a **Windows `.exe`**
  - No Node.js or browser required
  - Can be run directly on users’ own computers

- 🔐 **Safe by design**
  - Minimal bandwidth usage
  - No page scraping by default
  - Avoids unnecessary WAF triggers

---

## 🧪 How Proxy Testing Works

Each proxy is tested using the following pipeline:

