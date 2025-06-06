# klippy

![Screenshot 2025-05-19 at 11 42 49](https://github.com/user-attachments/assets/287666a1-8a7e-4f2c-a2f8-e5be5960d00f)

A sleek, efficient tool for converting Kindle highlights to Markdown files for Obsidian.

## Overview

Klippy extracts your Kindle highlights and notes, organizing them into neatly formatted Markdown files that integrate seamlessly with Obsidian or other Markdown-based note-taking systems.

## Features

- **Automatic Extraction**: Reads directly from your Kindle device
- **Markdown Conversion**: Transforms highlights into formatted Markdown
- **Obsidian Integration**: Creates backlinks and a Map of Content (MOC)
- **Rich UI**: Enhanced experience with progress indicators and colorful output (when Rich is installed)

## Prerequisites

- **Python 3.6+**: Klippy is written in Python and requires version 3.6 or higher
- **Git**: Required for cloning the repository
- **Pip**: Python package manager for installing dependencies
- **Rich** (optional): For enhanced UI with progress indicators and colorful output

## Installation

#### Clone Repository

**Linux and Mac**

```bash
# Clone the repository
git clone https://github.com/jackcasstlesjones/klippy.git ~/.config/klippy
```

```bash
# Make the script executable
chmod +x ~/.config/klippy/klippy
```

```bash
# Optional: Install Rich for enhanced UI
pip install rich
```

### Make Klippy Available System-wide

**Method 1: Add to PATH (Linux/Mac)**

Option A: Using echo command:

```bash
# For zsh users
echo 'export PATH="$HOME/.config/klippy:$PATH"' >> ~/.zshrc
```

```bash
# For bash users
echo 'export PATH="$HOME/.config/klippy:$PATH"' >> ~/.bashrc
```

Option B: Manual addition:

1. Open your shell configuration file in a text editor:
   - For zsh: `nano ~/.zshrc` or `vim ~/.zshrc`
   - For bash: `nano ~/.bashrc` or `vim ~/.bashrc`
2. Add this line to the file:
   ```
   export PATH="$HOME/.config/klippy:$PATH"
   ```
3. Save and close the file

Apply changes to current session:

```bash
# For zsh users
source ~/.zshrc
```

```bash
# For bash users
source ~/.bashrc
```

**Method 2: Create a Symlink (Linux/Mac)**

```bash
# Create a symlink to make klippy available system-wide
sudo ln -s ~/.config/klippy/klippy /usr/local/bin/klippy
```

## Usage

Start klippy with one of the following commands:

```bash
# Configure klippy settings
klippy --config
```

```bash
# Process clippings without deleting the source file
klippy --add
```

```bash
# Process clippings and delete the source file
klippy --sync
```

```bash
# Delete clippings file without processing
klippy --delete
```

## How It Works

1. Connect your Kindle device to your computer
2. Run klippy with your preferred command
3. Klippy extracts highlights from "My Clippings.txt"
4. Highlights are organized by book into separate Markdown files
5. A Map of Content (MOC) file links all your books together

## License

This project is available under the MIT License.
