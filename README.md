# A-Visual-History-of-Nobel-Prize-Winner
## Project Description
The Nobel Prize is perhaps the world's most well known scientific award. Every year it is given to scientists and scholars in chemistry, literature, physics, medicine, economics, and peace. The first Nobel Prize was handed out in 1901, and at that time the prize was Eurocentric and male-focused.

In this project, we'll figure out the characteristics prize winners have. Does male still get most of the prize? Which country gets it most often? And has anybody gotten it twice? 

The dataset used in this project is from The Nobel Foundation on Kaggle.

## Topics
- Importing and Cleaning data
- Data Manipulation
- Data Visualization

## Dependencies
- `pandas`
- `Seaborn`
- `numpy`

## The Structure of this Notebook is as Follows:
1. Read and load data with `pd.read_csv()`
2. Look at nobel winners from 1901 to 2016 by *sex* and *birth country* with `.value_counts()`.
    - Male and the US dominate.
3. Visualize USA dominance by calculating the proportion of USA born winners per decade.
    - `nobel['decade']=(np.floor(nobel['year']/10)*10).astype(int)`
    - `sns.lineplot()`
4. Visualize the share of female winner over year in different prize categories.
    - Gender imbalance is large with physics, economics and chemistry having the largest imbalance.
    - The first woman won the prize is found out by :`nobel[nobel['sex']=='Female'].nsmallest(1, 'year')`
5. Find out epeat laureates by `filter` method
6. Visualize how the age of laureates change over year.
    - The overall average increases from around 55 to around 65.
    - We also look at age trends within different prize categories.
