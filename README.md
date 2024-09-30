# automate
DIT Automation

# automate
DIT Automation Software

**Technology Stack:**

**C++** - Core file operations, transcoding, and drive erasure
**Python** - Application logic, GUI integration, and workflow management
**PyQt/PySide** - GUI framework
**Qt Designer** - Optional GUI design tool
**FFmpeg or similar** - Video transcoding
**ctypes or Pybind11** - Python-C++ interfacing

Project Structure:

cpp_core/
file_operations.cpp/.h
transcoding.cpp/.h
drive_erasure.cpp/.h
api.cpp/.h (Exposes functions for Python)
python_app/
main.py
gui.py (Generated with Qt Designer or created programmatically)
project_data.py
report_generator.py
C++ Core Components:

File Operations:
copy_file, verify_file (checksums, file size), format_drive
Transcoding:
transcode_video (Integrates FFmpeg, handles LUTs)
Drive Erasure:
secure_erase (Low-level drive manipulation)
API:
Well-defined functions callable from Python, e.g., cpp_copy_file, cpp_transcode_video
Python Framework:

GUI:
Build using Qt Designer or programmatically.
Forms for project setup, drive selection, transcoding options, progress bars, etc.
QSS for styling (DaVinci Resolve inspiration)
Workflow:
Guide the user through steps:
Project setup
Drive preparation/formatting
Folder structure creation
File copying
Verification
Transcoding (optional)
Final formatting (optional)
Project Data:
Store in a Python class or dictionary.
Call C++:
Use ctypes or Pybind11 to load the C++ library and call functions.
Reporting:
Generate detailed logs and reports using Python libraries.
Development Steps:

**C++ Core:**

Implement file operations, transcoding, and drive erasure in C++.
Create a clean API for Python to access these functionalities.
Compile the C++ code into a shared library (.dll or .so).
Python GUI:

Design the user interface using Qt Designer or code.
Connect GUI elements to Python functions to handle user interactions.
Python Logic:

Implement the workflow logic in Python.
Handle project data storage.
Use ctypes or Pybind11 to call C++ functions from Python.
Generate reports.
Integration:

Connect the Python GUI to the workflow logic.
Ensure smooth communication between Python and C++.
Additional Considerations:

Error Handling: Implement robust error handling in both C++ and Python to provide informative messages to the user.
Progress Reporting: Provide visual feedback to the user about the progress of each step.
Cross-Platform Compatibility: If targeting multiple platforms, ensure your code is portable.
Testing: Thoroughly test all components of your application to ensure correctness and reliability.

