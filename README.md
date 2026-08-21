# Academic SME Productivity Tracker

## 1. Project Overview

The **Academic SME Productivity Tracker** is an Excel/Google Sheets-based productivity and performance analytics system designed to monitor the performance of Academic Subject Matter Experts (SMEs).

Academic SMEs perform multiple activities such as question creation, content review, question solving, quality auditing, and student support. Measuring performance only through the number of tasks completed can be misleading because productivity must also consider **quality, accuracy, turnaround time, rework, timeliness, and productive working hours**.

This project develops a structured KPI-based framework that combines these dimensions to evaluate individual SME performance and provide managers with actionable performance insights.

The tracker contains:

* Employee Master Database
* Daily SME Productivity Log
* Productivity and Quality KPIs
* Accuracy and Rework Analysis
* Turnaround Time (TAT) Tracking
* On-Time Completion Analysis
* Productive Hours Tracking
* Overall KPI Score
* Employee-Level Performance Summary
* Weekly Productivity Analysis
* Manager's Index for SME Ranking
* Management Dashboard

---

# 2. Problem Statement

Academic content teams need to balance **quantity, quality, speed, and reliability**.

A simple productivity measure such as:

[
Productivity = \frac{Tasks\ Completed}{Tasks\ Assigned}
]

does not capture the complete performance of an SME.

For example, an SME completing 100 questions with low accuracy and high rework should not necessarily be considered more productive than an SME completing 80 high-quality questions.

Therefore, this project develops a **multi-dimensional performance measurement system** that evaluates SMEs using several complementary KPIs.

The primary objectives are:

1. Measure daily SME productivity.
2. Monitor content quality.
3. Measure accuracy.
4. Track rework.
5. Monitor turnaround time.
6. Measure on-time completion.
7. Track productive working hours.
8. Generate an overall KPI score.
9. Compare SME performance over time.
10. Provide managers with a structured basis for performance evaluation.

---

# 3. Project Objectives

The project aims to answer the following questions:

* How much work is assigned to each SME?
* How much work is actually completed?
* Is the SME meeting the expected productivity target?
* What proportion of the work meets quality standards?
* How accurate is the SME's output?
* How much work requires rework?
* How quickly does the SME complete assigned work?
* What proportion of tasks are completed on time?
* How many productive hours does the SME contribute?
* Which SMEs are performing consistently well?
* Which SMEs require performance improvement?
* How does SME performance change from week to week?

---

# 4. Data Structure

The tracker is organized into multiple sheets.

## 4.1 Employee Master

The Employee Master contains the basic information of each SME.

| Field             | Description                     |
| ----------------- | ------------------------------- |
| Employee ID       | Unique identifier of the SME    |
| Employee Name     | Name of the SME                 |
| Subject / Domain  | Academic subject handled        |
| Designation       | Employee's role                 |
| Team / Department | Functional team                 |
| Joining Date      | Date of joining                 |
| Reporting Manager | Manager responsible for the SME |
| Employment Status | Active/Inactive status          |

---

## 4.2 Daily Log

The Daily Log records the day-to-day activities of each SME.

| Field              | Description                     |
| ------------------ | ------------------------------- |
| Date               | Date of activity                |
| SME Name           | Employee performing the work    |
| Subject / Domain   | Academic subject                |
| Work Type          | Type of activity performed      |
| Tasks Planned      | Number of tasks assigned        |
| Tasks Completed    | Number of tasks completed       |
| Questions Created  | New questions/content created   |
| Questions Reviewed | Questions reviewed              |
| Quality Score      | Quality evaluation score        |
| Accurate Items     | Number of accurate items        |
| Items Audited      | Number of items evaluated       |
| Rework Items       | Items requiring correction      |
| Avg TAT            | Average turnaround time         |
| On-Time Items      | Tasks completed within deadline |
| Total Due Items    | Total tasks due                 |
| Productive Hours   | Productive working hours        |
| Attendance         | Attendance status               |
| Remarks            | Additional observations         |

The calculated KPI columns are derived from these input variables.

---

# 5. Productivity Metrics

## 5.1 Task Completion Rate

Task Completion Rate measures how much of the assigned workload was completed.

[
\boxed{
Completion\ Rate =
\frac{Tasks\ Completed}{Tasks\ Planned}
}
]

