# Naptick-Task-1
# Naptick AI - Generalized RAG Sleep & Wellness Coach

This repository contains the Python script (`Naptick_1.py`) for a Retrieval Augmented Generation (RAG) based AI assistant focused on sleep and wellness. It uses a generalized knowledge base and can be run in Google Colab.

## Features

*   Generates sample wearable data, chat history, user profiles, location data, and custom knowledge.
*   Builds FAISS vector stores for efficient information retrieval.
*   Utilizes the Mistral-7B-Instruct-v0.2 LLM for response generation.
*   Provides a Gradio web interface for interactive chat.

## Running in Google Colab

1.  **Prerequisites:**
    *   A Google Account.
    *   A Hugging Face Account. You'll need an Access Token (read permission is sufficient).

2.  **Setup Colab Environment:**
    *   Open a new Google Colab notebook: [colab.research.google.com](https://colab.research.google.com)
    *   **Set Runtime Type:** Go to `Runtime` -> `Change runtime type` and select `T4 GPU` (or any available GPU).
    *   **Add Hugging Face Token:**
        *   In Colab, click the "Key" icon (Secrets) in the left sidebar.
        *   Add a new secret:
            *   **Name:** `HF_TOKEN`
            *   **Value:** Paste your Hugging Face Access Token.
        *   Ensure "Notebook access" is enabled for this secret.

3.  **Load and Run the Script:**
    *   In a new code cell in your Colab notebook, clone this repository and navigate into it, or directly load the script:

      ```python
      # Option 1: Clone the repo (if you have other files or want to keep it organized)
      !git clone https://github.com/PratyushAggarwal1/Naptick-Task-1.git
      %cd Naptick-Task-1

      # Then, to run the script:
      !python Naptick_1.py
      ```

      OR

      ```python
      # Option 2: Directly download and run the script (simpler for a single file)
      !wget https://raw.githubusercontent.com/PratyushAggarwal1/Naptick-Task-1/main/Naptick_1.py
      !python Naptick_1.py
      ```

4.  **Execution Notes:**
    *   **First Run:** The script will take several minutes to install libraries, download models (embedding model & LLM), generate data, and build vector stores. You'll need to authorize Google Drive access when prompted by the script.
    *   **Subsequent Runs:** Will be faster as models are cached and data/vector stores are loaded from your Google Drive (`/content/drive/MyDrive/Naptick_Challenge/`).
    *   **Gradio Interface:** Once the script completes LLM loading and setup, it will launch a Gradio web interface. A public `*.gradio.live` link will appear in the Colab output. Click this link to interact with the chatbot.

5.  **Interacting with the Chatbot:**
    *   Open the `*.gradio.live` link in your browser.
    *   Use the chat interface to ask questions about sleep, simulated health data, or general wellness.
