# Minor_project_4
# 🎬 BingePlay — Streaming Analytics

Advanced SQL

BingePlay is a fictional Indian OTT streaming platform created for an industry-style **Advanced SQL analytics project**.

The project focuses on solving 12 real-world business questions using SQL to analyze user subscriptions, streaming behaviour, content performance, ratings, engagement patterns, upgrades and churn signals.

---

## 📌 Project Overview

BingePlay launched on **1 January 2024** with three subscription plans:

| Plan | Monthly Price |
|------|---------------|
| Basic | ₹199 |
| Premium | ₹399 |
| Family | ₹699 |

The platform contains a catalog of **100 shows** across multiple languages and approximately **3,000 users to date**.

The project simulates the work of a data analyst investigating user behaviour and answering business questions using SQL.

---

## 🎯 Project Objectives

The main objectives of this project were to:

- Analyze active subscriptions and recurring revenue
- Track monthly user signup trends
- Analyze viewing behaviour across devices
- Understand rating distributions
- Compare original and acquired content
- Detect binge-watching behaviour
- Identify users who signed up but never watched
- Identify Premium/Family users who only consume Basic-tier content
- Analyze subscription upgrades
- Detect users returning after incomplete viewing sessions
- Identify consecutive-week engagement patterns
- Detect potential churn signals

---

## 🗄️ Database Structure

The BingePlay database contains five main tables:

### 1. `users`

Contains user information and signup details.

### 2. `subscriptions`

Contains subscription history, plans, status and subscription dates.

### 3. `shows`

Contains information about the streaming catalog, including:

- Show title
- Category
- Language
- Release year
- IMDb rating
- Original/acquired status
- Minimum subscription plan

### 4. `watch_sessions`

Contains user viewing activity, including:

- Session date
- Show watched
- Watch duration
- Device type
- Completion status

### 5. `ratings`

Contains user ratings for shows.

---

## 📊 Dataset

The project dataset contains:

- **3,000 users**
- **4,497 subscription records**
- **100 shows**
- **100,351 watch sessions**
- **5,000 ratings**

The `watch_sessions` table also contains nullable `user_id` values, creating a deliberate NULL-handling challenge for the analysis.

---

# 🔎 Business Questions

The project consists of **12 business-focused SQL problems**.

## Q1 — Active Revenue

Calculate the number of active subscriptions and the total monthly recurring revenue as of **30 June 2024**.

---

## Q2 — Signup Momentum

Analyze new user signups for each month from **January to June 2024** and identify the month with the highest number of signups.

---

## Q3 — Device Analytics

Analyze streaming behaviour by device type:

- Total sessions
- Total watch minutes
- Average watch duration
- Completion rate

---

## Q4 — Rating Distribution

Analyze the distribution of ratings from **1 to 5 stars** and calculate the percentage of ratings that are 4 or 5 stars.

---

## Q5 — Originals vs Acquired

Compare BingePlay Originals with acquired content based on:

- Number of shows
- Average IMDb rating
- Average release year

---

## Q6 — Binge Day Detection

Identify binge-watching days where a user watches the **same show at least five times on the same calendar date**.

The analysis focuses specifically on **Q2 2024**.

---

## Q7 — Q1 Signups Who Never Watched

Identify users who signed up during **January–March 2024** but never recorded a watch session.

This question demonstrates NULL-safe SQL techniques.

---

## Q8 — Over-Paying Premium/Family Users

Identify Premium and Family subscribers whose viewing history consists only of shows available on the Basic plan.

This uses an anti-existence approach with `NOT EXISTS`.

---

## Q9 — Upgrade Success Cohort

Identify users who:

- Signed up in January 2024
- Started with a Basic plan
- Later upgraded to Premium or Family
- Were still active as of 30 June 2024

The analysis also calculates the average time from signup to first upgrade.

---

## Q10 — Cliffhanger Comebacks

Identify users who returned to the same show within **1–7 days** after an incomplete viewing session.

This uses a self-join on the `watch_sessions` table.

---

## Q11 — Consecutive-Week Engagement

Identify users who watched at least one session in **four or more consecutive calendar weeks** using ISO week numbering.

This problem uses the classic **gaps-and-islands** approach.

---

## Q12 — Churn Signal Detection

Identify users whose total watch time in June 2024 decreased by **50% or more** compared with May 2024.

Users must have had some viewing activity in May to be included.

---

# 🧠 SQL Concepts Applied

This project helped strengthen practical knowledge of:

- `SELECT`
- `WHERE`
- `GROUP BY`
- Aggregate functions
- `JOIN`
- `LEFT JOIN`
- `SELF JOIN`
- Subqueries
- `EXISTS`
- `NOT EXISTS`
- NULL handling
- Common Table Expressions (CTEs)
- `CASE`
- Date functions
- Window functions
- `ROW_NUMBER()`
- Ranking
- Gaps-and-islands
- Conditional aggregation
- Cohort analysis
- Time-based analysis

---

# 🛠️ Tech Stack

- **MySQL**
- **SQL**
- **Python**
- **Pandas**
- **SQLAlchemy**
- **PyMySQL**
- **Jupyter Notebook / Google Colab**

---

# 🧩 Key SQL Challenges

Some of the more challenging analytical problems in this project included:

- Handling `NULL` values in `watch_sessions`
- Using `NOT EXISTS` for anti-existence analysis
- Working with multiple subscription records per user
- Detecting binge-watching patterns through grouped date analysis
- Using self-joins to identify returning viewers
- Applying window functions to subscription and engagement data
- Solving consecutive-week engagement using the **gaps-and-islands** technique
- Comparing month-over-month viewing activity for churn detection

---

# 📚 Key Learning Outcomes

Through this project, I gained practical experience in applying SQL to business-oriented analytical problems.

The project helped strengthen my understanding of:

- Relational database analysis
- Advanced SQL querying
- Data aggregation and filtering
- Joins and subqueries
- NULL-safe analysis
- Window functions
- Time-based analysis
- User engagement analysis
- Cohort-based analysis
- Translating business questions into SQL solutions