### Example

If:

* Tasks Planned = 48
* Tasks Completed = 41

Then:

[
Completion\ Rate =
\frac{41}{48}
=0.8542
]

Therefore:

[
\boxed{Completion\ Rate = 85.4%}
]

A value above 100% indicates that the SME completed more tasks than originally planned.

For example:

[
\frac{56}{52}=107.7%
]

means the SME completed approximately 7.7% more than the planned workload.

---

# 6. Quality Measurement

Quality Score measures the quality of the SME's output based on the organization's quality evaluation process.

The quality score can be represented as:

[
\boxed{
Quality\ Score =
\frac{Quality\ Points\ Obtained}{Maximum\ Quality\ Points}
\times 100
}
]

### Example

If an SME obtains 92.3 quality points out of 100:

[
Quality\ Score = 92.3%
]

Quality is given a relatively high weight in the overall KPI because academic content must maintain a high standard even when productivity is high.

---

# 7. Accuracy Rate

Accuracy Rate measures the proportion of audited items that are accurate.

[
\boxed{
Accuracy\ Rate =
\frac{Accurate\ Items}{Items\ Audited}
}
]

### Example

Suppose:

* Accurate Items = 30
* Items Audited = 33

Then:

[
Accuracy\ Rate =
\frac{30}{33}
=0.9091
]

Therefore:

[
\boxed{Accuracy\ Rate = 90.9%}
]

Accuracy is particularly important for academic SMEs because high output with incorrect content can negatively affect students and the organization.

---

# 8. Rework Rate

Rework Rate measures the proportion of audited items that require correction or modification.

[
\boxed{
Rework\ Rate =
\frac{Rework\ Items}{Items\ Audited}
}
]

### Example

If:

* Rework Items = 2
* Items Audited = 33

Then:

[
Rework\ Rate =
\frac{2}{33}
=0.0606
]

Therefore:

[
\boxed{Rework\ Rate = 6.1%}
]

Unlike most KPIs, **lower rework is better**.

A lower rework rate indicates that the SME is producing more accurate work initially and therefore requires less corrective effort.

---

# 9. Turnaround Time (TAT)

Turnaround Time measures the time required to complete an assigned task.

[
\boxed{
TAT =
Completion\ Time - Start\ Time
}
]

For example, if work starts at 10:00 AM and is completed at 1:30 PM:

[
TAT = 3.5\ hours
]

For multiple tasks, average TAT can be calculated as:

[
\boxed{
Average\ TAT =
\frac{\sum TAT_i}{Number\ of\ Tasks}
}
]

### Example

Suppose four tasks have TATs of:

* 2 hours
* 3 hours
* 4 hours
* 3 hours

Then:

[
Average\ TAT =
\frac{2+3+4+3}{4}
=3\ hours
]

A lower TAT generally indicates greater operational efficiency, provided that quality is maintained.

---

# 10. On-Time Completion Rate

On-Time Completion Rate measures the proportion of due tasks completed within the required deadline.

[
\boxed{
On-Time\ Rate =
\frac{On-Time\ Items}{Total\ Due\ Items}
}
]

### Example

If:

* On-Time Items = 41
* Total Due Items = 48

Then:

[
On-Time\ Rate =
\frac{41}{48}
=85.4%
]

Therefore:

[
\boxed{On-Time\ Rate = 85.4%}
]

This KPI captures reliability and deadline adherence.

---

# 11. Productive Hours

Productive Hours represent the time spent by an SME on productive academic activities.

Examples include:

* Question creation
* Question review
* Content development
* Quality auditing
* Question solving
* Student support
* Research

Productive hours are used as an efficiency and capacity indicator.

For example:

[
Productive\ Hours = 7.4\ hours/day
]

However, productive hours should not be evaluated independently. A high number of hours with low output or poor quality does not necessarily indicate high productivity.

---

# 12. Attendance

Attendance provides context for interpreting daily productivity.

Possible values include:

* Present
* Half Day
* Leave
* Holiday

Attendance is important because daily output should be interpreted in relation to the amount of time the employee was actually available.

For example, an SME working a half day should not be compared directly with an SME working a full day using raw task counts alone.

---

# 13. KPI Target Framework

The tracker uses predefined performance targets.

