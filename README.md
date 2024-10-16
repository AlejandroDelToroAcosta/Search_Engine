# Task 1: Python Search Engine

## University of Las Palmas de Gran Canaria
### School of Computer Engineering
#### Bachelor's Degree in Data Science and Engineering

---

## Description
This project is designed as a search engine that connects to the Project Gutenberg web page and periodically downloads several books from it, saving them in a datalake. This functionality is implemented by the crawler module.

Then the Indexer module reads the datalake books and creates two inverted index structures as two datamarts that will provide the information to the final user. In one hand it creates a json file and in the other hand it creates a connection to MongoDB database.
Finally the runner module has the functionality of asking the user for a word to search in one of the two inverted indexes.

Additionally the project includes a test module that uses benchmark techniques to compare which of the two inverted indexes is more optimal when the user makes the query and when the data form the datalake is indexed.

--- 

## Resources

  This project has been developed entirely using  Pycharm. PyCharm is an integrated development environment (IDE) specifically designed for programming in Python. It is developed by JetBrains and provides a comprehensive set of tools to help Python developers write, debug, test, and maintain their code more efficiently.

  To create one of this datamart structures we have used Mongodb which is a NoSQL database designed for handling large-scale data in a flexible, scalable, and high-performance manner. Unlike traditional relational databases (like MySQL or PostgreSQL), which store data in structured tables with predefined schemas, MongoDB stores data in a document-oriented format, allowing for greater flexibility in data models.

  However the project is based in using the Gutenberg Project web page which is is a digital library that offers free access to a vast collection of public domain eBooks.

  This software uses pytest as a benchmark tool.

---

## Benchmarking Results

![Pytest results](results)

As we see in the picture MongoDB is extremely efficient for querying data (test test_user_query_Mongo), clearly outperforming JSON in the same operation.
However, saving the inverted index in MongoDB (test test_save_inverted_index_Mongo) is much slower compared to any other operation, with a significantly higher average execution time than the JSON version.

JSON is less efficient for both querying and saving overall, but it still outperforms MongoDB when saving the inverted index (test_save_inverted_index_Json).
These results suggest that MongoDB is more suitable for fast queries, but when it comes to saving large amounts of data (like an inverted index), its performance might not be the best compared to handling JSON files.

## Tools

- [MongoDb](https://www.mongodb.com/)
- [Pytest](https://docs.pytest.org/)
- [GutenberProject](https://www.gutenberg.org/)





  
