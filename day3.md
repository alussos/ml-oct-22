# Objectives
- Deeper dive into `pandas`
- More practice with ML algos

# Agenda
0. [30] Practice problem on linear regression
1. [45] Python warmup problems
2. [30] More `pandas` mechanics with sales dataset and practice
3. [30] Re-shaping data with `pandas`
4. [30] Basic data munging on the rock.csv data set
5. [45] Working with textual data & twitter data
6. [30] Working with timestamps
7. [30] Working with app pod data
8. [60] Lab: Crunchbase data analysis & ML

# Datasets
- [Sales funnel data](https://s3.amazonaws.com/python-level-2/sales-funnel.csv)
- [Rock song data](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/rock.csv)
- [Movie history for user](https://s3.amazonaws.com/simple-fractal-workshops/movie_history_for_user.csv)
- [Doctor visit data](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/health_data.csv)
- [Twitter data](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/clean_twitter_data.csv)
- [Citibike truncated data](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/datasets/citibike-data-truncated.csv
)
- [Crunchbase data](https://raw.githubusercontent.com/suneel0101/lesson-plan/master/crunchbase_monthly_export.csv)
- [Pod app data](https://s3-us-west-2.amazonaws.com/ga-dat-2015-suneel/app_data.csv)

# Linear regression practice
Work with a partner and build a linear regression on the doctor's visit data. Try to tune it. Make visual plots wherever helpful. Discuss results and we'll share as a class.

# Python warm up problems
1. Create a list of 10+ restaurants and assign to a global variable
2. Write a function that returns a random restaurant when called.
3. Write another function that returns a random restaurant but never repeats the same two.

# More `pandas` mechanics
## Concepts
- Boolean masks
- Adding new columns

1. How many rows have a price greater than $8,000?
2. How many rows are pending AND have a price greater than $8,000?
3. How many rows are pending OR have a price greater than $8,000?
4. Create an amount column that's equal to price * quantity. What's the total amount won?
5. What's the total amount won within the CPU product category?

# Reshaping data with `pandas`

## Pivot tables
Let's do one together and then separate and come up with pivot tables you think would be useful.

### Concepts
- Let's pivot using one index.
- Let's pivot on multiple indexes
- Let's reverse those indexes
- Let's specify which values we care about
- Let's specify which columns we want broken down
- Let's specify how we want the values to be aggregated (aggfunc)
- Let's fill N/A values
- Let's get subtotals 

## Cross tab
Let's look through `crosstab` docs together.

### Exercise
Compute a cross-tabulation that shows how many accounts are in each status for each product broken down by manager and rep.

# Basic data munging
Read in the rock data set.

## Exercise
- How many songs were released in 1981
- What is the earliest release year in the data 

- Let's clean up the data!
- Let's talk about lambda functions

# Working with textual data
- Let's use our sales data set again.
- Let's go to the pandas docs section on working with text data.

## Practice together 
- Let's use .str... to select the rows that contain either pending or won.
- Let's lowercase the Rep column with .str.lower

### Exercises
- Replace the product category CPU with monkey
- Upper case the product category column.
- Create a new column called "contains_monkey" using str.contains based on the product category value.

### Exercise
Let's read in the twitter data set together.

1. Brainstorm with partner what types of operations/munging you want to do.
2. Let's hack on it.

# Working with timestamp data
- Let's delete the Unnamed: 0 column
- Let's google pandas timestamps
- Let's convert necessary columns into timestamps.
- Let's compute the duration and add a column with the result.
- Let's create a column called "hour_periods".

## Exercise
- What is the average trip time? What is the minimum and maximum trip time? What is the standard deviation?
- What's average trip time broken down by station? Sort from longest to shortest, including only the top 15.
- Create a column called daily periods that assigns the starttime to a day-period.
- Create a column called month that contains the month of the starttime

# Working with app pod data
- Read in the app data set.
- What can we do with it?
- What kinds of analysis?
- Partner up on this one.

# Lab: Crunchbase data
- Read in the crunchbase data set
- What can we do with it?
- Tackle this one solo...

