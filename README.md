🚀 Building an End-to-End Sentiment Analysis Pipeline with GCP

I just completed a full MLOps workflow! This project takes raw movie reviews and predicts sentiment using a containerised NLP model deployed on Google Cloud. 🎬🤖
Here is the breakdown of how I built and deployed it:

🌟 Project Overview
A comprehensive ML web app that uses Streamlit for the UI and a trained model to classify text as Positive or Negative.

🛠 The Tech Stack
•	Core: Python & Streamlit
•	ML Ops: Docker & Containerization
•	Cloud: Google Cloud Platform (GCP)
•	Deployment: Google Cloud Run (Serverless)
🏗 Simple Deployment Steps
1. Containerisation (Docker)
I packaged the app into a Docker container to ensure "it works on my machine" translates to "it works in the cloud."
2. Building on the Cloud
Used Google Cloud Build to push the image directly to the Artifact Registry:
Run below code in cloud shell

“gcloud builds submit --tag gcr.io/[PROJECT_ID]/nlp-sent-app”

3. Deploying to Cloud Run
Leveraged Google Cloud Run for a serverless, auto-scaling deployment in the asia-south1 region:

Run below code in cloud shell

“gcloud run deploy nlp-sent-app --image gcr.io/[PROJECT_ID]/nlp-sent-app --region asia-south1 --allow-unauthenticated --port 8080 --platform managed --memory 2Gi --cpu 1 --timeout 300”



💡 Why Cloud Run?
•	Zero Management: No servers to provision or patch.
•	Cost-Efficient: It scales to zero when no one is using the app.
•	High Availability: Built-in redundancy and global scaling.
📂 Project Structure
•	app.py: Streamlit frontend.
•	model.py: Sentiment prediction logic.
•	Dockerfile: Container configuration.
•	requirements.txt: Python dependencies.
Check out the full repository here: https://github.com/Rajvas1/Sentiment-analysis-GCP 🔗
#MLOps #GCP #DataScience #NLP #CloudComputing #Python #Streamlit #Docker #MachineLearning
________________________________________

