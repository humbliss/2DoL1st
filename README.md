# Flask To-Do List Application

A simple, responsive to-do list application built with Flask and SQLite. The application can be run as a web app.

## Features

- Create, toggle, and delete tasks
- Filter tasks by status (All, Active, Completed)
- Responsive design that works on mobile and desktop
- Persistent storage using SQLite database
- Can be packaged as a standalone desktop application

## Screenshots

![To-Do List App](screenshots/todo-app.png)

## Installation

1. Clone the repository:
   
   ```
   git clone https://github.com/yourusername/flask-todo-app.git
   cd flask-todo-app
   ```

2. Create a virtual environment and activate it:
   
   ```
   python -m venv .venv
   .venv\Scripts\activate  # On Windows
   source .venv/bin/activate  # On macOS/Linux
   ```

3. Install the required packages:
   
   ```
   pip install -r requirements.txt
   ```

## Usage

### Running as a Web Application

1. Run the application:
   
   ```
   python app.py
   ```

2. Open your web browser and navigate to:
   
   ```
   http://127.0.0.1:5000/
   ```

### Building as a Desktop Application

1. Install the required packages:
   
   ```
   pip install -r requirements.txt
   ```

2. Build the application:
   
   **On Windows:**
   
   ```
   build_app.bat
   ```
   
   **On macOS/Linux:**
   
   ```
   chmod +x build_app.sh
   ./build_app.sh
   ```

3. The standalone application will be available in the `dist/TodoApp` directory.

4. To run the application:
   
   **On Windows:**
   
   - Navigate to `dist/TodoApp` and double-click on `TodoApp.exe`
   
   **On macOS:**
   
   - Navigate to `dist` and double-click on `TodoApp.app`
   
   **On Linux:**
   
   - Navigate to `dist/TodoApp` and run `./TodoApp`

## Project Structure

```
flask-todo-app/
├── app.py                  # Main application file
├── desktop_app.py          # Simple desktop wrapper using webbrowser
├── webview_app.py          # Advanced desktop wrapper using pywebview
├── todo_app.spec           # PyInstaller specification file
├── build_app.bat           # Windows build script
├── build_app.sh            # macOS/Linux build script
├── todo.db                 # SQLite database
├── requirements.txt        # Project dependencies
├── templates/              # HTML templates
│   └── index.html          # Main template
├── README.md               # Project documentation
└── LICENSE                 # MIT License file
```

## How It Works

### Web Application

- The application uses Flask as the web framework
- Data is stored in a SQLite database
- The front-end is built with HTML, CSS, and minimal JavaScript
- Tasks can be filtered by their completion status

### Desktop Application

- The desktop version uses PyWebView to create a native window
- PyWebView embeds a web browser component to display the Flask application
- PyInstaller packages everything into a standalone executable
- The application runs a local Flask server and connects to it via the embedded browser
- All data is stored locally in the SQLite database

## Future Improvements

- Add user authentication
- Add due dates for tasks
- Add categories/tags for tasks
- Implement task search functionality
- Add dark mode toggle

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 To-Do List App

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Acknowledgements

- Flask - Web framework
- SQLite - Database
- Font Awesome - Icons (if used)
