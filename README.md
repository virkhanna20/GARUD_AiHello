# 🚀 GARUD: AI-Powered Candidate-Job Matching System

GARUD is a **machine learning-powered job recommendation system** that uses **Natural Language Processing (NLP)** and **deep learning** to match candidates with job roles based on **skills, experience, education, location, and salary expectations**.

---

## 📌 Table of Contents
- [🎯 Features](#-features)
- [🛠 Tech Stack](#-tech-stack)
- [📂 Project Structure](#-project-structure)
- [🔥 Installation & Setup](#-installation--setup)
- [📊 How It Works](#-how-it-works)
- [🏆 Ranking & Scoring Method](#-ranking--scoring-method)
- [🛠 Customization](#-customization)
- [📝 To-Do](#-to-do)
- [🤝 Contributing](#-contributing)
- [📜 License](#-license)
- [💡 Author](#-author)

---

## 🎯 Features
✅ **Candidate Data Processing**: Cleans and transforms resumes using **TF-IDF** and **BERT embeddings**.  
✅ **Job Data Processing**: Extracts and encodes **job descriptions** for accurate matching.  
✅ **Candidate-Job Matching**: Uses **cosine similarity** to find the best candidates.  
✅ **Weighted Ranking System**: Scores candidates based on **experience, skills, education, location, and salary**.  
✅ **Interactive Dashboard**: View ranked candidates via a **Streamlit web app**.  

---

## 🛠 Tech Stack
- **Python**  
- **Pandas & NumPy** (Data Processing)  
- **NLTK & Scikit-learn** (NLP & TF-IDF Vectorization)  
- **Sentence-Transformers (BERT)** (Deep Learning for embeddings)  
- **Cosine Similarity** (Candidate-job matching)  
- **MinMaxScaler** (Score Normalization)  
- **Streamlit** (Interactive UI)  
- **ngrok** (For public access to the Streamlit app)  

---

## 📂 Project Structure
```
📁 GARUD
│── 📜 processed_candidate_data.csv    # Preprocessed candidate data
│── 📜 employer_profiles.csv           # Job descriptions dataset
│── 📜 processed_dataset1.csv          # TF-IDF and BERT embeddings
│── 📜 candidate_job_matches.csv       # Initial candidate-job matches
│── 📜 final_candidate_job_matches.csv # Matches with weighted scoring
│── 📜 ranked_candidate_job_matches.csv # Final ranked candidates
│── 📜 Take3.csv                        # Final output
│── 📜 app.py                          # Streamlit web app
│── 📜 requirements.txt                # Dependencies list
│── 📜 README.md                       # Project documentation
```

---

## 🔥 Installation & Setup
### 1️⃣ **Clone the Repository**
```sh
git clone https://github.com/yourusername/GARUD.git
cd GARUD
```

### 2️⃣ **Install Dependencies**
```sh
pip install -r requirements.txt
```

### 3️⃣ **Run Candidate-Job Matching**
```sh
python GARUD.py
```

### 4️⃣ **Start the Streamlit Web App**
```sh
streamlit run app.py
```

### 5️⃣ **Access the Web App**
- If using **local server**, open:  
  ```
  http://localhost:8501
  ```
- If using **ngrok**, a **public URL** (e.g., `https://xyz.ngrok.io`) will be displayed. Open it in your browser.

---

## 📊 How It Works
1. **Preprocess Candidate Data**  
   - Extracts **skills, experience, and education** from resumes.  
   - Converts text into **TF-IDF** and **BERT embeddings**.  

2. **Process Employer Job Data**  
   - Extracts **required skills, experience level, and location**.  
   - Encodes job descriptions using **TF-IDF & BERT**.  

3. **Compute Similarity & Rank Candidates**  
   - Calculates **cosine similarity** between candidate experience, skills, and job descriptions.  
   - Normalizes scores using **MinMaxScaler**.  
   - Computes a **final weighted fit score**.  

4. **Display Recommendations in Streamlit**  
   - Employers can **filter job roles** and **set a minimum fit percentage**.  
   - View **ranked candidates** for each job role.  

---

## 🏆 Ranking & Scoring Method
### 🎯 **Matching Criteria & Weights**
| Feature                 | Weight |
|-------------------------|--------|
| Experience Similarity   | 30%    |
| Skills Similarity      | 30%    |
| Education Match        | 20%    |
| Location Match        | 10%    |
| Salary Match         | 10%    |

### 📈 **Final Score Calculation**
```python
Final_Score = (0.3 * Experience_Similarity) +
              (0.3 * Skills_Similarity) +
              (0.2 * Education_Match) +
              (0.1 * Work_Location_Match) +
              (0.1 * Salary_Match)
```

---

## 🛠 Customization
- Adjust **weights** in the `weights` dictionary in `GARUD.py`.  
- Modify **TF-IDF features** by changing `max_features` in `TfidfVectorizer`.  
- Train with **different Sentence-Transformers models** by replacing `'all-MiniLM-L6-v2'`.  

---

## 📝 To-Do
- [ ] Improve **location-based ranking**  
- [ ] Implement **resume parsing** for automatic data extraction  
- [ ] Add **user authentication** for recruiters  
- [ ] Integrate with **ATS (Applicant Tracking System)**  
- [ ] Deploy on **AWS/GCP** for scalability  

---

## 🤝 Contributing
We welcome contributions! Follow these steps to contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes and commit (`git commit -m "Added feature"`).
4. Push to your branch (`git push origin feature-name`).
5. Open a pull request.

---

## 📜 License
This project is licensed under the **MIT License**.

---
