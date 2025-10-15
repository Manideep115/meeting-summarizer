# Meeting Summarizer

This project transcribes audio from a meeting file and uses a Large Language Model (LLM) to generate a concise summary, highlight key decisions, and list actionable items. This was created as an assignment for Unthinkable Applied.

---

## Evaluation Focus

This project was built to meet the following criteria:
-   **Transcription Accuracy**: Utilizes OpenAI's Whisper model for high-quality speech-to-text transcription.
-   **Summary Quality**: Leverages the `gpt-3.5-turbo` model to produce clear and relevant summaries.
-   [cite_start]**LLM Prompt Effectiveness**: The prompt is specifically engineered to extract a summary, key decisions, and action items as required by the assignment[cite: 14, 15].
-   **Code Structure**: The code is organized into clear, reusable functions for transcription and summarization.

---

## ⚠️ Important: OpenAI API Billing

Please be aware that the OpenAI API is **not a free service**.

-   **Free Trial Credits**: New OpenAI accounts may come with a small amount of free credit. The `429 - insufficient_quota` error means you have used up these credits.
-   **Paid Account Required**: To continue using the API, you must add a payment method to your OpenAI account and ensure your spending limits are set.

You can manage your billing details here: [https://platform.openai.com/account/billing](https://platform.openai.com/account/billing)

---

## Setup and Installation

Follow these steps to set up and run the project locally.

### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd meeting-summarizer
```

### 2. Create and Activate a Virtual Environment
```bash
# Create the environment
python -m venv venv

# Activate on Windows
venv\Scripts\activate

# Activate on macOS/Linux
source venv/bin/activate
```

### 3. Install Dependencies
Install the required Python libraries using the `requirements.txt` file.
```bash
pip install -r requirements.txt
```

### 4. Configure Your API Key
You need to provide your OpenAI API key.

-   Create a new file in the project folder named `.env`.
-   Add your API key to this file in the following format:
    ```
    OPENAI_API_KEY="sk-YourSecretApiKeyGoesHere"
    ```

---

## How to Run

1.  Place your meeting audio file (e.g., `meeting.mp3`) in the project's root folder.
2.  If you are using the Jupyter Notebook, open it and run the cells in order.
3.  If you are using the Python script (`summarizer.py`), run it from your terminal:
    ```bash
    python summarizer.py your_audio_file.mp3
    ```
4.  The output will be printed to the console and saved to a `summary_...txt` file.
