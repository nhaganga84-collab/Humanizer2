# Humanizer Fly.io App

Aplicativo Flask com SQLite para humanização local de textos e documentos, pronto para deploy no Fly.io.

## Teste local
```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python app.py
```

Abrir em `http://127.0.0.1:8080`.

## Deploy no Fly.io
1. Instalar `flyctl` e fazer login.
2. Na pasta do projeto: `fly launch --no-deploy`
3. Criar volume: `fly volumes create humanizer_data --region jnb --size 1`
4. Definir segredo: `fly secrets set SECRET_KEY=sua-chave-segura`
5. Deploy: `fly deploy`

O SQLite fica em `/data/humanizer.db`.
