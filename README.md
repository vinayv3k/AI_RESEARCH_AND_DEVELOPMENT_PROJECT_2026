Cricket Player Detection Notebook
🚀 How to Run
Open the Notebook
Upload and open cricket_player_detection.ipynb in Google Colab.
Enable GPU (Recommended)
Go to: Runtime > Change runtime type
Set Hardware accelerator → GPU (T4 preferred)
CPU will work but is significantly slower for YOLO detection and tracking.
Run Installation Cells
Execute all setup cells.
Each package installs with error handling, so failures won’t stop execution.
🎥 Video Setup (Required for Colab)
Download the Input Video
From Google Drive:
https://drive.google.com/file/d/10qKFhR9A3KFHcaWqyldC-J1tIeBG3nm4/view?usp=sharing
Upload to Google Drive
Place the file in MyDrive for easy access.

Update Video Path in Notebook

VIDEO_PATH = "/content/drive/MyDrive/MVI_0402.MP4"

(Adjust filename if needed — .MP4 or .MTS depending on your file)

⚙️ NumPy Compatibility Fix

Ensure correct NumPy version for pandas:

!pip show numpy

If not 1.26.4, run:

!pip install numpy==1.26.4

Then:

Restart runtime: Runtime > Restart runtime
▶️ Run the Notebook
Click: Runtime > Run all
What the Notebook Does:
Detects cricket players using YOLO
Tracks players across frames
Performs spatial and movement analysis
Generates outputs automatically
📦 Outputs Generated

After execution, you’ll get:

🎬 Annotated Video
Player detection + tracking overlays
📊 CSV Files
Frame-by-frame player coordinates
📈 Analysis Charts
Movement, positioning, and insights
📁 Video Folder Setup
In Google Colab:
Upload video to Google Drive
Ensure correct path in VIDEO_PATH
Notebook will automatically validate the file
✅ File Verification

The notebook checks:

✔ File exists / not found
✔ File size
🔍 If File Not Found

Run this in a new Colab cell:

!find /content/drive/MyDrive -name "*.MP4" -type f

(or use .MTS depending on your file format)

🛠 Troubleshooting
NumPy / Pandas Errors
Ensure NumPy = 1.26.4
Restart runtime after installation
Slow Processing
Use GPU (T4 recommended)
Long videos take significantly more time
YOLO Model Issues
Check internet connection
Models download automatically during execution
⏱ Performance Notes
Processing time depends on:
Video length
Frame rate
GPU availability
Expect:
Short clips → few minutes
Full matches → much longer
✅ Summary

This notebook provides a complete pipeline for:

Player detection
Multi-object tracking
Motion analysis
Data export and visualization

Just set up the video, ensure dependencies, and run all cells.
