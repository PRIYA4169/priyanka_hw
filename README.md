count how many student passes the exam.

select
count (result_status)
from
day_2_exam
where result_status = 'Pass'
