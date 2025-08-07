# 🖼️ Image to Story & Speech AI 🎤

This project is an AI-powered tool that transforms any uploaded image into a descriptive short story and then converts that story into a spoken audio file. It leverages a multi-step pipeline of advanced AI models to analyze the image, generate a creative narrative, and synthesize a voice to read it aloud.

The application is built with a user-friendly interface using Streamlit.

![Demo Screenshot](https://i.imgur.com/vHqY7tC.png)

---

## 🚀 How It Works

The application follows a three-step AI pipeline to generate the final audio story:

1.  **Image to Text:** When an image is uploaded, it is first sent to a pre-trained **Vision Transformer (ViT)** model from Hugging Face. This model analyzes the visual content of the image and generates a descriptive text caption (e.g., "A couple is sitting on a bench").

2.  **Text to Story (LLM)**: The descriptive caption is then used as a prompt for a powerful **Large Language Model (LLM)** via LangChain and OpenAI. The LLM expands on this simple description, creating a short, imaginative story based on the context of the image.

3.  **Text to Speech:** Finally, the generated story is passed to a **Text-to-Speech (TTS)** model from Hugging Face, which converts the text into a natural-sounding audio file that the user can play directly in the app.

---

## 🛠️ Tech Stack & Libraries

This project combines several powerful libraries and frameworks to create a seamless user experience:

* **Python:** The core programming language.
* **Streamlit:** For building and hosting the interactive web application.
* **LangChain:** To chain together the different AI models and manage the prompting logic.
* **OpenAI:** Used for the powerful GPT model that generates the creative story.
* **Hugging Face Transformers:** For the Image-to-Text and Text-to-Speech models.
* **Dotenv:** To manage API keys and environment variables securely.
* **Torch & Sentencepiece:** Core dependencies for running the machine learning models.

---

## 🏁 Getting Started

To run this project locally, you will need to have Python installed. Follow these steps to set it up.

### Prerequisites

* Python 3.8+
* An **OpenAI API Key**.
* A **Hugging Face API Token**.

### Installation & Setup

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/Ritesh-develops/Image-to-speech.git](https://github.com/Ritesh-develops/Image-to-speech.git)
    cd Image-to-speech
    ```

2.  **Install the required Python packages:**
    ```sh
    pip install -r requirements.txt
    ```

3.  **Create an environment file:**
    Create a file named `.env` in the root directory of the project. This file will store your secret API keys.

4.  **Add your API keys to the `.env` file:**
    Open the `.env` file and add your keys in the following format:
    ```
    OPENAI_API_KEY="sk-YourSecretOpenAIKey"
    HUGGINGFACE_API_TOKEN="hf_YourSecretHuggingFaceToken"
    ```

---

## ▶️ How to Run the Application

Once you have completed the setup, you can run the application using a single command:

```sh
streamlit run app.py
