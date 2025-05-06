# GrafanaCON 2025

## Best practices to level up your Grafana dashboarding skills

This repository contains the labs hands-on data for the **Best practices to level up your Grafana dashboarding skills** Hands-on Lab

This workshop was lead by:
- **Syed Usman Ahmad ([LinkedIn](https://www.linkedin.com/in/syed-usman-ahmad-b1415515/), [GitHub](https://github.com/usmangt), [YouTube](https://www.youtube.com/@freelinuxtutorials))**
- **Leon Sorokin ([GitHub](https://github.com/leeoniya/))**

## Movies Dashboard Queries

```sql
-- Summary
SELECT title, year, genre, duration, country FROM movies LIMIT 500;
-- Count stat panel
SELECT COUNT(*) FROM movies;
-- Average duration stat panel
SELECT AVG(duration) FROM movies;
-- Avg duration by country bar chart
SELECT country, AVG(duration) FROM movies WHERE country NOT LIKE '%,%' AND length(country) > 0 GROUP BY country ORDER BY AVG(duration);
-- Count by genre
SELECT genre, COUNT(*) FROM movies GROUP BY genre ORDER BY COUNT(*) DESC;
```

---
// Panel flow & Overrides
// Legend toggle, color change
// Table column width
---

**Title field link**

```
https://www.youtube.com/results?search_query=${__value}+${__data.fields.year}
```

**Genre field link**

```
/d/${__dashboard.uid}/${__dashboard}/?var-genre=${__value}
```

**Variable and data link university :D**

- https://grafana.com/docs/grafana/latest/panels-visualizations/configure-data-links/
- https://grafana.com/docs/grafana/latest/dashboards/variables/variable-syntax/

**Advanced Play Demos**

- https://play.grafana.org/d/ddvzyhqvzw83kf/dashboard-variables
- https://play.grafana.org/d/ddvpgdhiwjvuod/postgresql-overview

## How to use the CSV file

Just download the csv file name **gh-csv-data.csv** from this repo and save it on your machine.

Then follow along for the instructions that will be provided in the Hands-on Lab.

### Instructions for the Data links Exercise:

Use the following URL to paste in the URL text box when doing the exercise for the data links:
```
https://github.com/grafana/grafana/issues/
```
## Useful Links

- [Download](https://grafana.com/grafana/download) Grafana
- Get [free-forever Grafana Cloud Account](https://grafana.com/get/)
- Learn [about Grafana](https://grafana.com/docs/grafana/latest/?pg=oss-graf&plcmt=hero-btn-2)
- Getting Started with [Grafana Play](https://play.grafana.org/)
- Use, built and manage [Grafana Dashboards](https://grafana.com/docs/grafana/latest/dashboards/)
  - [Dashboard Variables](https://grafana.com/docs/grafana/latest/dashboards/variables/)
- Learn about [Grafana Transformations](https://grafana.com/docs/grafana/latest/panels-visualizations/query-transform-data/transform-data/)
- [Getting started wtih TestDB data source](https://community.grafana.com/t/using-grafana-test-data-datasource-plugin-for-learning-and-testing-scenarios/107115/3)
- Understanding [Panels and visualization](https://grafana.com/docs/grafana/latest/panels-visualizations/)
  - [Panel Inspect view](https://grafana.com/docs/grafana/latest/panels-visualizations/panel-inspector/)
  - [Data links](https://grafana.com/docs/grafana/latest/panels-visualizations/configure-data-links/)
  - [Overrides](https://grafana.com/docs/grafana/latest/panels-visualizations/configure-overrides/)
  - [Thresholds](https://grafana.com/docs/grafana/latest/panels-visualizations/configure-thresholds/)
  - [Value Mapping](https://grafana.com/docs/grafana/latest/panels-visualizations/configure-value-mappings/)
- [Dashboard data sources](https://grafana.com/docs/grafana/latest/datasources/#dashboard)
- [Dashboard Marketplace](https://grafana.com/dashboards)
- [Golden Grot Awards](https://grafana.com/golden-grot-awards/)

## Community Resources
- Join [Grafana Community Slack](https://slack.grafana.com/)
- [Grafana Community Forums](https://community.grafana.com/)
- Report issues, feature-requests, bugs at the [Official Grafana Repository](https://github.com/grafana/grafana)
