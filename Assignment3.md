# Assignment 3: Normalization and Standardization in Data Science

## Introduction

- **Normalization** scales numerical data into a specific range, usually between 0 and 1.
- **Standardization** transforms data so that it has a mean of 0 and a standard deviation of 1.

---

## 1. Normalization

**Normalization** is a data preprocessing technique used to scale numerical data into a specific range, usually between 0 and 1.

- It helps bring different features into a common scale.
- It prevents features with larger values from dominating smaller-valued features.
- It is commonly used in Machine Learning algorithms.

### Types of Normalization

There are two commonly used techniques:

#### A. Min-Max Normalization

- It scales the data into a fixed range, usually 0 to 1.
- The minimum value becomes 0, and the maximum value becomes 1.
- Other values are adjusted proportionally.

**Formula:**

$$
X' = \frac{X - X_{\min}}{X_{\max} - X_{\min}}
$$

Where:

| Symbol | Meaning |
| :-: | --- |
| $X$ | Original value |
| $X_{\min}$ | Minimum value |
| $X_{\max}$ | Maximum value |
| $X'$ | Normalized value |

**Example:**

If the minimum value is 10, the maximum value is 50, and the original value is 30:

$$
X' = \frac{30 - 10}{50 - 10} = \frac{20}{40} = 0.5
$$

#### B. Z-Score Normalization

- It transforms data based on its mean and standard deviation.
- The transformed data has a mean of 0 and a standard deviation of 1.
- Values can be positive, negative, or zero.

**Formula:**

$$
Z = \frac{X - \mu}{\sigma}
$$

Where:

| Symbol | Meaning |
| :-: | --- |
| $X$ | Original value |
| $\mu$ | Mean of the dataset |
| $\sigma$ | Standard deviation |

**Example:**

If $X = 70$, mean $\mu = 50$, and standard deviation $\sigma = 10$:

$$
Z = \frac{70 - 50}{10} = \frac{20}{10} = 2
$$

This means the value is 2 standard deviations above the mean.

---

## 2. Standardization

**Standardization** is a data preprocessing technique that transforms data so that it has a mean of 0 and a standard deviation of 1.

- It puts data on a common scale.
- It helps Machine Learning algorithms perform better.
- It does not restrict values to a fixed range like 0 to 1.
- It is useful when data follows a normal distribution.

**Formula:**

$$
X' = \frac{X - \mu}{\sigma}
$$

Where:

| Symbol | Meaning |
| :-: | --- |
| $X$ | Original value |
| $\mu$ | Mean of the dataset |
| $\sigma$ | Standard deviation |
| $X'$ | Standardized value |

**Example:**

If $X = 80$, mean $\mu = 60$, and standard deviation $\sigma = 10$:

$$
X' = \frac{80 - 60}{10} = \frac{20}{10} = 2
$$

The standardized value is 2.

---

## Comparison Table

| #  | Basis                  | Normalization                          | Standardization                                                               |
| :-: | ---------------------- | -------------------------------------- | ----------------------------------------------------------------------------- |
| 1  | **Meaning**            | Scales data into a specific range.     | Transforms data to have mean 0 and standard deviation 1.                      |
| 2  | **Range**              | Usually between 0 and 1.               | No fixed range.                                                               |
| 3  | **Method**             | Commonly uses Min-Max scaling.         | Uses mean and standard deviation.                                             |
| 4  | **Effect of Outliers** | Highly affected by outliers.           | Also affected by outliers, but generally less sensitive than Min-Max scaling. |
| 5  | **Use**                | Useful when data needs a fixed range.  | Useful when algorithms work better with centered data.                        |

---

## Conclusion

> **Z-score normalization and standardization use the same formula.**
> In many Data Science textbooks and libraries, Z-score normalization is simply another name for standardization.
