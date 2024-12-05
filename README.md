ChatGPT History Exporter
A Python script to export your ChatGPT conversation history for backup or sharing purposes.

Features
Automatically navigates your ChatGPT history.
Extracts unique conversations and saves them to a text file.
Works with undetected-chromedriver to bypass detection mechanisms.
Prerequisites
Python 3.8+

Dependencies: Install the required Python packages:

bash
Copy code
pip install undetected-chromedriver
Google Chrome: Ensure you have Chrome installed and accessible on your system.

Set Up Chrome for Remote Debugging: Launch Chrome with the following command to enable remote debugging:

bash
Copy code
"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --remote-debugging-port=9222 --user-data-dir="C:\ChromeDebug"
How to Use
Clone or Download the Repository:

bash
Copy code
git clone https://github.com/yourusername/chatgpt-history-exporter.git
cd chatgpt-history-exporter
Run the Script:

bash
Copy code
python chatgpt_history_exporter.py
Manual Login:

After running the script, the browser will open.
Log in to ChatGPT and navigate to your conversation history page.
Export Conversations:

Once logged in, return to the terminal and press Enter to let the script proceed.
The script will extract all conversations and save them to a file named chatgpt_chat_history.txt.
View Exported Chats: Open the chatgpt_chat_history.txt file in the same directory to review your exported conversations.

Notes
Ensure Chrome is launched using the exact command provided for remote debugging.
You may encounter delays if the ChatGPT website takes time to load.
License
This project is licensed under the MIT License.
