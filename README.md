Greenfield School Results Project

Name: Vivian Saye
Date: 30th of October 2026


1. About this project

I worked as the data assistant for Greenfield Secondary School. The school has 240 students in 6 classes (JSS1A, JSS1B, JSS2A, JSS2B, JSS3A, JSS3B). The data was typed by different teachers and was messy, so I cleaned it, used formulas to answer the principal’s 4 questions, and built a one-page summary.

The principal’s questions were:

Which class is doing best, and which needs the most help?
Which subject is the hardest?
Are students improving from First Term to Third Term?
Which students need extra support?

2. Sheets in this workbook
Sheet	What it contains
Results	The original data, untouched
Clean Data	The cleaned copy, with Total, Average, Grade and Class Rank (formulas)
Cleaning Report	What was wrong, how many, and how I fixed it
Class Summary	Number of students, average score and pass rate for each class and term
Subjects	Average score of each subject (all terms and each term)
Improvement	Each student’s First and Third Term average, the change, and Improved or Dropped
At Risk	Students with a Third Term average below 50 (red conditional formatting)
Summary	Five key numbers, three charts and my message to the principal

3. How I cleaned the data

I cleaned first, and removed duplicates last.

Class names: 30 spellings reduced to 6, using UPPER(SUBSTITUTE(...)).
Gender: changed to only Male or Female.
Names: fixed extra spaces and capital letters with PROPER(TRIM(...)).
Text scores: 30 scores changed to numbers with VALUE(TRIM(...)).
Scores above 100: 3 scores fixed by removing the extra zero (for example 680 became 68).
Blank scores: 12 left blank (not changed to 0).
Duplicates: 6 removed (Student ID + Term).

After cleaning: 720 rows, 240 students, 6 classes.

4. Main formulas used
Task	Formula
Total	SUM
Average	AVERAGE (not rounded, only formatted to 1 decimal place)
Grade	IFS
Class Rank	SUMPRODUCT (count students with a higher average, then add 1)
Class Summary	COUNTIFS and AVERAGEIFS
Improvement	AVERAGEIFS by Student ID and Term, then Third minus First
Top 5 improved	LARGE, INDEX and MATCH
At Risk count	COUNTIFS

5. Key findings
Best class (Third Term): JSS3B, with an average of 66.7.
Class needing most help: JSS3A, with the lowest Third Term average (62.7) and pass rate (80%).
Hardest subject: Maths (average 55.4). Easiest: Civic Education (67.3).
Third Term pass rate: 86.7%.
Improved from First to Third Term: 169 students (71 dropped).
Students below 50 in Third Term: 32.

6. Message to the principal

Dear Principal, JSS3A needs the most help, because it has the lowest Third Term average (62.7) and the lowest pass rate (80%). The school should focus on Maths, which is the hardest subject in every term, with an average of 55.4. In total, 32 students scored below 50 in the Third Term and need extra support. Before making a big decision, I would like to know whether the blank scores mean the students were absent or dropped the subject.


7. Notes and limits
Blank scores were skipped, not treated as 0, so a student’s average only uses the subjects they wrote.
The data cannot show why a score is blank (absence or a dropped subject), so I recommend finding this out before making big decisions.
If a formula shows an error, check that the Clean Data sheet is fully cleaned.
