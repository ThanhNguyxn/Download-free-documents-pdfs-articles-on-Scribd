# Scribd Document Downloader

A Python script that helps you download documents from Scribd by converting them to a printable format.

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Installation](#installation)
3. [Detailed Usage Guide](#detailed-usage-guide)
4. [Features](#features)
5. [Troubleshooting](#troubleshooting)
6. [Important Note](#important-note)

## Prerequisites

Before running the script, make sure you have:

1. Python 3.x installed on your system
2. Google Chrome browser installed
3. ChromeDriver (included in this repository)
4. Required Python packages (see Installation)

## Installation

1. Clone or download this repository to your local machine

2. Open PowerShell and navigate to the script directory:
```powershell
cd "e:\Python\Download-free-documents-pdfs-articles-on-Scribd"
```

3. Install all required Python packages using pip:
```powershell
python -m pip install -r requirements.txt
```

4. Verify Chrome and ChromeDriver:
   - Make sure Google Chrome is installed on your system
   - The script includes `chromedriver.exe` - verify it matches your Chrome version
   - If needed, download matching ChromeDriver from [ChromeDriver Downloads](https://sites.google.com/chromium.org/driver/)

## Detailed Usage Guide

### Step 1: Finding a Document
1. Go to [Scribd](https://www.scribd.com)
2. Find the document you want to download
3. Copy the document URL from your browser's address bar
   - The URL should look like: `https://www.scribd.com/document/123456789/Document-Name`
   - Make sure you're on the document's main page, not a preview or embed page

### Step 2: Running the Script
1. Open PowerShell or Command Prompt
2. Navigate to the script directory:
```powershell
cd "e:\Python\Download-free-documents-pdfs-articles-on-Scribd"
```
3. Run the script:
```powershell
python scribd.py
```

### Step 3: Using the Script
1. When prompted, paste the Scribd document URL you copied earlier
2. The script will:
   - Convert the URL to an embeddable format
   - Open Chrome browser with Developer Tools
   - Load the document in a special view
   - Automatically scroll through all pages (wait for this to complete)
   - Remove toolbars and other UI elements
   - Open the print dialog automatically

### Step 4: Saving the Document
1. When the print dialog appears:
   - Click on "More settings" to expand options
   - Set "Destination" to "Save as PDF"
   - Under "Layout", select "Portrait" or "Landscape" based on the document
   - In "Margins", select "None" for best quality
   - Enable "Background graphics" option
2. Click "Save" and choose where to save your PDF
3. The browser will stay open so you can verify the download

### Step 5: Verifying the Download
1. Open the saved PDF to ensure:
   - All pages were captured
   - The text is clear and readable
   - Images and graphics are properly included
2. Close Chrome when you're done

### Example Usage

Here's a complete example of downloading a public document:

1. Find a public document on Scribd, for example:
```
https://www.scribd.com/document/123456789/Sample-Document
```

2. Run the script and paste the URL:
```powershell
PS E:\Python\Download-free-documents-pdfs-articles-on-Scribd> python scribd.py
Input link Scribd: https://www.scribd.com/document/123456789/Sample-Document
Link embed: https://www.scribd.com/embeds/123456789/content
```

3. The script will show progress:
```
Last Page
'toolbar_top' was successfully deleted.
✅ 'toolbar_bottom' was successfully deleted.
-------  Deleted containers  ----------
```

4. When the print dialog appears, use these recommended settings:
   - Destination: Save as PDF
   - Pages: All
   - Layout: Portrait
   - Paper size: A4
   - Margins: None
   - Scale: 100%
   - Options: ✓ Background graphics

## Features

- Automatic URL conversion to embeddable format
- Automatic page scrolling with proper timing
- Smart removal of UI elements:
  - Removes top toolbar
  - Removes bottom toolbar
  - Cleans up document scroller
- Chrome DevTools integration
- Print dialog automation with optimal settings
- High-quality PDF output
- Clean document formatting

## Troubleshooting

### Common Issues and Solutions

1. Chrome Driver Issues:
   - Make sure Chrome is installed on your system
   - Verify that `chromedriver.exe` is in the same directory as the script
   - Check that your Chrome version matches the ChromeDriver version

2. Python Environment Issues:
   - Run `python --version` to verify Python 3.x is installed
   - Ensure selenium is installed: `python -m pip list | findstr selenium`
   - Try reinstalling selenium: `python -m pip install --force-reinstall selenium`

3. Document Loading Issues:
   - Check your internet connection
   - Verify the Scribd URL is correct and accessible
   - Make sure you're logged into Scribd if the document requires it
   - Try loading the URL in a regular browser first

4. PDF Quality Issues:
   - Enable "Background graphics" in print settings
   - Set margins to "None"
   - Try both Portrait and Landscape orientations
   - Increase zoom level if text is too small

5. Script Execution Issues:
   - Run PowerShell as administrator
   - Check Windows Defender or antivirus settings
   - Verify file permissions in the script directory

6. ChromeDriver Version Mismatch:
   - Check your Chrome version:
     1. Open Chrome
     2. Click Menu (⋮) > Help > About Google Chrome
     3. Note the version number (e.g., 113.0.5672.93)
   - Download matching ChromeDriver:
     1. Visit [ChromeDriver Downloads](https://sites.google.com/chromium.org/driver/)
     2. Download the version matching your Chrome
     3. Replace the existing `chromedriver.exe` in the script directory
   - If you see "ChromeDriver was started successfully" in the DevTools window, the version is correct

## Important Note

Please respect Scribd's terms of service and only download documents that you have permission to access.
