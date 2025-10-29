# DevTasks - Gerenciador de Tarefas para Equipes Ágeis

![DevTasks Logo](https://img.shields.io/badge/DevTasks-v1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Vue.js](https://img.shields.io/badge/Vue.js-3.4+-4FC08D)
![FastAPI](https://img.shields.io/badge/FastAPI-0.110+-009688)

## 📋 Sobre o Projeto

DevTasks é um sistema completo de gerenciamento de tarefas desenvolvido para equipes ágeis. Oferece uma interface intuitiva com quadro Kanban, calendário integrado e colaboração em tempo real.

## ✨ Funcionalidades

- 🔐 **Autenticação JWT** - Login seguro e gerenciamento de sessões
- 📊 **Dashboard Analytics** - Estatísticas e métricas de produtividade
- 📋 **Quadro Kanban** - Gestão visual de tarefas com drag & drop
- 📅 **Calendário Integrado** - Visualização de prazos e deadlines
- 👥 **Colaboração em Equipe** - Atribuição e comentários em tarefas
- 🔔 **Notificações** - Alertas em tempo real
- 📱 **Design Responsivo** - Interface adaptada para todos os dispositivos

## 🛠️ Tecnologias

### Frontend

- **Vue.js 3** - Framework progressivo
- **Pinia** - Gerenciamento de estado
- **Vue Router** - Roteamento SPA
- **Tailwind CSS** - Framework CSS utilitário
- **Vite** - Build tool moderna
- **Axios** - Cliente HTTP

### Backend

- **FastAPI** - Framework web Python
- **SQLAlchemy** - ORM Python
- **PostgreSQL/SQLite** - Banco de dados
- **JWT** - Autenticação
- **Uvicorn** - Servidor ASGI

## 🚀 Como Executar

### Pré-requisitos

- Node.js 18+
- Python 3.11+
- PostgreSQL (opcional, usa SQLite por padrão)

### 1. Clone o repositório

\`\`\`bash
git clone https://github.com/VitoriaMir/DevTasks.git
cd DevTasks
\`\`\`

### 2. Configuração do Backend

\`\`\`bash
cd backend

# Criar ambiente virtual
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
# ou
.venv\Scripts\activate     # Windows

# Instalar dependências
pip install -r requirements.txt

# Configurar variáveis de ambiente
cp .env.example .env
# Edite o arquivo .env com suas configurações

# Iniciar servidor
uvicorn server:app --reload
\`\`\`

### 3. Configuração do Frontend

\`\`\`bash
cd frontend

# Instalar dependências
npm install

# Configurar variáveis de ambiente
cp .env.example .env
# Edite o arquivo .env se necessário

# Iniciar desenvolvimento
npm run dev
\`\`\`

### 4. Acessar a aplicação

- **Frontend:** http://localhost:3000
- **Backend API:** http://localhost:8000
- **Documentação API:** http://localhost:8000/docs

## 📁 Estrutura do Projeto

\`\`\`
devtasks/
├── frontend/                 # Aplicação Vue.js
│   ├── src/
│   │   ├── components/      # Componentes reutilizáveis
│   │   ├── views/          # Páginas da aplicação
│   │   ├── stores/         # Gerenciamento de estado (Pinia)
│   │   ├── router/         # Configuração de rotas
│   │   └── utils/          # Utilitários e helpers
│   └── package.json
├── backend/                 # API FastAPI
│   ├── app/
│   │   ├── models/         # Modelos do banco de dados
│   │   ├── schemas/        # Schemas Pydantic
│   │   ├── services/       # Lógica de negócio
│   │   └── api/           # Endpoints da API
│   └── requirements.txt
└── README.md
\`\`\`

## 🤝 Contribuindo

1. Faça um fork do projeto
2. Crie uma branch para sua feature (\`git checkout -b feature/nova-funcionalidade\`)
3. Commit suas mudanças (\`git commit -m 'Adiciona nova funcionalidade'\`)
4. Push para a branch (\`git push origin feature/nova-funcionalidade\`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

### O que isso significa?

A licença MIT permite que você:

- ✅ **Use comercialmente** - Pode usar em projetos comerciais
- ✅ **Modifique** - Pode alterar o código como quiser
- ✅ **Distribua** - Pode compartilhar e redistribuir
- ✅ **Use privadamente** - Pode usar internamente na empresa
- ✅ **Sublicencie** - Pode aplicar outras licenças

**Única exigência:** Manter o aviso de copyright e licença nos arquivos.

## 👨‍💻 Equipe

- **Desenvolvedor Principal** - Vitória Miranda
- **Contribuidores** - Veja a lista completa em [Contributors](../../contributors)

## 📞 Suporte

- 📧 Email: <suporte@devtasks.com>
- 🐛 Issues: [GitHub Issues](../../issues)
- 📖 Documentação: [Docs](../../wiki)

---

<div align="center">
  <p>Feito com ❤️ para equipes ágeis</p>
  <p>DevTasks © 2025 - Todos os direitos reservados</p>
</div>
