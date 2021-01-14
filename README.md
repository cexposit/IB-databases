# IB-databases

# Create table with primary key:

## SQL Script

```CREATE TABLE students ( 
  id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY, 
  firstname VARCHAR(30) NOT NULL, 
  lastname VARCHAR(30) NOT NULL,  
  email VARCHAR(50), 
  reg_date TIMESTAMP 
); 

INSERT INTO `students` (`firstname`, `lastname`, `email`, `reg_date`) VALUES ('lucas', 'izquierdo', 'lucas.izquierdo@gmail.com', CURRENT_TIMESTAMP); 
INSERT INTO `students` (`firstname`, `lastname`, `email`, `reg_date`) VALUES ('andrea', 'arencibia', 'andrea.arencibia@hotmail.com', CURRENT_TIMESTAMP);
INSERT INTO `students` (`firstname`, `lastname`, `email`, `reg_date`) VALUES ('lucia', 'chinea', 'lucia.chinea@gmail.com', CURRENT_TIMESTAMP);
INSERT INTO `students` (`firstname`, `lastname`, `email`, `reg_date`) VALUES ('diego', 'moreno', 'diego.moreno@gmail.com', CURRENT_TIMESTAMP);
INSERT INTO `students` (`firstname`, `lastname`, `email`, `reg_date`) VALUES ('julia', 'lorenzo', 'julia.lorenzo@gmail.com', CURRENT_TIMESTAMP);
```

## SQL Query
1. `SELECT * FROM students;`
1. `SELECT firstname, lastname FROM students;`

# Create two tables with foreign key:

## SQL Script

```
CREATE TABLE institutions (
  name VARCHAR(30) NOT NULL,
  foundation YEAR NOT NULL,
  PRIMARY KEY (name)
);

CREATE TABLE students ( 
  id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY, 
  firstname VARCHAR(30) NOT NULL, 
  lastname VARCHAR(30) NOT NULL,  
  email VARCHAR(50),
  reg_date TIMESTAMP, 
  affiliation VARCHAR(50),
  FOREIGN KEY (affiliation) REFERENCES institutions(name)
); 

INSERT INTO `institutions` (`name`, `foundation`) VALUES ('ull', 1927); 
INSERT INTO `institutions` (`name`, `foundation`) VALUES ('ulpgc', 1989); 

INSERT INTO `students` (`firstname`, `lastname`, `email`, `affiliation`, `reg_date`) VALUES ('lucas', 'izquierdo', 'lucas.izquierdo@gmail.com', 'ull', CURRENT_TIMESTAMP); 
INSERT INTO `students` (`firstname`, `lastname`, `email`, `affiliation`, `reg_date`) VALUES ('andrea', 'arencibia', 'andrea.arencibia@hotmail.com', 'ulpgc', CURRENT_TIMESTAMP);
```

## SQL Query
```
SELECT * FROM institutions;
```
```
SELECT * FROM students;
```
