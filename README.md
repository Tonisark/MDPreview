# MDPreview - Offline Markdown Previewer

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Windows](https://img.shields.io/badge/Platform-Windows-blue.svg)](https://github.com/yourusername/mdpreview)

MDPreview is a lightweight, standalone Windows app for instantly previewing Markdown (.md) files. It renders your notes, docs, or code with full syntax highlighting, colorful emojis, tables, and themes—offline, no browser or online tools required. Built with Python and PyQt for a native feel.

Perfect for writers, devs, and note-takers who want double-click previews without the hassle.

## Features
- **Live Rendering**: Syntax-colored code blocks (Python, JS, etc.), tables, TOC, and emojis in full color.
- **Themes**: Light/dark mode toggle (Ctrl+D or menu).
- **Navigation**: File > Open (Ctrl+O) for quick switches; zoom with Ctrl+wheel.
- **Seamless Integration**: Drag-drop files onto the app, or right-click .md > "Open with MDPreview".
- **Offline & Fast**: No internet, no bloat—under 50MB install.

## Installation
1. Download the latest release from [Releases](https://github.com/yourusername/mdpreview/releases).
2. Run `MDPreviewSetup.exe` and follow the wizard.
3. On the "Select Additional Tasks" page:
   - **Create a desktop icon**: Quick access from your desktop.
   - **Add Open with MDPreview to .md file context menu**: Enables right-click preview (recommended!).
4. Click Install > Finish. The app launches automatically (optional).
5. .md files now open in MDPreview if associated—enjoy!

**Portable Mode**: Uncheck tasks for a simple extract-and-run (no registry changes).

## Usage
- **Drag & Drop**: Drag any .md file onto MDPreview.exe.
- **Double-Click**: If associated, just double-click .md files.
- **Right-Click**: Select "Open with MDPreview" from context menu.
- **From Explorer**: Type `MDPreview.exe yourfile.md` in the address bar.
- **Menus**: File > Open... | View > Toggle Dark Mode | File > Exit (Ctrl+Q).

Example: Drop a .md with code—see green keywords, red strings, blue functions, and striped tables pop!

```markdown
# Example Markdown
## Code Block
```python
def greet(name):
    print(f"Hello, {name}! 🌍")  # Green keyword, red string
```
```

## Uninstall
- Go to Settings > Apps > Search "MDPreview" > Uninstall.
- Context menu entry auto-removes; desktop icon vanishes.

## Building from Source
1. Clone the repo: `git clone https://github.com/yourusername/mdpreview.git`
2. Install deps: `pip install PyQt5 PyQtWebEngine markdown pygments pyinstaller`
3. Build .exe: `pyinstaller --onefile --windowed --name "MDPreview" md_viewer_pyqt.py`
4. For installer: Use Inno Setup with the provided `.iss` script.

## Troubleshooting
- **No Colors?**: Reinstall pygments (`pip install pygments`) and rebuild.
- **Drag-Drop Fails?**: Run as admin once, or check file paths for spaces.
- **Errors?**: Check Windows Event Viewer (search "Event Viewer" in Start). Open an issue here.
- **Build Issues?**: Ensure Python 3.8+ and Visual C++ Build Tools.

## Contributing
Pull requests welcome! For major changes, please open an issue first. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.
