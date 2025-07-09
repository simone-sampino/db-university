# Group by:

# 1. Contare quanti iscritti ci sono stati ogni anno

```sql
SELECT COUNT(*) AS `enrolled_students`, YEAR(`enrolment_date`) AS `year`
FROM `students`
GROUP BY `year`;
```

# 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```sql
SELECT COUNT(*) AS `teachers`, `office_address` AS `building`
FROM `teachers`
GROUP BY `building`;
```

# 3. Calcolare la media dei voti di ogni appello d'esame

```sql
SELECT FLOOR(AVG(`vote`)) AS `grade_point_average`, `exam_id` AS `exam`
FROM `exam_student`
GROUP BY `exam`;
```

# 4. Contare quanti corsi di laurea ci sono per ogni dipartimento

```sql
SELECT COUNT(*) AS `degrees`, `department_id` AS `department`
FROM `degrees`
GROUP BY `department`;
```
