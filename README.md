<<<<<<< HEAD
# Social Network Recommendation System

## Project Overview

This project is a mini social network analysis and recommendation system built with Python and JSON data. It focuses on three core features:

1. **People You May Know** — recommends users based on mutual friends.
2. **Pages You Might Like** — recommends pages based on shared interests.
3. **Data Cleaning Pipeline** — cleans raw user and page data before analysis.

The project simulates how social media platforms suggest friends and content using simple recommendation logic.

---

## Objectives

* Build a friend recommendation system using mutual connections.
* Build a page recommendation system using common interests.
* Clean and prepare noisy JSON data for reliable output.
* Practice Python data structures like dictionaries, sets, lists, loops, and sorting.
* Understand the basics of recommendation systems and graph-based logic.

---

## Features

### 1. People You May Know

This module recommends new friends to a selected user.

**Logic used:**

* Read all users and their friend lists.
* Store each user's friends in a dictionary.
* For the target user, look at each direct friend's friend list.
* Count mutual connections.
* Exclude the user themself and already existing friends.
* Sort recommendations by highest mutual friend count.

**Concepts used:**

* Graph thinking
* Mutual friend analysis
* Dictionary and set operations
* Sorting by score

**Example output:**

```text
Amit can be friends with Rahul
Amit can be friends with Sara
```

---

### 2. Pages You Might Like

This module recommends pages to a user based on page interests shared with other users.

**Logic used:**

* Read all users and their liked pages.
* Compare the target user's liked pages with other users.
* Find shared interests using set intersection.
* If another user likes extra pages the target user has not liked yet, add those pages as suggestions.
* Score page suggestions based on how many shared interests exist.
* Sort page recommendations by relevance.

**Concepts used:**

* Interest-based recommendation
* Collaborative filtering idea
* Set intersection
* Dictionary scoring
* Ranking logic

**Example output:**

```text
User may also like:
- Python Developers
- AI & ML Community
```

---

### 3. Data Cleaning

This module cleans the raw JSON dataset before applying recommendation logic.

**Cleaning steps used:**

* Remove users with missing names.
* Remove duplicate friend IDs.
* Remove inactive users with no friends and no liked pages.
* Remove duplicate pages based on page ID.

**Why this matters:**
Clean data improves accuracy and prevents errors during recommendation and analysis.

**Concepts used:**

* Data preprocessing
* Duplicate removal
* Filtering invalid records
* Dictionary-based deduplication

---

## Technologies Used

* **Python**
* **JSON**
* Built-in Python libraries:

  * `json`

---

## Python Concepts Used

* Functions
* Lists and list comprehensions
* Dictionaries
* Sets
* Loops
* Conditional statements
* Sorting with `lambda`
* File handling
* JSON read/write

---

## Project Structure

```text
project-folder/
│── New.json
│── data2.json
│── Cleaned_data2.json
│── friend_recommendation.py
│── page_recommendation.py
│── data_cleaning.py
│── README.md
```

---

## Input Data Format

The project uses JSON data in this structure:

```json
{
  "users": [
    {
      "id": 1,
      "name": "Amit",
      "friends": [2, 3],
      "liked_pages": [101, 102]
    }
  ],
  "pages": [
    {
      "id": 101,
      "name": "Python Developers"
    }
  ]
}
```

---

## How Each Module Works

### Friend Recommendation Workflow

1. Load JSON data.
2. Build a user-friends dictionary.
3. Select target user.
4. Find friends of friends.
5. Count mutual connections.
6. Sort and display recommended users.

### Page Recommendation Workflow

1. Load JSON data.
2. Build a user-pages dictionary.
3. Compare the target user with other users.
4. Find common liked pages.
5. Recommend extra pages liked by similar users.
6. Sort and display recommended pages.

### Data Cleaning Workflow

1. Load raw JSON.
2. Remove invalid or incomplete user records.
3. Remove duplicates in friends and pages.
4. Remove inactive users.
5. Save cleaned JSON output.

---

## Real-World Relevance

This project is inspired by recommendation logic used in social media platforms.

### Friend recommendation resembles:

* Mutual connections in social networks
* Graph-based relationship analysis

### Page recommendation resembles:

* Interest-based recommendation systems
* Beginner-level collaborative filtering

### Data cleaning resembles:

* Real-world preprocessing in analytics and machine learning workflows

---

## Key Learnings From This Project

* How recommendation systems work at a basic level.
* How to use Python for social network analysis.
* How data cleaning affects output quality.
* How dictionaries and sets improve performance and logic.
* How to structure JSON data for analysis projects.

---

## Strengths of the Project

* Simple and practical
* Easy to explain in interviews
* Shows problem-solving ability
* Combines logic building with real-world use case
* Good beginner project for Python and data analysis portfolio

---

## Limitations

* Recommendations are based only on mutual friends and shared pages.
* No weighting for page popularity or user activity.
* No UI or database integration yet.
* Works on static JSON data.

---

## Future Improvements

* Add score display for mutual friends.
* Recommend pages by category.
* Add user activity tracking.
* Build a dashboard for visualization.
* Connect the project with SQL or MongoDB.
* Create a web app using Flask or Streamlit.
* Add network graphs using `networkx` or `matplotlib`.

---

## Sample Resume / Portfolio Description

**Social Network Recommendation System**
Built a Python-based recommendation system using JSON data to suggest new friends based on mutual connections and recommend pages based on shared interests. Implemented a data cleaning pipeline to remove incomplete and duplicate records, improving recommendation quality and project reliability.

---

## Interview Explanation

If asked to explain this project, you can say:

> I built a mini social network recommendation system in Python. The first part suggests friends using mutual friend logic, similar to how social media platforms recommend connections. The second part recommends pages based on shared interests between users. I also added a data cleaning module to remove invalid users, duplicate friends, inactive records, and duplicate pages. This project helped me understand recommendation logic, graph-style relationships, JSON handling, and data preprocessing.

---

## Conclusion

This project combines **recommendation logic**, **data cleaning**, and **social network analysis** in a simple but strong Python project. It is useful for showcasing Python fundamentals, data handling, and real-world analytical thinking.
=======
# Code-Book-Social-Network-Analysis
>>>>>>> d0d1c711f7da9d5a556ed3c89264fde631b54c5b
