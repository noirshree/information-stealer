## README: System Information & Activity Monitor

This project is a modular Python-based utility designed to capture system-level data and user activity logs. It automates the collection of hardware specifications, clipboard history, screen captures, and keystroke logs for diagnostic or monitoring purposes.

### Core Functionalities


**System Profiling:** Extracts OS details, architecture, hostname, IP address, and CPU specifications.


* **Clipboard Monitoring:** Captures current text data from the system clipboard.
* **Screen Capture:** Takes a full-screen screenshot and saves it as a `.png` file.
* **Keystroke Logging:** Records keyboard input for a specified duration (default 30 seconds) and exports it to a text file.

---

### File Architecture

| File | Purpose |
| --- | --- |
| **`main.py`** | The primary entry point that orchestrates all monitoring modules. |
| **`system_info.py`** | Gathers hardware and network configuration. |
| **`clipdata.py`** | Accesses the system clipboard using the `pyperclip` library. |
| **`screenshot.py`** | Utilizes `pyautogui` to capture the current display. |
| **`keylogger.py`** | Uses `pynput` to listen for and record keyboard events. |

---

### Prerequisites & Installation

To run this project, you will need **Python 3.x** and the following third-party libraries:

```bash
pip install pyautogui pyperclip pynput

```

*Note: On some operating systems, you may need to grant the terminal or IDE "Accessibility" permissions to allow screen capture and keyboard listening.*

---

### Usage

1. **Navigate** to the project directory.
2. **Execute** the main script:
```bash
python main.py

```

3. **Output:** The script will generate the following files in the local directory:
* `system_info.txt`: Hardware and OS details.
* `clipboard.txt`: The text found on your clipboard at the time of execution.
* `screenshot.png`: An image of your current screen.
* `keylog.txt`: A record of keys pressed during the script's run time.

---

### Educational Disclaimer

This tool is intended for **authorized security testing and educational purposes only**. Unauthorized use of keyloggers or data collection tools on systems without consent is illegal and unethical. Always ensure you are operating within legal and policy boundaries.
