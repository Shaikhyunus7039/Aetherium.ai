## Aetherium.ai - An AI Chat Project

Aetherium.ai is a project that allows users to interact with text, images, audio, and PDFs through a chat interface powered by various AI models. It provides a convenient way to leverage AI functionalities for different data types.

### Features

* **Quantized Model Integration:** This app utilizes "quantized models" designed for efficient operation on regular hardware. These models offer similar performance to their larger counterparts while requiring less computational power.  Quantized Models from TheBloke: [https://huggingface.co/TheBloke](https://huggingface.co/TheBloke)

* **Audio Chatting with Whisper AI:** Aetherium.ai integrates Whisper AI for robust audio transcription, enabling seamless audio messaging and natural conversation flow through voice input. Whisper models: [https://huggingface.co/collections/openai/whisper-release-6501bba2cf999715fd953013](https://huggingface.co/collections/openai/whisper-release-6501bba2cf999715fd953013)

* **Image Chatting with LLaVA:** LLaVA, a fine-tuned LLaMA model, is integrated for image processing. It utilizes CLIP models to generate image embeddings, allowing the app to understand and respond to visual content, making image-based chat interactions more engaging. llama-cpp-python repo for Llava loading: [https://github.com/abetlen/llama-cpp-python](https://github.com/abetlen/llama-cpp-python)

* **PDF Chatting with Chroma DB:**  For professional and academic users, Aetherium.ai leverages Chroma DB, a vector database, enabling efficient interaction with local PDFs. Users can directly engage with their PDF content, extracting insights, summaries, and conversing with the text within the documents. Chroma website: [https://docs.trychroma.com/](https://docs.trychroma.com/)


## Getting Started

To set up Local Multimodal AI Chat, clone the repository and follow these steps:

**Note:** These instructions assume you already have Python and pip installed.

1. **Download Models (GGUF Format):**

    * Choose the models you want to use from Hugging Face ([https://huggingface.co/](https://huggingface.co/)), ensuring compatibility with the project and availability in GGUF format.
    * Download the model files specifically in the `.gguf` format and place them in the `models` folder within the project directory.

2. **Download LLaVA Files (Required):**

   * LLaVA files are mandatory for this project's image processing functionalities.
   * Download the necessary LLaVA files (e.g., `ggml-model-q5_k.gguf`, `mmproj-model-f16.gguf`).
   * Place these files in a separate folder named `llava` within the project directory.

3. **Update Configuration File:**

    * Open the `config.yml` file in a text editor.
    * Locate the sections for each model (e.g., `mistral`, `llava`).
    * Update the `model_path` key in each section with the **correct path** to the downloaded model file(s) in the `models` or `llava` folder (depending on the model).

4. **Optional - Change Profile Pictures:**

    * Place your user and/or bot profile pictures (user_image.pnd and/or bot_image.png) in the `chat_icons` folder.

5. **Run the Application:**

    * Open a terminal or command prompt and navigate to the project directory.
    * Run the following commands:

        1. `python3 SetupDatabase.py` (Initializes the sqlite database for chat sessions)
        2. `streamlit run main.py` (Runs the application)

**Note:** After running `streamlit run main.py`, a web interface will launch in your default browser. You can interact with the chat interface using text, images, audio, or uploaded PDFs based on the models you downloaded and configured.
