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

You will work in **Jupyter Notebook** using a **local Anaconda installation** (completed in Week 1).

Verify that the following libraries are available:

* `pandas`
* `matplotlib`

If any library is missing, install it using:

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
4. Display basic DataFrame information using the `.info()` method. Add your comments in the code explaining does this methods acheive.

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
2. Sort the filtered cities by failed_logins descending
3. Count how many high-risk cities there are.

### Reflection Questions based on Task3

- Why is it useful to sort and count high-risk cities?  
- How could this help a cybersecurity analyst prioritize investigations?  
---
## Task 4: Simple Analysis of Cities by State
**Goal:** Learn how to aggregate and count data using Pandas.
1. Count how many cities exist in each state.
2. Identify the state with the highest number of cities. Use the `idxmax()` method.
3. Display the top 5 states with the most cities.
4. Explain in your own words what idxmax() does and why it is used here.

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
- You can use a conditional list (if/else) to assign colors based on failed login values.
- Use `plt.show()` to display the chart

**Reflection Questions:**
- How could this type of visualization help a cybersecurity analyst respond faster to threats?

## Documentation Requirements

* Take a screenshot for **each task** above
* Each screenshot must clearly show:
  * The Python code
  * The output produced
  * Your username and current datetime from a separate windows terminal.
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

## Final Reflection

At the end of your document, answer the following questions:
1. Which task gave you the most insight into analyzing potential security events?
2. How did filtering and aggregation help you identify possible anomalies?
3. How could visualization help a cybersecurity analyst in real-time threat detection?
4. Which task did you find most challenging and why?
5. What Python or Pandas concept do you feel confident applying to cybersecurity data after completing this lab?
Each response should be **2–4 sentences**, written in your own words. AI based answers will lead to a grade of zero for the submission.

---

## Important Notes

* Late submissions receive **-20% per day**
* Submissions that do not follow the instructions will receive a **grade of zero**
* Academic integrity policies apply

---

✅ This lab builds essential skills for future cybersecurity data analysis labs.
