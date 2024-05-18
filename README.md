# Real-Time Video Recording with Flask

This project is a Flask-based web application that provides real-time video streaming and recording functionality using OpenCV. The application captures video from a webcam, streams it to a web interface, and allows users to start and stop recording the video.

## Features

- **Real-Time Video Streaming:** Streams video from a webcam to a web interface.
- **Video Recording:** Allows users to start and stop video recording with a single button click.
- **Multithreaded Recording:** Utilizes multithreading to handle video recording without interrupting the video stream.

## Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/video-streaming-recording.git
    cd video-streaming-recording
    ```

2. **Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Flask application:**
    ```bash
    python app.py
    ```

2. **Open your browser and navigate to:**
    ```
    http://127.0.0.1:5000/
    ```

3. **Start/Stop Recording:**
    - Click the "Start/Stop Recording" button to start recording the video.
    - Click the button again to stop recording. The recorded video will be saved in the `static` directory as `video.avi`.

## Code Overview

- **`app.py`:** The main Flask application file that sets up the web server, handles video streaming, and manages recording.
- **`templates/index.html`:** The HTML template for the web interface.

### Core Functions

- **`gen_frames()`:** Generates video frames from the webcam for streaming.
- **`record(out)`:** Handles the recording of video frames to a file.
- **`index()`:** Renders the main web page.
- **`video_feed()`:** Provides the video feed for the web interface.
- **`tasks()`:** Handles the start/stop recording functionality.

## Dependencies

- Flask
- OpenCV
- numpy
