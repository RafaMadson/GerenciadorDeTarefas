# Gerenciador de Tarefas - ASP.NET Core

Um sistema básico de gerenciamento de tarefas desenvolvido em **ASP.NET Core** com C#. Este projeto permite que os usuários criem, editem, excluam e filtrem tarefas. É uma ótima forma de praticar habilidades de programação e desenvolvimento web.

---

## Funcionalidades

- **Autenticação de Usuários**:
  - Cadastro de usuários.
  - Login e logout.

- **CRUD de Tarefas**:
  - Criar, editar e excluir tarefas.
  - Marcar tarefas como concluídas.
  - Atribuir categorias e prazos.

- **Filtragem e Listagem**:
  - Filtrar tarefas por categoria ou status (concluída/não concluída).
  - Exibir tarefas ordenadas por data de criação ou prazo.

---

## Tecnologias Utilizadas

- **Backend**: ASP.NET Core (versão LTS recomendada).
- **Frontend**: Razor Pages ou MVC com Bootstrap.
- **Banco de Dados**: SQLite ou SQL Server.
- **ORM**: Entity Framework Core.
- **IDE**: Visual Studio ou Visual Studio Code.

---

## Estrutura do Banco de Dados

### Tabela `Users`
| Coluna         | Tipo    | Descrição                  |
|----------------|---------|----------------------------|
| `Id`           | PK, int | Identificador único        |
| `Username`     | string  | Nome de usuário            |
| `PasswordHash` | string  | Senha armazenada (hash)    |

### Tabela `Tasks`
| Coluna         | Tipo     | Descrição                     |
|----------------|----------|-------------------------------|
| `Id`           | PK, int  | Identificador único           |
| `Title`        | string   | Título da tarefa              |
| `Description`  | string   | Descrição da tarefa           |
| `Category`     | string   | Categoria da tarefa           |
| `DueDate`      | DateTime | Prazo para conclusão          |
| `IsCompleted`  | bool     | Status da tarefa (concluída)  |
| `UserId`       | FK, int  | Identificador do usuário dono |

---

## Como Executar o Projeto

### Pré-requisitos
- [.NET SDK](https://dotnet.microsoft.com/download) instalado.
- Banco de dados configurado (SQLite ou SQL Server).

### Passos

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/RafaMadson/GerenciadorDeTarefas.git
   cd GerenciadorDeTarefas
