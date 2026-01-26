
# CYT180 – Lab 2: Pandas DataFrames

**Weight:** 3%  
**Work Type:** Individual  
**Submission Format:** Single PDF file containing screenshots from the Jupyter Notebook

---

## Lab Objectives

This lab introduces **Pandas DataFrames**, a foundational tool for data analytics used extensively in cybersecurity for analyzing logs, alerts, and structured datasets. The instructor will demonstrate the use of Pandas during the in-person lab session.

By the end of this lab, you should be able to:

* Load CSV data into a Pandas DataFrame
* Inspect and explore tabular data
* Filter data using conditions
* Perform simple analytical queries
* Apply insights to cybersecurity-relevant datasets
* Clearly document and explain analysis steps

---

## Topics Covered

- Pandas DataFrames basics: load, inspect, and explore data  
- Filtering data using conditions  
- Aggregating and counting events  
- Visualizing anomalies and alert levels  

---

## Environment Setup

You will work in **Jupyter Notebook** using a **local Anaconda installation** (completed in Week 1).<br>
Verify that the following libraries are available:

* `pandas`
* `matplotlib`

If any library is missing, please install it using:

```python
!pip install pandas matplotlib
```
## Dataset

Use the provided file **`cities.csv`**.

It includes the following columns:  
  - `City` → city name
  - `State` → state code
  - `failed_logins` → number of failed login attempts per city  
  - `login_attempts` → total login attempts per city  
  - `alerts` → Low / Medium / High alert level  
  - `last_incident` → timestamp of the last security incident
    
---

## Task 1: Load and Inspect the Dataset
You are provided with the file **`cities.csv`**.
1. Create a new Jupyter Notebook.
2. Import the Pandas library.
3. Read the CSV file into a Pandas DataFrame.
4. Display basic DataFrame information using the `.info()` method. Add comments in your code explaining what this method does and what information it provides.
5. Use the describe() method to explore the dataset. Understand what do the summary statistics represent. Explain in a markdown cell atleast 5 kind of information describe() provides.

---

## Task 2: Explore the DataFrame
1. Display the first five rows of the DataFrame.
2. Display the last five rows of the DataFrame.
3. Identify how many rows and columns exist in the dataset.

---
## Task 3: Data Filtering (Identify High-Risk Cities)
**Goal:** Find cities with potential security issues by analyzing failed login activity.
1. **Select cities with many failed logins**  
   - Identify cities where the `failed_logins` column is **greater than 50**.  
   - Hint: In Pandas, “filtering” means keeping only rows that meet a condition.  
   - After this step, your DataFrame should only show cities that might need attention based on **high number of failed logins**.
2. Sort the filtered cities by `failed_logins` in **descending order**.
3. Count how many high-risk cities there are.

### Reflection questions based on Task 3
- Why is it useful to sort and count high-risk cities?  
- How could this help a cybersecurity analyst prioritize investigations?
  
---

## Task 4: Simple Analysis of Cities by State
**Goal:** Learn how to aggregate and count data using Pandas.
1. Count how many cities exist in each state.
2. Identify the state with the highest number of cities. Use the `idxmax()` method.
3. Display the top 5 states with the most cities.
4. Explain in your own words (1–2 sentences) what idxmax() does and why it is used here.
   
---

## Task 5: Basic Visualization of Failed Logins
**Goal:** Use visualization to identify cities with unusually high failed login activity.

1. **Create a bar chart showing failed logins per city**
   - The x-axis should represent **City**
   - The y-axis should represent **failed_logins**
   - Rotate the city names so they are readable.
   - Add a title and axis labels.

2. **Highlight high-risk cities**
   - Cities with more than **50 failed logins** should appear in a different color
   - This helps visually separate normal activity from suspicious activity.

**Hints:**
- Use the `matplotlib.pyplot` library
- A bar chart is created using `plt.bar()`
- You can use a conditional list (if/else) to assign colors based on failed login values
- Use `plt.show()` to display the chart

**Reflection question based on Task 5:**
- How could this type of visualization help a cybersecurity analyst respond faster to threats?

---

## Task 6: Calculate Failed Login Rate
**Goal:*** Create  a new analytical column that helps identify cities with a high proportion of failed login attempts.
Raw counts alone can be misleading. A city with fewer total login attempts but many failures may represent a higher security risk. In this task, you will calculate a failed login rate to better assess risk.
1. Create a new column called `failed_login_rate`.
   - Calculate this value by dividing `failed_logins` by `login_attempts`.
   - This value represents the proportion of login attempts that failed.
2. Display the DataFrame to confirm that the new column was created successfully.
3. Sort the DataFrame by `failed_login_rate` in **descending order**.
4. Display the **top 5 cities** with the highest failed login rate.
5. In markdown cell, explain why is the failed login rate more informative than looking at failed login counts alone?

## Documentation Requirements

* Take one or multiple screenshots for **each task** above.
* Each screenshot must clearly show:
  * The Python code
  * The output produced (If the output is too big, only show the first few lines)
  * Your username and current datetime from a separate Windows Terminal.
* Paste all screenshots into **one MS Word document**
  
---

## Reference Material

The following materials are **optional** and provided for additional support:

1. Instructor in-class demonstration
2. W3Schools Pandas Tutorial: [https://www.w3schools.com/python/pandas/default.asp](https://www.w3schools.com/python/pandas/default.asp)
3. Pandas Crash Course (YouTube): [https://www.youtube.com/watch?v=EhYC02PD_gc](https://www.youtube.com/watch?v=EhYC02PD_gc)  
   *Watch at minimum up to the **Data Exploration** section (~17 minutes)*

---

## Submission Instructions

All lab work must be submitted as a **single PDF file** on Blackboard.

### Required Steps

1. Create a Word document and paste screenshots in order under labeled headings (Task 1, Task 2, etc.).
2. At the top of each task section, include your **name and student ID as comments** in the notebook.

```python
# Name: Your Name
# Student ID: 123456789
```

3. Demonstrate the work was completed on your own machine:
   * Open **Windows Terminal / Command Prompt**
   * Display your **system username**, **current date**, and **current time**
4. Capture screenshots showing:
   * Notebook code and output
   * System username, date, and time visible in the terminal
5. Convert the Word document to **PDF** before submission.

### Before You Submit

Ensure that:

* All tasks are included and clearly labeled
* Screenshots are readable
* Code executes correctly
* Your name, student ID, system username, date, and time are visible
  
---

## Important Notes

* Late submissions receive **-20% per day**
* Submissions that do not follow the instructions will receive a **grade of zero**
* Academic integrity policies apply.
* AI-generated answers are not permitted and may result in a grade of zero.

