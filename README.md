Cricket Player Detection Notebook
How to Run
Open cricket_player_detection.ipynb in Google Colab.
Set runtime to T4 GPU:
Runtime > Change runtime type
Hardware accelerator: GPU
CPU also works, but is significantly slower for YOLO inference and tracking.
Run the installation cells.
All packages install with individual error handling.
Video Setup (Required for Colab):
Download the cricket video from this Google Drive link:
https://drive.google.com/file/d/10qKFhR9A3KFHcaWqyldC-J1tIeBG3nm4/view?usp=sharing
Upload the downloaded .MP4 file to your Google Drive (preferably in the MyDrive folder).
Update VIDEO_PATH in the notebook to the correct path of the uploaded file (e.g., /content/drive/MyDrive/MVI_0402.MP4).
Ensure NumPy version 1.26.4 for pandas compatibility:
Run !pip show numpy in a new cell to check the current version.
If not 1.26.4, install it with !pip install numpy==1.26.4 and restart the runtime.
Run all cells:
Runtime > Run all
The notebook will detect and track cricket players, perform analysis, and generate annotated output videos and CSV files.
Use the final cells to download outputs:
Annotated video with player detections and tracking
CSV files with frame-by-frame player positions
Analysis charts and plots
Video Folder Setup
Google Colab
Upload your .MP4 video file into your Google Drive.
The notebook expects the file to be accessible via the path set in VIDEO_PATH.
If the file is missing, the notebook will print an error and provide instructions to locate it.
Confirm File
The notebook will check if the file exists at VIDEO_PATH and report:

File found/not found
File size
Troubleshooting
If a numpy compatibility error occurs (especially with pandas):
Ensure NumPy is version 1.26.4
Restart the runtime after installing
Processing time depends on video length and frame count; expect longer times for full videos.
If YOLO models fail to load, check internet connection for downloading models.
