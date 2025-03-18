# 🚀 **LinkedIn Post Generator**

An **AI-powered LinkedIn post generator** that creates customized, engaging posts based on **topic, length, and language** preferences. It uses **LangChain + Groq’s LLaMA 3 model** for content generation and **Streamlit** for the front-end interface.

---

## 🌟 **Features**

✅ Generate LinkedIn posts by selecting:
- **Topic** (e.g., Job Search, Motivation, Influencer, etc.)  
- **Length** (Short, Medium, Long)  
- **Language** (English, Hinglish)  

✅ **Few-shot prompting** for enhanced content quality using relevant examples.  
✅ **Dynamic post filtering** based on tags, language, and length.  
✅ **Efficient metadata extraction** with line count, tags, and language detection.  
✅ **User-friendly Streamlit interface** for easy interaction.  

---

## 🔥 **Tech Stack**

- **Backend:** LangChain + Groq’s LLaMA 3  
- **Frontend:** Streamlit  
- **Data Handling:** JSON, Pandas  
- **Environment Variables:** `dotenv`  
- **API Integration:** Groq API  

---

## 📂 **Project Structure**

```
📁 LinkedInPostGenerator  
 ┣ 📁 data  
 ┃ ┣ 📄 raw_posts.json              # Original LinkedIn posts  
 ┃ ┗ 📄 processed_posts.json        # Posts enriched with metadata  
 ┣ 📄 main.py                        # Streamlit interface & app launcher  
 ┣ 📄 post_generator.py              # Post generation logic  
 ┣ 📄 preprocess.py                  # Metadata extraction & processing  
 ┣ 📄 few_shot.py                    # Few-shot prompting logic  
 ┣ 📄 llm_helper.py                  # Groq API configuration  
 ┣ 📄 .env                           # Environment variables  
 ┣ 📄 requirements.txt               # Dependencies  
 ┣ 📄 README.md                      # Project documentation  
```

---

## ⚙️ **Installation**

### 1️⃣ Clone the repository:
```bash
git clone https://github.com/shindepooja00/LinkedInPostGenerator.git  
cd LinkedInPostGenerator
```

### 2️⃣ Create and activate a virtual environment:
```bash
# For Windows
python -m venv .venv  
.venv\Scripts\activate  

# For Mac/Linux
python3 -m venv .venv  
source .venv/bin/activate  
```

### 3️⃣ Install dependencies:
```bash
pip install -r requirements.txt  
```

### 4️⃣ Set up environment variables:
Create a `.env` file in the root directory with the following content:
```
GROQ_API_KEY=your_groq_api_key
```

---

## 🚀 **Running the Project**

Start the Streamlit app:
```bash
streamlit run main.py
```

---

## 🔧 **Usage**

1. **Select your preferences:**  
   - Choose a **topic**, post **length**, and **language**.  
2. **Click "Generate"**:  
   - The app will generate a LinkedIn post based on your preferences.  
3. **View and copy**:  
   - The generated post will be displayed for easy copying and sharing.  

---

## 🔍 **How It Works**

1. **Data Preprocessing:**  
   - `preprocess.py` extracts metadata (line count, language, and tags) from raw posts.  
   - It unifies similar tags for consistency.  

2. **Few-Shot Prompting:**  
   - `few_shot.py` filters relevant posts based on topic, length, and language.  
   - Provides examples for better context during post generation.  

3. **Post Generation:**  
   - `post_generator.py` creates a prompt with user preferences and examples.  
   - Sends the prompt to **Groq’s LLaMA 3 model** for post creation.  

---

## 🛠️ **Customization**

- **Add more topics:**  
   - Update the `raw_posts.json` and re-run `preprocess.py` to include new tags.  
- **Modify prompt style:**  
   - Edit the `generate_post()` function in `post_generator.py` to adjust prompt formatting.  

---

## 🚦 **Troubleshooting**

- If you encounter the error `model_decommissioned`, update the model name in `llm_helper.py`:
```python
llm = ChatGroq(groq_api_key=os.getenv("GROQ_API_KEY"), model_name="new_groq_model_name")
```

---

## 📚 **Dependencies**

- `streamlit`
- `langchain`
- `pandas`
- `python-dotenv`
- `json`
- `groq`
- `llama-index`

Install all dependencies:
```bash
pip install -r requirements.txt
```

---

## 🌟 **Future Enhancements**

- Add **user authentication** for personalized post generation.  
- Enable **custom themes** and styling for the Streamlit interface.  
- Integrate **LinkedIn API** for direct post sharing.  
- Add **multi-language support** for more regional variations.  

---

## 🤝 **Contributing**

Contributions are welcome!  
1. Fork the repository.  
2. Create a new branch: `git checkout -b feature-branch`  
3. Make your changes and commit: `git commit -m "Add new feature"`  
4. Push to the branch: `git push origin feature-branch`  
5. Create a pull request.  

---

##  **Author**
**Pooja Shinde**  
[GitHub](https://github.com/shindepooja00) | [LinkedIn](https://www.linkedin.com/in/pooja-dattatray-shinde/)

---

✅ **Enjoy creating powerful LinkedIn posts with AI!** 
