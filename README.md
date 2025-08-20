🚀 Setup Instructions
Step 1: Download Required Files

Ensure you have the following in one main project folder:

MODEL/ folder (contains trained .sav models)

MultipleDiseasePrediction.py

streamlit run command.txt

Step 2: Install Anaconda Navigator

Download Anaconda from Anaconda Downloads
.

Install it (tutorials available on YouTube).

Open Anaconda Navigator after installation.

Step 3: Create a New Conda Environment (Recommended)

Instead of using the base environment, create a separate one for this project:

Open Anaconda Prompt and run:

conda create -n disease_prediction python=3.9


Activate the new environment:

conda activate disease_prediction


Install required packages:

pip install streamlit


(You can add more dependencies later if needed.)

Step 4: Open Spyder IDE

From Anaconda Navigator, launch Spyder.

Open MultipleDiseasePrediction.py inside Spyder.

Step 5: Set Model Paths

Inside MultipleDiseasePrediction.py, locate the model loading section:

import pickle

# Example for heart model
heart_disease_model = pickle.load(open("path_to_saved_model/heart_disease_model.sav", "rb"))

# Example for diabetes model
diabetes_model = pickle.load(open("path_to_saved_model/diabetes_model.sav", "rb"))

# Example for parkinson model
parkinson_model = pickle.load(open("path_to_saved_model/parkinson_model.sav", "rb"))


👉 Replace path_to_saved_model with the actual path of your MODEL folder.

For example, if your models are in:

C:\Users\YourName\Desktop\MultipleDiseasePrediction\MODEL\


Update the code as:

heart_disease_model = pickle.load(open("C:/Users/YourName/Desktop/MultipleDiseasePrediction/MODEL/heart_disease_model.sav", "rb"))


⚠️ Use forward slashes / instead of \ in Python paths.

Step 6: Run the Streamlit App

Open Anaconda Prompt and activate your environment:

conda activate disease_prediction


Navigate to your project folder:

cd C:\Users\YourName\Desktop\MultipleDiseasePrediction


Run the Streamlit app:

streamlit run MultipleDiseasePrediction.py

✅ This will launch the app in your browser.
