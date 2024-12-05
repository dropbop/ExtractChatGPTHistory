# ChatGPT Chat History Scraper

A Python script to automate the extraction of chat history from ChatGPT's web application using **undetected-chromedriver** and **Selenium**.

## Features

- **Automated Browser Control**: Uses undetected-chromedriver to bypass detection and interact with the ChatGPT website.
- **Chat History Extraction**: Retrieves chat URLs and content from the history section.
- **Output to Text File**: Saves all chat messages in a structured format to `chatgpt_chat_history.txt`.
- **Error Handling**: Skips problematic chats and logs errors without halting the process.

## Requirements

- Python 3.8+
- Google Chrome installed
- The following Python libraries:
  - `undetected-chromedriver`
  - `selenium`

Install the dependencies with:

```bash
pip install undetected-chromedriver selenium
Usage
Clone the repository or download the script.

Open a terminal and navigate to the script's directory.

Run the script:

bash
Copy code
python chatgpt_chat_scraper.py
The script will:

Open a Chrome browser.
Navigate to the ChatGPT login page (https://chatgpt.com).
Manual Login: Log in to ChatGPT and navigate to the history screen.

Press Enter when prompted to start extracting chats.

Wait for the script to process all chats. The content will be saved in chatgpt_chat_history.txt.

Output
The script generates a file chatgpt_chat_history.txt in the same directory, containing all chat messages organized by chat session.

Example Output:
vbnet
Copy code
--- Chat 1 ---
User: Hello, how are you?
ChatGPT: I'm doing great, thank you!

--- Chat 2 ---
User: What is the capital of France?
ChatGPT: The capital of France is Paris.
Known Issues
Manual Interaction: Requires manual login to ChatGPT due to security restrictions.
Selectors May Change: The script relies on specific HTML structure and CSS selectors, which may change if the ChatGPT website is updated.
Error Handling: Skips chats that cause errors during processing.
Contributing
Feel free to submit pull requests to enhance functionality or improve stability. Please test changes thoroughly before submitting.

License
This project is licensed under the MIT License.
