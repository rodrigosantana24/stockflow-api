
---
# StockFlow 🚀

O **StockFlow** é uma API RESTful robusta desenvolvida para o gerenciamento inteligente de estoques. O sistema foca na rastreabilidade total de movimentações, garantindo que cada entrada e saída de mercadoria seja registrada com segurança, integridade transacional e alertas automáticos de níveis críticos.

---

## Tecnologias

* **Linguagem:** Java 17+
* **Framework:** Spring Boot 3+
* **Segurança:** Spring Security + JWT (JSON Web Token)
* **Banco de Dados Relacional:** PostGreSQL (Dados transacionais e cadastros)
* **Banco de Dados NoSQL:** MongoDB (Logs de auditoria e histórico de movimentações)
* **Gerenciador de Dependências:** Maven

---

## Funcionalidades
* **Gestão de Inventário:** CRUD completo de produtos e fornecedores.
* **Movimentação Transacional:** Registro atômico de entradas e saídas (Rollback em caso de erro).
* **Controle de Saldo:** Bloqueio automático de saídas caso o estoque seja insuficiente.
* **Alertas de Estoque Mínimo:** Monitoramento em tempo real de itens que atingiram o limite crítico.
* **Histórico de Auditoria:** Consulta detalhada de movimentações por período ou produto.
* **Autenticação Segura:** Acesso protegido via tokens JWT e criptografia BCrypt.

---

## Arquitetura e Estrutura
O sistema segue o padrão **MVC (Model-View-Controller)** aplicado a APIs, utilizando a separação em camadas para alta manutenibilidade:

```text
src/main/java/com/rodrigo/stockflow/
├── controller/    # Endpoints da API
├── service/       # Regras de negócio e transações
├── model/         # Entidades (JPA e MongoDB)
├── repository/    # Interfaces de persistência
├── dto/           # Objetos de transferência de dados
└── security/      # Configurações de acesso e filtros JWT

```

---

## Principais Endpoints

| Método | Endpoint | Descrição |
| --- | --- | --- |
| `POST` | `/auth/login` | Autenticação e geração de Token |
| `GET` | `/api/v1/products` | Lista todos os produtos |
| `POST` | `/api/v1/stock/in` | Registra entrada de mercadoria |
| `POST` | `/api/v1/stock/out` | Registra saída de mercadoria |
| `GET` | `/api/v1/history/{id}` | Histórico de movimentações de um produto |

---

## 👤 Autor

**Rodrigo Santana**  

Estagiário de Desenvolvimento Backend | Estudante de Sistemas de Informação (UFRPE)
<br></br>**LinkedIn:** [linkedin.com/in/rodrigo-santana24/](https://www.linkedin.com/in/rodrigo-santana24/)
---

