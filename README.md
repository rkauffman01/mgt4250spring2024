# MGT4250 Spring 2024 Course Project: Alcohol Consumption Effect on Grades
Authors: Ryan Kauffman (rkauffman@elon.edu), Paul Walker (pwalker3@elon.edu), Grant Ardell (gardell@elon.edu)

## Project Description
This repository is a course project for MGT4250 at Elon University. Using data found on Kaggle, we set out to create a project in which we could use visualizations to explain and discuss its relevance in response to questions of interest. The goal of this project is to identify the factors that best indicate a tendency for a student to consume alcohol, and to determine how alcohol consumption affects academic efforts or success.

### Questions of interest
- What factors indicate a tendency for a student to consume alcohol?
- Does alcohol affect academic efforts or success?
  
### Importance

Alcohol can impair judgment, memory, and concentration, making it difficult for students to focus and learn effectively. Drinking alcohol at a young age can harm physical development and increase the risk of developing long-term health problems such as liver disease, heart disease, and certain cancers. Furthermore, excessive drinking can lead to risky behaviors such as violence, unprotected sex, and drunk driving, which can have serious consequences for students and others. What’s more, underage drinking is illegal in many places, and students who are caught drinking or possessing alcohol can face legal consequences such as fines, community service, or even juvenile detention. Finally, alcohol use among teenagers is often associated with an increased risk of mental health issues such as depression and anxiety.

Reference for above content: https://www.cdc.gov/alcohol/fact-sheets/alcohol-use.htm#:~:text=Long%2DTerm%20Health%20Risks,liver%20disease%2C%20and%20digestive%20problems.&text=Cancer%20of%20the%20breast%2C%20mouth,liver%2C%20colon%2C%20and%20rectum.

## Data Description
Kaggle Link: https://www.kaggle.com/datasets/uciml/student-alcohol-consumption

The dataset we have chosen was obtained in a survey of students’ math and Portuguese language courses in a secondary school. It can be accessed via the link above, and can be downloaded as a .zip file, which can be unzipped to reveal the student-mat.csv which is the dataset we used. It contains features regarding social, gender and academic information about students. The math dataset covers students from a math class, and has 345 rows spread across 33 columns. Some of our primary variables for observation were ‘G3’, which represents the students’ final grade in the class, ‘absences’, ‘Walc’ and ‘Dalc’, which represent weekend and weekday alcohol consumption, and ‘studytime’. Variables are in a variety of forms: strings, integers,  binary (y/n). There is a full data dictionary under the Kaggle dataset linked above.

The dataset contains numerous categories that could shed light on what causes student drinking as well as the affects of student alcohol consumption. The columns of data used in our visualizations include:

- Weekday alcohol consumption (Dalc), and weekend alcohol consumption (Walc), is a rating of 1-4, with 4 being the highest.
- Grades were not on a 100 point scale, but a 20 point scale. There were two mid-term grades, G1 and G2, and the final grade of G3 for each student.
- Absences are the number of times each student was not present in class.
- Failures are the number of times each student failed a class.

There are other columns of data for each student in the data set, however, they did not appear impactful in the level of weekday and weekend alcohol consumption and/or in analyzing how the level of drinking impacted the academic performance for the students.

## Interpreting Visualizations

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
In order to determine what demographical/behavioral factors are most associated with students' alcohol usage, we trained two more decision trees. This is the first, which was trained to find the variables best at predicting weekend alcohol consumption. Here, we see that 'goout', the variable that judges how much students go out with their friends, is the most significant predictor of how much alcohol they use. Alcohol is typically regarded as a social substance, which supports this notion. Age, too, proves to be a significant indicator, which also checks out, due to substance use trends among young adults especially around the age of 16.

### Decision tree (predictor variable: Weekday Alcohol Consumption)

