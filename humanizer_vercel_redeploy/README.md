# Humanizer Vercel App

Aplicativo em Python + Flask + SQLite para humanizar textos e documentos gerados no ChatGPT.

## Estrutura importante para Vercel

- `main.py`: lógica principal da aplicação
- `app.py`: execução local
- `api/index.py`: entrypoint para o Vercel
- `public/`: ficheiros estáticos
- `templates/`: páginas HTML
- `vercel.json`: rotas do Vercel

## Como testar localmente

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Abre `http://127.0.0.1:5000`

## Como fazer deploy no Vercel

1. Envia os ficheiros para o GitHub.
2. Importa o repositório no Vercel.
3. Adiciona a variável `SECRET_KEY` nas Environment Variables.
4. Faz o deploy.

## Nota

No Vercel, o SQLite fica em `/tmp`, então o histórico não é durável entre instâncias e novos deploys.
