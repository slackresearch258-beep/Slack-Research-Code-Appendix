# Slack Research Code Appendix

This repository contains the code appendix for a research paper analyzing how digital interactions reorganize work during organizational growth. The study explores changes in member interactions as a tech company rapidly scales, as seen through Slack use (692K+ messages, 438+ employees, 2018–2022).


## Accessing the notebooks
Download the repository as a zip folder by clicking on green code button and then Download ZIP

## Notebooks

### Descriptives.html
Reproduces Table S1 from the paper — growth indicators, employee demographics, and Slack usage statistics. Includes unique user counts, message volumes, and organizational growth metrics.

### Networks.html
Network analysis using Erdos-Renyi random models. Builds yearly interaction networks (replies, mentions, reactions) and welcome networks, then generates 500 random networks per year to compute Z-scores for five network measures: density, assortativity, modularity, efficiency, and diameter.

### Behavior (5 Items outliers removed).html
Behavioral analysis reproducing Figure 2 from the paper. Calculates thread conversion rates (percentage of original posts receiving at least one reply) by management level (Top Management, Middle Management, Individual Contributor) and quarter. Also includes average thread length per year.

### Behavior (12 Items outliers removed).html
Extended behavioral analysis with 12 outlier items removed instead of 5. Same structure as the 5-item version.

### Affect.html
Factor analysis of affective (emotional) communication patterns in Slack messages.

## Variable Files

### employees_variables.csv
Variable names and descriptions for the employee dataset.

### messages_anonymous_variables.csv
Variable names and descriptions for the anonymized messages dataset.

### networks_measures_quarters.csv
Network measures computed by quarter for empirical networks.

### slack_analytics_variables.csv
Variable names and descriptions for the Slack analytics dataset.

## Data Sources

The original datasets used in this analysis (not included in this repository for privacy):
- `messages_anonymous.csv` — 786K+ anonymized Slack messages
- `employees.csv` — 472 employees with anonymized IDs
- `Employee_Management_Levels_with_Codes.csv` — Management level classifications
- `null Enterprise Analytics All Time - Jun 9 2023.csv` — Daily workspace analytics

## Requirements

- Python 3.9+
- pandas, numpy, networkx, matplotlib, seaborn, scikit-learn, factor_analyzer
