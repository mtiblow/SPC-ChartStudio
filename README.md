# SPC-ChartStudio

A comprehensive process control charting application for statistical process control (SPC) with Individual and Moving Range (I-MR) charts, distribution analysis, and advanced data management capabilities.


## 📊 Overview

SPC-ChartStudio is a professional-grade standalone application designed for quality control and process monitoring in manufacturing environments. It provides real-time statistical analysis, control charts, and comprehensive data management with multi-user support through file locking.

## ✨ Features

### Core Functionality
- **I-MR Control Charts**: Individual and Moving Range charts with automatic control limit calculations
- **Statistical Analysis**: Cp, CpK, standard deviation, population deviation, and more
- **Distribution Analysis**: Normal distribution curves with specification limit overlays
- **Go/No-Go Gage Analysis**: Visual color-coded pass/fail analysis with customizable gauge pins

### Data Management
- **Guided Setup Wizard**: Step-by-step process for creating new files with intelligent defaults
- **Template System**: Save and reuse configurations for consistent setups across multiple RPO numbers
- **Multi-Entry Support**: Manage up to 10 entries per file with independent configurations
- **File Locking**: Multi-user environment support with automatic file locking and read-only mode
- **Dual Export Format**: Automatic saving to both JSON and tab-delimited text files

### User Interface
- **Keyboard Shortcuts**: Comprehensive keyboard navigation (F1-F12, Ctrl+shortcuts)
- **Machine List Management**: Centralized machine number management with import/export
- **Characteristics Library**: Image-based characteristics selection with automatic loading
- **Real-time Updates**: Charts update automatically as data is entered

### Advanced Features
- **Control Limit Locking**: Lock control limits after baseline establishment (configurable points)
- **External Change Detection**: Monitor and alert for external file modifications
- **Tolerance Protection**: Administrator-level tolerance unlocking for data integrity
- **Control Rule Violations**: Automatic detection of Rule 1 (out of limits), Rule 2 (trends), and Rule 3 (bias)
- **Watermark Indicators**: Visual "OUT OF SPEC" and "OUT OF CONTROL" watermarks on charts



## 📖 Usage Guide

### Getting Started

1. **Launch the Application**
   - Double-click the Process Chart icon
   - Choose "New File" or "Open File" from the startup dialog

2. **Creating Your First File**
   - Click "📊 New File"
   - Enter Item Number (required for file organization)
   - Enter RPO Number
   - Choose configuration method:
     - **Manual Setup**: Configure entries and gauge pins manually
     - **Use Template**: Load a previously saved configuration

3. **Data Entry Workflow**
   - **Entry 1**: Contains Part Weight, Actual Value, and Notes columns
   - **Entry 2+**: Contains Actual Value and Notes columns
   - Use `F11` to cycle through entries quickly
   - Charts update automatically as you enter data

4. **Saving Your Work**
   - Press `Ctrl+S` or click the Save button
   - Files are automatically organized in item-specific folders
   - Both JSON and tab-delimited text files are created

### Keyboard Shortcuts

There is a list of keyboard shortcuts within the application under the Help menu.

<img width="702" height="832" alt="keyboard_shortcut" src="https://github.com/user-attachments/assets/9485da29-3ad8-4b1b-9689-150aa5686caf" />


## 📁 Data Organization

The application automatically creates and manages the following folder structure:

```
Main_Data_Location/
├── [ItemNumber1]/              # Auto-created folders for each item
│   ├── RPO[number].json       # Saved data files
│   ├── RPO[number].txt        # Tab-delimited export
│   └── [ItemNumber]_template.txt  # Reusable templates
├── [ItemNumber2]/
│   └── ...
└── [ItemNumber3]/
    └── ...

Software_Installation_Folder/
├── Process Chart version #.exe    # Main application
├── Machine List/               # Machine configurations
│   └── machine_list.txt       # Default machine list
└── characteristics/            # Characteristics reference
    ├── characteristics.txt     # Text-based characteristics
    └── [optional images]       # Supporting images (if needed)
```

### Directory Behavior:
- **Item Number Folders**: Created automatically in your chosen data location when saving charts for new items
- **Software Folder**: Contains the application executable and reference data (Machine List, characteristics)
- **Data Separation**: Keeps your process data separate from the application installation


## 🔧 Configuration

### Setting Up Machine Lists

1. Navigate to `Machine List` menu
2. Click "Manage Machine Lists..."
3. Add machine numbers (one per row)
4. Save the list for use across all files

### Adding Characteristics Images

1. Create a `characteristics` folder in the application directory
2. Add PNG, JPG, or JPEG images
3. Give proper names to the images. The names of the images will be shown within the dropdown list.
4. Images automatically appear in the Characteristics dropdown
5. For text-only options, create `characteristics.txt` with one item per line

### Creating Templates

Templates save time when working with the same item number repeatedly:

1. Set up your first file with all configurations
2. In the wizard confirmation screen, click "💾 Save as Template"
3. Template is saved for the item number
4. Next time, select "Use existing template" for instant setup

## 📊 Understanding the Charts

### Process Chart (I-MR)
- **Upper Chart**: Individual values with control limits
- **Lower Chart**: Moving ranges between consecutive points
- **Yellow Lines**: Control limits (UCL/LCL)
- **Orange Line**: Mean/center line
- **Red Lines**: Specification limits

### Control Rules
- **Rule 1**: Points outside control limits (marked with yellow circles)
- **Rule 2**: Six points in a row increasing/decreasing (marked with purple squares)
- **Rule 3**: Six points in a row on same side of mean (marked with orange X's)

### Distribution Chart
- **Bell Curve**: Normal distribution based on your data
- **Shaded Areas**: Regions outside specification limits
- **Statistics Box**: Live calculations of mean, standard deviation, and sample size

## 🔒 Multi-User Features

### File Locking
- Automatic file locking prevents simultaneous editing
- Clear indication of who has a file open
- Read-only mode for viewing locked files
- Lock files are automatically cleaned up

### Working with Locked Files
When opening a file that's in use:
1. You'll see who has it locked and since when
2. Choose "Open Read-Only" to view without editing
3. The title bar shows "(READ-ONLY)" status
4. Save button is disabled in read-only mode



## 🆕 Checking for Updates

1. Go to **Help → Check for Updates**
2. The application will check GitHub for newer versions
3. If newer version found, it will provide a direct link to the new version



## 🤝 Support & Feedback

For questions, issues, or feature requests, please:

- Open an issue on GitHub
- Contact the developer by email: <mtiblow_github@proton.me>


## System Requirements

- Windows operating system
- No additional software dependencies required
- Internet connection (for update checking only)

## Installation

1. Download the latest release from the GitHub repository
2. Run the executable file

## Documentation

For detailed information about using Process Chart application, refer to the tutorial in the help menu of the application.

## License

This software is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Updates

Process Chart includes automatic update checking to ensure you're always using the latest version. Updates can be checked manually through Help → Check for Updates.



---
© 2025 Matthew Tiblow. All rights reserved.
