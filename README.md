# merge-video

This repository contains a Python script for merging two video files into a single video file. The script utilizes the `moviepy` library to perform the merging process.

## Usage
1. Install the required dependencies, primarily `moviepy`.
2. Specify the paths to the input video files (`video1_path` and `video2_path`) in the script.
3. Run the script to merge the videos.
4. The merged video will be saved at the specified output path (`output_path`).

## Dependencies
- `moviepy`: A Python library for video editing.

## Example
```python
from moviepy.editor import VideoFileClip, concatenate_videoclips

# Specify the paths to your video files
video1_path = "C:\\Users\\Home\\Desktop\\Vij\\Videos\\Initial Videos\\Nani.mp4"
video2_path = "C:\\Users\\Home\\Desktop\\Vij\\Videos\\End.mp4"

# Load the video clips
clip1 = VideoFileClip(video1_path)
clip2 = VideoFileClip(video2_path)

# Concatenate the clips
final_clip = concatenate_videoclips([clip1, clip2])

# Save the merged video
output_path = "C:\\Users\\Home\\Desktop\\Vij\\Nani_Final.mp4"
final_clip.write_videofile(output_path)

# Print success message
print("Videos merged successfully! Output saved as:", output_path)
