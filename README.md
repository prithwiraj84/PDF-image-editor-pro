# PDF & Photo Text Editor

A powerful Python desktop application for editing text in PDFs and photos with advanced features including font detection, click-to-edit functionality, and multiple export formats.

## Features

### Core Features
- ✅ **PDF Text Editing**: Edit text in PDF documents while preserving exact position, font, size, and style
- ✅ **Photo Text Editing**: Extract and edit text from images using OCR
- ✅ **Font Detection & Matching**: Automatically detects and matches fonts from original documents
- ✅ **Click-to-Edit**: Click on any text in the PDF to edit it directly
- ✅ **Undo/Redo**: Full undo/redo functionality for all edits
- ✅ **Multiple Export Formats**: Save as PDF, DOCX, or PNG

### Advanced Features
- Modern, user-friendly GUI built with PyQt5
- Real-time text preview with font controls
- Color picker for text color customization
- Page navigation for multi-page PDFs
- OCR text extraction from photos
- Font family and size controls
- Interactive canvas with zoom and pan capabilities

## Installation

### Prerequisites

1. **Python 3.8 or higher**

2. **Tesseract OCR** (for photo text extraction):
   - **Windows**: Download and install from [GitHub Releases](https://github.com/UB-Mannheim/tesseract/wiki)
     - Default installation path: `C:\Program Files\Tesseract-OCR\tesseract.exe`
   - **macOS**: `brew install tesseract`
   - **Linux**: `sudo apt-get install tesseract-ocr` (Ubuntu/Debian)

### Setup

1. Clone or download this repository

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
python pdf_photo_editor.py
```

## Usage

### Opening Documents

1. **Open PDF**: Click "📄 Open PDF" in the toolbar and select a PDF file
2. **Open Photo**: Click "🖼️ Open Photo" in the toolbar and select an image file (PNG, JPG, JPEG, BMP, TIFF, GIF)

### Editing Text

1. **Enable Edit Mode**: Click the "✏️ Edit Mode" button in the toolbar
2. **Select Text**: Click on any text in the PDF document
3. **Edit Text**: The selected text will appear in the text editor panel on the left
4. **Customize Font**: 
   - Choose font family from the dropdown
   - Adjust font size using the spin box
   - Select text color using the color picker
5. **Apply Changes**: Click "Apply Changes" to update the document

### Exporting Documents

- **Save as PDF**: Click "💾 Save as PDF" to export the edited PDF
- **Save as DOCX**: Click "📝 Save as DOCX" to export as a Word document
- **Save as PNG**: Click "🖼️ Save as PNG" to export the current page/image as PNG

### Navigation

- Use "◀ Previous" and "Next ▶" buttons to navigate between PDF pages
- The page indicator shows current page number and total pages

### Undo/Redo

- Click "↶ Undo" to undo the last action
- Click "↷ Redo" to redo an undone action

## Technical Details

### Libraries Used

- **PyQt5**: Modern GUI framework
- **PyMuPDF (fitz)**: PDF manipulation and rendering
- **Pillow (PIL)**: Image processing
- **pytesseract**: OCR for text extraction from images
- **python-docx**: DOCX file generation

### Architecture

- **PDFCanvas**: Custom widget for PDF display and interaction
- **PhotoEditor**: Widget for photo editing with OCR
- **MainWindow**: Main application window with toolbar and panels

## Troubleshooting

### Tesseract Not Found

If you get an error about Tesseract not being found:
- Make sure Tesseract is installed
- On Windows, the application will automatically look for Tesseract at `C:\Program Files\Tesseract-OCR\tesseract.exe`
- If installed elsewhere, you may need to modify the path in the code

### PDF Not Loading

- Ensure the PDF is not password-protected
- Check that the PDF file is not corrupted
- Try opening the PDF in another PDF viewer to verify it's valid

### Font Issues

- Some fonts may not be available on your system
- The application will attempt to use the closest matching font
- Custom fonts can be added to your system's font directory

## Future Enhancements

Potential features for future versions:
- Batch processing of multiple PDFs
- Advanced text formatting options (bold, italic, underline)
- Text search and replace
- Annotation tools
- Watermark addition
- PDF merging and splitting
- More export formats (HTML, TXT, etc.)

## License

This project is open source and available for personal and commercial use.

## Support

For issues or feature requests, please create an issue in the repository.
