<h1 align="center"> TURMA 05 - Preparação de HTML e CSS 💻 </h1>

<p align="center"> <a href="https://prozeducacao.com.br/" target="_blank">Proz</a> - Talento Cloud - <a href="https://aws.amazon.com/pt/" target="_blank">AWS</a> - <a href="https://www.nexaresources.com/" target="_blank">Nexa</a> </p>

<p align="center">
<a href="#sobre">Sobre</a>&nbsp;&nbsp;&nbsp|&nbsp;&nbsp;&nbsp;
<a href="#tecnologia">Tecnologia</a>&nbsp;&nbsp;&nbsp|&nbsp;&nbsp;&nbsp;
<a href="#autor">Autor</a>.</p>

# Sobre 

Aula pratica de Git e Github 😻: 


<p align="center">
  <figure>
<img src="https://github.com/Daniela2319/Aula_github/assets/106537496/9720039e-075f-4462-be61-dd7e7363f417" height="400" width="800">
  </figure>
  <br>
   <figcaption>Logotipo do <a href="https://github.com" target="_blank">Github</a></figcaption>
</p>


# Tecnologia 
Esse projeto foi desenvolvindo com as seguintes tecnologias:

* IDE VisualStudio Code
* Texto
* Git e Github



# Autor 
  
  _Daniela Velter_
  <br>
  <br>
  [![Linkedin](https://img.shields.io/badge/DANIELA-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniela-velter-231485f/)

```mermaid
classDiagram

class Post {
    + int id
    + string title
    + string content
    + string author
    + datetime publish_date
    + str __str__()
}

class Comment {
    + int id
    + Post post
    + string author
    + string content
    + datetime publish_date
    + str __str__()
}

class Blog {
    + list~Post~ home()
    + Post view_post(int post_id)
    + list~Post~ search_posts(string keyword)
}

class Admin {
    + bool login()
    + void manage_posts()
    + void manage_comments()
}

class User {
    + bool login()
    + void register()
    + void comment_on_post(int post_id, string content)
}

Post "1" --> "0..*" Comment : contains
Blog "1" --> "0..*" Post : displays
Admin "1" --> "0..*" Post : manages
User "1" --> "0..*" Comment : submits
User --> Blog : interacts with

