# verou-3-sql-introduction-BeerensJian

## Get all data from the groups

- SELECT * FROM groups

## Get the name and email of the first learner, and alias the name to learner_name

```
SELECT name AS learner_name,email
FROM learners
WHERE id=1

```