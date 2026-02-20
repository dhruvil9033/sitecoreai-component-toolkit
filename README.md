# 🚀 SitecoreAI Component Toolkit

Enterprise-grade Helix refactor utility for **SitecoreAI / XM Cloud (SXA Headless)**.

---

## 📦 Overview

**SitecoreAI Component Toolkit** is a PowerShell-based refactor engine that allows developers to safely move a component (Json Rendering) between Helix modules while automatically handling all related artifacts.

When components are cloned or incorrectly structured, Helix boundaries can break. This tool realigns components across:

- `/sitecore/layout/Renderings`
- `/sitecore/templates`
- `/sitecore/templates/Branches`
- `/sitecore/system/Settings`
- `/sitecore/layout/Placeholder Settings`

All in a single guided operation.

---

## 🎯 Problem It Solves

In SitecoreAI (XM Cloud + SXA Headless), cloning a component creates multiple dependent items across the Sitecore tree.

Manually moving these items is:

- ❌ Error-prone  
- ❌ Time-consuming  
- ❌ Risky for SXA setup  
- ❌ Likely to break Available Renderings references  

**Component Toolkit automates this safely.**

---

## ✨ Features

### ✅ Helix-Aware Module Refactor

Moves component between:

- Feature
- Foundation
- Project

Layer is automatically detected from context.

---

### ✅ Moves Related Artifacts

The toolkit can move:

- ✔ Datasource Template  
- ✔ Folder Template (`<Template> Folder`)  
- ✔ Rendering Parameters Template  
- ✔ Branch Template  
- ✔ Default `<Rendering Name>` Variant Branch  
- ✔ Placeholder Settings  
- ✔ SXA Headless "Add Data Item"  
- ✔ SXA Rendering Variant  
- ✔ Json Rendering (final step)

---

### ✅ Updates References Automatically

After move, the tool:

- 🔄 Updates `Datasource Template` field binding  
- 🔄 Updates Branch `$name` → Available Headless Renderings  
- 🔄 Updates Content-level Available Renderings  
- 🔄 Removes reference from old module  
- 🔄 Adds reference to new module  

No manual fixes required.

---

## 🏗 Supported Architecture

Designed for:

- Sitecore 10.2+
- SitecoreAI (XM Cloud)
- SXA Headless
- Helix-based solutions
- Sitecore PowerShell Extensions 6.4+

---

## 📂 Example

If your rendering is:/sitecore/layout/Renderings/Feature/Test A/Promo A

And you move it to:/sitecore/layout/Renderings/Feature/Test B


The tool evaluates and moves all related artifacts automatically, including templates, branches, settings, and rendering references.

---

## 🛠 Installation

### 1️⃣ Install Sitecore PowerShell Extensions

Required version: **6.4+**

---

### 2️⃣ Install Module Package

1. Navigate to: 
The tool evaluates and moves all related artifacts automatically, including templates, branches, settings, and rendering references.

---

## 🛠 Installation

### 1️⃣ Install Sitecore PowerShell Extensions

Required version: **6.4+**

---

### 2️⃣ Install Module Package

1. Navigate to:/sitecore/admin/PackageInstaller.aspx
2. Upload:
3. Install the package.

---

### 3️⃣ Usage

1. Open **Content Editor**
2. Navigate to a **Json Rendering**
3. Right-click
4. Select:Scripts -> Component Toolkit -> Move/ Refactor Component
5. Choose target module
6. Select artifacts to move
7. Confirm

Done.

---

## 🔁 Safe Execution Order

To prevent broken bindings, execution order is:

1. Folder Template  
2. Datasource Template  
3. Rendering Parameters  
4. Branch Templates  
5. SXA Headless Settings  
6. Rendering Variant  
7. Json Rendering (last)  
8. Reference updates  

This ensures structural stability.

---

## 🧠 Smart Detection Logic

The tool:

- Detects current layer automatically
- Detects current module path
- Scans within layer scope
- Filters by module path to avoid cross-module conflicts
- Shows only relevant move options

---

## 🔒 Safety Features

- Does not move items already aligned
- Prevents duplicate Available Rendering entries
- Prevents orphaned branch references
- Supports forward and backward refactors

---

## 👤 Author

**Dhruvil Gajera**  
SitecoreAI Developer  

---

## ⭐ Support

If this toolkit helped you:

- Star the repository
- Share it with the community
- Submit improvements via PR

---

## ⚠ Disclaimer

Test in lower environments before production use.  
Designed for Helix-based SitecoreAI solutions using SXA Headless architecture.
