# Anime Dataset Analysis - Project Summary

This document provides a precise overview of the data preprocessing, feature engineering, and key analytical findings executed on the `anime.csv` dataset.

---

## 🛠️ Data Preprocessing & Feature Engineering

- **Data Loading:** 
  Loaded the raw dataset using pandas: `df = pd.read_csv('anime.csv')`.

- **Episode Count Extraction:**
  Extracted numeric episode counts from parentheses within titles (e.g., `(64 eps)`) via a custom parser `extract_episode()`, cleaned trailing characters, and cast to integer format.

- **Broadcast Period Extraction:**
  Isolated airing timeframes (e.g., `'Apr 2011 - Sep 2011'`) from titles using `extraction_time()` and saved them in a new `'Total Time'` column.

- **Duration Calculation:**
  Computed the total span of the broadcasting window in months using `datetime.strptime` and `dateutil.relativedelta` (adding `+1` to include the starting month).

---

## 📊 Key Findings

- **Highest Rated Anime:** 
  *Fullmetal Alchemist: Brotherhood* with a score of **9.10**.

- **Highest Episode Count:** 
  *Gintama* with **201 episodes**.

- **Longest Running Anime:** 
  *Ginga Eiyuu Densetsu*, broadcasting for **111 months** (approx. 9 years, from Jan 1988 to Mar 1997).
