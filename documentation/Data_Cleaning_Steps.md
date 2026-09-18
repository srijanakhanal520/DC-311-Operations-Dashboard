# Data Cleaning Steps

## DC 311 Service Operations Dashboard — 2025

The 2025 DC 311 service-request dataset was cleaned and transformed in Power Query before being used for dashboard analysis. The following steps were performed to improve consistency, support KPI calculations, and prepare the data for visualization.

### 1. Data Import and Review
The DC 311 City Service Requests in 2025 dataset was imported into Power BI. Column names, data types, missing values, and important service-request fields were reviewed before analysis.

### 2. Date and Time Preparation
Request, resolution, and service-due-date fields were prepared for analysis. RequestDate was used to support monthly analysis and was connected to a separate DateTable containing the 2025 calendar.

### 3. Organization Standardization
Organization information was prepared using the organization acronym field. Missing organization values were designed to be categorized as "Unassigned" so they could be identified during data-quality checks.

### 4. Service Status Standardization
Service-request statuses were standardized into consistent categories for reporting. Status values were used to distinguish Closed, Open, In-Progress, Canceled, Duplicate, and Transferred records.

### 5. Performance Classification
A PerformanceStatus field was created to classify records into:
- Completed
- Backlog
- Excluded - Canceled
- Excluded - Duplicate
- Excluded - Transferred

Closed requests were classified as Completed, while Open and In-Progress requests were treated as Backlog. Canceled, duplicate, and transferred records were retained for transparency but excluded from completion-rate calculations.

### 6. Resolution-Time Preparation
ResolutionDays was prepared to measure the number of days between a service request and its resolution. The field supports average and median resolution-time analysis.

### 7. Due-Date Performance
Completed requests with the required resolution and service-due-date information were classified as either "Completed by Due Date" or "Completed After Due Date." Records without the required dates were not included in due-date performance calculations.

### 8. Backlog Aging
Unresolved requests were grouped into backlog-aging categories:
- 0–3 Days
- 4–7 Days
- 8–14 Days
- 15–30 Days
- More Than 30 Days

Numeric prefixes were added to the categories to maintain the correct order in Power BI visualizations.

### 9. Data Quality Checks
The cleaned data was reviewed for missing resolution dates, missing organization information, missing ward information, excluded requests, and invalid duration values. Sensitive location-level information such as street addresses and exact coordinates was not included in dashboard visuals.

### 10. Final Validation
The cleaned model contained approximately 440,600 source records. Status classifications, monthly coverage from January through December 2025, backlog measures, completion measures, and due-date performance measures were reviewed before the dashboard was finalized.