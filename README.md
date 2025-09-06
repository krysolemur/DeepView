# DeepView

DeepView is a cyber analysis tool for inspecting web pages and detecting potential issues, bugs, or security misconfigurations.  
It provides a desktop application (based on PyQt) that loads and previews target web pages in a sandbox-like environment.  

---

## Features (planned)

- Cross-platform desktop application (Linux, Windows, macOS).  
- Built with PyQt5 + QtWebEngine for modern web rendering.  
- Simple toolbar with common actions:
  - Reload page
  - Copy current URL
  - Save / Save As (planned)
  - Settings dialog (planned)
  - About & Shortcuts dialogs
- Logging system with configurable verbosity.  
- Configuration system (JSON-based).  
- (Future) Extended analysis modules:
  - HTTP header inspection
  - Script/content analysis
  - Dangerous patterns detection  

---

## Project Structure

DeepView/
│
├── main.py # Entry point for application
├── requirements.txt # Python dependencies
├── README.md # Project documentation
│
├── config/ # Configuration system
│ └── config_manager.py
│
├── ui/ # User interface components
│ ├── init.py
│ ├── app.py
│ ├── main_window.py
│ └── settings_window.py
│
├── resources/ # Icons, assets, etc.
│ └── icons/
│ └── deepview.png
│
└── logger_utils.py # Logging utilities


---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/DeepView.git
cd DeepView
```

3. Create and activate virtual enviroment:
```bash
# Linux/MacOS
python3 -m venv venv
source venv/bin/activate

# Windows (PowerShell)
python -m venv venv
venv\Scripts\Activate.ps1
```

4. Install dependencies:
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

5. Run app:
```bash
# Python
python main.py http://example.com

# Python3
python3 main.py http://example.com
```

The application will:
 - Start a PyQt window
 - Load the given URL into the embedded browser
 - Provide basic toolbar functionality