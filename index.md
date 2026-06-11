<!-- 🌓 PocketPyCharm UI Engine (Dark Mode + Footer Remover) --> 
<div style="text-align: right; margin: 15px 0;"> 
  <button id="theme-toggle-btn" style="padding: 8px 16px; border-radius: 20px; border: 1px solid #ccc; background: #ffffff; color: #24292e; cursor: pointer; font-weight: bold; font-family: sans-serif; transition: all 0.2s ease;">🌙 Dark Mode</button> 
</div> 

<style> 
/* 🚫 Completely delete the footer */ 
footer, .site-footer, .footer { 
  display: none !important; 
} 

/* 🌓 Dark Mode configurations */ 
body.dark-mode-active { 
  background-color: #0d1117 !important; 
  color: #c9d1d9 !important; 
} 
body.dark-mode-active h1, body.dark-mode-active h2, body.dark-mode-active h3, body.dark-mode-active h4 { 
  color: #f0f6fc !important; 
  border-bottom-color: #21262d !important; 
} 
body.dark-mode-active a { 
  color: #58a6ff !important; 
} 
body.dark-mode-active code { 
  background-color: #161b22 !important; 
  color: #ff7b72 !important; 
} 
body.dark-mode-active pre { 
  background-color: #161b22 !important; 
  border: 1px solid #21262d !important; 
} 
body.dark-mode-active hr { 
  background-color: #21262d !important; 
  border: none !important; 
  height: 1px !important; 
} 
body.dark-mode-active #theme-toggle-btn { 
  background: #21262d !important; 
  color: #f0f6fc !important; 
  border-color: #30363d !important; 
} 
</style> 

<script> 
const themeButton = document.getElementById('theme-toggle-btn');

// 1. Initial theme application logic
if (localStorage.getItem('site-theme') === 'dark' || (!localStorage.getItem('site-theme') && window.matchMedia('(prefers-color-scheme: dark)').matches)) { 
  document.body.classList.add('dark-mode-active'); 
  themeButton.textContent = '☀️ Light Mode'; 
}

// 2. Click event handler to toggle modes
themeButton.addEventListener('click', () => {
  document.body.classList.toggle('dark-mode-active');
  
  if (document.body.classList.contains('dark-mode-active')) {
    themeButton.textContent = '☀️ Light Mode';
    localStorage.setItem('site-theme', 'dark');
  } else {
    themeButton.textContent = '🌙 Dark Mode';
    localStorage.setItem('site-theme', 'light');
  }
});
</script>

# PocketPyCharm 

A portable, zero-installation PyCharm development environment.

> [!WARNING]
> **IMPORTANT DISCLAIMER:** This is a 100% independent, fan-made open-source project. This project is **NOT** official software, is **NOT** made by JetBrains, and is **NOT** affiliated with or endorsed by JetBrains s.r.o. All credit for the core PyCharm software, logos, and the trademark "PyCharm" belongs entirely to **JetBrains**. Please support them by checking out the official version at [jetbrains.com](https://jetbrains.com).

## 📦 Available Packages

* **[Download Standard Archive (ZIP)](https://github.com/m97493578-ops/PocketPyCharm/releases)**
    * Optimized for restricted school or enterprise environments.
    * Requires manual folder extraction.

## ⚡ Features

* **No Admin Rights**: Runs entirely within user folders without registry modifications.
* **Fully Portable**: Carry your complete Python IDE workspace directly on a USB drive.
* **AMD64 Native**: Optimized to run smoothly on modern 64-bit Windows machines.

## 🚀 Quick Start Guide

1. Download the latest version package from our official **[Releases Page](https://github.com/m97493578-ops/PocketPyCharm/releases)**.
2. Unpack or extract the file bundle into your local directory (e.g., `Documents` or a `USB`).
3. Open the `bin` folder and run `pycharm64.exe` to launch your portable IDE!