| KPI                  |      Target |
| -------------------- | ----------: |
| Task Completion Rate |         90% |
| Quality Score        |         90% |
| On-Time Rate         |         90% |
| Accuracy Rate        |         95% |
| Productive Hours     | 7 hours/day |
| Rework Rate          |          5% |

These targets can be modified according to the organization's requirements.

---

# 14. KPI Weighting

Different KPIs contribute different proportions to the overall performance score.

| KPI                  |   Weight |
| -------------------- | -------: |
| Task Completion Rate |      20% |
| Quality Score        |      30% |
| On-Time Rate         |      15% |
| Accuracy Rate        |      15% |
| Productive Hours     |      10% |
| Rework Rate          |      10% |
| **Total**            | **100%** |

Quality receives the highest weight because academic content quality is critical to the SME's role.

---

# 15. Overall KPI Score

The overall KPI score combines the individual KPI performances using the predefined weights.

The conceptual structure is:

[
Overall\ KPI =
C_wC_s+
Q_wQ_s+
O_wO_s+
A_wA_s+
H_wH_s+
R_wR_s
]

where:

* (C_s) = Completion performance
* (Q_s) = Quality performance
* (O_s) = On-Time performance
* (A_s) = Accuracy performance
* (H_s) = Productive Hours performance
* (R_s) = Rework performance
* (C_w,Q_w,O_w,A_w,H_w,R_w) = corresponding weights

The KPI components are compared against their respective targets.

For example, if the completion target is 90% and the SME achieves 85%:

[
Completion\ Performance =
\frac{85%}{90%}
]

The score is capped at the target-equivalent maximum for the corresponding component so that extreme over-performance in one metric does not completely dominate the overall score.

For rework, the direction is reversed because lower rework represents better performance.

---

# 16. Why a Weighted KPI Model Is Used

A single productivity measure can create undesirable incentives.

For example:

> SME A completes 100 questions but has 75% accuracy.

versus:

> SME B completes 85 questions with 98% accuracy.

A pure output-based system would rank SME A higher.

However, for academic content, accuracy and quality are essential.

The weighted KPI framework therefore attempts to balance:

[
\boxed{
Quantity + Quality + Accuracy + Speed + Reliability
}
]

This creates a more comprehensive performance assessment.

---

# 17. Employee KPI Summary

The Employee KPI Summary aggregates daily records at the employee level.

For each SME, the tracker calculates:

* Number of days logged
* Total tasks planned
* Total tasks completed
* Overall completion rate
* Average quality score
* Overall accuracy rate
* Overall rework rate
* Overall on-time rate
* Average TAT
* Average productive hours
* Average KPI score
* Performance band

This allows managers to compare employees using multiple performance dimensions rather than a single output metric.

---

# 18. Performance Bands

Employees can be grouped into performance bands according to their overall KPI score.

The current framework uses:

| KPI Score | Performance Band  |
| --------- | ----------------- |
| ≥ 90%     | Excellent         |
| 75%–89.9% | Good              |
| 60%–74.9% | Needs Improvement |
| < 60%     | Critical          |

These thresholds can be customized according to organizational requirements.

---

# 19. Weekly Performance Analysis

Daily performance is aggregated into weekly periods to identify trends.

Weekly metrics include:

* Tasks Planned
* Tasks Completed
* Completion Rate
* Average Quality
* Average Productive Hours
* Average KPI Score

Weekly analysis helps identify:

* Improvement in productivity
* Declining performance
* Consistent high performers
* Consistent low performers
* Changes in workload
* Changes in quality
* Operational bottlenecks

Weekly analysis is generally more useful for managerial decision-making than relying only on individual daily observations.

---

# 20. Manager's Index

## Manager's Index for Weekly SME Ranking

<!-- Fill this section later -->

---

# 21. Management Dashboard

The Dashboard provides a high-level view of SME performance.

Key indicators include:

* Total number of SMEs
* Average completion rate
* Average quality score
* Average KPI score
* Employee-level performance
* Weekly productivity trends

The Dashboard allows managers to quickly identify performance patterns without reviewing every individual daily record.

---

# 22. Workflow of the System

The complete workflow can be represented as:

