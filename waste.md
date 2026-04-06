# ♻️ Waste Classification using YOLOv8

This project is a **Streamlit web application** that uses a **YOLOv8 model** to detect and classify waste from images or webcam input.

---

## 🚀 Features

- 📷 Upload an image and detect waste objects
- 🎥 Real-time detection using webcam
- 🎯 Adjustable confidence threshold
- 🖼️ Visual output with bounding boxes
- 📊 Display detection details (coordinates, scores)

---

## 🧠 Tech Stack

- Python
- Streamlit
- YOLOv8
- PIL (Python Imaging Library)

---

## 📁 Project Structure

```bash
.
├── app.py              # Main Streamlit app
├── helper.py           # Helper functions (model loading, webcam)
├── settings.py         # Configuration (paths, constants)
├── models/             # Trained YOLOv8 models
├── images/             # Default images
└── README.md           # Project documentation

## ⚙️ Installation

Install dependencies:

```bash
pip install -r requirements.txt
```

## ▶️ Usage

Run the Streamlit app:

```bash
streamlit run app.py
```

## 🖥️ How It Works

### 1. Select Model Settings
- Choose detection task  
- Set confidence threshold  

### 2. Choose Input Source
- Upload image 📷  
- Use webcam 🎥  

### 3. Detection Process
- Model processes input  
- Objects are detected using YOLOv8  
- Bounding boxes are drawn  

### 4. View Results
- Detected image displayed  
- Detection data shown (optional)  

---

## 📌 Code Explanation (Simplified)

### 1. Page Setup
Configures Streamlit layout and title  

### 2. Sidebar Controls
- Select task (Detection)  
- Adjust confidence level  

### 3. Model Loading
Loads pre-trained YOLOv8 model from path  

### 4. Image Handling
- Upload or use default image  
- Display input image  

### 5. Detection

Run:

```python
model.predict(image, conf=confidence)
```

- Extract bounding boxes  
- Plot results  

### 6. Webcam Mode
Uses helper function for real-time detection  

---

## 📊 Output Example

- Input Image → Displayed on left  
- Detected Image → Displayed on right  

### Detection Data:
- Bounding box coordinates  
- Confidence scores  
- Class labels  

---

## ❗ Error Handling

Displays error if:
- Model fails to load  
- Image cannot be opened  
- Invalid input source selected  

---

## 🔮 Future Improvements

- Add segmentation support  
- Improve UI/UX  
- Add more waste categories  
- Deploy on cloud (Streamlit Cloud / AWS)  

---

## 🤝 Contributing

Feel free to fork this repo and submit pull requests.

---

## 📜 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

- YOLOv8 by Ultralytics  
- Streamlit for UI framework

  
