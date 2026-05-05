# 🏏 Cricket Player Detection Notebook

##  How to Run

1. **Open the Notebook**

   * Upload and open `cricket_player_detection.ipynb` in Google Colab.

2. **Enable GPU (Recommended)**

   * Go to: `Runtime > Change runtime type`
   * Set **Hardware accelerator → GPU (T4 preferred)**
   * CPU works but is significantly slower for YOLO detection and tracking.

3. **Run Installation Cells**

   * Execute all setup cells.
   * Packages include error handling for smooth installation.

---

## 🎥 Video Setup (Required for Colab)

1. **Upload Your Video to Google Drive**

   * Upload the `.MTS` file to your **MyDrive** folder.

2. **Update Video Path in Notebook**

   ```python
   VIDEO_PATH = "/content/drive/MyDrive/England U19 Women Game 1 vs Australia Part 5.MTS"
   ```

3. **Ensure Filename Matches Exactly**

   * Case-sensitive
   * Includes spaces and extension `.MTS`

---

## ⚙️ NumPy Compatibility Fix

Check installed version:

```python
!pip show numpy
```

If not **1.26.4**, install:

```python
!pip install numpy==1.26.4
```

Then restart runtime:

```
Runtime > Restart runtime
```

---

## ▶️ Run the Notebook

* Click:

  ```
  Runtime > Run all
  ```

### 🔍 What the Notebook Does

* Detects cricket players using YOLO
* Tracks players across frames
* Performs movement and positional analysis
* Generates outputs automatically

---

## 📦 Outputs Generated

After execution, you’ll get:

* 🎬 **Annotated Video**

  * Player detection and tracking overlays

* 📊 **CSV Files**

  * Frame-by-frame player positions

* 📈 **Analysis Charts**

  * Movement and positional insights

---

## 📁 Video Folder Setup

### Google Colab

1. Upload `.MTS` video to Google Drive
2. Ensure correct `VIDEO_PATH`
3. Notebook validates file automatically

---

## ✅ File Verification

The notebook checks:

* ✔ File found / not found
* ✔ File size

---

## 🔍 If File Not Found

Run this in Colab:

```bash
!find /content/drive/MyDrive -name "*.MTS" -type f
```

---

## 🛠 Troubleshooting

### NumPy / Pandas Errors

* Ensure NumPy = **1.26.4**
* Restart runtime after installing

### Slow Processing

* Use GPU (T4 recommended)
* Longer videos take more time

### YOLO Model Issues

* Check internet connection
* Models download automatically

---

## ⏱ Performance Notes

* Depends on:

  * Video length
  * Frame count
  * Hardware (GPU vs CPU)

---

## ✅ Summary

This notebook provides a complete pipeline for:

* Player detection
* Multi-object tracking
* Movement analysis
* Exporting annotated videos and datasets

Update the video path, run all cells, and outputs will be generated automatically.

---