```text
Employee Master
       ↓
Daily SME Activity
       ↓
Daily Productivity Log
       ↓
Raw Performance Metrics
       ↓
┌──────────────────────────────┐
│ Completion Rate              │
│ Quality Score                │
│ Accuracy Rate                │
│ Rework Rate                  │
│ TAT                          │
│ On-Time Rate                 │
│ Productive Hours             │
└──────────────┬───────────────┘
               ↓
        KPI Normalization
               ↓
        Weighted KPI Score
               ↓
      Employee KPI Summary
               ↓
       Weekly Aggregation
               ↓
        Manager's Index
               ↓
      Management Dashboard
```

---

# 23. Technology Used

The project was developed using:

* **Microsoft Excel**
* **Google Sheets compatibility**
* Spreadsheet formulas
* Data validation
* Conditional formatting
* KPI calculations
* Dashboarding
* Employee-level aggregation
* Weekly performance analysis

---

# 24. Key Features

### Employee Management

* Employee master database
* Employee ID system
* Subject/domain classification
* Reporting manager mapping

### Productivity Tracking

* Daily task allocation
* Task completion
* Question creation
* Question review
* Productive hours

### Quality Management

* Quality score
* Accuracy rate
* Rework rate
* Quality audit tracking

### Operational Efficiency

* Turnaround Time
* On-time completion
* Attendance tracking

### Performance Analytics

* Weighted KPI score
* Employee performance summary
* Performance bands
* Weekly performance analysis
* Manager's Index
* Management dashboard

---

# 25. Business Value

The tracker can help academic content organizations:

1. Standardize SME performance measurement.
2. Identify high-performing employees.
3. Identify employees requiring additional support.
4. Monitor quality alongside productivity.
5. Detect excessive rework.
6. Identify turnaround-time bottlenecks.
7. Improve workload allocation.
8. Monitor weekly performance trends.
9. Support data-driven managerial decisions.
10. Create a transparent performance evaluation framework.

---

# 26. Important Design Principle

The project does not treat productivity as simply:

[
\text{Number of Tasks Completed}
]

Instead, it recognizes that effective SME performance requires a balance between:

[
\boxed{
Productivity,\ Quality,\ Accuracy,\ Timeliness,\ Efficiency
}
]

This prevents excessive emphasis on output volume at the expense of academic content quality.

---

# 27. Future Improvements

Potential future extensions include:

* Difficulty-weighted productivity
* Subject-specific productivity benchmarks
* Automated attendance integration
* Real-time Google Sheets dashboard
* Automated weekly reports
* Individual SME dashboards
* Manager-level filtering
* Automated performance alerts
* Trend and variance analysis
* Productivity forecasting
* Integration with task-management systems
* Integration with HR systems
* Automated Manager's Index calculation
* Statistical analysis of productivity drivers

---

# 28. Limitations

The current tracker is designed as a productivity and performance monitoring framework and should not be treated as a complete employee evaluation system.

Performance evaluation should also consider factors such as:

* Task complexity
* Subject difficulty
* Experience level
* Training requirements
* Type of work assigned
* Team responsibilities
* Non-production activities

Therefore, the KPI score should be used as a **decision-support measure**, rather than the sole basis for employee evaluation.

---

# 29. Sample Data

The repository uses synthetic/sample employee data for demonstration purposes.

No confidential employee information or proprietary organizational data should be included in the public version of the project.

---

# 30. Project Structure

```text
academic-sme-productivity-tracker/
│
├── README.md
│
├── Academic_SME_Productivity_Tracker.xlsx
│
├── screenshots/
│   ├── dashboard.png
│   ├── daily-log.png
│   └── employee-kpi-summary.png
│
└── documentation/
    └── KPI_Methodology.md
```

---

# 31. Conclusion

The Academic SME Productivity Tracker provides a structured framework for monitoring and analyzing Academic SME performance.

By combining productivity, quality, accuracy, rework, turnaround time, timeliness, and productive hours into a weighted KPI framework, the system provides a more comprehensive view of employee performance than simple task-count-based measurement.

The addition of weekly performance analysis and the Manager's Index further enables managers to compare SME performance and make more informed operational decisions.

---

# 32. Author

**Durgesh Yadav**

M.Sc. Economics
Indian Institute of Technology Kanpur

---

# 33. Project Status

**Status:** Completed / Ongoing Enhancement

The project can be further extended with automated dashboards, difficulty-weighted productivity, advanced Manager's Index methodology, and integration with real-time data sources.
