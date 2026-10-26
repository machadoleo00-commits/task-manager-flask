# Task Manager (Flask)

Aplicação web para gerenciar tarefas, feita com Flask durante o curso "Create Your First Web App with Python and Flask" (Coursera). Permite criar, listar, editar e excluir tarefas, com persistência em banco SQLite.

## Funcionalidades

- Listar todas as tarefas cadastradas
- Adicionar nova tarefa por formulário
- Editar o título de uma tarefa existente
- Excluir tarefas
- Mensagens de confirmação após cada ação (flash messages)
- Data e hora de criação gravadas em UTC, sem microssegundos

## Tecnologias

- Python 3.13
- Flask
- Flask-SQLAlchemy
- Flask-WTF (formulários e proteção CSRF)
- SQLite
- HTML com templates Jinja2
- Bootstrap

## Rotas

| Rota | Método | Descrição |
|------|--------|-----------|
| `/` | GET | Lista as tarefas |
| `/add` | GET, POST | Formulário para criar tarefa |
| `/edit/<id>` | GET, POST | Edita uma tarefa |
| `/delete/<id>` | GET, POST | Exclui uma tarefa |

## Como rodar

1. Clone o repositório:

```
git clone https://github.com/machadoleo00-commits/task-manager-flask.git
cd task-manager-flask
```

2. Crie e ative o ambiente virtual (Windows PowerShell):

```
python -m venv venv
.\venv\Scripts\Activate.ps1
```

3. Instale as dependências:

```
pip install -r requirements.txt
```

4. Rode o app:

```
python app.py
```

5. Abra no navegador: http://127.0.0.1:5000

O banco de dados (`instance/data.db`) é criado automaticamente na primeira execução.

## Estrutura

```
├── app.py          # configuração do app e do banco
├── models.py       # modelo Task
├── routes.py       # rotas (listar, adicionar, editar, excluir)
├── forms.py        # formulário de tarefa
└── templates/      # páginas HTML (base, index, add, edit)
```

## Aprendizados

- Rotas dinâmicas com parâmetros (`/edit/<int:task_id>`)
- Operações CRUD completas com SQLAlchemy
- Formulários com validação e proteção CSRF (Flask-WTF)
- Application context do Flask-SQLAlchemy 3.x
- Datas em UTC com `datetime.now(UTC)`
- Herança de templates com Jinja2
- Teste de rotas com Insomnia