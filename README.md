
# ChatGPT Chat History Extractor

This Python script uses [undetected_chromedriver](https://github.com/ultrafunkamsterdam/undetected-chromedriver) and [Selenium](https://www.selenium.dev/) to automatically extract and save your ChatGPT conversation history to a text file.

## How It Works

1. The script launches an undetected Chrome browser session and navigates to the ChatGPT website.
2. You manually log into ChatGPT and open your chat history page.
3. Once you press Enter in the terminal, the script will:
    - Identify all chat history links available on the page.
    - Open each chat and scrape the conversation text.
    - Write all conversations to a single text file (`chatgpt_chat_history.txt`).

## Requirements

- Python 3.x
- [undetected-chromedriver](https://pypi.org/project/undetected-chromedriver/)  
  Install via:
  ```bash
  pip install undetected-chromedriver
  ```
- [Selenium](https://pypi.org/project/selenium/)  
  Install via:
  ```bash
  pip install selenium
  ```

## Usage

1. **Clone or Download** this repository.
2. **Install dependencies:**
   ```bash
   pip install undetected-chromedriver selenium
   ```
3. **Run the script:**
   ```bash
   python3 extract_chatgpt_history.py
   ```
   
   *Replace `extract_chatgpt_history.py` with the name of your script file if different.*

4. **Login to ChatGPT:**
   - The script will open a Chrome browser window using `undetected_chromedriver`.
   - Go to the **History** section in ChatGPT.
   - Once you have navigated to the desired history screen, return to the terminal and press Enter.

5. **Extraction:**
   - The script will iterate through all detected chat history items and extract their content.
   - Each chat conversation will be saved in `chatgpt_chat_history.txt` for easy reviewing.

## Notes

- The script uses a CSS selector (`li[data-testid^="history-item-"] a`) to identify chat history links. If the ChatGPT interface changes, you may need to update this selector.
- The `messages_selector` variable targets chat messages (`"div.text-base.gap-4"`). Adjust this if ChatGPT changes its HTML structure.
- **Manual Login:** There's a pause in the script to allow you to log into ChatGPT. This ensures that you are logged in before the script tries to access your chat history.
- **Headless Mode (Optional):** If you wish to run this without opening a browser window, you can add:
  ```python
  options.add_argument("--headless")
  ```
  However, for login and history access, headless mode might not be ideal since you need to manually interact with the page.

## Troubleshooting

- **No chats found:**  
  Make sure you are on the correct page showing your ChatGPT conversation history before pressing Enter.
- **Selectors not working:**  
  If you encounter errors or no content is extracted, inspect the ChatGPT page and update the CSS selectors in the script accordingly.
- **Timeouts or Slow Loading:**  
  If chats take longer to load, increase the `time.sleep(3)` duration.
