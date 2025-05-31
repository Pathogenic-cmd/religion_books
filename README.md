
# 📘 Gender and Religion in Publishing: A Data-Driven Analysis

This project explores the intersection of **gender**, **religion**, and **economic access** in the context of book publishing. Using a dataset of religion-related books, we performed exploratory data analysis to understand gender representation, publishing trends, religious traditions, and economic disparities among authors.

---

## 📌 Project Goals

- Assist religion and gender researchers by identifying patterns in authorship.
- Quantify representation across different religious traditions and subfields.
- Examine trends over time and across publisher types.
- Evaluate potential gender biases and disparities in religious publishing.

---

## 🔍 Key Research Questions

1. **Author Gender Representation**
   - Are women or men more likely to author religion-related books?
   - Does this vary across subtopics or religious traditions?

2. **Thematic Content vs. Gender**
   - Are male and female authors writing about different aspects of religion?

3. **Temporal Trends**
   - How has female representation changed over time?
   - Were there periods of growth linked to historical movements?

4. **Religious Tradition Breakdown**
   - Which religious traditions show greater gender diversity in authorship?

5. **Publishing & Economic Access**
   - Are women more likely to self-publish?
   - Do major publishers disproportionately publish male authors?
   - Are there pricing disparities by gender or publisher type?

---

## 📊 Dataset Overview

- **Source**:[Kaggle Project](https://www.kaggle.com/your-kaggle-username/your-kaggle-project)
- **Size**: ~103,000 records
- **Fields used**: `Authors`, `Category`, `Publish_Date`, `Description`, `Price`, `Publisher`, `is_religion`,`Religion_Tradition`

---

## ⚙️ Data Preparation

- Extracted `First_Name` from author names using regular expressions.
- Inferred `Author_Gender` using a rule-based approach (e.g., common name matching).
- Cleaned categories to group books into major **religious traditions**: Christianity, Islam, Eastern, New Age, Other.
- Extracted `Publish_Year` from publication dates.
- Categorized `Publisher` type (Traditional vs. Indie) based on heuristics (e.g., presence of known major publishers).

---

## 📈 Key Findings

### 📌 1. Gender Representation
- **Male authors** dominate religious publishing:
  - 52,322 male vs. 35,710 female authors.
- **Gender gaps** persist in most religious categories.

### 📌 2. Thematic Differences
- Used **NLP** to refine thematic grouping via **LDA topic modeling**.
- Early observations suggest women more often write about spirituality and family.

**Male author themes**
      ![Trends](\Outputs\charts\Male_Authors.png)

**Female author themes**
    ![Trends](\Outputs\charts\female_Authors.png)



### 📌 3. Temporal Trends
- **Female authorship grew gradually** over the decades.
- Notable increases post-1970s may correspond with second-wave feminism.
   ![Trends](\Outputs\charts\trends.png)


### 📌 4. Religious Tradition Breakdown

| Religion Tradition | Female | Male  | Unknown | Total  |
|--------------------|--------|-------|---------|--------|
| Other              | 31,859 | 45,838| 13,950  | 91,647 |
| Christianity       | 2,463  | 4,009 | 696     | 7,168  |
| Eastern            | 724    | 1,310 | 220     | 2,254  |
| New Age            | 592    | 926   | 147     | 1,665  |
| Islam              | 72     | 239   | 37      | 348    |

- **Christianity and Eastern religions** show slightly better gender balance than **Islam**.
- **New Age** shows relatively higher female presence by proportion.

### 📌 5. Publishing & Economic Access

| Gender | Publisher Type | Mean Price | Median | Count |
|--------|----------------|------------|--------|--------|
| Female | Traditional    | $6.31      | $5.29  | 35,692 |
|        | Indie          | $9.69      | $7.22  | 18     |
| Male   | Traditional    | $6.96      | $5.29  | 52,297 |
|        | Indie          | $9.69      | $6.71  | 25     |

- Indie authors of all genders **price books higher**, likely due to cost recovery.
- **Few women use indie publishing**, but when they do, their median price is higher than men’s.

---

## 📂 Folder Structure

```
📦 Religion_Gender_Analysis
├── 📄 README.md
├── 📊 data/
│   └── BooksDataset.csv
├── 📓 notebooks/
│   └── religion_gender_analysis.ipynb
├── 📈 outputs/
│   └── charts/
│       ├── gender_distribution_pie.png
│       ├── religious_tradition_bar.png
│       └── pricing_by_gender.png
```

---

## 🛠️ Tools Used

- **Python** (Pandas, Matplotlib, Seaborn)
- **Jupyter Notebook**
- **Regex** for name parsing
- **Exploratory Data Analysis (EDA)**
- **NLP (LDA topic modeling)** for content clustering


## 🚀 How to Run the Project
 🚀 Getting Started with the Gender & Religion Publishing Project

This section will guide you through opening, running, and exploring the project via GitHub.

---

## 📁 Clone the Repository

First, clone the repository to your local machine:

```bash
git clone https://github.com/Pathogenic-cmd/religion-gender-analysis.git
cd religion-gender-analysis
```
📦 Set Up Your Environment

## Create a virtual environment
```
python -m venv venv
```

Activate the environment
## Windows
```
venv\\Scripts\\activate
```
## Mac/Linux
```
source venv/bin/activate
```

## Install the required packages
```
pip install -r requirements.txt
```
## 🧠 Open the Jupyter Notebook

```
jupyter notebook
```
```
notebooks/v1.0.ipynb
```
## 📊 View as Web App
```
voila v1.0.ipynb
```
## Explore the Data
Inside the notebook, you can:

View gender distribution

Analyze temporal trends

Compare religious traditions

Visualize pricing disparities

Use LDA for topic modeling



---

## 📌 Future Work

- Incorporate external name-to-gender APIs for better accuracy.
- Track publisher name frequency to validate "indie" classification.
- Compare with mainstream retail data (e.g., Amazon/Goodreads).
- Improve topic modeling by fine-tuning number of topics and preprocessing techniques.

---

## 🙋 Acknowledgements

Special thanks to the research direction on gender and religion, and to the Kaggele team who help make Books publishing data publicly accessible.
