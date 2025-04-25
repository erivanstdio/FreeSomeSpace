# FreeSomeSpace
A shell script that interactively asks the user to delete node_modules from unused projects.

# Delete `node_modules` Script 🗑️

A powerful and interactive script to help you find and delete `node_modules` directories, freeing up valuable disk space on your Mac. Perfect for developers juggling multiple projects! 🚀

---

## Features ✨

- **Interactive Selection**: Use `fzf` (fuzzy finder) to easily select which `node_modules` directories to delete.
- **Safe Deletion**: Prompts for confirmation before deleting each directory—no accidental deletions!
- **Cross-Project Support**: Works across multiple projects in a specified directory.
- **Dependency Check**: Automatically checks for and installs missing dependencies (like `fzf`).
- **User-Friendly**: Designed with clear instructions and prompts for ease of use.

---

## Prerequisites 📋

- **MacOS**: This script is optimized for MacOS.
- **Homebrew**: Required to install missing dependencies (like `fzf`).
- **Basic Terminal Knowledge**: You should be comfortable running commands in the terminal.

---

## Installation 🛠️

### 1. Download the Script
Download the script to your desired location using `curl`:
```bash
curl -O https://raw.githubusercontent.com/erivanstdio/FreeSomeSpace/main/delete_node_modules.sh
```

## 2. Make the Script Executable

Run the following command to make the script executable:

```bash
chmod +x delete_node_modules.sh
```


## 3. (Optional) Add the Script to Your PATH

To run the script from anywhere, move it to a directory in your PATH, such as `/usr/local/bin` or `~/bin`:

```bash
mkdir -p ~/bin
mv delete_node_modules.sh ~/bin/delete_node_modules
```

Then, add `~/bin` to your PATH by adding the following line to your shell configuration file (`~/.zshrc` or `~/.bashrc`):

```bash
export PATH="$HOME/bin:$PATH"
```

Reload your shell configuration:

```bash
source ~/.zshrc  # or ~/.bashrc
```

## Usage 🚀

### Basic Usage

Run the script in the current directory:

```bash
delete_node_modules
```

### Specify a Directory

To search for `node_modules` in a specific directory, use the `--dir` option:

```bash
delete_node_modules --dir /path/to/your/directory
```

### Help

To see the help message, use the `--help` option:

```bash
delete_node_modules --help
```

## How It Works ⚙️

- The script searches for all `node_modules` directories starting from the specified directory (or the current directory if none is specified).
- It displays the size of each `node_modules` directory.
- You can interactively select which directories to delete using `fzf`.
- The script asks for confirmation before deleting each selected directory.

## Example Workflow 📂

### Step 1: Navigate to Your Projects Directory

```bash
cd /path/to/your/projects
```

### Step 2: Run the Script

```bash
delete_node_modules
```

### Step 3: Select Directories to Delete

- Use the arrow keys to navigate the list of `node_modules` directories.
- Press Tab to select multiple directories.
- Press Enter to confirm your selection.

### Step 4: Confirm Deletion

For each selected directory, the script will ask for confirmation before deleting it.  
Type `y` to delete or `n` to skip.

## Troubleshooting 🛠️

### Script Is Not Executable

If you see an error like **Permission denied**, make sure the script is executable:

```bash
chmod +x delete_node_modules.sh
```

### Missing Dependencies

If the script reports missing dependencies (e.g., `fzf`), you can install them using Homebrew:

```bash
brew install fzf
```

### Script Not Found

If you see an error like **command not found: delete_node_modules**, ensure the script is in your PATH:

```bash
echo $PATH
```

If `~/bin` is not listed, add it to your PATH as described in the **Installation** section.

## License 📜

This script is provided under the MIT License. Feel free to use, modify, and distribute it as needed.

## Author 👨‍💻

**Erivan Brunno**  
GitHub: [erivanstdio](https://github.com/erivanstdio)  
Email: erivanstdio@gmail.com

## Feedback 💬

If you have any questions, suggestions, or issues, please open an issue on GitHub or contact me directly. Your feedback is highly appreciated! 🙌