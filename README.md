# Project: Analysis and Visualization of Adult Census Data

---

## About the Data 
- This data was extracted from the 1994 Census Bureau database by Ronny Kohavi and Barry Becker (Data Mining and Visualization, Silicon Graphics). A set of reasonably clean records was extracted using the following conditions: ((AAGE>16) && (AGI>100) && (AFNLWGT>1) && (HRSWK>0)). The prediction task is to determine whether a person makes over $50,000 a year.
- Description of fnlwgt (final weight)
  - The weights on the Current Population Survey (CPS) files are controlled to independent estimates of the civilian noninstitutional population of the US. These are prepared monthly for us by the Population Division here at the Census Bureau. We use 3 sets of controls. These are:
- A single-cell estimate of the population of 16+ for each state.
- Controls for Hispanic origin by age and sex.
- Controls by race, age, and sex.

We use all three sets of controls in our weighting program and "rake" through them six times so that by the end we come back to all the controls we used. The term estimate refers to population totals derived from CPS by creating "weighted tallies" of any specified socioeconomic characteristics of the population. People with similar demographic characteristics should have similar weights. There is one important caveat to remember about this statement. That is since the CPS sample is actually a collection of 51 state samples, each with its own probability of selection, the statement only applies within the state.


----
### **Problem Description**

- Use basic visualization techniques to gain an initial understanding of the dataset. Specifically, you are required to visualize the relationship between each attribute and the class label. For a continuous attribute, you might need to discretize it first using a simple strategy such as equi-width. Please experiment with at least three different bin widths if you decide to discretize a continuous attribute. Observe these basic visualizations and summarize your main insights. You are strongly recommended to use Tableau for this task.

- Handling missing values: suggest and implement at least two strategies to handle the missing values for categorical and numeric attributes, respectively.  These strategies should be based on your observations made in the previous step.

- Implement a Naïve Bayesian Classifier for this dataset. This dataset contains continuous attributes. Take the following two different approaches to handle a continuous attribute:

  - (1) using the equal-width binning method to transform this attribute into a categorical attribute before building the classifier. Select a “proper” width based on your observations made in step (i); 
  - (2) assume this attribute follows a Gaussian distribution.
    - Implement the k-fold cross-validation strategy and evaluate your classifier by setting k=10.  Also evaluate the impact of different strategies implemented in step (ii) for missing values and the two approaches for handling continuous attributes in step (iii).
