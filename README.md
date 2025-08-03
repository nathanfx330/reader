# Python File Reader

A Flask-based application to display and view contents of multiple file types within a directory. It scans a given directory for viewable files (e.g., Python, HTML, CSS, etc.) and renders them on a simple web interface.

## Features

- Browse and view Python files, HTML, CSS, JavaScript, YAML, Markdown, and more.
- Supports viewing of file contents within the browser.
- Skips system directories such as `.venv`, `__pycache__`, `.git`, and `node_modules`.
- Handles files with different encodings (UTF-8, Latin-1).
- Simple, user-friendly interface built with Flask.

## File Types Supported

The application recognizes and displays the following file types:
- `.py` (Python)
- `.html` (HTML)
- `.css` (CSS)
- `.js` (JavaScript)
- `.csl` (Cite-Style Language)
- `.yml` (YAML)
- `.md` (Markdown)
- `.txt` (Text)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>

    Navigate to the project folder:

cd <project-folder>

Set up a virtual environment (optional but recommended):

python3 -m venv venv
source venv/bin/activate  # For macOS/Linux
venv\Scripts\activate     # For Windows

Install required dependencies:

pip install -r requirements.txt

    Ensure you have Flask installed. You can create a requirements.txt file with:

    pip freeze > requirements.txt

Usage

    Ensure your directory contains the files you want to display.

    Run the Flask app:

python reader.py

Open a web browser and navigate to:

    http://127.0.0.1:5000/

    You should see the directory structure along with the contents of supported files.

How It Works

    The reader.py script serves as the backend that scans the target directory for files with supported extensions.

    The application uses Flask to render a UI that displays a list of viewable files, along with their contents.

    Only viewable files (Python, HTML, CSS, etc.) are shown, and system files are ignored.

    Each file is read and rendered on the page for easier inspection.

Error Handling

The application attempts to read each file and will report errors if a file cannot be read. Errors such as unsupported encodings or other file issues will be logged and shown in the file content area.
License

This project is open-source and available under the MIT License.


This README explains how to use your app, its functionality, and how to set it up. You can customize it further based on your exact setup, especially if you add additional dependencies or features later!

You said:
well it's for projects
ChatGPT said:

Got it! Since it's meant for projects, I'll adjust the README to reflect that it's for managing multiple files from Python projects, including handling project directories and content viewing. Here’s an updated version:

# Project File Viewer

A Flask-based web application for browsing and viewing multiple files from Python projects. This tool allows you to navigate through the directories of a project, view the contents of supported files (such as Python, HTML, CSS, etc.), and gain insights into the structure of your project.

## Features

- View files from a Python project with extensions like `.py`, `.html`, `.css`, `.js`, `.yml`, `.md`, `.txt`, and more.
- Automatically skips irrelevant system directories (`.venv`, `__pycache__`, `.git`, `node_modules`).
- Displays file contents directly in the browser.
- Supports files with different encodings (UTF-8, Latin-1).
- Easy-to-navigate interface with Flask to explore project files.

## Supported File Types

The application recognizes the following file extensions:
- `.py` - Python
- `.html` - HTML
- `.css` - CSS
- `.js` - JavaScript
- `.csl` - Cite-Style Language
- `.yml` - YAML
- `.md` - Markdown
- `.txt` - Text

## Installation

### 1. Clone the repository
```bash
git clone <repository-url>

2. Navigate to the project directory

cd <project-folder>

3. Set up a virtual environment (recommended)

python3 -m venv venv
source venv/bin/activate   # For macOS/Linux
venv\Scripts\activate      # For Windows

4. Install the required dependencies

pip install -r requirements.txt

Make sure that Flask is installed in your environment. If you don't have a requirements.txt, you can generate one:

pip freeze > requirements.txt

Usage
1. Run the application

To launch the application, run the following command:

python reader.py

2. Access the application

Open your web browser and go to:

http://127.0.0.1:5000/

The application will display your project’s directory structure and provide you the option to view the content of supported files.
How It Works

    Directory Scanning: The app scans your project’s directory and subdirectories, looking for files with specific extensions.

    Filtering: System directories like .venv, __pycache__, .git, and node_modules are excluded from being displayed.

    File Viewing: When a user selects a file, its content is read and displayed directly in the browser. For large projects with many files, this is a helpful way to quickly review project contents without manually opening each file.

File Handling:

    The app reads files with different encodings (UTF-8 and Latin-1) to handle any text file gracefully.

    If a file cannot be read due to errors, an appropriate error message is displayed, and the issue is logged.

License

This project is open-source and licensed under the MIT License.

Note: This tool is particularly useful for inspecting code files in a project, especially when you have a large number of files spread across multiple directories.


### Changes made:
- Clarified that this is a tool to view files from a project.
- Emphasized the project structure scanning and file viewing.
- The example URL is now generic for local access (`http://127.0.0.1:5000/`).

Let me know if there’s anything else you’d like to add!
