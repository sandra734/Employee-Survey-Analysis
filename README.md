# Employee-Survey-Analysis
## Project Overview 
This project involves analyzing employee responses collected from government workers in Pierce County, WA. The objective is to assess employee sentiments, identify key concerns, and understand the factors influencing job satisfaction and workplace morale. By examining the survey data, the analysis aims to uncover patterns and insights that can inform county leadership on how to improve employee engagement, enhance workplace conditions, and foster a more positive organizational culture. The findings will contribute to making strategic decisions that support the well-being and productivity of government employees in Pierce County
## Data Sources
The data for this analysis is "Employee Survey.xlsx"[View here](https://docs.google.com/spreadsheets/d/1nbhfp2ModgqDAPveYQG9CknRw2PYJQxbOTs3xSKOB8E/edit#gid=61186505)
## Tools
- Excel for data cleaning and exploration
- Power BI for data visualization
## Data Cleaning and preparation 
- Handled missing data
- Removed duplicate values
- Standardized the data
## Exploratory Data analysis
The exploratory phase aimed to answer questions such as 
- Which survey questions did respondents agree with or disagree with most?
- Is there any patterns or trends by department or role?
## Data Analysis
### Data modeling 
Sub-tables were created to identify the staff, manager, supervisors and directors in the employee table.
![image](https://github.com/user-attachments/assets/83a17da7-c6da-4a65-93b9-26b36814a1df)

### Dax codes used in creating the tables 
``` DAX
   Manager Table = FILTER('Employee',Employee[Manager]=1)
   StaffTable = FILTER(Employee,Employee[Staff]=1)
    SupervisorTable = FILTER(Employee,Employee[Supervisor]=1)
  Director table = FILTER('Employee',Employee[Director]=1)
  Total Director = COALESCE(CALCULATE(COUNTA(Employee[Director]),FILTER(ALL(Employee[Director],Employee[Question]),Employee[Director]=1 && Employee[Question]="3. In the last seven days, I have received 
  recognition or praise for doing good work")),0)
```
## Results /Findings 
- The respondents expressed the strongest agreement(92.29%) with the statement "I know what is expected of me at work", while they showed the least agreement(41.56%) with the statement "I have a best friend at my place of employment."
- We observe that, across all roles, there is a significant level of disagreement with the statement "I have a best friend at work.
-Across all departments, except for the Sheriff's Department and the Clerk of Superior Courts, there is a notable level of disagreement with the statement "I have a best friend at work.
## Recommendations 
Based on the analysis, To enhance relationships among colleagues and boost overall employee satisfaction, employers should consider organizing team-building activities and social events, such as scavenger hunts and icebreaker games, to encourage bonding. Additionally, fostering open communication and regular feedback can create a supportive work environment. Implementing policies that promote work-life balance and reduce workplace stress is also essential. Providing digital collaboration tools can streamline communication, while recognizing and rewarding teamwork can further strengthen interpersonal connections. By prioritizing these strategies, employers can cultivate a positive workplace culture that leads to higher employee satisfaction and retention.


