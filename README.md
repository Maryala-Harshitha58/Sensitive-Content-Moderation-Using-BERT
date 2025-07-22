# Sensitive Content Moderation System using BERT Algorithm 🔍

Sensitive Content Moderation using BERT employs a deep learning model to detect and filter offensive, harmful, or inappropriate content online. By understanding context and meaning in text, BERT enhances accuracy in identifying hate speech, explicit language, or abuse, promoting safer communication on digital platforms.


## ✨ Features

- 📊 Real-time text analysis using BERT models
- 🎨 Modern, responsive UI with dark mode support
- 📁 File upload support for batch analysis
- 📈 Interactive visualization of analysis results
- 💾 History tracking with MongoDB integration
- 🔄 API endpoint for text classification
- 💬 Positive alternative suggestions for toxic content
- 🔍 Advanced emoji detection and analysis
- 📊 Real-time progress tracking for batch processing
- 🌓 Customizable dark/light theme toggle

## 🛠️ Tech Stack

### Frontend
- React.js
- Tailwind CSS
- Framer Motion
- React Icons
- Chart.js

### Backend
- Flask
- Transformers (Hugging Face)
- MongoDB with local storage fallback
- Python 3.8+
- Emoji detection

## 🚀 Getting Started

### Prerequisites
- Node.js (v14+)
- Python 3.8+
- MongoDB (optional - the system can work with local storage)

### Installation

1. Clone the repository
```bash
git clone https://github.com/YourUsername/Sensitive-Content-Moderation-System
```

2. Setup Backend
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: .\venv\Scripts\activate
pip install -r requirements.txt
```

3. Setup Frontend
```bash
cd frontend
npm install
```

4. Environment Variables
Create `.env` files in both frontend and backend directories (see `.env.example` for reference)

### Running the Application

1. Start Backend
```bash
cd backend
python app.py
```

2. Start Frontend
```bash
cd frontend
npm start
```

Visit `http://localhost:3000` to access the application.

### ScreenShots
---
### 🏠 1. Moderation Home Page

<img width="753" height="407" alt="image" src="https://github.com/user-attachments/assets/6b13f547-056f-4723-961e-c9d92b428bd3" />

---

### 💬 2. Text Analysis

<img width="754" height="453" alt="image" src="https://github.com/user-attachments/assets/5f08c761-2a38-41ed-844c-81bf9b88a3cb" />

---

### 🤖 3. BERT Algorithm Analysis

<img width="759" height="470" alt="image" src="https://github.com/user-attachments/assets/23dcea04-2e3a-4170-9af8-6fc9c052a389" />

---

### 🧠 4. Result of Single Comment

<img width="756" height="421" alt="image" src="https://github.com/user-attachments/assets/30fe2d60-929d-484c-a1c7-614cd3c4b2ab" />

---

### 🗃️ 5. Dataset Comment Classification

<img width="719" height="426" alt="image" src="https://github.com/user-attachments/assets/c4f703a7-030e-4a5b-b654-8af9081db70f" />

---

### 🥧 6. Pie Chart Visualization

<img width="721" height="455" alt="image" src="https://github.com/user-attachments/assets/0f2226f5-5d07-403b-8148-44f2661ec96c" />

---

## 📝 API Documentation

### Text Classification Endpoint
- **URL**: `/api/content/classify`
- **Method**: `POST`
- **Body**: `{ "text": "string" }`
- **Response**: 
```json
{
  "text": "string",
  "classification": "string", 
  "confidence": number,
  "toxic_words": ["string"],
  "has_emoji": boolean,
  "positive_suggestion": "string",
  "direct_positive_alternative": "string",
  "timestamp": "string"
}
```

### File Classification Endpoint
- **URL**: `/api/content/classify-file`
- **Method**: `POST`
- **Body**: Form data with file
- **Response**: 
```json
{
  "results": [
    {
      "text": "string",
      "classification": "string",
      "confidence": number,
      "toxic_words": ["string"],
      "has_emoji": boolean,
      "positive_suggestion": "string",
      "direct_positive_alternative": "string"
    }
  ],
  "total": number
}
```

### Progress Tracking Endpoint
- **URL**: `/api/content/progress`
- **Method**: `GET`
- **Response**: 
```json
{
  "total": number,
  "processed": number,
  "in_progress": boolean,
  "error": "string" (optional)
}
```

## 🌟 Key Features Explained

### Toxicity Detection
The system uses a BERT-based model to analyze and classify text as toxic, offensive, or neutral. It can detect toxic words, phrases, and even emojis in the input text.

### Positive Alternative Suggestions
For toxic or offensive content, the system provides two types of suggestions:
1. **Direct Positive Alternatives**: Transforms the original message into a positive version by replacing toxic words with positive ones.
2. **Constructive Responses**: Suggests how to respond to toxic content in a more constructive way.

### Visualization
The BERT visualization feature shows the step-by-step process of how the BERT model analyzes text, from tokenization to final classification.

### Batch Processing
Upload text files or CSV files for batch analysis, with real-time progress tracking.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- HarshithaMaryala - [GitHub Profile](https://github.com/Maryala-Harshitha58)
- SanjayCheekati - [GitHub Profile](https://github.com/SanjayCheekati)

## 🙏 Acknowledgments

- HuggingFace for BERT models
- MongoDB Atlas for database hosting

