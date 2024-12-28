# Contract RAG Chatbot
This app is built for users who are dealing with a lot of contracts by finding accurate information searching through contract DB.<br>
Not only answering to user's questions, it also offers specific references of contracts with groundness cheking by RAG architecture.<br>
User can upload and initiate personal contracts DB privately and securely via this app.<br>

[👉 Go to Live APP](https://prototype-787703115620.us-central1.run.app)

# Workflow
![GCP-Kodebox-diagram](https://github.com/user-attachments/assets/8e67ed66-3433-4545-b341-0289b364ae01)
- User uploads PDF contracts via the app.
  - PDF files are stored in Google Storage(GS).
  - When GS bucket is updated, cloud function is triggered to import the files into data store integrated with Google Search App.
- User asks questions with chatbot.
  - Chatbot AI generates the answer by searching the stored contracts with Google Search App.
  - Answer contains answer, groundness check, metadata of referenced contracts(title, store address, contents, etc.)
- The conversations are saved as a session to enhance the performance of the answering.

# Performance 
- 97% accurancy
- scalable for adding documents, new users, creating new buckets.
- secrue

# Technical Stack
- Python, streamlit, GCP(Google Cloud Platform)
