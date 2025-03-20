# Image to Text to Audio
Mini Project: Image to Text to Audio 

This Python script converts text from an image to an audio file. The script uses the `pytesseract` library to extract text from the image and the `gtts` library to convert the extracted text to speech.

## Requirements :

- Python 3.x
- `pytesseract` library
- `Pillow` library
- `gtts` library
- Tesseract-OCR

You also need to install Tesseract-OCR. Instructions for different operating systems are as follows:

Use the package manager to install Tesseract.

```bash
sudo apt-get install tesseract-ocr
```

## Usage :

### 1. Clone the Repository -
Clone the repository to your local machine.

### 2. Prepare an Image -
Place the image file you want to process in the same directory as the script.

### 3. Set the Path -
Modify the script to include the path to your image file. Example:

```python
image_path = "your_image.jpg"
```
## Script Explanation :

### Text Extraction -
The script uses the `pytesseract` library to extract text from an image:

```python
result = pytesseract.image_to_string(img)
```
### Text-to-Speech Conversion -
The script uses the `gtts` library to convert the extracted text to speech and save it as an MP3 file:

```python
tts = gtts.gTTS(result)
tts.save("output_audio.mp3")
