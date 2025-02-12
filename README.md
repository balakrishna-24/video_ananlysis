
# Video Analysis with YOLOv5, Places365, and Whisper

This Python script performs video analysis by combining object detection, scene classification, and audio transcription. It utilizes the YOLOv5 model for object detection, the Places365 model for scene classification, and the Whisper model for audio transcription.

## Features

- Downloads a YouTube video given its URL
- Extracts frames from the video at specified intervals
- Performs object detection on each frame using the YOLOv5 model
- Classifies the scene in each frame using the Places365 model
- Extracts the audio from the video and transcribes it using the Whisper model
- Combines the visual and audio information and analyzes it using an OpenAI language model (GPT-4 or GPT-3.5-turbo)
- Generates a detailed analysis and explanation of the video's content

## Prerequisites

Before running the script, ensure you have the following dependencies installed:

- Python 3.x
- OpenCV (cv2)
- PyTorch
- torchvision
- yt-dlp
- Pillow
- requests
- imutils
- whisper
- openai

You can install the required packages using pip:

```
pip install opencv-python torch torchvision yt-dlp pytube whisper openai gtts
```

Additionally, clone the YOLOv5 repository and install its requirements:

```
git clone https://github.com/ultralytics/yolov5
cd yolov5
pip install -r requirements.txt
```

## Usage

1. Set your OpenAI API key in the script by replacing `'Your_api'` with your actual API key.

2. Run the script:

```
python video_analysis.py
```

3. Enter the YouTube video URL when prompted.

4. The script will download the video, process the frames, extract and transcribe the audio, and generate an analysis using an OpenAI language model.

5. The analysis and explanation will be displayed in the console.

## Customization

- You can adjust the `capture_interval` parameter in the `process_frames` function to change the interval at which frames are captured from the video.

- The script uses the "base" model of Whisper for audio transcription. You can modify this by changing the argument in `whisper.load_model()`.

- The OpenAI language model used for analysis can be changed by modifying the `model` parameter in the `openai.chat.completions.create()` function. You can use "gpt-4" or "gpt-3.5-turbo".

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

- [YOLOv5](https://github.com/ultralytics/yolov5) - Object detection model
- [Places365](http://places2.csail.mit.edu/) - Scene classification model
- [Whisper](https://github.com/openai/whisper) - Automatic speech recognition (ASR) system
- [OpenAI](https://www.openai.com/) - Language models for analysis and explanation
```

