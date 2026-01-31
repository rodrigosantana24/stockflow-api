# PetCare

**PetCare** é um microserviço web para conectar tutores de animais de estimação a cuidadores, permitindo cadastro de pets, busca de cuidadores por localização, agendamento de serviços e avaliações pós-atendimento.

O projeto foi desenvolvido aplicando conceitos de **Engenharia de Software**, com definição de MVP, user stories, modelagem de dados e arquitetura em camadas.

---

## Documentação

A documentação completa do projeto, incluindo requisitos, user stories, regras de negócio e endpoints, está disponível em:

**📄 Documentação:**  
[docs/petcare-documentacao.pdf](docs/petcare-documentacao.pdf)

---

## Funcionalidades

- Cadastro e autenticação de usuários (Tutor ou Cuidador)
- Gerenciamento de pets (Tutor)
- Busca de cuidadores por localização
- Solicitação e gerenciamento de agendamentos
- Avaliação de cuidadores após o serviço

---

## Tecnologias

- Java  
- Spring Boot  
- Spring Security + JWT  
- MySQL e MongoDB  
- Maven  
- Arquitetura MVC  

---

## Diagramas

### Diagrama de Entidades

<img src="docs/diagramas/diagrama-entidades.png"
     alt="Diagrama de Entidades"
     width="300" />

### Diagrama de Arquitetura

<img src="docs/diagramas/diagrama-arquitetura.png"
     alt="Diagrama de Arquitetura"
     width="300" />

### Diagrama de Fluxo de Usuário

<img src="docs/diagramas/diagrama-fluxo-usuario.png"
     alt="Diagrama de Fluxo de Usuário"
     width="300" />


---

<h2>Estrutura do Projeto</h2>

<pre>
petcare/
├── .gitignore
├── .editorconfig
├── README.md
├── pom.xml                      
├── .env.example                 
├── docker/
│   ├── Dockerfile
│   └── docker-compose.yml      
├── scripts/
│   ├── [seed.sh](http://seed.sh/)                 
│   └── [dev.sh](http://dev.sh/)                   
├── .github/
│   └── workflows/
│       └── ci.yml              
└── src/
├── main/
│   ├── java/
│   │   └── com/meuprojeto/
│   │       ├── PetcareApplication.java
│   │       ├── config/                 
│   │       ├── security/               
│   │       ├── exception/              
│   │       ├── entity/                 
│   │       ├── repository/             
│   │       ├── dto/                    
│   │       │   ├── auth/
│   │       │   ├── user/
│   │       │   ├── pet/
│   │       │   ├── schedule/
│   │       │   └── review/
│   │       ├── service/               
│   │       │   ├── auth/
│   │       │   ├── user/
│   │       │   ├── pet/
│   │       │   ├── schedule/
│   │       │   └── review/
│   │       ├── controller/            
│   │       │   ├── auth/
│   │       │   ├── user/
│   │       │   ├── pet/
│   │       │   ├── schedule/
│   │       │   └── review/
│   │       ├── mapper/                
│   │       ├── util/                   
│   │       └── common/                
│   └── resources/
│       ├── application.yml
│       ├── application-dev.yml
│       ├── application-test.yml
│       ├── db/
│       │   └── migration/             
│       ├── messages.properties         
│       ├── static/                     
│       └── templates/                  
└── test/
├── java/
│   └── com/meuprojeto/
│       ├── unit/                  
│       │   ├── service/
│       │   │   ├── auth/
│       │   │   ├── user/
│       │   │   ├── pet/
│       │   │   ├── schedule/
│       │   │   └── review/
│       │   ├── security/
│       │   └── util/
│       ├── web/                   
│       │   ├── auth/
│       │   ├── user/
│       │   ├── pet/
│       │   ├── schedule/
│       │   └── review/
│       ├── repository/             
│       ├── integration/            
│       ├── testutils/              
│       └── fixture/                
└── resources/
├── application-test.yml
├── data/                      
└── stubs/                      


---

## Principais Endpoints

| Método | Rota | Descrição |
|------|-----|----------|
| POST | /api/auth/register | Cadastro de usuário |
| POST | /api/auth/login | Login |
| POST | /api/pets | Cadastro de pet |
| GET | /api/cuidadores | Buscar cuidadores |
| POST | /api/agendamentos | Solicitar agendamento |
| PATCH | /api/agendamentos/{id}/status | Atualizar status |
| POST | /api/reviews | Criar avaliação |

---

## Autor

**Rodrigo Santana**  
https://www.linkedin.com/in/rodrigo-santana24/

