✅ FastAPI To-Do API
Uma API simples e direta para gerenciamento de tarefas, construída com FastAPI. Ideal para testar, brincar, ou servir de base para algo mais robusto. Simples, elegante e sem banco de dados — é na força do Python mesmo!

🚀 Funcionalidades
📋 Listar todas as tarefas

➕ Criar nova tarefa

🔄 Alternar status de conclusão (done)

❌ Deletar uma tarefa

📦 Requisitos
Python 3.7+

FastAPI

Uvicorn (para rodar o servidor)

Instale os pacotes com:

bash
Copiar
Editar
pip install fastapi uvicorn
▶️ Como rodar
No terminal:

bash
Copiar
Editar
uvicorn main:app --reload
Acesse no navegador: http://127.0.0.1:8000/docs

(Tem Swagger UI prontinha pra testar a API visualmente)

🛠 Endpoints
GET /tasks
Lista todas as tarefas cadastradas.

📦 Resposta:

json
Copiar
Editar
[
  {
    "id": 1,
    "title": "Estudar FastAPI",
    "done": false
  }
]
POST /tasks
Cria uma nova tarefa.

📝 Corpo da requisição:

json
Copiar
Editar
{
  "id": 1,
  "title": "Estudar FastAPI",
  "done": false
}
PUT /tasks/{task_id}
Alterna o status de conclusão (done) da tarefa com ID informado.

DELETE /tasks/{task_id}
Remove a tarefa com o ID informado.

💡 Observações
Não utiliza banco de dados — os dados são armazenados em memória (ideal para testes ou protótipos).

O campo done sempre começa como False, a menos que você envie como True no corpo do POST.

