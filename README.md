# Scribd Document Downloader

A Python script that helps you download documents from Scribd by converting them to a printable format.

## Prerequisites

Before running the script, make sure you have:

1. Python 3.x installed on your system
2. Google Chrome browser installed
3. ChromeDriver (included in this repository)
4. Required Python packages (see Installation)

## Installation

1. Install the required Python packages using pip:
```powershell
python -m pip install selenium
```

## How to Use

1. Run the script:
```powershell
python scribd.py
```

2. When prompted, enter the Scribd document URL. The URL should be in the format:
```
https://www.scribd.com/document/DOCUMENT_ID/...
```

3. The script will:
   - Convert the URL to an embeddable format
   - Open Chrome browser
   - Load the document
   - Automatically scroll through all pages
   - Remove toolbars and other UI elements
   - Open the print dialog

4. In the print dialog:
   - Select "Save as PDF" as the destination
   - Click "Save" to download the document

## Features

- Automatic URL conversion
- Automatic page scrolling
- Removal of UI elements for cleaner output
- Print dialog automation

## Troubleshooting

If you encounter any errors:

1. Make sure Chrome is installed on your system
2. Verify that ChromeDriver is in the same directory as the script
3. Check that your Python environment has all required packages installed
4. Ensure you have a stable internet connection
5. Verify that the Scribd URL is correct and accessible

## Important Note

Please respect Scribd's terms of service and only download documents that you have permission to access.
