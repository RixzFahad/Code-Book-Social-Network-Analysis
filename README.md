# 🌐 Social Network Recommendation System

> A Python-based mini social network engine that suggests friends & pages using real recommendation logic.

---

## 🚀 What This Project Does

| Module | What It Does |
|---|---|
| 👥 **People You May Know** | Recommends friends via mutual connections |
| 📄 **Pages You Might Like** | Suggests pages based on shared interests |
| 🧹 **Data Cleaning Pipeline** | Cleans noisy JSON before analysis |

---

## 🧠 How Each Feature Works

### 👥 Friend Recommendation
```
User → Friends → Friends-of-Friends → Count Mutuals → Sort → Recommend
```
- Builds a user-friends dictionary from JSON
- Looks up friends-of-friends for the target user
- Scores by **mutual friend count**, excludes existing friends
- Output: `Amit can be friends with Rahul`

---

### 📄 Page Recommendation
```
User Likes → Compare with Others → Set Intersection → Score → Recommend
```
- Compares target user's liked pages with all others
- Uses **set intersection** to find shared interests
- Surfaces pages liked by similar users but not yet by the target
- Output: `User may also like: Python Developers, AI & ML Community`

---

### 🧹 Data Cleaning
- ❌ Remove users with missing names
- ❌ Remove duplicate friend IDs
- ❌ Remove inactive users (no friends & no liked pages)
- ❌ Remove duplicate pages by ID
- ✅ Save cleaned output to `Cleaned_data2.json`

---

## 🗂️ Project Structure

```
📁 project-folder/
├── 📄 New.json
├── 📄 data2.json
├── 📄 Cleaned_data2.json
├── 🐍 friend_recommendation.py
├── 🐍 page_recommendation.py
├── 🐍 data_cleaning.py
└── 📝 README.md
```

---

## 📦 Input Format

```json
{
  "users": [
    { "id": 1, "name": "Amit", "friends": [2, 3], "liked_pages": [101, 102] }
  ],
  "pages": [
    { "id": 101, "name": "Python Developers" }
  ]
}
```

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![JSON](https://img.shields.io/badge/Data-JSON-yellow?logo=json&logoColor=white)
![No Libraries](https://img.shields.io/badge/Libraries-Built--in%20Only-green)

**Concepts used:** `dict` · `set` · `list` · `lambda sort` · `JSON I/O` · `collaborative filtering`

---

## 💡 Real-World Parallel

| This Project | Real World |
|---|---|
| Mutual friend count | LinkedIn "People You May Know" |
| Shared page interests | Facebook page suggestions |
| Data cleaning pipeline | ML preprocessing workflows |

---




> *"Built a Python recommendation system using mutual friend analysis and collaborative filtering on JSON data, with a data cleaning pipeline — mimicking how real social platforms suggest connections and content."*

---

*Built with 🐍 Python · Inspired by real social media recommendation engines*
