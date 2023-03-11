# Investment-memo-LLM
Generate VC-grade investment memos using LLMs.

Investment Memo Generator
This script is designed to generate an investment memo using OpenAI's language model, prompt the user for input, and then save the memo as a text file and send it via email. The script uses the langchain library to interact with OpenAI's language model and the smtplib library to send emails.

# Prerequisites
Before running this script, you need to have an OpenAI API key. You can obtain one by signing up for OpenAI's GPT-3 program. Additionally, you will need to have Python 3 and the following libraries installed:

- ```openai```
- ```smtplib```
- ```ssl```
- ```datetime```
- ```langchain```

# Setup

- Clone the repository or download the script.
- Install the required libraries by running pip install -r requirements.txt in the terminal.
- Enter your OpenAI API key in the script by replacing the empty string with your API key: ```os.environ["OPENAI_API_KEY"] = "" #Enter your OpenAI API key here```
- Enter your email provider's SMTP server in the sendEmail function: ```smtp_server = "smtp.gmail.com" #Enter your email provider's SMTP server here - Yahoo doesn't work```
- If you want to load the password from a text file, comment out the hardcoded password line and uncomment the loadPassword() line in the sendEmail function.

# How to Use

To use the script, run it from the command line using python investment_memo_generator.py. The script will prompt you for input, including the name of the company you want to create an investment memo for and the email addresses of the sender and receiver.

Once you provide the necessary inputs, the script will generate an investment memo using OpenAI's language model, format it, save it as a text file, and send it via email. You will be prompted to enter a filename for the saved memo.

The script also includes an option to ask for more information about the company. If you choose this option, the script will prompt you for a question and use OpenAI's language model to generate a response.

Notes

- The langchain library is used to interact with OpenAI's language model. The LLMChain class is used to set up the model, and the PromptTemplate class is used to customize the input prompt.
- The ConversationBufferMemory class is used to store previous conversation history and improve the accuracy of the language model's responses.
- The sendEmail function uses the smtplib library to send emails via SMTP. You will need to enter your email provider's SMTP server and your email address and password to use this function.
The saveMemo function saves the investment memo as a text file. You will be prompted to enter a filename for the saved file.
