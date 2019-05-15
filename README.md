# project-iris
A classic supervised learning project of data science

### Table of contents

* [Iris dataset](#iris-dataset)
* [Exploratory Data Analysis](#exploratory-data-analysis)
* [What is Data Science?](#what-is-data-science)
* [Colleges](#colleges)
* [MOOC's](#moocs)
* [Data Sets ](#data-sets)
* [Bloggers](#bloggers)
* [Podcasts](#podcasts)
* [Books](#books)


## Iris dataset

Iris dataset contains data pertaining to iris flowers in which the features consist of four mesurements: petal length, petal width, sepal length and sepal width. The target variable encodes the species of flowers and there are three possibilities: versicolor, virginica and setosa.

As this is one of the datasets included in scikit-learn, we will import it from the scikit-learn and it will not be included in the project files.


## Exploratory Data Analysis

*This is a specification of the file **Iris_EDA.ipynb**. You will need to check the results in that file.*

We will import the dataset from scikit-learn with the code: from sklearn import datasets
We also need to import the other packages like pandas and matplotlib. You can check this importing things in the very first part of the file **Iris_EDA.ipynb**.

In addition, we set the plot style to 'ggplot' in order to have goodlooking plots. We then load the dataset as a variable named iris. We can find its type is a bunch which is similar to the type dictionary. It contains the key-value pairs. Printing the keys, we can see they are the feature names: 'DESCR', which provides a description of the dataset; the target names; the data, which contains the values features; and the 'target' which is the target data.

As you can see in the file, both the feature and target data are provided as NumPy array. The dot shape attribute of the array feature tells us that there are 150 samples and 4 features. Moreover, note that the target variable is encoded as: Zero for 'setosa'; 1 for 'versicolor'; and 2 for 'virginica'. We can see this by printing 'iris.target_names', in which 'setosa' corresponds to index 0, 'versicolor' to index 1 and 'virginica' to index 2.

In order to perform some initial **Exploratory Data Analysis(EDA)**, we will assign the feature and target data to X and y, respectively. We will then build a DataFrame using the feature data and also passing columns names. Viewing the head of the DataFrame shows us the first five rows.

Then we do a bit of **visual EDA**. We use the pandas function 'scatter_matrix' to visualize our dataset. As you can see in the file, we pass it to our DataFrame, along with our target variable as argument to the parameter c which stand for color ensuring that our datapoints in our figure will be colored by the species. We will also pass a list to 'figsize', which specifies the size of our figure, as well as a marker size and shape. The result is a matrix of figures, which on the diagonal are histograms of the features corresponding to the row and column. The off-diagonal figures are scatter plots of the column feature versus row feature colored by the target variable. From the 'scatter matrix', we can see that the petal width and length are highly correlated and the flowers are clustered according to species.
