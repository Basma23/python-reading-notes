# Data Science in a nutshell

**Data Science**

It is a set of disciplines and practices that handle data in a scientific manner. The foundations of data science are mostly Mathematics and Statistics, sometimes Software Engineering would play a role as well.
Usually, it includes but not limited to these steps:

1- Data acquisition: The data could be in the form of .CSV files. Excel file (.XLSX) is a typical form, or it could be available by API calls, or someone has done the dirty work already and they are all in DWH(Data WareHouse) or Data Lake.
![Data acquisition](https://miro.medium.com/max/755/0*zaoqsiRK_7Mxxidb.png)

2- Data cleaning & wrangling: Data could be in the nested structure for storage saving purpose (e.g. Bigquery and NoSQL), could be normalized (like general databases). The data need to be flattened before usage.
Or, the application generating data went haywire and polluted the data recently. That would require sanity checking and data cleaning as well.
This is usually the most time-consuming and painful part for Data Scientists, Analysts and Data Engineers.

3- Data Engineering: Simply put, the point of Data Engineering is building a stable and reliable architecture for data storage and consumption. It is a extremely vital part as all kinds of data science tricks depends on it.
If there is no good data to use, NONE of the data science gimmicks could work.
Well engineered data should be clean, fast and cheap (in terms of computational resources, hence money as well) for robust consumption right away.

4- Utilization of data: From traditional consumption like building an application, doing ad hoc analysis, dashboarding and the recent fancy thing such as Machine Learning, this is the step people care so much.

**Big Data**

![Big Data](https://miro.medium.com/max/875/1*hvVfvzIvrTw0COyaBCFnwQ.png)

As for “Big Data”, there are other formats of data as well: images, videos, voice recordings, etc. Good examples would be Google Photos for images data, Netflix for videos, voices recordings (songs) in Spotify.
And of course, “Big Data” would be BIG. Big enough to make it impossible for a regular laptop to process. Hence, solutions like Google Bigquery, Hadoop and MapReduce are introduced.

**“Analytics” & “Business Intelligence”**

“Analytics”:
Analytics is the discovery, interpretation, and communication of meaningful patterns in data; and the process of applying those patterns towards effective decision making.

“Business Intelligence”:
Business intelligence (BI) comprises the strategies and technologies used by enterprises for the data analysis of business information. BI technologies provide historical, current and predictive views of business operations.

**“Machine Learning”**

**Machine Learning** is like human learning new knowledge. Human picks up new knowledge through experience, machines pick up new knowledge with data.
Machine Learning aims at building algorithms, and algorithms can be divided into 2 categories: Supervised Learning and Unsupervised Learning.

An iconic example of a Supervised Learning algorithm would be Linear Regression. And Logistic Regression is widely used as well. But most of the people are usually introduced with Decision Trees first.

**“Deep Learning”**

**Deep Learning** has a lot of connections with Machine Learning, but they are not exactly the same thing in practice.
Machine Learning focus on tabular data, and Deep Learning handles untraditional data such as images, text, voice recordings. Deep Learning algorithms work on computer vision, speech recognition, NLP (Natural Language Processing) and so on.

**“Reinforcement Learning”**

Reinforcement Learning focuses on maximizing rewards by taking action(s) in a given environment.



# What is Jupyter Lab

**JupyterLab** is a next-generation web-based user interface for Project Jupyter.

**JupyterLab** enables us to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner. 

# Data Analysis with Python

**NumPy** is a commonly used Python data analysis package. By using NumPy, we can speed up our workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. This longevity means that almost every data analysis or machine learning package for Python leverages NumPy in some way.

**SSV** (semicolon separated values) format — each record is separated by a semicolon (;), and rows are separated by a new line. 

**Lists Of Lists for CSV Data**

```
import csv
with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))
print(wines[:3])
[['fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', 'quality'], ['7.4', '0.7', '0', '1.9', '0.076', '11', '34', '0.9978', '3.51', '0.56', '9.4', '5'], ['7.8', '0.88', '0', '2.6', '0.098', '25', '67', '0.9968', '3.2', '0.68', '9.8', '5']]
```
The data has been read into a list of lists. Each inner list is a row from the SSV file. Each item in the entire list of lists is represented as a string, which will make it harder to do computations.

**Numpy 2-Dimensional Arrays**

With NumPy, we work with multidimensional arrays. **A 2-dimensional array** is also known as a matrix. In fact, it’s just a different way of thinking about a list of lists. A matrix has rows and columns. By specifying a row number and a column number, we’re able to extract an element from a matrix.

**Creating A NumPy Array**

We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. Because we want all of the elements in the array to be float elements for easy computation, we’ll leave off the header row, which contains strings. One of the limitations of NumPy is that all the elements in an array have to be of the same type, so if we include the header row, all the elements in the array will be read in as strings. 

**Alternative NumPy Array Creation Methods** 
There are a variety of methods that you can use to create NumPy arrays. To start with, we can create an array where every element is zero.
```
import numpy as np
empty_array = np.zeros((3,4)) empty_array
```
**Using NumPy To Read In Files**

It’s possible to use NumPy to directly read CSV or other files into arrays. We can do this using the ```numpy.genfromtxt``` function. 

**Indexing NumPy Arrays**

We can use array indexing to select individual elements, groups of elements, or entire rows and columns. One important thing to keep in mind is that just like Python lists, NumPy is zero-indexed, meaning that the index of the first row is 0, and the index of the first column is 0. If we want to work with the fourth row, we’d use index 3, if we want to work with the second row, we’d use index 1, and so on.

**Slicing NumPy Arrays**

If we want to select the first three items from the fourth column, we can do it using a colon (:). A colon indicates that we want to select all the elements from the starting index up to but not including the ending index. 

**Assigning Values To NumPy Arrays**

We can also use indexing to assign values to certain elements in arrays. 

**Dimensional NumPy Arrays**

**N-Dimensional NumPy Arrays**

**NumPy Data Types**

**Converting Data Types**
We can use the ```numpy.ndarray.astype``` method to convert an array to a different type. The method will actually copy the array, and return a new array with the specified data type. 

**NumPy Array Operations**

NumPy makes it simple to perform mathematical operations on arrays. This is one of the primary advantages of NumPy, and makes it quite easy to do computations.

**Single Array Math**

If we do any of the basic mathematical operations (```/```, ```*```, ```-```, ```+```, ```^```) with an array and a value, it will apply the operation to each of the elements in the array.

**Multiple Array Math**

It’s also possible to do mathematical operations between arrays. This will apply the operation to pairs of elements. 

**Broadcasting**

Unless the arrays that you’re operating on are the exact same size, it’s not possible to do elementwise operations. In cases like this, NumPy performs broadcasting to try to match up elements. 

**NumPy Array Methods**

In addition to the common mathematical operations, NumPy also has several methods that you can use for more complex calculations on arrays. An example of this is the numpy.ndarray.sum method.

**NumPy Array Comparisons**

NumPy makes it possible to test to see if rows match certain values using mathematical comparison operations like ```<```, ```>```, ```>=```, ```<=```, and ```==```.

**Subsetting**

One of the powerful things we can do with a Boolean array and a NumPy array is select only certain rows or columns in the NumPy array.

**Reshaping NumPy Arrays**

We can change the shape of arrays while still preserving all of their elements. This often can make it easier to access array elements. The simplest reshaping is to flip the axes, so rows become columns, and vice versa.

**Combining NumPy Arrays**

With NumPy, it’s very common to combine multiple arrays into a single unified array. We can use numpy.vstack to vertically stack multiple arrays.


