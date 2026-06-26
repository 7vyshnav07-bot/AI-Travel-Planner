# 🌴 Kerala AI Travel Planner

An AI-powered travel assistant that helps users explore Kerala by providing personalized travel recommendations, weather information, tourist attractions, local food suggestions, transportation details, and budget-friendly itineraries.

The application combines Retrieval-Augmented Generation (RAG) with Large Language Models (LLMs) to answer travel-related questions accurately using a curated Kerala tourism knowledge base.

---

## 📌 Features

- 🤖 AI-powered travel chatbot
- 📚 Retrieval-Augmented Generation (RAG)
- 🌦️ Live weather information
- 🗺️ District-wise travel recommendations
- 🍛 Local food suggestions
- 🚗 Transportation guidance
- 💰 Budget travel planning
- 📍 Tourist attraction recommendations
- 💬 Natural language conversation interface

---

## 🛠️ Tech Stack

### Frontend
- Streamlit

### Backend
- Python
- LangChain
- LangGraph

### AI & Machine Learning
- Groq LLM
- HuggingFace Embeddings
- FAISS Vector Database

### APIs
- Open-Meteo Weather API

---

## 🏗️ Project Architecture

```
                User
                  │
                  ▼
          Streamlit Interface
                  │
                  ▼
           User Question
                  │
                  ▼
             LangGraph Flow
                  │
      ┌───────────┴───────────┐
      ▼                       ▼
 Weather Tool           RAG Retriever
(Open-Meteo API)            │
                             ▼
                    FAISS Vector Store
                             │
                     Kerala Documents
                             │
                             ▼
                         Groq LLM
                             │
                             ▼
                      Final Response
```

---

## 📂 Project Structure

```
Kerala-AI-Travel-Planner/
│
├── app.py
├── chatbot.py
├── weather.py
├── district_data.py
├── vectorstore.py
├── requirements.txt
├── README.md
│
├── data/
│   ├── Thiruvananthapuram.txt
│   ├── Kollam.txt
│   ├── Pathanamthitta.txt
│   ├── Alappuzha.txt
│   ├── Kottayam.txt
│   ├── Idukki.txt
│   ├── Ernakulam.txt
│   ├── Thrissur.txt
│   ├── Palakkad.txt
│   ├── Malappuram.txt
│   ├── Kozhikode.txt
│   ├── Wayanad.txt
│   ├── Kannur.txt
│   └── Kasaragod.txt
│
└── faiss_db/
```

---

## 🚀 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Kerala-AI-Travel-Planner.git
```

Move into the project folder

```bash
cd Kerala-AI-Travel-Planner
```

Install dependencies

```bash
pip install -r requirements.txt
```

Create a `.env` file

```env
GROQ_API_KEY=YOUR_GROQ_API_KEY
```

Run the application

```bash
streamlit run app.py
```

---

## 💬 Example Questions

- Suggest a 3-day trip to Munnar.
- Best beaches in Kerala.
- What is the weather in Wayanad today?
- Budget trip under ₹10,000.
- Famous food in Kozhikode.
- Places to visit near Alleppey.
- Romantic destinations in Kerala.
- Family trip itinerary for Kochi.

---

## 📊 Dataset

The knowledge base contains curated information for all districts of Kerala, including:

- Tourist attractions
- Local cuisine
- Transportation
- Accommodation
- Budget information
- Travel tips
- District highlights

This information is converted into embeddings using HuggingFace and stored inside a FAISS vector database for semantic retrieval.

---

## ⚙️ Workflow

1. User enters a travel query.
2. LangGraph routes the request.
3. Weather-related queries call the Open-Meteo API.
4. Travel queries retrieve relevant district information using FAISS.
5. Retrieved context is sent to the Groq LLM.
6. The chatbot generates a personalized response.

---

## 📈 Future Improvements

- Hotel recommendation system
- Google Maps integration
- Image-based destination search
- Voice assistant
- Multi-language support
- User authentication
- Trip history
- PDF itinerary generation

---

## 👨‍💻 Author

**Vyshnav Manoharan**

BCA (Cloud Computing)

Kristu Jayanti University

---

## 📄 License

This project is developed for educational purposes as part of a Bachelor of Computer Applications (BCA) final-year project.
