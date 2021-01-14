# IB-databases

# Create table with primary key:

## SQL Script

```
CREATE TABLE students ( 
  id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY, 
  firstname VARCHAR(30) NOT NULL, 
  lastname VARCHAR(30) NOT NULL,  
  email VARCHAR(50), 
  reg_date TIMESTAMP 
); 

INSERT INTO `students` (`firstname`, `lastname`, `email`, `reg_date`) VALUES ('lucas', 'izquierdo', 'lucas.izquierdo@gmail.com', CURRENT_TIMESTAMP); 
INSERT INTO `students` (`firstname`, `lastname`, `email`, `reg_date`) VALUES ('andrea', 'arencibia', 'andrea.arencibia@hotmail.com', CURRENT_TIMESTAMP);
INSERT INTO `students` (`id`, `firstname`, `lastname`, `email`, `reg_date`) VALUES ('1', 'antonio', 'ruiz', 'antonio.ruiz@gmail.com', CURRENT_TIMESTAMP);
```

## SQL Query
```
SELECT * FROM students;
```
