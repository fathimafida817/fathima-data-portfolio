# Customer Support Tracker — SQL + Excel

## Project Overview
This project analyzes ticket data to understand resolution time, issue types, repeated issues, and SLA performance. It simulates a real customer support environment.

## Business Problem
Managers needed insights into:
Daily ticket inflow
SLA breaches
Categories with high volume
Average resolution time
Categories causing repeated issues

## Tools Used
SQL
Excel

## Steps Followed
1. Cleaned raw ticket data in Excel by removing duplicates and fixing date formats.
2. Imported the cleaned file into an SQL database.
3. Wrote SQL queries to analyze ticket volume, SLA breaches, and resolution time.
4. Exported SQL output into Excel for summary tables.

## Example SQL Queries
SELECT category, COUNT(*) AS ticket_count
FROM tickets
GROUP BY category;

SELECT AVG(resolution_hours) AS avg_resolution_time
FROM tickets;

SELECT category, COUNT(*)
FROM tickets
WHERE sla_breached = 'Yes'
GROUP BY category;

## Key Insights
Repeat issues mainly came from Hardware Alignment category.
SLA breaches reduced after workflow improvements.
Tickets raised on weekends showed higher resolution time compared to weekdays.

## Project Outcome
This project demonstrates ability to:
Clean and prepare operational data
Write SQL queries for real support processes
Understand workflow and SLA performance patterns
Present findings clearly for management use
