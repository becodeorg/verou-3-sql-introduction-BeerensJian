# verou-3-sql-introduction-BeerensJian

## Get all data from the groups
```
- SELECT * FROM groups
```
## Get the name and email of the first learner, and alias the name to learner_name
```
SELECT name AS learner_name,email
FROM learners
WHERE id=1
```
## Update the start date of the first_group (make it two months later)
```
UPDATE groups
SET `start_date` = DATE_ADD(`start_date`, INTERVAL 60 DAY)
WHERE id = 1
```
## Delete a user from the learners since he decided to become an astronaut instead
```
DELETE FROM learners WHERE name="Jordy"
```
## Select a coach and all related groups
```
select * from coaches
INNER JOIN groups ON coaches.id = groups.coach_id
WHERE coaches.id = "1"
```
## Select all the above, but also all learners from this group who are still active
```
select * from coaches
INNER JOIN groups ON coaches.id = groups.coach_id
LEFT JOIN learners ON learners.group_id = groups.id AND learners.active="1"
WHERE coaches.id = "1"
```