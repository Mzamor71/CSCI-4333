
---
Michael Zamora & Brandon Duberney
---

# Robot Movement Analysis
This project uses Python, Pandas, and SQLite to store and analyze robot movement data from CSV files. The goal is to determine when robots are close to each other and whether they move below a given speed threshold during specific time intervals.




## Tools Used
- Python 3
- SQLite
- Pandas
- Jupyter Notebook

---

## Database Tables
- **Robot**: stores robot IDs and names  
- **SensorReading**: stores robot position (x, y) at each timestamp  
- **TargetInterval**: stores labeled time intervals for analysis  

---

## Input Files
All CSV files must be placed in a `csv_files/` directory.

- `robot.csv` – robot IDs and names  
- `t1.csv` – `t5.csv` – robot sensor readings  
- `interval.csv` – start/end times and event labels  

Sensor files may include either `(x, y)` or `(timestamp, x, y)`.  
Missing timestamps are automatically generated.

---

## Analysis Tasks
1. **Robot Proximity**  
   Finds times when robots *Astro* and *IamHuman* are within 1 unit in both x and y directions.

2. **Time Spent Close**  
   Counts how many seconds the two robots remain close.

3. **Speed Threshold Check**  
   Calculates robot movement speed during intervals and reports whether it is below `0.2` units/second.



