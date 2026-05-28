# QuizAI — Deploy na Vercel

## Estrutura
```
quizai/
├── api/
│   └── chat.js        ← proxy da API Anthropic (resolve o CORS)
├── public/
│   └── index.html     ← o app
└── vercel.json
```

## Como fazer deploy

### 1. Sobe pro GitHub
```bash
git init
git add .
git commit -m "quizai"
git remote add origin https://github.com/SEU_USER/quizai.git
git push -u origin main
```

### 2. Importa no Vercel
- Acessa vercel.com/new
- Conecta o repositório
- Clica em Deploy

### 3. Adiciona a variável de ambiente
- No painel do projeto: Settings → Environment Variables
- Nome: `ANTHROPIC_API_KEY`
- Valor: sua chave (começa com `sk-ant-...`)
- Clica em Save e faz Redeploy
