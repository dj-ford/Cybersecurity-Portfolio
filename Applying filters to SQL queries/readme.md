# Applying Filters to SQL Queries

## Project Description
As part of my role as a security professional, I investigate unusual login activity and ensure that employee devices receive the proper security updates. To support these efforts, I used SQL queries with filters to analyze data from the `log_in_attempts` and `employees` tables. These queries helped me identify suspicious login behavior, isolate potential threats, and locate employees whose systems required updates.

---

## Retrieve After-Hours Failed Login Attempts
One potential security issue occurred outside regular working hours. Any failed login attempts after 18:00 needed to be reviewed for possible unauthorized activity.

image

This query filters for login attempts occurring after 18:00 and marked as unsuccessful. By combining conditions with AND, I isolated only the records that matched both the time and failure criteria.

---

## Retrieve Login Attempts on Specific Dates

A suspicious event was reported on 2022-05-09, and I needed to check login activity from that day as well as the previous day.
image

Using OR, this query returns all login attempts from either of the two dates. This made it easier to investigate events that may have occurred just before the main incident.

---

##Retrieve Login Attempts Outside of Mexico

Some login attempts were recorded from locations that did not appear to match expected user activity. Any attempts from outside Mexico required investigation.
image

Because data entries may use either MEX or MEXICO, I used LIKE 'MEX%' along with NOT to exclude all Mexican entries. The wildcard % captures variations in how the country is listed.


---

## Retrieve Employees in Marketing

The Marketing department in the East building required a round of security updates. I filtered the employee records to identify the correct machines.
image

The AND operator ensures results include only Marketing employees located in the East building. The LIKE pattern helps identify all office numbers that begin with "East."

---

## Retrieve Employees in Finance or Sales

Another update needed to be deployed to employees in the Finance and Sales departments. I used a filter to retrieve records from both groups.

image

Using OR captured employees from either department, allowing me to collect all necessary machine information for the update.


---

Retrieve All Employees Not in IT

A final update was required for employees outside of the Information Technology department.


By applying NOT IN, I returned every employee whose role falls outside the IT department, ensuring that non-IT systems received the proper updates.


---

## Summary

Using SQL filtering techniques, I analyzed login activity and employee data to support the organization’s security operations. I used logical operators such as AND, OR, and NOT to narrow down results and applied pattern matching with LIKE and % when necessary. These queries helped identify possible security threats and ensured that employee devices received appropriate updates.
