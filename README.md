# School_District_Analysis

Overview of the School District Analysis
THe students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered and are being asked to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact

How is the district summary affected?

Before DATA CLEANUP
Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
79.0, 81.9, 75, 86, 65
After DATA CLEANUP
Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
78.9, 81.9, 74, 85, 64

Slight down change in district average

How is the school summary affected?

BEFORE CLEANUP: Thomas High School's % Overall Passing = 91, placing second
AFTER CLEANUP: % Overall Passing = 65, placing eight

Overall ranking order change due to THOMAS HS, which slipped from 2ND to 13TH position, with the other intervening schools moving up.

How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?


 The ranking for THOMAS HS changed from 2ND to 8TH, as it's % OVERALL PASSING number decreased from 91% to 65%.

How does replacing the ninth-grade scores affect the following?

Math and Reading Scores by Grade

Thomas HS 9th grade math & reading scores set to "nan" and equivalent to 0
Totals for passing math & reading across grades are reduced as all of 9th grade scores are equivalent to failing
Average scores calculation not significantly affected by removal of 9th grade scores, seems due to count() function NOT including 9th grade scores = nan
Cacluate number of students with a math grade - use "student_school_math.groupby(["school_name"]).count()""
Before cleanup: Thomas High School       1635
After cleanup: Thomas High School       1174
"%age passing" score is reduced as Total number of students (denominator) remains unchanged, but total passing value (numerator) is reduced by the number of removed 9th grade scores.

Scores by School Spending

Thomas HS is in the spending bucket "$630-644"
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for spending bucket "$630-644" as follows
Before: 73, 84, 63
After: 67, 77, 56

Scores by School Size

Thomas HS is in the "Medium (1000-2000)" size bucket
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for size bucket "Medium (1000-2000)" as follows
Before:94, 97, 91
After: 88, 91, 85


Scores by School Type

Thomas HS is in the "CHARTER" type bucket
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for type bucket "CHARTER" as follows
Before:94, 97, 90
After: 90	93	87
