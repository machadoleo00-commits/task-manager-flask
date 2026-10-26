# Task Manager (Flask)

Aplicação web simples para cadastrar e listar tarefas, feita com Flask durante o curso "Create Your First Web App with Python and Flask" (Coursera).

## Funcionalidades

- Listar tarefas cadastradas
- Adicionar nova tarefa por formulário
- Registro automático da data/hora de criação em UTC
- Persistência em banco SQLite

## Tecnologias

- Python 3.13
- Flask
- Flask-SQLAlchemy
- Flask-WTF
- SQLite
- HTML (templates Jinja2)

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
├── routes.py       # rotas (/ e /add)
├── forms.py        # formulário de nova tarefa
└── templates/      # páginas HTML
```

## Aprendizados

- Rotas e templates com Flask e Jinja2
- Modelagem e persistência com SQLAlchemy
- Formulários com validação e proteção CSRF (Flask-WTF)
- Application context do Flask-SQLAlchemy 3.x
- Datas em UTC com `datetime.now(UTC)`