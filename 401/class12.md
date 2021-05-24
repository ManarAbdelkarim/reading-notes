# Pandas

![](https://liwaiwai.com/wp-content/uploads/2019/10/python-pandas-install-cover.jpg)

## What is Pandas?
- pandas is a Python package providing fast, flexible, and expressive data structures designed to make working with “relational” or “labeled” data both easy and intuitive. It aims to be the fundamental high-level building block for doing practical, real world data analysis in Python. Additionally, it has the broader goal of becoming the most powerful and flexible open source data analysis / manipulation tool available in any language. It is already well on its way toward this goal.
- Pandas is a game-changer for data science and analytics, particularly if you came to Python because you were searching for something more powerful than Excel and VBA. Pandas uses fast, flexible, and expressive data structures designed to make working with relational or labeled data both easy and intuitive.
- The Pandas library is one of the most preferred tools for data scientists to do data manipulation and analysis, next to matplotlib for data visualization and NumPy, the fundamental library for scientific computing in Python on which Pandas was built.

- The fast, flexible, and expressive Pandas data structures are designed to make real-world data analysis significantly easier, but this might not be immediately the case for those who are just getting started with it. Exactly because there is so much functionality built into this package that the options are overwhelming.

- Pandas handle the vast majority of typical use cases in finance, statistics, social science, and many areas of engineering
- pandas is built on top of NumPy and is intended to integrate well within a scientific computing environment with many other 3rd party libraries.

## The most elementary functions of pandas

* Reading data : `data = pd.read_csv('my_file.csv')`
* Writing data : `data.to_csv('my_new_file.csv', index=None)`
* Checking the data : `data.shape` OR `data.describe()`
* Seeing the data : `data.head(3)` OR `data.loc[8]` OR `data.loc[8, 'column_1']` OR `data.loc[range(4,6)]`
## The basic functions of pandas

* Logical operations :
  * `data[data['column_1']=='french']`
  * `data[(data['column_1']=='french') & (data['year_born']==1990)]`
  * `data[(data['column_1']=='french') & (data['year_born']==1990) & ~(data['city']=='London')]`
  * `data[data['column_1'].isin(['french', 'english'])]`
* Basic plotting

  * `data['column_numerical'].plot()`
  * `data['column_numerical'].hist()`
  * `%matplotlib inline/`
  
* Updating the data
  * `data.loc[8, 'column_1'] = 'english'`
  * `data.loc[data['column_1']=='french', 'column_1'] = 'French'`
### Medium level functions
* Counting occurrences
  * `data['column_1'].value_counts()`
* Operations on full rows, columns, or all data
  * `data['column_1'].map(len)`
  * `data['column_1'].map(len).map(lambda x: x/100).plot()`
  * `data.apply(sum)`
* Correlation and scatter matrices
  * `data.corr()`
  * `data.corr().applymap(lambda x: int(x*100)/100)`
  * `pd.plotting.scatter_matrix(data, figsize=(12,8))`
### Advanced operations in pandas

* The SQL join
  * `data.merge(other_data, on=['column_1', 'column_2', 'column_3'])`
* Grouping
  * `data.groupby('column_1')['column_2'].apply(sum).reset_index()`
* Iterating over rows
  * `dictionary = {}`
  * `for i,row in data.iterrows():`
  * ` dictionary[row['column_1']] = row['column_2']`