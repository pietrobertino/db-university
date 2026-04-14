Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:
sono presenti diversi `Dipartimenti` (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più `Corsi di Laurea` (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi `Corsi` (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi `Insegnanti`;
ogni Corso prevede più `appelli d'Esame`;
ogni `Studente` è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il `voto ottenuto`, anche se non sufficiente.
Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

Utilizzare https://www.drawio.com/ per la creazione dello schema.
Esportare quindi il diagramma in png, caricarlo in un file html e pushare tutto nella repo.




# departments
- id 
- name 
- location


# degree_courses
- id 
- department_id (un dipartimento unico per corso di laurea)
- time_commitment
- name


# courses
- id 
- name
- semester

(Un corso può appartenere anche a più corsi di laurea)


# teachers
- id
- name
- surname
- email
- phone_number
- birthdate
- qualifications
- years_of_teaching

(Un insegnante può tenere più di un corso)



# exam-dates
- id
- course_id
- date



# students
- id
- degree_course_id (un solo corso di laurea per studente)
- name
- surname
- student_id_number
- email
- university_year



# grades
- id
- student_id (uno studente per ogni voto per ogni appello a cui ha partecipato)
- grade
- is_sufficient
