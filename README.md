# 🚀 SitecoreAI Component Toolkit

**Dependency-aware Component Refactor & Cleanup Engine for Sitecore XM Cloud (SXA Headless)**

---

## 🔥 Why This Exists

In Sitecore XM Cloud (SitecoreAI), a component is **not just a rendering**.

It is a distributed structure across:

* `/layout/Renderings`
* `/templates`
* `/templates/Branches`
* `/system/Settings`
* SXA Headless configurations
* Available Renderings
* Layout references

👉 Moving or deleting only the rendering **breaks the system silently**.

This leads to:

* ❌ Broken Experience Editor
* ❌ Orphaned templates & branches
* ❌ Corrupted SXA configurations
* ❌ Invalid Available Renderings

---

## 🧠 What This Toolkit Does

This toolkit introduces a **dependency-aware engine** that safely manages component lifecycle:

### 🧩 Move / Refactor Component

* Moves component across Helix modules
* Automatically relocates all related artifacts
* Updates all references safely

### 🧹 Safe Delete (Cleanup Engine)

* Deletes component **with full dependency cleanup**
* Removes:

  * Templates
  * Branch templates
  * SXA Headless settings
  * Rendering variants
  * Available Renderings
* Prevents orphaned structures and broken references

---

## 📦 Full Toolkit Package Available

A **combined package** is included in the repository:

✔ `SitecoreAI.ComponentToolkit.v1.0.0.zip`

Includes:

* Move Component module
* Safe Delete Component module

👉 Recommended for quick and complete setup

---

## ⚙️ Core Capabilities

✔ Helix-aware module detection
✔ Dependency graph-based processing
✔ SXA Headless compatibility
✔ Automatic reference updates
✔ Safe execution order
✔ Prevents duplicate or broken references

---

## 🏗️ What Gets Handled Automatically

* Datasource Templates
* Folder Templates
* Rendering Parameters
* Branch Templates
* Default Variant Branch
* SXA “Add Data Item” settings
* Rendering Variants
* Available Renderings (global + content)
* Json Rendering (final step)

---

## 🔄 Safe Execution Order

To prevent broken bindings and inconsistent states:

1. Folder Template
2. Datasource Template
3. Rendering Parameters
4. Branch Templates
5. SXA Settings
6. Rendering Variants
7. Json Rendering
8. Reference updates

---

## 🧪 Real Scenario

You created or cloned a component into the wrong Helix module.

👉 Moving only the rendering → broken system
👉 Manual cleanup → time-consuming and error-prone
👉 Toolkit → full dependency-safe refactor in correct order

---

## 🖥️ Installation

### 1. Install Sitecore PowerShell Extensions

* Version: **6.4+**

---

### 2. Install Package

Navigate to:
`/sitecore/admin/PackageInstaller.aspx`

You have **two options**:

---

### ✅ Option 1 — Full Toolkit (Recommended)

Install:

`SitecoreAI.ComponentToolkit.v1.0.0.zip`

✔ Includes:

* Move Component
* Safe Delete Engine

👉 Best for quick setup

---

### ⚙️ Option 2 — Individual Modules

Install separately:

* `SitecoreAI.ComponentToolkit.MoveComponent.*.zip`
* `SitecoreAI.ComponentToolkit.DeleteComponent.*.zip`

👉 Use for modular control

---

## ▶️ Usage

1. Open **Content Editor**
2. Navigate to a **Json Rendering**
3. Right-click →
   **Scripts → Component Toolkit**
4. Choose action:

   * Move / Refactor Component
   * Safe Delete Component
5. Select target or confirm deletion

---

## 🛡️ Safety Features

* Prevents duplicate Available Renderings
* Prevents orphaned branch references
* Skips already aligned items
* Supports forward and reverse refactors
* Ensures consistent SXA configuration

---

## 🧱 Supported Architecture

* Sitecore 10.2+
* XM Cloud (SitecoreAI)
* SXA Headless
* Helix Architecture
* SPE 6.4+

---

## 📦 Modules Overview

| Module         | Purpose                                         |
| -------------- | ----------------------------------------------- |
| Move Component | Safe Helix refactor with dependency handling    |
| Safe Delete    | Complete cleanup engine with dependency removal |

---

## ⭐ Why It Matters

In large XM Cloud solutions:

* Components evolve frequently
* Teams refactor across modules
* Dependencies become fragmented

This toolkit ensures:

✔ Structural integrity
✔ Helix compliance
✔ Clean SXA configuration
✔ Reduced technical debt
✔ Safe refactoring workflows

---

## 📣 Contribute

* ⭐ Star the repository
* 🛠 Submit pull requests
* 🧠 Suggest improvements

---

## 👤 Author

Dhruvil Gajera
Sitecore XM Cloud Developer

---

## ⚠ Disclaimer

Always test in lower environments before using in production.
