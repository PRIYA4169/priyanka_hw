Q1: count how many student passes the ex
select
count (result_status)
from
day_2_exam
where result_status = 'Pass'

Q2: find the average score of all students who failed.
select
avg(total_score)
from
day_2_exam
where result_status = 'Fail

Q3: Get the highest score among all students.
select
 max (total_score) AS hightest_score
from
day_2_exam

Q4: Get the lowest score among passed students.
select
min (total_score) As lowest_score
from 
day_2_exam
where result_status = 'Pass'

Q5: Sum the total marks of all students who scored above 40.
select
SUM(total_score) As total_marks
from
day_2_exam
where total_score > 40

Q6: Count students by result status for those who scored 35 or more.
select
count(result_status)
from
day_2_exam
where total_score >=35

Q8: Get maximum and minimum scores grouped by result status for students who scored less than 35.
select
min(total_score),
max(total_score)
from
day_2_exam
where total_score<35

Q10: Sum total scores grouped by result status for students who scored exactly 35, 40, or 45.
select
result_status,
SUM(total_score) As total_marks
from
day_2_exam
where total_score IN (35,40,45)
group by result_status;

Q11: Count students by each score value, ordered by score descending.
select
total_score,
count(*) student_name
from 
day_1_exam
group by total_score
order by total_score desc

Q12: Show average score for each result status, ordered by average score.
select
result_status,
AVG(total_score)
from
day_2_exam
group by result_status
order by AVG(total_score)

Q13: Count how many students got each score, only for scores above 30, ordered by frequency.
select
total_score  
from
day_2_exam
where total_score > 30
order by total_score desc

Q14: Get total marks sum for each result status, ordered by sum.
select
result_status,
sum(total_score) As total_marks
from
day_2_exam
group by result_status
order by total_marks

Q15: Find minimum score for each result status, ordered by min score.
select
result_status,
min(total_score) As highest_score
from
day_2_exam
group by result_status
order by highest_score

Q16: For passed students only, show count, average, max and min scores grouped by whether score is above 40.
select
avg(total_score),
max(total_score),
min(total_score),
count(*) hall_ticket_no
where result_status = 'Pass'

Q17: Count and average score for each result status, only for scores not equal to 35.
select
result_status,
count(*) As student_name,
avg(total_score)
from
day_2_exam
where total_score <> 35
group by result_status 

Q19: For each result status, show count of students with scores greater than 30 and less than 4
select
result_status,
count(*) student_name
from
day_2_exam
where total_score > 30 and total_score < 40
group by result_status


