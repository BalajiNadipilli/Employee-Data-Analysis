# Employee-Data-Analysis
  This repository contains Python code for reading and visualizing employee data stored in an Excel file (data.xlsx). The project makes use of various data manipulation and visualization techniques with libraries such as Pandas, Seaborn, and Matplotlib to analyze employee data, including salary, experience, and other details.

**Project Structure:**
data.xlsx: The Excel file containing employee details like Name, Domain, Age, Location, Salary, and Experience.
employee_data_analysis.ipynb: Jupyter Notebook containing code for data analysis and visualization of employee data.

**Features:**
  1.Data Extraction: The dataset is loaded from an Excel file (data.xlsx) using pandas.read_excel().
  2.Data Inspection: The notebook displays various statistics about the dataset, including its shape and columns.
  3.Data Visualization: The project generates visualizations for salary and experience data using Seaborn and Matplotlib:
      -Distribution of Salaries: Visualizes the distribution of employee salaries using displot and distplot.
      -Histogram: Visualizes the distribution of employee salaries with a histogram using plt.hist().
      -Linear Regression Plot: Visualizes the relationship between experience and salary using sns.lmplot().
  4.Figure Customization: Adjusts the figure size of the plots to customize how they are displayed.

**Data Analysis**
1.Reading Data: The Excel file data.xlsx is read into a pandas DataFrame.
    emp = pd.read_excel(r'C:\\path\\to\\data.xlsx')
2.Exploring Data: The shape and columns of the dataset are examined.
    emp.shape
    emp.columns
3.Data Selection: The columns SALARY and EXP are selected for analysis.
    emp[['SALARY', 'EXP']]
4.Visualization:
    Distribution of Salaries: The distribution of salaries is plotted using Seaborn's displot() and distplot().
          vis1 = sns.displot(emp['SALARY'])
          vis2 = sns.distplot(emp['SALARY'])
    Histogram of Salaries: A histogram of salaries is plotted using matplotlib.pyplot.
          vis3 = plt.hist(emp['SALARY'])
    Linear Regression Plot: A linear regression plot is used to visualize the relationship between experience (EXP) and salary (SALARY).
          vis5 = sns.lmplot(data=emp, x='EXP', y='SALARY')
          vis5 = sns.lmplot(data=emp, x='EXP', y='SALARY', fit_reg=False)
          vis5 = sns.lmplot(data=emp, x='EXP', y='SALARY', fit_reg=True)
**Outputs**
-Salary Distribution: The displot and distplot functions plot the salary distribution for all employees.
-Histogram: A histogram showing the frequency of different salary ranges across employees.
-Linear Regression Plot: A regression plot to visualize the correlation between employee experience and salary.

Example Output

sns.displot(emp['SALARY'])
This will display the distribution of salaries of all employees.

sns.lmplot(data=emp, x='EXP', y='SALARY')
This will display a linear regression plot between experience and salary, helping to visualize the trend.
