# Resume Gap Analysis Using Natural Language Processing on Job Listings

This project uses NLP and machine learning to analyze skill gaps between our current resume and the requirements of real-world data science job postings. The goal is to guide future career development by identifying missing or underrepresented skills.

## 🔍 Problem Statement

As data scientists preparing for future job applications, we want to ensure our resume reflects the most in-demand skills. This project analyzes 1500 real job postings to:

- Extract and cluster job skill requirements
- Compare them with personal resume content
- Recommend skill updates to close the gap

## 🧠 Methodology

### Part 1: Job Selection

1. **Data Collection**  
   - Collected 1500 job postings from online job platforms using data science-related keywords.
   - Extracted posting titles and body content using BeautifulSoup.

2. **Relevance Ranking**  
   - Extracted skills from both the resume and the book’s table of contents.
   - Used **TF-IDF vectorization** + **cosine similarity** to rank job postings by relevance.

3. **Output**  
   - A sorted list of job postings most related to personal data science interests and goals.

![Job Selector Diagram](https://drive.google.com/file/d/1So4NHnJy50cpN99ANzAnImm1KAgWKpt3/view?usp=drive_link)

---

### Part 2: Skill Clustering

1. **Skill Extraction & Vectorization**  
   - Parsed bullet points from selected relevant job descriptions.
   - Vectorized with **TF-IDF**.

2. **Dimensionality Reduction**  
   - Applied **SVD (Singular Value Decomposition)** to reduce dimensions and retain semantic meaning.

3. **Clustering**  
   - Used **K-Means** to identify latent clusters of technical and soft skills.

4. **Visualization**  
   - Generated word clouds and cluster summaries to visualize core skill groups.

![Skill Clustering Diagram](./images/part2-skill-clustering.png)

---

## 📊 Key Technologies

- Python
- BeautifulSoup
- Scikit-learn (TF-IDF, SVD, KMeans)
- NLP Techniques
- Word Cloud Visualization
- Resume & Job Matching Algorithms

## 📈 Output Examples

- Cosine similarity scores for job relevance
- Skill clusters (e.g., ML tools, communication, degrees)
- Word clouds for each cluster
- Highlighted missing skills vs. current resume

## 📌 Future Improvements

- Incorporate LLMs for better semantic parsing
- Extend to include company-specific skill patterns
- Build an interactive dashboard

