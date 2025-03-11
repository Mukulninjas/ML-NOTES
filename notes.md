# Machine Learning Class Notes

## Types of Data

### 1. Numerical Data 📊🔢📈

Numerical data consists of values that have a meaningful numerical representation.

- **Example:** Age, Gas in a tank, Temperature

### 2. Categorical Data 🎭📋📌

Categorical data represents qualitative attributes that do not have inherent mathematical meaning.

- **Example:** Gender (Male, Female, Other), Colors (Red, Blue, Green)

### 3. Ordinal Data 🔢📊📏

Ordinal data is a mix of numerical and categorical data where the order of values matters, but the differences between values may not be uniform.

- **Example:** Ratings (Poor, Average, Good, Excellent), Education Level (High School, Bachelor's, Master's, PhD)

## Measures of Central Tendency

### 1. Mean (Average) ➗📉📊

The mean is the sum of all values divided by the number of values.

**Formula:** \(\text{Mean} = \frac{\sum X_i}{n}\)

**Example:**

- If we have the numbers \(1, 2, 3, 4, 5\), the mean is: \(\frac{1+2+3+4+5}{5} = 3\)
- The mean household income in the US is \$72,641, but the median is only \$51,939 because the mean is skewed by a handful of billionaires. 💰📉📊

### 2. Median 📏🔢📊

The median is the middle value in an ordered data set. If there is an even number of values, it is the average of the two middle values.

**Example:**

- Data: \(0,0,0,0,1,2,2,2,3\)
  - Sorted: \(0,0,0,0,1,2,2,2,3\)
  - Median = **1** (middle value)
- The median is often a better representation of a "typical" case when the data is skewed. 📉📊📏

### 3. Mode 🔄📊🔢

The mode is the most frequently occurring value in a dataset.

**Example:**

- Data: \(1, 2, 2, 3, 3, 3, 4, 5\)
  - Mode = **3** (as it appears most frequently) 🏆🔢📊

## Python Code Examples

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy import stats

# Generate a dataset with 10,000 random values
incomes = np.random.normal(27000, 15000, 10000)

# Calculate mean
mean_income = np.mean(incomes)
print("Mean Income:", mean_income)

# Plot histogram of incomes
plt.hist(incomes, 50)
plt.title("Income Distribution")
plt.xlabel("Income")
plt.ylabel("Frequency")
plt.show()

# Calculate median
median_income = np.median(incomes)
print("Median Income:", median_income)

# Generate random ages
ages = np.random.randint(18, high=90, size=500)

# Calculate mode of ages
mode_age = stats.mode(ages)
print("Mode Age:", mode_age.mode[0])
```

### Explanation of Code: 🖥️📊💡

1. `np.random.normal(27000, 15000, 10000)`: Generates 10,000 income samples with a normal distribution (mean=27,000, std=15,000).
2. `np.mean(incomes)`: Computes the mean of the dataset.
3. `plt.hist(incomes, 50)`: Plots a histogram to visualize income distribution.
4. `np.median(incomes)`: Finds the median income.
5. `np.random.randint(18, high=90, size=500)`: Generates an array of 500 random ages between 18 and 90.
6. `stats.mode(ages)`: Finds the most frequently occurring age. 📉📊📌

## Homework Questions 📚📝🤔

1. What is the difference between numerical, categorical, and ordinal data? Give an example for each.
2. Why is the median often a better representation of data than the mean in a skewed distribution?
3. Compute the mean, median, and mode for the following dataset manually: \(4, 7, 2, 9, 3, 7, 7, 8, 10, 2\).
4. Write a Python function to calculate the mean, median, and mode of a given list.
5. Generate a dataset of 1,000 values with a normal distribution in Python and plot its histogram. What do you observe?
6. How does outlier data affect the mean, median, and mode? 🎯📉📊

---

These notes should help you understand the basics of data types and measures of central tendency. Make sure to complete the homework questions to solidify your understanding! 🚀📖✅