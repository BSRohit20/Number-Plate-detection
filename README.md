# Number Plate Detection and Recognition

This project demonstrates a simple system to detect vehicle number plates from an image and recognize the text using Optical Character Recognition (OCR). It utilizes OpenCV for image processing and Tesseract for OCR.

## Features

- Preprocesses the input image to detect edges.
- Identifies the contours of potential number plates.
- Extracts the number plate area from the image.
- Uses Tesseract OCR to recognize the text on the number plate.
- Visualizes different stages of the detection process using Matplotlib.

## Requirements

- Python 3.x
- OpenCV
- Numpy
- Matplotlib
- Tesseract-OCR

### Python Libraries

Install the required libraries using pip:

```bash
pip install opencv-python numpy matplotlib pytesseract
```

### Tesseract OCR Installation

You need to install Tesseract OCR to perform text recognition. Download and install Tesseract from [here](https://github.com/tesseract-ocr/tesseract).

After installation, ensure that the `tesseract_cmd` is set to the correct path in the code. You can modify this line as needed:

```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```

## How to Run the Script

1. Place your image in the appropriate directory and update the `image_path` variable in the script to point to the image file. For example:
   
   ```python
   image_path = 'D:\\Desktop\\dip2\\car.jpg'  # Update this with your image path
   ```

2. Run the Python script:
   
   ```bash
   python number_plate_detection.py
   ```

3. The script will:
   - Preprocess the image (convert it to grayscale, blur, and detect edges).
   - Detect potential number plate contours.
   - Extract and display the number plate.
   - Perform OCR to recognize and print the text on the number plate.

## Example Workflow

1. The script loads and preprocesses the image to highlight edges.
2. It identifies and draws contours around rectangular objects that resemble number plates.
3. If a number plate is detected, the area is extracted and displayed.
4. Tesseract OCR is applied to read the text on the number plate.

## Output

- If a number plate is detected, the system will display the contours, the extracted number plate, and print the recognized text.
- If no number plate is detected, it will output a message saying "Number plate not detected."

## Acknowledgments

- [OpenCV](https://opencv.org/) for image processing.
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) for text recognition.

---
