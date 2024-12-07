# Document Anonymizer 🕵️‍♀️🔒

## Problem Statement

In an era of increasing digital document sharing, protecting personal and sensitive information has become crucial. Individuals often need to share documents like passports, PAN cards, and Aadhaar cards for various purposes, but revealing full personal details can lead to privacy risks and potential identity theft.

The Document Anonymizer addresses this critical challenge by providing a user-friendly, secure solution to automatically blur and mask sensitive information in documents before sharing.

## Key Features 🌟

### 1. Intelligent Document Anonymization

- Automatically detects and blurs sensitive personal information
- Supports multiple document types:
  - Passport
  - PAN Card
  - Aadhaar Card
  - Other government-issued identification documents

### 2. Advanced Anonymization Techniques

- Uses multiple layered anonymization approaches:
  - Machine Learning-based anonymization
  - Regex-based pattern matching
  - Advanced blurring techniques
- Detects and masks:
  - Personal identification numbers
  - Dates of birth
  - Place of birth/residence
  - Other sensitive textual information

### 3. User-Friendly Interface

- Drag and drop file upload
- Preview of original and anonymized documents
- One-click document download
- Support for pre-loaded sample documents
- Dark and light mode support

### 4. Cross-Platform Compatibility

- Web-based application
- Responsive design
- Works on desktop and mobile browsers

## How It Works 🔍

### Anonymization Process

1. **Initial Upload**

   - User uploads a document or selects a pre-loaded sample
   - Image is immediately sent to backend for processing

2. **Machine Learning Anonymization**

   - Eden AI API performs initial anonymization
   - Removes basic recognizable personal information

3. **Advanced OCR Processing**

   - Pytesseract performs Optical Character Recognition
   - Identifies text patterns using predefined regex rules
   - Detects sensitive information like:
     - Passport numbers
     - Date formats
     - Location names
     - PAN card numbers
     - Aadhaar number segments

4. **Intelligent Blurring**

   - Applies Gaussian blur to detected sensitive regions
   - Blurs bottom section of document for additional privacy
   - Ensures readability while protecting personal details

5. **Image Rendering**
   - Processed image returned to frontend
   - Side-by-side comparison of original and anonymized documents
   - Option to download anonymized document

## Tech Stack 💻

### Backend

- **Language**: Python
- **Web Framework**: Flask
- **Image Processing**:
  - OpenCV (cv2)
  - Pytesseract
- **API Integration**:
  - Eden AI Anonymization API
- **Additional Libraries**:
  - NumPy
  - Requests
  - Logging

### Frontend

- **Language**: TypeScript
- **Framework**: React
- **State Management**: React Hooks
- **Styling**:
  - Tailwind CSS
  - Framer Motion (animations)
- **HTTP Client**: Axios
- **Icons**: Lucide React

### Deployment

- **Backend**: Flask development server
- **Frontend**: React development server
- **Potential Production Deployment**:
  - Backend: Gunicorn/uWSGI
  - Frontend: Vercel/Netlify
  - Containerization: Docker

## Prerequisites 🛠️

### Backend

- Python 3.8+
- Tesseract OCR installed
- pip packages:
  - flask
  - flask-cors
  - opencv-python
  - pytesseract
  - requests
  - numpy

### Frontend

- Node.js 14+
- npm/yarn
- React 17+

## Installation & Setup 🚀

### Backend Setup

```bash
# Clone the repository
git clone <repository-url>

# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set Tesseract OCR path in script
# Modify pytesseract.pytesseract.tesseract_cmd in server.py

# Run the server
python server.py
```

### Frontend Setup

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Run development server
npm start
```

## Security Considerations 🔐

- No personal documents are stored server-side
- Temporary file processing
- CORS configured for controlled access
- Uses secure API for initial anonymization

## Limitations ⚠️

- Accuracy depends on document quality
- Not 100% foolproof anonymization
- Limited to specific document types
- Requires good quality, clear document scans

## Future Roadmap 🗺️

- Support more document types
- Improve OCR accuracy
- Add user authentication
- Create mobile app version
- Implement more advanced ML models

## Contributing 🤝

Contributions are welcome! Please read our contributing guidelines before submitting pull requests.

## License 📄

[Specify your license here]

## Contact 📧

[Your contact information]
