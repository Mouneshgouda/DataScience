# Tools and Applications of Data Science

## 1. Introducing Neo4j for Dealing with Graph Databases

Graph databases are used to store and manage data in the form of graphs, where the focus is on relationships between data rather than tables.

Neo4j is a popular graph database management system used for handling highly connected data.

In a graph database:

- Nodes represent entities such as people, objects, or concepts.  
- Relationships represent connections between nodes.  
- Properties store additional information about nodes and relationships.  

Neo4j allows efficient traversal of relationships and is suitable for applications where connections between data are important.

---

## 2. Graph Query Language: Cypher

Cypher is the query language used in Neo4j to interact with graph databases.

It is a declarative query language, meaning the user specifies what results are needed rather than how to compute them.

### Basic Operations

Create a node:
```cypher
CREATE (n:Person {name: 'Alice', age: 25})

MATCH (a:Person {name: 'Alice'}), (b:Person {name: 'Bob'})
CREATE (a)-[:FRIENDS_WITH]->(b)

#retrive
MATCH (n:Person)
RETURN n

#pattern Matching

MATCH (a)-[:FRIENDS_WITH]->(b)
RETURN a, b

```

## 3. Applications of Graph Databases

Graph databases are widely used in scenarios where relationships between data are important.

### Common Applications

Social Networks  
Represent users and their connections such as friendships and followers.  

Recommendation Systems  
Provide suggestions based on user behavior and relationships.  

Fraud Detection  
Detect unusual patterns in transactions and relationships.  

Knowledge Graphs  
Store and manage structured knowledge and relationships.  

Network Analysis  
Analyze connectivity, influence, and centrality in networks.  

---

## 4. Text Mining and Analytics

Text mining involves extracting useful information from textual data using computational techniques.

### Python Libraries for Text Mining

Natural Language Toolkit (NLTK)  

NLTK is a Python library used for natural language processing and text analytics.

### Key Functionalities

Tokenization: Splitting text into words or sentences.  
Stopword Removal: Removing common words like "the", "is".  
Stemming: Reducing words to root form.  
Lemmatization: Converting words to meaningful base form.  
POS Tagging: Identifying parts of speech.  

Example
```python
import nltk
from nltk.tokenize import word_tokenize

text = "Data Science is powerful"
tokens = word_tokenize(text)
print(tokens)

```

### SQLite for Handling Text Data

SQLite is a lightweight, embedded database used to store structured data locally.

It is useful for storing processed text, metadata, and intermediate results in text mining and analytics tasks.

### Example

```python
import sqlite3

conn = sqlite3.connect('data.db')
cursor = conn.cursor()

cursor.execute('CREATE TABLE posts (id INTEGER, content TEXT)')
cursor.execute('INSERT INTO posts VALUES (1, "Sample text data")')

conn.commit()
conn.close()
```

## 5. Case Study: Classifying Reddit Posts

### Objective
The goal of this case study is to classify Reddit posts into different categories based on their textual content.

### Steps Involved

1. **Data Collection**  
   - Collect Reddit posts using APIs or publicly available datasets.

2. **Data Preprocessing**  
   - Convert text to lowercase.  
   - Remove punctuation and stopwords.  
   - Perform tokenization to split text into words or sentences.

3. **Feature Extraction**  
   - Convert text into numerical representations suitable for machine learning:  
     - Bag of Words  
     - TF-IDF (Term Frequency - Inverse Document Frequency)

4. **Model Building**  
   - Apply classification algorithms to categorize posts:  
     - Naive Bayes  
     - Logistic Regression  
     - Support Vector Machines (SVM)

5. **Model Evaluation**  
   - Assess the performance of the classification model using:  
     - Accuracy  
     - Precision  
     - Recall  
     - F1-score

6. **Data Storage**  
   - Store processed data and classification results using SQLite for easy retrieval and analysis.
