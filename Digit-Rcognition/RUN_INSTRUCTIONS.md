# How to Run the Digit Recognition Code

This project contains multiple digit recognition implementations. Here's how to run each one:

## Prerequisites

First, install the required Python packages:

```bash
pip3 install tensorflow opencv-python pandas matplotlib numpy
```

For macOS users, you may need to install additional dependencies:
```bash
pip3 install pillow
```

---

## Option 1: Simple MNIST Training and Prediction (`Digit-Recognition--main/main.py`)

This script trains a model and tests it on images 1.png-4.png.

### Steps:

1. Navigate to the directory:
   ```bash
   cd Digit-Recognition--main
   ```

2. Make sure the image files (1.png, 2.png, 3.png, 4.png) are in the same directory

3. Run the script:
   ```bash
   python3 main.py
   ```

**What it does:**
- Downloads and trains on MNIST dataset (3 epochs)
- Tests on 4 PNG images (1.png, 2.png, 3.png, 4.png)
- Shows predictions and displays the images

---

## Option 2: CNN Training (`Handwritten digit recognizer/train_digit_recognizer.py`)

This script trains a more advanced CNN model and saves it as `mnist.h5`.

### Steps:

1. Navigate to the directory:
   ```bash
   cd "Handwritten digit recognizer"
   ```

2. Run the training script:
   ```bash
   python3 train_digit_recognizer.py
   ```

**What it does:**
- Trains a CNN model with 10 epochs
- Saves the model as `mnist.h5` in the same directory
- This will take longer but produces a better model

---

## Option 3: GUI Application (`Handwritten digit recognizer/gui_digit_recognizer.py`)

⚠️ **NOTE**: This GUI application uses `win32gui` which is **Windows-only**. It won't work on macOS without modifications.

### For macOS Users:
You would need to modify the code to use a different method for capturing the canvas image (not using `win32gui`).

### For Windows Users:
1. Install additional dependency:
   ```bash
   pip3 install pywin32
   ```

2. Make sure `mnist.h5` model exists in the same directory (run `train_digit_recognizer.py` first)

3. Run:
   ```bash
   python3 gui_digit_recognizer.py
   ```

---

## Quick Start (Recommended)

If you just want to see the code in action quickly:

```bash
cd Digit-Recognition--main
python3 main.py
```

This will train a simple model and test it on the provided images.

---

## Troubleshooting

1. **Import errors**: Make sure all dependencies are installed with `pip3 install tensorflow opencv-python pandas matplotlib numpy`

2. **Image not found errors**: Make sure image files (1.png, 2.png, etc.) are in the correct directory

3. **TensorFlow/Keras warnings**: These are usually safe to ignore, but you can suppress them if needed

