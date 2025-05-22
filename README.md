🌿 AI-Powered Crop Disease Prediction Web App
This project is a Python-based web application that uses a Convolutional Neural Network (CNN) model to predict plant diseases from leaf images. It also suggests appropriate supplements and allows users to explore and purchase them.

🔍 Features
📷 Upload leaf images for disease prediction.

🧠 CNN-based image classification model trained on 39 plant disease classes.

📊 Detailed disease descriptions, preventive steps, and supplement suggestions.

🛒 Marketplace to view and "buy" supplements.

💳 Simulated payment system for purchasing products.

🧠 Model Details
The CNN model is built using PyTorch.

It accepts 224x224 RGB leaf images.

Trained on a dataset of 39 classes of plant diseases.

Final layer predicts the class index which maps to:

disease_info.csv — contains disease names, descriptions, steps, and images.

supplement_info_modified.csv — contains supplement recommendations and buying info.

🗂️ Project Structure
csharp
Copy
Edit
.
├── CNN.py                           # CNN architecture
├── app.py                           # Main Flask application
├── plant_disease_model_1_latest.pt  # Trained CNN model weights
├── disease_info.csv                 # Disease-related information
├── supplement_info_modified.csv     # Supplement product info
├── static/
│   └── uploads/                     # Uploaded images
├── templates/
│   ├── home.html
│   ├── index.html
│   ├── contact-us.html
│   ├── mobile-device.html
│   ├── submit.html
│   ├── market.html
│   └── product_details.html
│   └── payment.html
└── README.md
🚀 How to Run
Clone the Repository

bash
Copy
Edit
git clone https://github.com/yourusername/plant-disease-predictor.git
cd plant-disease-predictor
Install Dependencies
Make sure you have Python 3.7+ and install the required packages:

bash
Copy
Edit
pip install flask torch torchvision pandas pillow
Ensure CSV and Model Files Exist

disease_info.csv

supplement_info_modified.csv

plant_disease_model_1_latest.pt

Run the App

bash
Copy
Edit
python app.py
The app will be available at http://127.0.0.1:5000.

📸 Prediction Flow
User uploads an image of a plant leaf.

The image is preprocessed and passed to the CNN model.

The predicted index is matched to disease and supplement data from CSV files.

Results are rendered on the submit.html page with:

Disease name

Description and preventive steps

Supplement recommendations and purchase link

📦 Additional Routes
Route	Description
/	Home page
/index	AI Engine Page
/contact	Contact Page
/mobile-device	Mobile device notice
/submit	Prediction result page
/market	List of supplements with buy links
/product/<index>	Individual product details
/payment	Simulated payment page
/payment-success	(You may add this template optionally)

📌 Notes
CNN model must be placed as plant_disease_model_1_latest.pt in the root directory.

Make sure the image upload path (static/uploads) exists.

Check the encoding of the CSV files (cp1252) when modifying.

📃 License
This project is for educational purposes only. You may modify and use it under an open-source license of your choice.

