# Postmortem : Database Connection Outage on Web Application

### Issue Summary
**Duration**: 2024-08-20, 15:15 GMT+1 to 16:05 GMT+1 (50 minutes)
**Impact**: The web application's database was incaccessible, leading to a full outage of the service.
All users were affected, experiencing server errors and the inability to access any part of the application.
**Root Cause**: The outage was due to misconfiguration in the database connection settings following a routine deployment, resulting in the exhaustion of database connections.

## Timeline
- 15:15 GMT+1 --> Issue detected by automated monitoring alert indicating a spike in server errors (500 responses).

- 15:16 GMT+1 --> The engineering team began investigating the web server logs, suspecting a recent code deployement as the root cause.

- 15:23 GMT+1 --> The team checked the deployement logs, verifting that no errors occurred during deployement, ruling out a deployement failure.

- 15:30 GMT+1 --> Investigation shifted to the database server, where high CPU usage and a significant number of active connections were observed.

- 15:35 GMT+1 --> Initial assumption was that a database query in the new deployement was causing performance issues.

- 15:40 GMT+1 --> After further analysis, the team realized that the connection pool configuration had been altered, causing the application to open more connections than the database could handle.

- 15:45 GMT+1 --> Incident escalated to the database administration team to validate the findings.

- 15:50 GMT+1 --> The database configuration was reverted to its previous state, and a restartof the web servers was initiated.

- 16:02 GMT+1 --> Monitoring confirmed that the application was back online, and the number of database connections had stabilized.

- 16:08 GMT+1 --> Full service was restorted, and the incident was declared resolved.

## Root Cause and Resolution