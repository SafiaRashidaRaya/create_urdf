# 📝 Project Overview

This repository contains configuration files and scripts used to generate **URDF** and **MuJoCo** models from Onshape using `onshape-to-robot`.

The repo includes:

* `config.json` — **Main/default configuration used when running the script**
* `config_urdf.json` — Reference config specifically for URDF output
* `config_mujoco.json` — Reference config specifically for MuJoCo output
* `keys1.json` — API keys needed to access the Onshape API *(included intentionally for testing; **not sensitive**)*

---

## 📦 Requirements

Make sure you have:

* Python ≥ 3.8
* A virtual environment (optional but recommended)
* The `onshape-to-robot` Python package
* Your system dependencies for URDF/MuJoCo generation (default Onshape-to-Robot dependencies)

To install the package:

```bash
pip install onshape-to-robot
```

or, if running in a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate      # Linux / macOS
.\venv\Scripts\activate       # Windows
pip install onshape-to-robot
```

---

## 📁 Files Explained

### `config.json`

This is the **default** config the script uses.
If you run `onshape-to-robot` without specifying a config file, this is the one that gets loaded.

### `config_urdf.json`

Alternate configuration optimized for URDF output.
Not used automatically — only for reference.

### `config_mujoco.json`

Alternate configuration optimized for MuJoCo output.
Not used automatically — only for reference.

### `keys1.json`

Contains API keys for Onshape access — included intentionally for quick testing.

> ⚠️ **Note:** These keys are for testing only.
> Don’t use them for production or personal accounts.

---

## ▶️ How to Run the Converter

To generate the robot model:

```bash
onshape-to-robot config.json
```

If you want to explicitly use one of the alternate configs:

```bash
onshape-to-robot config_urdf.json
```

or

```bash
onshape-to-robot config_mujoco.json
```

The output will appear in the folder specified inside the config.

---

## 🔧 Optional: Editing the Config

You can modify:

* Onshape document ID
* Workspace ID
* Element ID
* Output directory
* File format (URDF / MJCF)

Use whichever config is most convenient.

---

## 🙋 Need Help?

If something fails:

* Make sure your Python environment has `onshape-to-robot` installed
* Check your internet connection
* Ensure the Onshape document is public or accessible via the included keys

---

