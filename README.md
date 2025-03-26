# Handwriting Recognition using MNIST

This project is a **handwriting digit recognition** system using a **Convolutional Neural Network (CNN)** trained on the MNIST dataset. It allows users to draw a digit using a Pygame interface and predicts the digit using a trained deep learning model.

## Features
- Train a CNN model on the MNIST dataset.
- Save and load the trained model.
- Use a simple **Pygame GUI** to draw digits.
- Predict handwritten digits in real-time.

---

## Installation. (pycharm editor preferred)

### **1. Clone the Repository**
```sh
git clone https://github.com/yourusername/Handwriting_Digit_Recognition.git
cd Handwriting_Digit_Recognition
```

### **2. Create a Virtual Environment**
```sh
python -m venv mnist_env
```
Activate the virtual environment:
- **Windows:** `mnist_env\Scripts\activate`
- **Mac/Linux:** `source mnist_env/bin/activate`

### **3. Install Dependencies**
```sh
pip install -r requirements.txt
```
TO NOTE
---
```pip3 install pygame numpy tensorflow```

if you haven't installed 
---

## Model Training
To train the model, run:
```sh
python handwriting.py model.h5
```
This will:
- Train a CNN model on the MNIST dataset.
- Save the trained model as `model.h5`.

---

## Running the Digit Recognition App
Once the model is trained, launch the Pygame interface:
```sh
python recognition.py model.h5
```
### **Usage Instructions**
- **Draw a digit** using the mouse.
- **Press 'P'** to predict the digit.
- **Press 'C'** to clear the screen.
- **Close the window** to exit the program.


---

## Troubleshooting
### **1. Model Not Found Error**
**Error:** `No such file or directory: 'mnist_model.h5'`
- **Solution:** Ensure you have trained the model using `python mnist_cnn.py` before running `runner.py`.

### **2. Wrong Predictions**
- Ensure the model is properly compiled after loading:
```python
model.compile(optimizer="adam", loss="categorical_crossentropy", metrics=["accuracy"])
```
- **Try increasing training epochs in `handwriting.py`.**
- Ensure digits are drawn clearly inside the canvas.

---

## Contributing
Feel free to fork this repository and submit pull requests to improve the project.

## License
This project is licensed under the MIT License.

