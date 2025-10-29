# Guia de Contribuição - DevTasks

Obrigado por considerar contribuir com o DevTasks! 🎉

## 🤝 Como Contribuir

### 1. Fork e Clone
```bash
# Fork o repositório no GitHub
# Clone seu fork
git clone https://github.com/SEU-USUARIO/DevTasks.git
cd DevTasks
```

### 2. Configuração do Ambiente
Siga as instruções do [README.md](README.md) para configurar o ambiente de desenvolvimento.

### 3. Criar Branch
```bash
git checkout -b feature/sua-nova-funcionalidade
# ou
git checkout -b fix/correcao-de-bug
```

### 4. Padrões de Código

#### Frontend (Vue.js)
- Use **Composition API**
- Siga os padrões do **ESLint**
- Use **TypeScript** quando possível
- Componentes em **PascalCase**
- Props e eventos em **camelCase**

#### Backend (FastAPI)
- Siga **PEP 8**
- Use **type hints**
- Documente funções com **docstrings**
- Mantenha linhas com máximo 88 caracteres

### 5. Commits
Use o padrão **Conventional Commits**:
```bash
feat: adiciona autenticação JWT
fix: corrige erro de login
docs: atualiza README
style: formata código
refactor: reorganiza estrutura de pastas
test: adiciona testes unitários
```

### 6. Testes
- **Frontend:** `npm run test`
- **Backend:** `pytest`

### 7. Pull Request
1. Certifique-se que todos os tests passam
2. Atualize documentação se necessário
3. Descreva claramente as mudanças
4. Referencie issues relacionadas

## 🐛 Reportar Bugs

Use o template:
```markdown
**Descrição do Bug**
Descrição clara do problema.

**Passos para Reproduzir**
1. Vá para '...'
2. Clique em '....'
3. Veja o erro

**Comportamento Esperado**
O que deveria acontecer.

**Screenshots**
Se aplicável, adicione screenshots.

**Informações do Sistema**
- OS: [ex: Windows 10]
- Browser: [ex: Chrome 91]
- Versão: [ex: 1.0.0]
```

## 💡 Sugerir Funcionalidades

Use o template:
```markdown
**Problema/Necessidade**
Que problema esta funcionalidade resolveria?

**Solução Proposta**
Descreva a solução que você gostaria.

**Alternativas**
Outras soluções que você considerou.

**Contexto Adicional**
Qualquer informação adicional.
```

## 📋 Checklist do PR

- [ ] Testes passando
- [ ] Código segue padrões do projeto
- [ ] Documentação atualizada
- [ ] Commits seguem padrão conventional
- [ ] Branch atualizada com main
- [ ] Screenshots para mudanças visuais

## 🏷️ Labels

- `bug` - Correção de bugs
- `enhancement` - Nova funcionalidade
- `documentation` - Melhorias na documentação
- `good first issue` - Bom para iniciantes
- `help wanted` - Precisa de ajuda
- `priority: high` - Alta prioridade

## 📞 Comunidade

- 💬 Discussions: Para perguntas gerais
- 🐛 Issues: Para bugs e features
- 📧 Email: devtasks@exemplo.com

## 📄 Código de Conduta

Este projeto adere ao [Contributor Covenant](https://www.contributor-covenant.org/). 
Ao participar, você deve seguir este código.

---

**Obrigado por contribuir! 🚀**