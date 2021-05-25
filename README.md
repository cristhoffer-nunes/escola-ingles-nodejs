### About

API for a system of students and classes for an English school using a diagram.

### Database diagram

![database](https://github.com/cristhoffer-nunes/escola-ingles-nodejs/blob/main/img/diagram.jpg)

### Diagram description

Database diagram consisting of four tables: Pessoas, Níveis, Turmas e Matrículas. <br><br>

**The Pessoas table is composed of the columns:**
* ID: dado do tipo inteiro
* nome: dado do tipo string
* ativo: dado do tipo boolean
* email: dado do tipo string
* role: dado do tipo string

**The Niveis table is composed of the columns:**
* ID: dado do tipo inteiro
* descr_nivel: dado do tipo string

**The Turmas table is composed of the columns:**
* ID: dado do tipo inteiro
* docente_id: dado do tipo ID/inteiro
* data_inicio: dado do tipo dateonly
* nivel_id: dado do tipo ID/inteiro




### Pessoas - Routes

Person table routes

* **estudanteId** refers to the **estudante_id** column of the **Matriculas** table.
* **matriculaId** refers to the **id** column of **Matriculas** table.

| Method  |  Route  | Description |
| ------------------- | ------------------- | ------------------- |
|  GET |  /pessoas |  get all people  | 
|  GET |  /pessoas/ativas |  get active people  | 
|  GET |  /pessoas/:id |  get person by id  | 
|  GET |  /pessoas/:estudanteId/matricula |  get enrollment  | 
|  GET |  /pessoas/:estudanteId/matricula/:matriculaId |  get a registration by id  | 
|  GET |  /pessoas/matricula/:turmaId/confirmadas |  get class registration  | 
|  GET |  /pessoas/matricula/lotada |  get crowded classes  | 
|  POST |  /pessoas |  create person  | 
|  POST |  /pessoas/:id/restaura |  restore person by id  | 
|  POST |  /pessoas/:estudanteId/cancela |  cancel person  | 
|  POST |  /pessoas/:estudanteId/matricula |  create registration  | 
|  POST |  /pessoas/:estudanteId/matricula/:matriculaId/restaura |  restore registration  | 
|  PUT |  /pessoas/:id |  update person  | 
|  PUT |  /pessoas/:estudanteId/matricula/:matriculaId |  update registration  | 
|  DELETE |  /pessoas/:id |  delete person  | 
|  DELETE |  /pessoas/:estudanteId/matricula/:matriculaId |  delete registration  | 
