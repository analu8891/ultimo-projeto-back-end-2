 Gerenciador de Produtos – API + Streamlit

Um sistema completo para gerenciar produtos com CRUD, banco PostgreSQL e interface visual em Streamlit.


 Estrutura do Projeto
 projeto/
│
├── back-end/
│   ├── conexao.py        # Conexão com PostgreSQL
│   ├── crud.py           # Lógica de CRUD organizada
│   └── api.py            # API FastAPI
│
├── front-end/
│   └── app.py            # Painel Streamlit
│
├── .env                  # Variáveis de ambiente
├── requirements.txt
└── README.md

 Funcionalidades
| Função                 | Descrição                                    |
| ---------------------- | -------------------------------------------- |
|  Cadastrar produto     | Registra nome, categoria, preço e quantidade |
|  Listar produtos       | Mostra todos os itens do banco               |
|  Buscar por ID         | Retorna informações de um produto            |
|  Atualizar quantidade  | Edita estoque                                |
|  Deletar produto       | Remove um item                               |

Configuração do Ambiente

1 Criar ambiente virtual

python -m venv .venv
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows

2 Criar o arquivo .env
DB_NAME=seubanco
DB_USER=usuario
DB_PASSWORD=senha
DB_HOST=localhost
DB_PORT=5432


Rodar o Back-End (API)
uvicorn back-end.api:app --reload

API rodará em:
http://127.0.0.1:8000

Documentação automática:
http://127.0.0.1:8000/docs

Rodar o Front-End (Streamlit)
python -m streamlit run front-end/app.py

Autor

Projeto desenvolvido para estudos de API + Banco de Dados + Interface Web.
Sinta-se livre para melhorar, modificar e aprender com ele!