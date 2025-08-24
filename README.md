
# Symptom Checker Chatbot

## Overview  
This project is a **Symptom Checker Chatbot** designed to assist users in identifying potential health issues and recommending nearby healthcare specialists. Additionally, it includes a future phase to provide personalized insurance suggestions based on user health data. The chatbot streamlines the healthcare journey using AI-driven techniques for report summarization, health insights, and service recommendations.

---

## Features  

### **Phase 1: Medical Report Summarization and Health Issue Identification**
- **Text Extraction:** Extracts content from medical reports using OCR and text parsing techniques.
- **Vector Embeddings:** Converts extracted text into vector embeddings using **Qdrant** for semantic understanding.
- **Normal Range Validation:** Compares extracted data with a prebuilt **normal range database** to identify deviations.
- **LLM Integration:** Utilizes **Monster API** to process and verify data with context-specific responses.
- **Validation Layer:** Ensures only valid medical health reports are processed, adding a domain restriction for chatbot responses.

### **Phase 2: Recommendation of Nearby Specialists and Healthcare Centers** *(Work in Progress)*
- Integrates location-based services to recommend nearby healthcare providers.
- Tailors recommendations based on identified health issues and user preferences.

### **Additional Phase: Insurance Premium Recommendation** *(Future Phase)*
- Analyzes health risks from summarized reports.
- Suggests personalized insurance policies for optimal coverage and affordability.

---

## Tech Stack
- **Programming Language:** Python  
- **Database:** Qdrant for vector embeddings  
- **AI/ML:** Large Language Model (LLM) integration using **Monster API**  
- **Validation Layer:** Custom logic for domain-specific content validation  

---

## Project Structure  
```
symptom-checker-chatbot/
├── data/                   # Sample medical reports and datasets
├── embeddings/             # Vectorized data storage
├── scripts/                # Core processing scripts (text extraction, vectorization, etc.)
├── validation/             # Domain restriction and validation logic
├── app/                    # Backend API and chatbot implementation
├── docs/                   # Documentation and resources
└── README.md               # Project documentation
```

---

## Installation and Setup  

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/symptom-checker-chatbot.git
   cd symptom-checker-chatbot
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up Normal Range Database**
   - Prepare your **normal range database** and save it in the `data/` directory.  
   - Ensure it is in a compatible format (e.g., CSV or JSON).

4. **Run the Application**
   ```bash
   python app/main.py
   ```

5. **Access the Chatbot**
   - Navigate to `http://localhost:5000` in your browser or API client.

---

## Usage  

1. **Upload Medical Reports**  
   Users can upload their medical reports in PDF format.  

2. **Receive Summarized Insights**  
   The chatbot processes the report and provides a summarized view of key information, including potential health risks.

3. **Explore Recommendations** *(Phase 2 forthcoming)*  
   - Nearby healthcare centers and specialists based on identified issues.

---

## Future Work
- **Phase 2 Implementation:** Location-based specialist recommendations.
- **Additional Phase Implementation:** Health insurance policy recommendation system.
- Advanced natural language understanding for symptom-based queries.

---
