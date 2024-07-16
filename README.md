# python-stockton-pd-responses

![Stockton CA](https://images.unsplash.com/photo-1596687876907-b9431dd5b636?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

## Stockton PD Responses

### This project is an overview of how safe the areas in Stockton CA are. The dataset that I obtained is from the Stockton County Website. The original dataset spanned from 2019 - June 2024. The file size was massive and I thought it would make sense to focus on 2023 - June 2024. 

## Technologies Used

### Excel, Python, SQL, and Amazon QuickSight.

## EDA and Data Cleaning

### You can checkout the python notebooks to see how I cleaned and explored the data. It is detailed with the steps I took.

## SQL

### All the data
```
SELECT COUNT(*) FROM data_final;
```

// *********************************************************************************** //

### Amount of responses from 2023: 449038
```
SELECT 
  COUNT(*)
FROM data_final
WHERE call_entry_date <= '2023-12-31';
```

// *********************************************************************************** //

### Amount of responses from 2024: 205850
```
SELECT 
	COUNT(*)
FROM data_final
WHERE call_entry_date >= '2024-01-01';
```

// *********************************************************************************** //

| DISTRICT_COUNT | DISTRICT_NAME |
| -------------- | ------------- |
| 181484		     | CIVIC         |
| 108081		     | LAKEVIEW      | 
| 96621		       | SEAPORT       |
| 93007		       | VALLEY OAK    |
| 88484		       | PARK          |
```
SELECT 
	COUNT(*) AS DISTRICT_COUNT, district_name
FROM data_final
GROUP BY district_name
LIMIT 5;
```

// *********************************************************************************** //

## Visualizating the Data

### You can go through the following pdf walkthrough that I put together.

[amazon-quicksight-project-analytics.pdf](https://github.com/user-attachments/files/16241634/amazon-quicksight-project-analytics.pdf)

## The Finished Dashboard

![stockton-pd-dashboard](https://github.com/user-attachments/assets/196aefba-fb8d-4f1b-ba6e-ad85433e918a)

## The conclusions that we can draw from what is presented is the following:
- 654,888 from 2023 - June 2024 and counting
- Bear Creek and SJC are the two districts with the least amount of police presence
- Top Three reasons for police calls are 911 hangups, ambulance requests, and disturbing the peace
- Year over Year SJC and Bear Creek have kept a low police call count


