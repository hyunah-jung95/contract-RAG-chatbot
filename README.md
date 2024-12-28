# Contract RAG Chatbot
This application is designed for users _managing extensive contract collections_,<br>
enabling them to efficiently find accurate information through a searchable contracts database.

Not only does it provide answers to user queries,<br> 
but it also references specific contract sections with grounding verification using _Retrieval-Augmented Generation (RAG) architecture._

Users can securely and privately upload and initiate their personalized contract databases via this app.

[👉 Go to Live APP](https://prototype-787703115620.us-central1.run.app)


# Workflow
![GCP-Kodebox-diagram](https://github.com/user-attachments/assets/8e67ed66-3433-4545-b341-0289b364ae01)
### 1.	Uploading Contracts
  - Users upload PDF contracts via the app.
  - The uploaded PDFs are stored in Google Storage (GS).
  - A Google Cloud Function is triggered when the GS bucket is updated, importing the files into a datastore integrated with the Google Search App.

### 2.	Querying via Chatbot
  - Users ask questions through the chatbot.
  - The chatbot AI generates answers by searching the stored contracts using the Google Search App.
  - The response includes: The answer, Grounding verification, Metadata from referenced contracts.

### 3. Conversation Logging
  - Conversations are saved as sessions to improve answer accuracy and chatbot performance over time.


# Key Features
  - **97% Accuracy**: Optimized for high precision in contract-related queries.
  - **Specialization**: Tailored for contract analysis and database searching.
  - **Scalability**: Supports additional documents, new users, and custom bucket creation.
  - **Security**: Fully encapsulated within the Google Cloud Platform (GCP).
  - **Compatibility**: Designed with future migration to other platforms (Azure, AWS) and compatibility with other generative AI models(ChatGPT).


# My contribution
- _Designed_ the system architecture, collaborating with the PM to align with client business requirements.
- _Developed_ backend logic using Python and created a user-friendly frontend UI with Streamlit.
- _Deployed_ the app using CI/CD pipelines on GCP, ensuring reliability and scalability.


# Technical Stack
- Programming: Python, streamlit
- Cloud Platform: Google Cloud Platform(GCP)


# License
- This project is worked with jigo.ai
- The license of app is owned by jigo.ai
