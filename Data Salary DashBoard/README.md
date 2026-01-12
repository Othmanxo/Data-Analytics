# Data Jobs Salary Dashboard (Excel)

This repository contains an interactive **Excel dashboard** built to explore **salary insights for data-related roles** based on job-posting data. The workbook is designed as a portfolio artifact to demonstrate practical Excel data analytics skills (data modeling, aggregation, KPI creation, and dashboarding).

**Creator:** Othman Alabed  
**Purpose:** Created after completing an **Excel Data Analytics** course to showcase my understanding and competence in using Excel for data analytics and dashboard development.

---

## What this dashboard does

The dashboard enables quick, filter-driven exploration of how **annual salaries** vary by:

- **Job Title** (e.g., Data Analyst, Data Scientist, Senior Data Scientist)
- **Country**
- **Employment / Schedule Type** (e.g., Full-time, Contractor)

It also summarizes **where postings come from** (job platform/source) for the selected filters.

---

## How to use (recommended workflow)

1. Open `data_salary_dashboard.xlsx` in **Microsoft Excel (desktop)** for the best experience.
2. Go to the **`Salary Calculator`** sheet (this is the main dashboard).
3. Use the dropdown selectors to set:
   - **Job Title**
   - **Country**
   - **Type** (schedule type)
4. Review the updated KPIs and charts (they refresh automatically based on your selections).

> Note: Some combinations may return blanks or `#NUM!` / `#N/A` where the underlying dataset has insufficient salary records for that segment.

---

## What you will see on the dashboard

### Key KPIs (cards)
The dashboard surfaces high-level metrics for the selected filters, such as:

- **Median annual salary**
- **Number of job postings**
- **Top posting platform/source** (e.g., the platform with the highest count under the filters)

### Visuals (charts)
The dashboard includes bar charts that update with your selections, including:

1. **Median salary by Job Title** (within the selected Country & Type)  
   - The selected job title is highlighted for fast comparison.
2. **Median salary by Type** (within the selected Country & Job Title)  
   - The selected type is highlighted for contrast versus alternatives.

---

## Workbook structure

The file is organized into a main dashboard sheet plus supporting analysis sheets:

- **`Salary Calculator`**  
  The user-facing dashboard (filters, KPIs, and charts).

- **`Data`**  
  The raw dataset used by the dashboard (stored as an Excel Table for structured references).

- **`Title`**  
  Helper calculations that compute median salary by job title for the current filters and generate chart-ready series (including a highlighted series for the selected title).

- **`Type`**  
  Helper calculations that compute median salary by schedule type for the current filters and generate chart-ready series (including a highlighted series for the selected type).

- **`Country`**  
  Helper table(s) for salary by country under the active filters (used for lookups/analysis).

- **`Platform`**  
  Helper calculations that compute job-posting counts by platform/source using multi-condition aggregation under the active filters.

- **`Data Validation`**  
  Clean lists used for dropdowns and helper lookups (e.g., titles, countries, types).

---

## Data fields (high level)

The dataset in `Data` includes fields commonly used for segmentation and analysis, such as:

- `job_title_short`, `job_title`
- `job_country`, `job_location`
- `job_schedule_type`
- `job_via` (posting platform/source)
- `salary_year_avg`, `salary_hour_avg`, `salary_rate`
- flags such as `job_work_from_home`, `job_no_degree_mention`, `job_health_insurance`
- `company_name`, `job_skills`
- `job_posted_date`

---

## Excel techniques demonstrated

This workbook was built to demonstrate practical, job-relevant Excel analytics capabilities, including:

- **Structured tables** and structured references (e.g., `jobs[salary_year_avg]`)
- **Multi-condition aggregation** (e.g., `COUNTIFS(...)` and similar patterns)
- **Lookups** (e.g., `XLOOKUP(...)`)
- **Dashboard-ready helper tables** that feed visuals
- **Dynamic chart highlighting** using `IF(..., NA())` series splitting
- **Data validation lists** to create controlled dropdown selectors
- **Error handling** to gracefully deal with missing/insufficient data

---

## Notes and disclaimer

- This dashboard is a **portfolio/learning project** created for educational demonstration purposes.
- Salary values may be missing for some postings; results depend on available data for each filter combination.
- This is **not financial advice** and should not be used as the sole basis for compensation decisions.

---

## Author

**Othman Alabed**  
Excel Data Analytics Dashboard (Portfolio Project)
