
# VSCode and Python Setup Guide for Windows

## Prerequisites

-   A Windows computer (Windows 10 or 11 recommended)
-   Administrator access to install software
-   Stable internet connection

## Part 1: Installing Python

### Step 1: Download Python

1.  Open your web browser and go to [python.org](https://python.org/)
2.  Click the yellow "Download Python" button (it will show the latest version)
3.  This will download the Python installer (a .exe file)

### Step 2: Install Python

1.  Navigate to your Downloads folder and double-click the Python installer
2.  **IMPORTANT**: Check the box that says "Add Python to PATH" at the bottom of the installer window
3.  Click "Install Now" (recommended for beginners)
4.  Wait for the installation to complete
5.  Click "Close" when finished

### Step 3: Verify Python Installation

1.  Press `Windows + R` to open the Run dialog
2.  Type `cmd` and press Enter to open Command Prompt
3.  Type `python --version` and press Enter
4.  You should see something like "Python 3.12.x" (the exact version may vary)
5.  Type `pip --version` and press Enter to verify pip (Python's package manager) is installed

## Part 2: Installing Visual Studio Code

### Step 1: Download VSCode

1.  Go to [code.visualstudio.com](https://code.visualstudio.com/)
2.  Click the "Download for Windows" button
3.  This will download the VSCode installer

### Step 2: Install VSCode

1.  Run the downloaded installer
2.  Accept the license agreement
3.  Choose installation location (default is fine)
4.  **Important**: Check these boxes:
    -   "Add to PATH"
    -   "Create a desktop icon"
    -   "Add 'Open with Code' action to Windows Explorer file context menu"
    -   "Add 'Open with Code' action to Windows Explorer directory context menu"
5.  Click "Install"
6.  Click "Finish" and choose to launch VSCode

## Part 3: Setting up VSCode for Python

### Step 1: Install the Python Extension

1.  Open VSCode
2.  Click the Extensions icon in the left sidebar (it looks like four squares)
3.  Search for "Python" in the search box
4.  Find the extension by Microsoft (it should be the first result)
5.  Click "Install"
6.  Wait for the extension to install

### Step 2: Install Additional Helpful Extensions

While you're in the Extensions marketplace, consider installing these beginner-friendly extensions:

-   **Python Indent**: Helps with proper Python indentation
-   **Python Docstring Generator**: Helps create documentation
-   **Code Runner**: Allows you to run Python code with a simple keyboard shortcut
-   **GitLens**: Enhances Git capabilities (useful for version control later)

### Step 3: Configure Python Interpreter

1.  Open VSCode
2.  Press `Ctrl + Shift + P` to open the Command Palette
3.  Type "Python: Select Interpreter" and select it
4.  Choose the Python version you installed (it should show the path)

## Part 4: Creating Your First Python Project

### Step 1: Create a Project Folder

1.  Create a new folder on your desktop or in Documents called "my-python-projects"
2.  In VSCode, go to File > Open Folder
3.  Select your "my-python-projects" folder

### Step 2: Create Your First Python File

1.  In VSCode, click "New File" or press `Ctrl + N`
2.  Save the file as "hello.py" (File > Save As)
3.  Type this simple code:

```python
print("Hello, World!")
name = input("What's your name? ")
print(f"Nice to meet you, {name}!")

```

### Step 3: Run Your Python Code

There are several ways to run your code:

**Method 1: Using the Run Button**

1.  Click the triangle "Run" button in the top-right corner
2.  Your code will run in the terminal at the bottom

**Method 2: Using the Terminal**

1.  Open the terminal in VSCode (View > Terminal or `Ctrl + ``)
2.  Type `python hello.py` and press Enter

**Method 3: Using Code Runner (if installed)**

1.  Press `Ctrl + F5` to run the code

## Part 5: Essential VSCode Settings for Python

### Customize Your Setup

1.  Go to File > Preferences > Settings (or press `Ctrl + ,`)
2.  Search for these settings and adjust as needed:

-   **Python Default Interpreter Path**: Should point to your Python installation
-   **Python Linting Enabled**: Keep this checked for error detection
-   **Python Formatting Provider**: Set to "autopep8" or "black" for automatic code formatting
-   **Files Auto Save**: Set to "afterDelay" to automatically save your work

### Useful Keyboard Shortcuts

-   `Ctrl + S`: Save file
-   `Ctrl + Z`: Undo
-   `Ctrl + Shift + Z`: Redo
-   `Ctrl + /`: Comment/uncomment line
-   `Ctrl + Shift + P`: Open command palette
-   `F5`: Run with debugger
-   `Ctrl + F5`: Run without debugger

## Part 6: Installing Python Packages

### Using pip in VSCode Terminal

1.  Open the terminal in VSCode (`Ctrl + ``)
2.  Install packages using pip:

```bash
pip install requests
pip install numpy
pip install matplotlib

```

### Creating a Virtual Environment (Recommended)

1.  Open terminal in VSCode
2.  Create a virtual environment:

```bash
python -m venv myenv

```

3.  Activate it:

```bash
myenv\Scripts\activate

```

4.  Install packages in the virtual environment:

```bash
pip install package_name

```

## Troubleshooting Common Issues

### Python Not Recognized

-   Make sure you checked "Add Python to PATH" during installation
-   Restart your computer after installation
-   Try reinstalling Python with the PATH option checked

### VSCode Not Finding Python

-   Use `Ctrl + Shift + P` and type "Python: Select Interpreter"
-   Choose the correct Python installation path
-   Restart VSCode

### Extensions Not Working

-   Make sure you've installed the Python extension
-   Reload VSCode (Ctrl + Shift + P, then type "Developer: Reload Window")
-   Check that your Python interpreter is selected

## Next Steps for Learning

1.  **Practice Basic Python**: Work through online tutorials or books
2.  **Learn Git**: Version control for your projects
3.  **Explore Jupyter Notebooks**: Great for data science and learning
4.  **Try Different Projects**: Web development, data analysis, automation scripts
5.  **Join Communities**: Python Discord servers, Reddit communities, Stack Overflow

## Useful Resources

-   [Python.org Tutorial](https://docs.python.org/3/tutorial/)
-   [VSCode Python Documentation](https://code.visualstudio.com/docs/languages/python)
-   [Real Python](https://realpython.com/) - Excellent tutorials
-   [Python Package Index (PyPI)](https://pypi.org/) - Find packages to install

## Final Tips

-   Always save your work frequently (`Ctrl + S`)
-   Use meaningful file and folder names
-   Comment your code to remember what it does
-   Don't be afraid to experiment and make mistakes
-   Use the built-in terminal for running Python commands
-   Take advantage of VSCode's IntelliSense for code completion

You're now ready to start your Python programming journey! Remember, the best way to learn is by doing, so start creating small projects and gradually work your way up to more complex applications.
