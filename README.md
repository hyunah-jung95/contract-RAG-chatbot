# Contract RAG Chatbot
This app is built for users who are dealing with a lot of contracts by finding accurate information searching through contract DB.<br>
Not only answering to user's questions, it also offers specific references of contracts with groundness cheking by RAG architecture.<br>
User can upload and initiate personal contracts DB privately and securely via this app.<br>

[👉 Go to Live APP](https://prototype-787703115620.us-central1.run.app)

# Workflow
![GCP-Kodebox-diagram](https://github.com/user-attachments/assets/8e67ed66-3433-4545-b341-0289b364ae01)
1. User uploads PDF contracts via the app.
  - PDF files are stored in Google Storage(GS).
  - When GS bucket is updated, cloud function is triggered to import the files into data store integrated with Google Search App.
2. User asks questions with chatbot.
  - Chatbot AI generates the answer by searching the stored contracts with Google Search App.
  - Answer contains answer, groundness check, metadata of referenced contracts(title, store address, contents, etc.)
3. The conversations are saved as a session to enhance the performance of the answering.

# Speciality
- 97% accurancy
- specified for the contracts analysis and searching.
- scalable for adding documents, new users, creating new buckets.
- secrued data pipeline capsulated in GCP(Google Cloud Platform).
- Considered migration to other cloud platform(Azure, AWS) and other Gernerativa AI(ChatGPT, etc.)

# My contribution
- Designed architecture communicating with PM from beginning to meet client's business needs.
- Developed both backend logic with python and frontend UI with streamlit.
- Deployed and monitored the app using CI/CD pipelines in GCP.

# Technical Stack
- Python, streamlit, GCP
