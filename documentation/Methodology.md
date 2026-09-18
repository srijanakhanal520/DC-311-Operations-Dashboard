# Methodology

## DC 311 Service Operations Dashboard — 2025

This dashboard analyzes DC 311 service-request data for 2025 to evaluate service volume, completion performance, resolution time, due-date performance, and backlog patterns.

### Request Classification

Completed requests include records with a standardized status of Closed. Open and In-Progress requests are categorized as backlog.

Canceled, duplicate, and transferred requests are retained in the dataset for source transparency but are excluded from completion-rate calculations.

### Completion Rate

The completion rate measures the percentage of performance-eligible service requests that were completed. Excluded records such as canceled, duplicate, and transferred requests are not included in the calculation.

### Resolution Time

Resolution time represents the number of days between the service-request date and resolution date. Average and median resolution days are used to evaluate how long completed requests typically take to resolve.

### Due-Date Performance

Due-date performance is calculated only for completed requests that contain both a resolution date and a service due date.

Eligible requests are classified as:

- Completed by Due Date
- Completed After Due Date

Requests without the required date information are excluded from this calculation.

### Backlog Analysis

Open and In-Progress requests are treated as backlog. Backlog requests are grouped into aging categories of 0–3 days, 4–7 days, 8–14 days, 15–30 days, and more than 30 days.

### Time Analysis

Source timestamps were retained in their published UTC format. Hour-of-day analysis was not included in this version of the dashboard.

### Interpretation

Dashboard results are intended to support operational monitoring and identify patterns that may warrant further review. Differences in resolution time or backlog should not automatically be interpreted as poor organizational performance because service categories can have different complexity, workload, and expected completion timelines.
