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

## **Contributing**

Contributions are welcome\! If you have ideas for improvements or find any issues, please open an issue or submit a pull request.

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for details.
