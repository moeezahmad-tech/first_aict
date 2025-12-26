drop table students;

create table students(
	id int identity(1,1) primary key,
	f_name varchar(20),
	l_name varchar(20),
	roll int unique,
	section varchar(1),
	age int,
	gpa float
)

INSERT INTO students (f_name, l_name, roll, section, age, gpa) VALUES
('John',   'Smith',   101, 'A', 20, 3.45),
('Emma',   'Brown',   102, 'A', 19, 3.80),
('Liam',   'Johnson', 103, 'A', 14, 3.10),
('Olivia', 'Davis',   104, 'A', 20, 3.65),
('Noah',   'Wilson',  105, 'A', 22, 2.95),
('Ava',    'Taylor',  106, 'B', 19, 3.90),
('Mason',  'Anderson',107, 'B', 15, 3.25),
('Sophia', 'Thomas',  108, 'B', 20, 3.70),
('Ethan',  'Moore',   109, 'B', 22, 2.85),
('Isabella','Martin', 110, 'B', 13, 3.55);

select * from students;

select f_name , l_name , section from students; 

select id , roll from students where age >= 18;

select f_name, section , l_name from students;

select f_name from students where age > 18 and gpa > 3;

select avg(gpa) from students; 

select roll from students where gpa > (select avg(gpa) from students);