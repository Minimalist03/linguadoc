# LinguaDoc 🌍

App para estudar idiomas usando seus próprios documentos (PDF/TXT) com IA.

---

## 🚀 Deploy no Netlify (recomendado)

### 1. Suba o projeto para o GitHub
Crie um repositório com esses arquivos:
```
linguadoc/
├── netlify/
│   └── functions/
│       └── chat.mjs       ← Função serverless (guarda a API key)
├── lingua_app.html         ← Frontend
├── netlify.toml            ← Config do Netlify
└── package.json
```

### 2. Conecte ao Netlify
- Acesse https://netlify.com e faça login
- Clique em "Add new site" → "Import an existing project"
- Conecte seu GitHub e selecione o repositório

### 3. Configure a variável de ambiente
No painel do Netlify:
- Vá em Site configuration → Environment variables
- Clique em "Add a variable"
- Nome: OPENAI_API_KEY
- Valor: sk-proj-sua-key-aqui

### 4. Faça o deploy
Clique em "Deploy site" — pronto!

---

## 💻 Rodar localmente (com Netlify CLI)

```bash
npm install -g netlify-cli
npm install
netlify dev
```
Acesse: http://localhost:8888

---

## Segurança
- A API key fica apenas nas variáveis de ambiente do Netlify
- O navegador nunca tem acesso direto à key
- Nunca suba um arquivo .env para o GitHub
