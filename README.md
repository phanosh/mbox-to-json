# **Gmail to JSON Converter for LLM Automation**

A simple and effective command-line tool to convert emails exported from Gmail (as an `.mbox` file) into a structured JSON file. This is the first step in building automated workflows and intelligent agents powered by Large Language Models (LLMs) using your email data.

## **The Goal**

The primary goal of this project is to create a clean, machine-readable dataset from your Gmail emails. This structured JSON data can then be fed into LLMs to:

* Fine-tune models on your specific communication style.  
* Automate responses to common inquiries.  
* Summarize email threads.  
* Build intelligent agents that can manage your inbox.

## **How It Works**

The process is straightforward:

1. **Export Your Gmail Data**: Use [Google Takeout](https://takeout.google.com/) to export your Gmail messages. Make sure to select the **Mbox** format.  
2. **Run the Conversion Script**: Use the `mbox_to_json.py` script provided in this repository to process the downloaded `.mbox` file.  
3. **Get Your JSON File**: The script will output a `.json` file containing your emails, ready for your NLP projects.

## **Usage**

### **Prerequisites**

* Python 3.6 or higher.  
* No external libraries are needed.

### **Instructions**

1. **Clone the repository:**

```
git clone <your-repository-url>
cd <your-repository-directory>
```

2.   
   **Place your Mbox file in the directory.** You can download this file from [Google Takeout](https://takeout.google.com/).  
3. **Run the script from your terminal.** Use the `-i` flag for the input `.mbox` file and the `-o` flag for the desired output `.json` file.

```
python mbox_to_json.py -i YourEmails.mbox -o output.json

```

5.   
   If you don't provide arguments, it will look for a default `Sent-001.mbox` file and create `Sent-001.mbox.json`.

### **Command-Line Arguments**

* `--input` or `-i`: (Optional) The path to your input `.mbox` file. Defaults to `Sent-001.mbox`.  
* `--output` or `-o`: (Optional) The name of the output JSON file. Defaults to the input file name with a `.json` extension.

## **Output JSON Format**

The script will generate an array of JSON objects, where each object represents an email with the following structure:

```
[
  {
    "from": "Sender Name <sender@example.com>",
    "to": "Recipient Name <recipient@example.com>",
    "subject": "Example Subject",
    "date": "2023-10-27T10:30:00",
    "body": "This is the plain text body of the email..."
  },
  {
    "from": "Another Sender <another@example.com>",
    "to": "you@example.com>",
    "subject": "Following up",
    "date": "2023-10-26T15:45:12",
    "body": "Just following up on our previous conversation.\\n\\nBest regards"
  }
]

```

## **Next Steps & Roadmap**

* Integrate with LLM APIs (like OpenAI, Gemini, etc.).  
* Develop example "agent" scripts for tasks like summarization and auto-reply.  
* Add support for parsing HTML content and attachments.  
* Build a simple UI for easier conversion.

## **Contributing**

Contributions are welcome\! If you have ideas for improvements or find any issues, please open an issue or submit a pull request.

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.
