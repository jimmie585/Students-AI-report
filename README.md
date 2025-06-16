# Students-AI-report
# 📘 Kurasa AI Report Summary

**Kurasa AI Report Summary** is a student performance prediction system developed for the **Kurasa** platform. Using machine learning, the system forecasts student scores based on historical data and generates insightful visual reports to aid teachers, administrators, and learners in understanding academic trends.

---

## 🚀 Features

- 🔮 Predicts scores for subjects using student ID and term.
- 📊 Visualizes predictions using bar, line, and radar charts.
- 🏁 Automatically classifies students as Pass or Fail.
- 🏆 Highlights best and weakest performing subjects.
- 🧹 Cleans and prepares input data with handling for missing values.
- 🧠 Powered by a Random Forest multi-output regression model.

---

## 🧪 How It Works

1. **Data Preparation**
   - Drops non-numeric fields like `student_name`, `assessment_type`, `Year`, `Result`.
   - Fills missing subject scores with the mean.

2. **Model Training**
   - Trains a `RandomForestRegressor` using:
     - Features: `student_id`, `TermNumber`
     - Targets: Subject scores

3. **Prediction & Reporting**
   - Generates predictions for a specific student and term.
   - Computes average score and result.
   - Visualizes data with:
     - 📊 Bar Chart
     - 📈 Line Chart
     - 🕸️ Radar Chart

4. **Outputs**
   - Student report summary
   - Predicted scores by subject
   - Performance classification

---

## 📁 Sample Output

```text
📘 Report for: Mary Atieno | Term: 1 | Assessment: formative
✅ Average Score: 59.06 → Result: Pass

                               Predicted Score
Christian Religious Education        71.65
English                              73.10
Mathematics                          57.97
Science                              59.62
Social Studies                       51.04

🏆 Best Subject: English (73.1)
⚠️  Weakest Subject: Social Studies (51.0)
