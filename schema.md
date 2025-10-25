
## Table: dipartimenti

- id BIGINT PK AI U
- name VARCHAR(50) NN
- description TEXT N

### Table: corsi_di_aurea

- id BIGINT PK AI U
- dipartimento_id FK
- name VARCHAR(50) NN
- level VARCHAR(15) NN

## Table: corsi

- id BIGINT PK AI U
- corso_di_laurea_id FK
- name VARCHAR(50) NN
- cfu TINYINT NN
- anno_di_corso TINYINT N

## Table: teachers

- id BIGINT PK AI U
- name VARCHAR(50) NN
- last_name VARCHAR(50) NN
- email VARCHAR(50) N U

## Table Pivot: corso_teacher

- corso_id FK
- teacher_id FK

## Table: appelli

- id BIGINT PK AI U
- corso_id FK
- teacher_id FK
- aula VARCHAR(20) NN
- data_appello DATE NN

## Table: studenti

- id BIGINT PK AI U
- corso_di_laurea_id FK
- name VARCHAR(50) NN
- last_name VARCHAR(50) NN
- email VARCHAR(50) NN U
- matricola VARCHAR(20) NN
- birth_date DATE NN

## Table Pivot: appello_studente

- appello_id FK
- studente_ id FK
- voto TINYINT NN
- lode CHAR(2) NN
- esito CHAR(8) NN
