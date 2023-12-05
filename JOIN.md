1. *Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia*
    - SELECT `degrees`.`id` AS 'degree', `students`.`name` ,`students`.`degree_id`, `students`.`id`
    - FROM `degrees`
    - INNER JOIN `students`
    - ON `degrees`.`id` = `students`.`degree_id`
    - WHERE `degrees`.`id`= 56;
2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze
    - SELECT `degrees`.`id` AS 'degree', `departments`.`id`AS 'department', `degrees`.`name` AS 'degree_name', `departments`.`name`AS 'department_name' 
    - FROM `degrees` INNER JOIN `departments` ON `departments`.`id`= `degrees`.`department_id` 
    - WHERE department_id = 7 AND `degrees`.`level` = 'magistrale';
3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
    - SELECT `teacher_id` AS 'Fulvio_Amato_id', `courses`.`name`
    - FROM `course_teacher`
    - INNER JOIN `courses`
    - ON `course_teacher`.`course_id` = `courses`.`id`
    - WHERE `course_teacher`.`teacher_id`=44;
4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
nome
5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
6. Selezionare tutti i docenti che insegnano nel Dipartimento di
Matematica (54)
7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti
per ogni esame, stampando anche il voto massimo. Successivamente,
filtrare i tentativi con voto minimo 18.