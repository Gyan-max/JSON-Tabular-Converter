# 🔄 JSON to Tabular Converter

A powerful Python desktop application that transforms nested JSON data into flat, structured tabular format for easy analysis and processing.

## 🎯 Project Overview

This application solves the common problem of converting complex, nested JSON structures into usable tabular data. Built with Python and Tkinter, it provides an intuitive GUI for importing JSON files, configuring conversion options, and exporting results to CSV or Excel formats.

## ✨ Features

### Core Functionality
- **JSON File Import**: Load JSON files with drag-and-drop interface
- **Intelligent Flattening**: Automatically flatten nested JSON structures
- **Configurable Options**: Customize separator characters, nesting levels, and data handling
- **Multiple Export Formats**: Save results as CSV or Excel files
- **Real-time Preview**: View original JSON and converted tabular data side-by-side

### Advanced Options
- **Custom Separators**: Choose how nested keys are joined (default: underscore)
- **Nesting Level Control**: Limit flattening depth for complex structures
- **Array Handling**: Convert JSON arrays into separate table rows
- **Data Cleaning**: Remove null/empty values automatically
- **Memory Optimization**: Efficient processing of large JSON files

### User Interface
- **Modern GUI**: Clean, professional interface with tabbed navigation
- **Status Updates**: Real-time feedback during conversion process
- **Data Summary**: Comprehensive statistics about converted data
- **Error Handling**: User-friendly error messages and validation

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.7+ installed with the following packages:

```bash
pip install -r requirements.txt
```

### Installation

1. Clone or download the project files
2. Navigate to the project directory
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the application:
   ```bash
   python json_converter.py
   ```

## 💻 Usage Guide

### Basic Workflow

1. **Launch Application**
   ```bash
   python json_converter.py
   ```

2. **Import JSON File**
   - Click "Choose JSON File" button
   - Select your JSON file from the file dialog
   - The original JSON will display in the "Original JSON" tab

3. **Configure Conversion Options**
   - **Separator**: Character used to join nested keys (e.g., `_`, `.`, `-`)
   - **Max Level**: Maximum nesting depth to flatten (leave empty for all levels)
   - **Handle Arrays**: Convert array elements to separate rows
   - **Remove Nulls**: Automatically remove empty/null columns

4. **Convert Data**
   - Click "Convert to Tabular Format"
   - View results in the "Tabular Data" tab
   - Check conversion statistics in the "Summary" tab

5. **Export Results**
   - Click "Export as CSV" for comma-separated values
   - Click "Export as Excel" for spreadsheet format

### Example JSON Structures

The converter handles various JSON formats:

**Simple Nested Object:**
```json
{
  "user": {
    "name": "John Doe",
    "contact": {
      "email": "john@example.com",
      "phone": "123-456-7890"
    }
  }
}
```

**Array of Objects:**
```json
[
  {
    "id": 1,
    "product": {
      "name": "Laptop",
      "specs": {
        "cpu": "Intel i7",
        "ram": "16GB"
      }
    }
  },
  {
    "id": 2,
    "product": {
      "name": "Mouse",
      "specs": {
        "type": "Wireless",
        "dpi": "1600"
      }
    }
  }
]
```

## 🛠️ Technical Details

### Architecture
- **Main Class**: `JSONToTabularConverter` - Handles application logic and GUI
- **JSON Processing**: Uses `pandas.json_normalize()` for efficient flattening
- **GUI Framework**: Tkinter with modern styling and responsive design
- **Data Handling**: Pandas DataFrames for robust data manipulation

### Key Methods
- `load_json_file()`: Imports and validates JSON data
- `convert_json_to_tabular()`: Performs the flattening operation
- `display_tabular_data()`: Shows converted results in table format
- `export_to_csv()` / `export_to_excel()`: Handles data export

### Conversion Strategy
- **Nested Objects**: Flattened using configurable separators
- **Arrays**: Can be exploded into separate rows or kept as strings
- **Data Types**: Automatically inferred and preserved where possible
- **Missing Values**: Handled gracefully with user-configurable options

## 📁 Project Structure

```
json-to-tabular-converter/
├── json_converter.py    # Main application file
├── requirements.txt     # Python dependencies
├── README.md           # Project documentation
└── sample_data/        # Example JSON files (optional)
```

## 🎨 Interface Features

### Color Scheme
- **Primary**: Professional blue (#2563eb)
- **Success**: Green for successful operations (#10b981)
- **Warning**: Orange for warnings (#f59e0b)
- **Clean Layout**: Light backgrounds with clear visual hierarchy

### Responsive Design
- **Tabbed Interface**: Organized display of data and options
- **Scrollable Text Areas**: Handle large datasets efficiently
- **Status Bar**: Real-time feedback on operations
- **Error Dialogs**: Clear error messaging and recovery suggestions

## 🔧 Customization

### Adding New Export Formats
To support additional export formats:

1. Add new export method to the `JSONToTabularConverter` class
2. Create corresponding button in `create_export_section()`
3. Handle file type in the export dialog

### Modifying Conversion Logic
Customize flattening behavior by:
- Updating parameters in `convert_json_to_tabular()`
- Adding preprocessing steps for specific JSON structures
- Implementing custom normalization functions

## 🐛 Troubleshooting

### Common Issues

**Large File Performance**
- For very large JSON files (>100MB), consider chunked processing
- Increase system memory if encountering memory errors
- Use nesting level limits to reduce output complexity

**Invalid JSON Format**
- Ensure JSON files are properly formatted
- Check for trailing commas or syntax errors
- Use online JSON validators for verification

**Export Errors**
- Verify write permissions in target directory
- Ensure sufficient disk space for output files
- Check that target applications can handle the column count

### Error Messages
- **"JSON data must be an object or array"**: Input must be valid JSON structure
- **"Failed to convert JSON"**: Check JSON syntax and format
- **"No data to export"**: Perform conversion before attempting export

## 🤝 Contributing

This project is part of the GUVI Data Science program. Contributions and improvements are welcome!

### Development Setup
1. Fork the repository
2. Create a virtual environment
3. Install development dependencies
4. Make changes and test thoroughly
5. Submit pull request with clear description

## 📄 License

This project is created for educational purposes as part of the GUVI Data Science curriculum.

## 🎯 Future Enhancements

- [ ] Support for JSONL (JSON Lines) format
- [ ] Batch processing for multiple JSON files
- [ ] Custom column renaming and reordering
- [ ] Data type inference and conversion options
- [ ] Integration with database systems
- [ ] Command-line interface for automation
- [ ] Advanced filtering and transformation rules
- [ ] Support for XML to tabular conversion

---

**Project**: GUVI Data Science - JSON to Tabular Converter  
**Created**: August 2025  
**Technology Stack**: Python, Pandas, Tkinter, JSON Processing
# JSON-Tabular-Converter
