# Seeds
- [schools](#schools)
- [students](#students)
- [classes](#classes)
- [class_students](#class_students)
- [class_teachers](#class_teachers)
- [administrators](#administrators)
- [coordinators](#coordinators)
- [monitors](#monitors)
- [accounts](#accounts)
- [activities](#activities)
- [lesson_plans](#lesson_plans)
- [lessons](#lessons)

## schools
```sql
INSERT INTO mydb.schools (`name`, `cnpj`, `address`, `email`, `phone`, `account_id`) VALUES
('Escola do Saber', '12.345.678/0001-90', 'Rua das Flores, 123, Fortaleza, CE', 'contato@saber.com.br', '+55 (85) 3211-4321', 1),
('Colégio Aprender', '98.765.432/0002-10', 'Av. Central, 456, São Paulo, SP', 'info@aprender.com.br', '+55 (11) 4002-8922', 1),
('Instituto Conhecer', '56.789.012/0003-00', 'Rua Horizonte, 789, Rio de Janeiro, RJ', 'suporte@conhecer.org', '+55 (21) 3303-7788', 1),
('Centro Educacional Futuro', '34.567.890/0004-12', 'Av. Brasil, 1010, Belo Horizonte, MG', 'admin@futuro.edu.br', '+55 (31) 3500-9191', 1),
('Escola Crescer', '23.456.789/0005-01', 'Rua da Alegria, 2020, Salvador, BA', 'crescer@escola.com.br', '+55 (71) 3030-5050', 1);
```
```sql
SELECT id, name, cnpj, address, email, phone, image_url, created_at, updated_at
FROM mydb.schools;
```

## students
```sql
INSERT INTO mydb.students (`name`, `email`, `enrollment`, `school_id`) VALUES
('Alice Silva', 'alice.silva@email.com', '20240001', 1),
('Bob Santos', 'bob.santos@email.com', '20240002', 1),
('Carlos Oliveira', 'carlos.oliveira@email.com', '20240003', 1),
('Daniele Costa', 'daniele.costa@email.com', '20240004', 1),
('Elena Pereira', 'elena.pereira@email.com', '20240005', 1),
('Felipe Souza', 'felipe.souza@email.com', '20240006', 1),
('Gabriela Rocha', 'gabriela.rocha@email.com', '20240007', 1),
('Helena Martins', 'helena.martins@email.com', '20240008', 1),
('Igor Almeida', 'igor.almeida@email.com', '20240009', 1),
('Juliana Ferreira', 'juliana.ferreira@email.com', '20240010', 1),
('Kleber Mendes', 'kleber.mendes@email.com', '20240011', 1),
('Luana Lima', 'luana.lima@email.com', '20240012', 1),
('Marcelo Pinto', 'marcelo.pinto@email.com', '20240013', 1),
('Nathalia Carvalho', 'nathalia.carvalho@email.com', '20240014', 1),
('Otávio Silva', 'otavio.silva@email.com', '20240015', 1),
('Priscila Santos', 'priscila.santos@email.com', '20240016', 1),
('Ricardo Pereira', 'ricardo.pereira@email.com', '20240017', 1),
('Sabrina Almeida', 'sabrina.almeida@email.com', '20240018', 1),
('Tiago Costa', 'tiago.costa@email.com', '20240019', 1),
('Ulisses Oliveira', 'ulisses.oliveira@email.com', '20240020', 1),
('Valentina Rocha', 'valentina.rocha@email.com', '20240021', 1),
('Wesley Souza', 'wesley.souza@email.com', '20240022', 1),
('Ximena Martins', 'ximena.martins@email.com', '20240023', 1),
('Yago Pinto', 'yago.pinto@email.com', '20240024', 1),
('Zilda Ferreira', 'zilda.ferreira@email.com', '20240025', 1),
('André Lima', 'andre.lima@email.com', '20240026', 1),
('Bianca Mendes', 'bianca.mendes@email.com', '20240027', 1),
('Carlos Rocha', 'carlos.rocha@email.com', '20240028', 1),
('Diana Almeida', 'diana.almeida@email.com', '20240029', 1),
('Eduardo Costa', 'eduardo.costa@email.com', '20240030', 1);


INSERT INTO mydb.students (`name`, `email`, `enrollment`, `school_id`) VALUES
('Ana Costa', 'ana.costa@email.com', '20240031', 2),
('Bruno Silva', 'bruno.silva@email.com', '20240032', 2),
('Carla Oliveira', 'carla.oliveira@email.com', '20240033', 2),
('Daniela Rocha', 'daniela.rocha@email.com', '20240034', 2),
('Eduardo Pereira', 'eduardo.pereira@email.com', '20240035', 2),
('Fernanda Almeida', 'fernanda.almeida@email.com', '20240036', 2),
('Gustavo Souza', 'gustavo.souza@email.com', '20240037', 2),
('Heloísa Lima', 'heloisa.lima@email.com', '20240038', 2),
('Igor Mendes', 'igor.mendes@email.com', '20240039', 2),
('Júlia Pinto', 'julia.pinto@email.com', '20240040', 2),
('Karla Martins', 'karla.martins@email.com', '20240041', 2),
('Leandro Ferreira', 'leandro.ferreira@email.com', '20240042', 2),
('Mariana Silva', 'mariana.silva@email.com', '20240043', 2),
('Nicolas Costa', 'nicolas.costa@email.com', '20240044', 2),
('Olga Rocha', 'olga.rocha@email.com', '20240045', 2),
('Patrícia Almeida', 'patricia.almeida@email.com', '20240046', 2),
('Quirino Oliveira', 'quirino.oliveira@email.com', '20240047', 2),
('Roberta Lima', 'roberta.lima@email.com', '20240048', 2),
('Samuel Pinto', 'samuel.pinto@email.com', '20240049', 2),
('Tatiane Mendes', 'tatiane.mendes@email.com', '20240050', 2),
('Uanderson Souza', 'uanderson.souza@email.com', '20240051', 2),
('Verônica Costa', 'veronica.costa@email.com', '20240052', 2),
('Walter Silva', 'walter.silva@email.com', '20240053', 2),
('Xandra Pereira', 'xandra.pereira@email.com', '20240054', 2),
('Yasmin Rocha', 'yasmin.rocha@email.com', '20240055', 2),
('Zezé Almeida', 'zeze.almeida@email.com', '20240056', 2),
('Amanda Pinto', 'amanda.pinto@email.com', '20240057', 2),
('Breno Martins', 'breno.martins@email.com', '20240058', 2),
('Cláudia Souza', 'claudia.souza@email.com', '20240059', 2),
('Débora Ferreira', 'debora.ferreira@email.com', '20240060', 2);
```
```sql
SELECT id, name, email, enrollment, has_account, created_at, updated_at, account_id, school_id
FROM mydb.students;
```

## classes
```sql
INSERT INTO mydb.classes (`name`, `shift`, `academic_year`, `account_id`, `school_id`) VALUES
('1º Ano A', 'MORNING', '2025.1', 1, 1),
('1º Ano B', 'AFTERNOON', '2025.1', 1, 1),
('2º Ano A', 'MORNING', '2024.2', 1, 2),
('2º Ano B', 'EVENING', '2024.2', 1, 2),
('3º Ano A', 'AFTERNOON', '2025.1', 1, 3),
('3º Ano B', 'MORNING', '2025.1', 1, 3),
('4º Ano A', 'EVENING', '2024.2', 1, 4),
('4º Ano B', 'MORNING', '2024.2', 1, 4),
('5º Ano A', 'AFTERNOON', '2025.1', 1, 5),
('5º Ano B', 'EVENING', '2025.1', 1, 5);
```
```sql
SELECT id, name, shift, academic_year, created_at, updated_at, school_id
FROM mydb.classes;
```

## class_students
```sql
INSERT INTO mydb.class_students (student_id, class_id) VALUES (1, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (2, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (3, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (4, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (5, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (6, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (7, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (8, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (9, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (10, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (11, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (12, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (13, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (14, 1);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (15, 1);

INSERT INTO mydb.class_students (student_id, class_id) VALUES (16, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (17, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (18, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (19, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (20, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (21, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (22, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (23, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (24, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (25, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (26, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (27, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (28, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (29, 2);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (30, 2);

INSERT INTO mydb.class_students (student_id, class_id) VALUES (31, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (32, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (33, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (34, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (35, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (36, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (37, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (38, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (39, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (40, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (41, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (42, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (43, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (44, 3);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (45, 3);

INSERT INTO mydb.class_students (student_id, class_id) VALUES (46, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (47, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (48, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (49, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (50, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (51, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (52, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (53, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (54, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (55, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (56, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (57, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (58, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (59, 4);
INSERT INTO mydb.class_students (student_id, class_id) VALUES (60, 4);
```
```sql
SELECT id, created_at, updated_at, student_id, class_id
FROM mydb.class_students;
```
```sql
SELECT
	student_id,
	student.name AS student_name,
	school.name AS school_name,
	class.name AS class_name
FROM mydb.class_students cs
INNER JOIN mydb.classes class ON cs.class_id = class.id
INNER JOIN mydb.students student ON cs.student_id = student.id
INNER JOIN mydb.schools school ON school.id = student.school_id;
```

## class_teachers
```sql
INSERT INTO mydb.class_teachers (account_id, class_id) VALUES (2, 1);
```
```sql
SELECT id, created_at, updated_at, account_id, class_id
FROM mydb.class_teachers;
```

## administrators
```sql
INSERT INTO mydb.administrators (`name`, `email`)
VALUES ('Alexandre Pereira', 'alexandre.pereira@email.com');
```
```sql
SELECT id, name, email, has_account, created_at, updated_at, account_id
FROM mydb.administrators;
```

## coordinators
```sql
INSERT INTO mydb.coordinators (`name`, `email`)
VALUES ('Lucas Andrade', 'lucas.andrade@email.com');
```
```sql
SELECT id, name, email, has_account, created_at, updated_at, account_id
FROM mydb.administrators;
```

## monitors
```sql
INSERT INTO mydb.monitors (`name`, `email`)
VALUES ('Ana Carolina Souza', 'ana.carolina.souza@email.com');
```
```sql
SELECT id, name, email, has_account, created_at, updated_at, account_id
FROM mydb.monitors;
```

## accounts
```sql
INSERT INTO mydb.accounts (`email`, `password`, `image_url`, `role`)
VALUES ('alexandre.pereira@email.com', 'alexandre123', 'https://ui-avatars.com/api/?name=alexandre.pereira&background=random', 'ADMINISTRATOR');

INSERT INTO mydb.accounts (`email`, `password`, `image_url`, `role`)
VALUES ('lucas.andrade@email.com', 'lucas123', 'https://ui-avatars.com/api/?name=lucas.andrade&background=random', 'COORDINATOR');

INSERT INTO mydb.accounts (`email`, `password`, `image_url`, `role`)
VALUES ('gabriel.lima@email.com', 'gabriel123', 'https://ui-avatars.com/api/?name=gabriel.lima&background=random', 'SCHOLARSHIP');

INSERT INTO mydb.accounts (`email`, `password`, `image_url`, `role`)
VALUES ('ana.carolina.souza@email.com', 'ana123', 'https://ui-avatars.com/api/?name=ana.carolina.souza&background=random', 'MONITOR');
```
```sql
SELECT id, email, password, image_url, status, `role`, created_at, updated_at, role_id
FROM mydb.accounts;
```

## activities
```sql
INSERT INTO mydb.activities
(`title`, `description`, `max_score`, `due_date`, `account_id`, `class_id`) VALUES
(
  'Introdução ao Git e GitHub',
  'Crie um repositório no GitHub e configure um README.md com as informações sobre seu projeto. Inclua no repositório pelo menos 3 commits bem descritos.',
  10,
  '2025-01-15',
  2,
  1
);
```
```sql
SELECT id, title, description, max_score, due_date, created_at, updated_at, account_id, class_id
FROM mydb.activities;
```

## lesson_plans
```sql
INSERT INTO mydb.lesson_plans
(`title`, `description`, `objectives`, `materials`, `account_id`)
VALUES
(
  'Introdução ao Git e GitHub',
  'Neste plano de aula, os alunos aprenderão como criar um repositório no GitHub, configurar um README.md e realizar commits em um projeto.',
  '1. Criar um repositório no GitHub\n2. Configurar um README.md\n3. Realizar pelo menos 3 commits descritivos\n4. Subir o código para o GitHub',
  'Computadores com acesso à internet, Git instalado, conta no GitHub',
  2
);
```
```sql
SELECT id, title, description, objectives, materials, created_at, updated_at
FROM mydb.lesson_plans;
```

## lessons
```sql
INSERT INTO mydb.lessons
(`title`, `description`, `date`, `lesson_plan_id`, `class_id`, `account_id`)
VALUES
(
  'Git Básico: Criando um Repositório',
  'Nesta lição, os alunos aprenderão como criar um repositório no GitHub, fazer o commit inicial e entender o fluxo básico do Git.',
  '2025-01-20 10:00:00',
  1,
  1,
  2
);
```
```sql
SELECT id, title, description, `date`, created_at, updated_at, lesson_plan_id, class_id
FROM mydb.lessons;
```
