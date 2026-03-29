# Reader

A Flask-based web application for browsing and viewing files across software projects. It lets you explore directory structures, inspect supported source files, and copy their contents directly from a simple web interface.

## Key Features

- **Copy file contents**: View and copy individual files' contents (Python, HTML, CSS, JavaScript, and more).
- **Copy all files**: Copy the content of all supported files in the project, excluding certain directories if desired.
- **Easy directory navigation**: Browse your project’s directory structure in a simple, clean interface.
- **Exclude directories**: Exclude specific directories from being copied using a checkbox filter.
- **No need to open files manually**: Quickly view and copy the contents of any file without opening an editor.

## Supported File Types

- `.as` — ActionScript
- `.py` — Python
- `.html` — HTML
- `.css` — CSS
- `.js` — JavaScript
- `.csl` — Cite-Style Language
- `.yml` — YAML
- `.md` — Markdown
- `.txt` — Text
- `.dart` — Dart

## Installation

### 1. Clone the repository
```bash
git clone <repository-url>
cd <project-folder>
````

### 2. Set up a virtual environment (recommended)

```bash
python3 -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate      # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

If needed, generate requirements:

```bash
pip freeze > requirements.txt
```

## Usage

### Run the Flask app

```bash
python reader.py
```

### Open in browser

```
http://127.0.0.1:5000/
```

You should see your project directory and be able to browse and view files.

## How It Works

* The backend scans your project directory for supported file types
* System and dependency folders are ignored (`.git`, `.venv`, `__pycache__`, `node_modules`)
* Files are read and rendered in the browser for quick inspection
* Encoding fallback ensures files load safely when possible

## Error Handling

* Files that cannot be read are safely skipped or reported
* Errors (encoding issues, permissions, etc.) are shown in the UI instead of crashing the app

## License

This project is open-source and available under the MIT License.