![image](https://github.com/rkauffman01/mgt4250spring2024/assets/168774318/6e11d60b-49b7-4db8-9f67-b991710e02b4)

### Explanation:
The second decision tree was trained to find the variables best at predicting weekday alcohol consumption. 'Goout' is once again the most significant predictor of alcohol consumption. However, 'famrel', or family relationship level is also a significant predictor. This shifts our attention to nuclear family dynamics. It seems that that the better relationship a family has, the more likely a student would be to have a higher alcohol consumption. This might be tied to our understandind of alcohol as a social substance, one that is commonly used among people who are more extroverted. Or, the student might be more inclined to rate their family relationship level higher if their parents condone bad habits like drinking. 


### Discussion & Summary
### Article Summary
In an article written by Campus Drug Prediction, the effects of drug and alcohol consumption by students are discussed. According to the article, there are a number of ways in which students can be negatively impacted by excessive amounts of alcohol. First, drinking can have decrease one's ability to process information, sometimes long term. With excessive alcohol consumption, a student's brain can become dependent on the use of alcohol, causing them to spend less time studying and going to class, leading to absences, lower grades, and failed classes. 
https://www.campusdrugprevention.gov/views-from-the-field/data-show-alcohol-and-drug-use-hinder-academic-performance#:~:text=They%20are%20likely%20to%20commit,graduating%20are%20likely%20to%20decline.
### ChatGPT Queries
The first query to ChatGPT was: What factors indicate a tendency for a student to consume alcohol? The response was: 
Several factors can indicate a tendency for a student to consume alcohol. These may include:
Peer Influence: Students may be more likely to consume alcohol if their peers do so. Peer pressure can play a significant role in shaping behavior during adolescence and early adulthood.

Family Environment: The family environment, including parental attitudes toward alcohol and family history of alcohol use, can influence a student's likelihood of consuming alcohol. For example, students with parents who drink heavily or have permissive attitudes toward alcohol may be more inclined to do so themselves.

Social Environment: Social events and gatherings where alcohol is present can increase the likelihood of alcohol consumption among students, especially if these events are perceived as opportunities for socializing and having fun.
Stress and Coping Mechanisms: Students may turn to alcohol as a way to cope with stress, anxiety, or other negative emotions. High levels of stress from academic pressures, relationship issues, or other sources can increase the risk of alcohol use as a maladaptive coping mechanism.

Personality Traits: Certain personality traits, such as sensation-seeking or impulsivity, may predispose individuals to engage in risky behaviors like alcohol consumption.

Mental Health Issues: Students with underlying mental health conditions, such as depression or anxiety, may be more susceptible to alcohol use as a form of self-medication or as a means of escaping from their problems.

Accessibility and Availability: Easy access to alcohol, whether at home or through social networks, can increase the likelihood of consumption among students.
Cultural and Societal Factors: Cultural norms and societal attitudes toward alcohol can also influence student behavior. In some cultures, alcohol consumption may be more socially acceptable or even encouraged, which can impact individual attitudes and behaviors.

Advertising and Media Influence: Advertising and media portrayals of alcohol consumption can shape perceptions and attitudes toward drinking, particularly among young people.
Educational Programs and Prevention Efforts: Effective educational programs and prevention efforts aimed at raising awareness about the risks associated with alcohol use and promoting healthier alternatives can help reduce the likelihood of student alcohol consumption.

Understanding these factors can inform prevention and intervention strategies aimed at reducing alcohol-related harm among students.

The second query to ChatGPT was: Does alcohol affect academic efforts or success? The response was: 
Yes, alcohol can have a significant impact on academic efforts and success. Here are some ways in which alcohol consumption can affect academic performance:

Impaired Cognitive Functioning: Alcohol consumption can impair cognitive functioning, including memory, attention, and decision-making abilities. This can make it difficult for students to concentrate, retain information, and perform well on academic tasks such as studying, taking exams, or completing assignments.

Decreased Motivation and Productivity: Excessive alcohol use can lead to decreased motivation and productivity, making it harder for students to stay focused and engaged in their academic pursuits. This can result in procrastination, missed deadlines, and lower overall academic performance.

Poor Judgment and Risky Behaviors: Alcohol can impair judgment and increase the likelihood of engaging in risky behaviors, such as substance abuse, reckless driving, or unprotected sexual activity. These behaviors can have negative consequences that interfere with academic success, such as legal problems, health issues, or interpersonal conflicts.

Missed Classes and Poor Attendance: Students who consume alcohol excessively may be more likely to miss classes or have poor attendance due to hangovers, fatigue, or other alcohol-related issues. This can result in missed lectures, incomplete coursework, and a lack of participation, all of which can impact academic performance.

Negative Impact on Mental Health: Alcohol misuse is associated with an increased risk of mental health problems such as depression, anxiety, and stress. These mental health issues can interfere with a student's ability to focus, concentrate, and effectively manage academic responsibilities.

Long-Term Consequences: Chronic alcohol misuse can have long-term consequences on academic success, including academic probation, dismissal from school, or delayed graduation. These consequences can have a lasting impact on a student's educational and career prospects.

Overall, alcohol consumption can undermine academic efforts and success by impairing cognitive functioning, decreasing motivation and productivity, promoting risky behaviors, interfering with attendance and participation, exacerbating mental health issues, and leading to long-term consequences. Encouraging responsible alcohol use and providing support services for students struggling with alcohol-related issues can help mitigate these negative effects and promote academic success.


The visualizations for this project focused on what causes students to consume alcohol during the week and on the weekends and how the level of drinking affects their academic effort and performance. Numerous factors were examined in two decision trees finding reasons for weekend and weekday alcohol consumption. In both decision trees, the factor 'goout', which is a rating from 1-5, was the most influential factor in determining the level of alcohol consumption. Family relationship factors also were a helpful predictor, showing that a better relationship with one's family led to higher level of alcohol consumption. 
For academic effort, the visualizations above showed a clear trend of a higher level of alcohol consumption, during the week and weekend, led to a larger number of absences for the students. With more absences and higher level of drinking, the students had failed more classes. When examining the final grades for the students and their rating of alcohol consumption, the students with lower drinking levels had higher final grades in the classes. 
