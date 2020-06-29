# School_District_Analysis
jupyter notebook

The module 4 took around 16 hours to go step by step through the breakdown of the School district data. Throughout the entire analysis, there were multiple data points broken down which helped the analyst see the potential harm the 9th graders at Thomas High School delivered to their alma mater. I provided both sets of code, the first being the PyCitySChools.ipnyb which was completed during the 16 hours of the module and I also provide the PyCitySchools_Challenge which includes the erasing, or replacing of the 9th grader's math and reading scores due to suspicion of academic dishonesty with NAN. I compared and contrast both codes, as one being the benchmark with all the data from the entire schools, grades, districts, monies spent etc to help arrive to the below answers. The one key piece of code in the _Challenge ipnyb is the additiion of the below code which replaced the 9th graders math and reading scores at Thomas High:

student_data_df.loc[(student_data_df['grade'] =='9th') & (student_data_df['school_name'] =='Thomas High School') & (student_data_df['math_score'] >0), ['math_score']] = np.nan
                                                                                                                       
student_data_df

Analysis:
The School District Analysis requested we replace the reading and math scores for 9th graders at the Thomas High School with "NAN" due to irregularities with their grades which is under the suspicion that academic dishonesty is in play. After changing the 9th grader's scores, we are prompted to answer a few questions in order to see the material changes due to the NAN of reading and math scores for 9th graders at the Thomas High School.

How is the district summary affected?
After updating the 9th grade NAN update: The passing math % dropped from 75% to 74%; the passing reading % dropped from 86% to 85% and the overall passing % dropped from 65% to 64%.

How is the school summmary affected?
After updating the 9th grade NAN update: The passing math % dropped from 93.27% 66.91%; the passing reading score dropped from 97.30% to 69.66% resulting in an overall passing % drop from 90.94% to 65.07%.This update/change places this medium school size school, Thomas High School, which was near the top of its peers is now in the bottom of its Medium size peers.

How does changing the reading and math scores for 9th graders at the Thomas High School affect their performance, relative to the other schools?
Before dropping the 9th grade reading and math, Thomas High School was the #2 overall performing school, below Cabrera High School and above Griffin High School. Unfortunately, after the 9th grade reading and math drop, Thomas High School fell to the middle of the pack; just below Holden High School. Furthermore, it dropped to the bottom of all Charter Schools. 

Now that we changed the reading and math scores for 9th graders at the Thomas High School, I can answer the bottom 4 key questions:
 1) After replacing the ninth grade math and reading scores with Nan, Thomas High School went from a Passing Math %  of 93.27% down to NaN and an average of 83.72% reading score to NAN.
 2) Scores by School Spending dropped in the $630 - $644 range from Passing Math % going from 73% down to 66.91% and Passing Reading %dropping from 84% down to 77% which          represents the largest drop among spending ranges per students.
 3) Scores by Schools Size: Thomas High School is in the Medium School size of (1000-2000) and the Passing Math for Medium School Size (1000 - 2000) dropped from 94% down to 88% and the Passing Reading for Medium School size (1000 - 2000) dropped from 97% down to 91%
 4) Concerning School Type: the District score's were unchanged but the Charter Schools, which Thomas High School is, experienced a passing math % drop of 94% to 90% and a drop in passing reading % drop from 97% to 93%.
 
  
