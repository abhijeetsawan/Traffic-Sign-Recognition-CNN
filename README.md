🚦 Traffic Sign Recognition using CNN

This project implements a **Convolutional Neural Network (CNN)** to classify German traffic signs using the **GTSRB dataset** (\~60,000 images, 43 classes).

It can recognize signs like **Stop, Speed Limit, No Entry, Pedestrian Crossing, Roundabout** and more.

---

 📌 Features

* ✅ Trained CNN model with high accuracy
* ✅ Supports **43 traffic sign classes**
* ✅ Predicts uploaded images with **real class names** (not just class numbers)
* ✅ Easy-to-use Colab notebook
* ✅ Pre-trained model (`.h5` file) for instant predictions

---

 📂 Dataset
 
# GTSRB - German Traffic Sign Recognition Benchmark

# Context
The German Traffic Sign Benchmark is a multi-class, single-image classification challenge held at the International Joint Conference on Neural Networks (IJCNN) 2011. We cordially invite researchers from relevant fields to participate: The competition is designed to allow for participation without special domain knowledge. Our benchmark has the following properties:

* Single-image, multi-class classification problem
* More than 40 classes
* More than 50,000 images in total
* Large, lifelike database
---

 🛠️ Technologies Used

* Python 🐍
* TensorFlow / Keras
* OpenCV
* NumPy, Matplotlib
* Google Colab

---

 🚀 How to Run

 1️⃣ Open in Google Colab

Clone the repo or directly open the `.ipynb` notebook in Colab.

2️⃣ Mount Google Drive
"First download the Dataset in your Desktop then upload the archive.zip file in your drive then Import it using the below code"
```python
from google.colab import drive
drive.mount('/content/drive')
```

 3️⃣ Download Pretrained Model

If you don’t want to train from scratch, download the pre-trained model:

```python
!pip install gdown
!gdown --id 1ICqwuiEvdgT5bDeOWA-PqOMudAlLFSI3
```



4️⃣ Load Model

```python
from tensorflow.keras.models import load_model
model = load_model('traffic_control_system_cnn.h5')
```

 5️⃣ Upload an Image to Predict

```python
from google.colab import files
uploaded = files.upload()

for fn in uploaded.keys():
    result = predict_traffic_sign(fn)
    print("🚦 Predicted Traffic Sign:", result)
```

📊 Example Prediction

**Input:**
![Stop Sign](example_stop.jpg)

**Output:**

```
Prediction: Stop 🚦
```
📜 Class Labels (43)

* Speed limit (20km/h)
* Speed limit (30km/h)
* Speed limit (50km/h)
* …
* Stop
* No entry
* Roundabout mandatory
* End of no passing
* End of no passing for vehicles > 3.5 tons

---

👨‍💻 Author

Abhijeet Sawan
B.Tech CSE (AI/ML)
