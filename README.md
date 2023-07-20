# Keylogger with Google Drive Uploader

This project is a simple keylogger written in Python that records the keys pressed by the user and uploads the log file to Google Drive using the Google Drive API. Please note that keyloggers can be considered malicious if used without the user's knowledge and consent. Make sure to use this script responsibly and only for legitimate purposes.

## Requirements

Before running the script, make sure you have the following requirements installed:

- Python 3.x
- pynput library (for capturing keyboard events)
- pydrive library (for uploading files to Google Drive)

You can install the required libraries using pip:

```bash
pip install pynput pydrive
```

## Configuration:
---------------

**1. Google Drive API Setup:**

- Go to the [Google Developers Console](https://console.cloud.google.com/projectselector2/apis/dashboard?supportedpurview=project).
- Create a new project (or use an existing one).
- Enable the Google Drive API for the project.
- Create credentials for the project and download the `client_secrets.json` file.

**2. Keylogger Configuration:**

- Set the `ATTACHMENT_FILE_NAME` variable to specify the name of the log file to be uploaded.

## Running the Keylogger:
To run the keylogger, execute the Python script:
```bash
python keylogger.py
```
## How It Works
The keylogger captures the keys pressed by the user using the `pynput` library.

It stores the recorded keys in a list, and when the number of recorded keys exceeds 10, it writes them to the log file specified by the `ATTACHMENT_FILE_NAME` variable. 

The keylogger continues recording until the `Esc` key is pressed, at which point it saves the remaining keys to the log file and uploads it to Google Drive using the `pydrive` library.

**Note:** The script will keep running and capturing key events until the `Esc` key is pressed, so make sure to terminate it appropriately.

## Disclaimer
The use of keyloggers to record a user's keystrokes without their knowledge and consent may violate privacy laws and is considered unethical.
This script is provided for educational and informational purposes only. The developer is not responsible for any misuse or damage caused by the use of this script. Use it responsibly and only on systems you own or have explicit permission to monitor.

**Use at your own risk.**
