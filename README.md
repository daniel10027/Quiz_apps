## [Proposition de la base de donnée d'une application de quiz](https://github.com)

### Nombre de table : 8

### Identification des tables :

### users

- [x] id primary key autoincrement 
- [x] nom varchar
- [x] prenom varchar
- [x] email varchar
- [x] password varchar

### niveau

- [x] id primary key autoincrement
- [x] nom varchar
- [x] recompense varchar

### theme
- [x] id primary key autoincrement 
- [x] nom varchar

### question
- [x] id primary key autoincrement 
- [x] id_theme foreign key references theme(id)
- [x] id_solution foreign key references solution(id)
- [x] description varchar

### solution

- [x] id primary key autoincrement 
- [x] nom varchar
- [x] id_question foreign key references question(id)
- [x] valeur varchar



### quiz_question
- [x] id primary key autoincrement 
- [x] id_quiz foreign key references quiz(id)
- [x] id_question foreign key references question(id)

### quiz_valide
- [x] id primary key autoincrement 
- [x] id_quiz foreign key references quiz(id)
- [x] id_user foreign key references user(id)
- [x] date_validation date

### quiz
- [x] id primary key autoincrement 
- [x] id_quiz foreign key references quiz(id)
- [x] id_question foreign key references question(id)
- [x] id_user foreign key references user(id)

![alt text](https:github.com/daniel10027/Quiz_apps/img.png)







