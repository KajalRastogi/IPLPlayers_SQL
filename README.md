# IPL Players Database – SQL Project

This project provides a structured MySQL database for managing IPL (Indian Premier League) player information. It includes a schema definition and sample data for use in data analysis or application development.
---
## Contents

- **IPLPlayers_SQL.sql** – SQL script to:
  - Create the `IPLPlayers` database
  - Define the `Players` table
  - Insert sample player records
---
##  Database Structure
**Database:** `IPLPlayers`  
**Table:** `Players`

### Columns:
| Field         | Type            | Description                      |
|---------------|-----------------|----------------------------------|
| Player        | VARCHAR(120)    | Name of the player               |
| Price_in_cr   | DECIMAL(10,2)   | Price in Crores (INR)            |
| Type          | VARCHAR(50)     | Player type (e.g., Indian, Overseas) |
| Acquisition   | VARCHAR(50)     | How player was acquired (e.g., Retained) |
| Role          | VARCHAR(50)     | Player role (e.g., Batter, All-rounder) |
| Team          | VARCHAR(100)    | IPL Team name                    |
---
## 🚀 Usage Instructions

1. **Run the Script**  
   Execute `IPLPlayers_SQL.sql` in your MySQL environment.
2. **Sample Queries**
```sql
-- View all players
SELECT * FROM Players;
-- Total spend by team
SELECT Team, SUM(Price_in_cr) AS Total_Spend FROM Players GROUP BY Team;
-- Players by role
SELECT Role, COUNT(*) AS Count FROM Players GROUP BY Role;
