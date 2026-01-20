count how many student passes the ex
select
count (result_status)
from
day_2_exam
where result_status = 'Pass'

find the average score of all students who failed.
select
avg(total_score)
from
day_2_exam
where result_status = 'Fail

Get the highest score among all students.
select
 max (total_score) AS hightest_score
from
day_2_exam

Get the lowest score among passed students.
select
min (total_score) As lowest_score
from 
day_2_exam
where result_status = 'Pass'

Sum the total marks of all students who scored above 40.
select
SUM(total_score) As total_marks
from
day_2_exam
where total_score > 40
