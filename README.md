# MGT4250 Spring 2024 Course Project: Alcohol Consumption Effect on Grades
Authors: Ryan Kauffman (rkauffman@elon.edu), Paul Walker (pwalker3@elon.edu), Grant Ardell (gardell@elon.edu)

## Project Description
The goal of this project is to identify the factors that best indicate a tendency for a student to consume alcohol, and to determine how alcohol consumption affects academic efforts or success.
### Questions of interest
- What factors indicate a tendency for a student to consume alcohol?
- Does alcohol affect academic efforts or success?
  
### Importance

Alcohol can impair judgment, memory, and concentration, making it difficult for students to focus and learn effectively. Drinking alcohol at a young age can harm physical development and increase the risk of developing long-term health problems such as liver disease, heart disease, and certain cancers. Furthermore, excessive drinking can lead to risky behaviors such as violence, unprotected sex, and drunk driving, which can have serious consequences for students and others. What’s more, underage drinking is illegal in many places, and students who are caught drinking or possessing alcohol can face legal consequences such as fines, community service, or even juvenile detention. Finally, alcohol use among teenagers is often associated with an increased risk of mental health issues such as depression and anxiety.

## "Data Description"
The datasets we have chosen were obtained in a survey of students’ math and Portuguese language courses in a secondary school. It contains features regarding social, gender and academic information about students. The math dataset, which we used for the project, covers students from a math class, and has 345 rows spread across 33 columns. Some of our primary variables for observation were ‘G3’, which represents the students’ final grade in the class, ‘absences’, ‘Walc’ and ‘Dalc’, which represent weekend and weekday alcohol consumption, and ‘studytime’. There is a full data dictionary under the Kaggle dataset linked above.

The dataset contains numerous categories that could shed light on what causes student drinking as well as the affects of student alcohol consumption. The columns of data used in our visualizations include:

- Weekday alcohol consumption (Dalc), and weekend alcohol consumption (Walc), is a rating of 1-4, with 4 being the highest.
- Grades were not on a 100 point scale, but a 20 point scale. There were two mid-term grades, G1 and G2, and the final grade of G3 for each student.
- Absences are the number of times each student was not present in class.
- Failures are the number of times each student failed a class.

There are other columns of data for each student in the data set, however, they did not appear impactful in the level of weekday and weekend alcohol consumption and/or in analyzing how the level of drinking impacted the academic performance for the students.

## "Interpreting Visualizations"
### Tableau Public Link
URL: https://public.tableau.com/views/AlcoholConsumputionDashboard/Dashboard1?:language=en-US&publish=yes&:sid=&:display_count=n&:origin=viz_share_link

### JupyterNotebook Link (for decision tree code)
URL: http://localhost:8888/notebooks/Alcohol%20Consumption%20ML.ipynb

### Decision Tree (predictor variable: final grade)
![image](https://github.com/rkauffman01/mgt4250spring2024/assets/168774318/7921f8a1-77e6-49a1-b70e-50ec34b7f79f)
### Explanation: 

Because we had so many variables within this dataset, we decided to use a decision tree to help us determine variables that had the greatest impact on predicting the final grades of the students. We used our existing data set with the train_test_split import from sklearn in order to create our training data. We found that absences, failures, and weekend alcohol consumption were the 3 biggest predictor variables for determining final grade. However, failures and absences were the two most significant indicators of grade. Going forward, we will be investigating how much alcohol consumption is correlated with failures and absences. 

### Final Grades by Drinking Averages
![image](https://github.com/rkauffman01/mgt4250spring2024/assets/168774318/072e4f59-be7e-44cb-9d40-c811c94e5671)
### Explanation: 
This visualization investigates the final grades of the courses and compares those grades with the amount of drinking each student partakes in. The results show a direct correlation between better grades and less alcohol consumption. This is a clear indicator that alcohol consumption can inhibit academic ability.

### Final Grades by Absences and Failures
![image](https://github.com/rkauffman01/mgt4250spring2024/assets/168774318/5b516f98-8b0c-42e6-a355-60264cd66755)
### Explanation:
This visualization is a histogram that shows the final grades, G3, in bins of 2. Included in the detail for each bin, is the average number of absences and failures for the students included in that bin. As can be seen in the visualization, the average failures and absences decreases as the final grade increases. This can be interpreted as a clear indication that more failures and absences leads to worse grades.

### Absences and Alcohol
![image](https://github.com/rkauffman01/mgt4250spring2024/assets/168774318/8371a498-2583-4e70-a55e-e0e79a80c493)
### Explanation:
This visualization looks at the level of weekend and weekday alcohol consumption and the number of absences for each student. While the relationship is not an exact linear correlation, as some people still go to class and consume alcohol, the trendline shows a clear positive linear relationship overall. This trendline slope indicates that the higher level of alcohol consumption tends to lead to more class absences from students.

### Failures and Alcohol
![image](https://github.com/rkauffman01/mgt4250spring2024/assets/168774318/c89b8ffa-dc05-4b11-a210-7f9c510c5d5e)
### Explanation:
This visualization examines the relationship between alcohol consumption and number of failures. The maximum number of failures a student could have was 3, and there is a clear correlation that shows the higher number of absences has a higher level of alcohol consumption. Going back to the original question: How does alcohol consumption affect academic effort/performance? This visualization clearly indicates that a causation of receiving a failing grade in a class can be linked to higher levels of alcohol consumption. 

## What factors are correlated with students drinking?
So, we have some definitive evidence that alcohol consumption is causing absences and failures, which in turn, is keeping students from performing well academically. But what are the factors that are most associated with their alcohol usage?
### Decision tree (predictor variable: Weekend Alcohol Consumption)

![image](https://github.com/rkauffman01/mgt4250spring2024/assets/168774318/ddded9c0-c996-4773-971c-532635d0bc8a)

### Explanation:
Here, we see that 'goout', the variable that judges how much students go out with their friends, is the most significant predictor of how much alcohol they use. Alcohol is typically regarded as a social substance, which supports this notion. 
Age, too, proves to be a significant indicator, which also checks out, due to substance use trends among young adults especially around the age of 16.

### Decision tree (predictor variable: Weekday Alcohol Consumption)

![image](https://github.com/rkauffman01/mgt4250spring2024/assets/168774318/6e11d60b-49b7-4db8-9f67-b991710e02b4)

### Explanation:
'Goout' is once again the most significant predictor of alcohol consumption. However, 'famrel', or family relationship level is also a significant predictor. This shifts our attention to nuclear family dynamics. It seems that that the better relationship a family has, the more likely a student would be to have a higher alcohol consumption. This might be tied to our understandind of alcohol as a social substance, one that is commonly used among people who are more extroverted. Or, the student might be more inclined to rate their family relationship level higher if their parents condone bad habits like drinking. 


### "Discussion & Summary"
age and culture of being social with friends leads to drinking blah blah blah and parents can also condone drinking which can be harmful blah blah blah
something something conclusion.
