# 💰 Financeiro Pro — Controle Financeiro Pessoal

> Aplicação web mobile-first para gestão financeira pessoal completa. Funciona 100% offline, sem backend, sem dependências externas — basta abrir o arquivo HTML no navegador.

![Version](https://img.shields.io/badge/versão-v30-blue)
![Tech](https://img.shields.io/badge/tech-HTML%20%7C%20CSS%20%7C%20JS-orange)
![Status](https://img.shields.io/badge/status-ativo-green)
![License](https://img.shields.io/badge/licença-MIT-lightgrey)

---

## 📱 Demonstração

| Dashboard | Extrato | Metas | Configurações |
|-----------|---------|-------|---------------|
| Receitas, despesas, saldo e previsão | Filtros multi-conta e categoria | Acumulado anual detalhado | Multi-contas e categorias |

---

## ✨ Funcionalidades

### 🔐 Autenticação
- Login e cadastro com senha criptografada (hash local)
- Sessão persistente via `localStorage`
- **Recuperação de senha** com código temporário de 6 dígitos e timer de 10 minutos
- **Modo visitante** — acesso sem cadastro, dados não persistidos
- **Foto de perfil** — upload, preview e remoção

### 📊 Dashboard
- Cards de Receita, Despesa, Saldo e Economia %
- Card de Investimentos do mês com rentabilidade
- Previsão para o fim do mês com gasto médio/dia
- **Gráfico de pizza por Categoria e Multi-Contas** (abas alternáveis)
- Gráfico de Evolução Anual (receitas vs despesas)
- Partículas financeiras animadas no header

### 📜 Extrato Detalhado
- Busca por descrição ou categoria
- **Filtros multi-seleção**: tipo (Receita/Despesa), contas e categorias simultaneamente
- Chips visuais dos filtros ativos
- Totalizador dinâmico: Receitas | Despesas | Saldo
- Total geral dos lançamentos com hint informativo

### 🎯 Metas
- Metas mensais por categoria com barra de progresso
- Acumulado do Ano com **detalhamento mensal** e **total por despesa**
- Subtotais por mês dentro de cada categoria
- Total por item (ex: "Purificador Consul — 6× R$ 80,00 → R$ 480,00")

### ➕ Lançamentos
- Despesas e Receitas com conta vinculada
- **Parcelamentos**: geração automática de parcelas mensais
  - Hint explicativo ao marcar "Parcelado"
  - Editar "Apenas este mês" ou "Este e todos os futuros"
  - Excluir "Apenas este mês" ou "Este e todos os futuros"
- **Nova categoria inline** — sem precisar ir às configurações
- Categorias salvas automaticamente

### 🏦 Multi-Contas
- Cadastro de contas com nome, tipo e cor automática
- Tipos: C. Corrente, C. Poupança, Cartão de Crédito, Cartão de Débito, Carteira, Investimento, Crypto
- Edição e exclusão com aviso de lançamentos vinculados
- Filtro do extrato por tipo de conta ou conta específica

### 📈 Investimentos
- Registro de aportes mensais com rentabilidade
- Metas de investimento com progresso

### 🏠 Bens & Patrimônio
- Registro de bens com valor e categoria

### 🔁 Fixas
- Despesas e receitas recorrentes
- Geração automática de lançamentos

### ⚙️ Configurações
- **Gestão Multi-Contas** — adicionar, editar, excluir contas
- **Gestão de Categorias** — adicionar e remover categorias de Receita e Despesa
- **Sistema** — exportar backup JSON, exportar CSV, exportar PDF, importar backup
- Alternância de tema claro/escuro

### 🌙 UX & Visual
- Design mobile-first (iOS-inspired)
- Tema dark/light com persistência
- Toasts de notificação com badge no sino
- Alertas inteligentes (apenas no primeiro acesso, badge nos demais)
- Partículas financeiras no header (`$`, `%`, `↑`, `R$`)
- Favicon "FIN" SVG inline
- Botão Voltar ao Topo com fade suave
- Meta tags SEO e Open Graph completos

---

## 🚀 Como Usar

### Opção 1 — Clonar o repositório
```bash
git clone https://github.com/Martinswillians/PlanejamentoFinanceiro.git
cd PlanejamentoFinanceiro

# Abra no navegador
start index.html        # Windows
open index.html         # macOS
xdg-open index.html     # Linux
```

### Opção 2 — Download direto
1. Acesse [github.com/Martinswillians/PlanejamentoFinanceiro](https://github.com/Martinswillians/PlanejamentoFinanceiro)
2. Clique em **Code → Download ZIP**
3. Extraia e abra o `index.html` no navegador

### Opção 3 — Como PWA (mobile)
1. Abra o arquivo no Chrome mobile
2. Menu → "Adicionar à tela inicial"
3. Use como app nativo

> **Não requer servidor, Node.js, banco de dados ou internet.**  
> Todos os dados são salvos no `localStorage` do navegador.

---

## 🗃️ Estrutura dos Dados

Todos os dados ficam no `localStorage` com as seguintes chaves:

| Chave | Conteúdo |
|-------|----------|
| `will_users_v1` | Lista de usuários cadastrados |
| `will_dados_{uid}` | Lançamentos, metas, contas, categorias por usuário |
| `will_sessao` | Sessão ativa (id + timestamp) |
| `will_dark` | Preferência de tema |
| `will_foto_{uid}` | Foto de perfil em base64 |

---

## 🛠️ Tecnologias

| Tecnologia | Uso |
|-----------|-----|
| HTML5 | Estrutura e canvas de partículas |
| CSS3 | Design mobile-first, variáveis, dark mode |
| JavaScript ES6+ | Toda a lógica da aplicação |
| Chart.js v4.5.1 | Gráficos de pizza e linha (embutido inline) |
| localStorage | Persistência de dados sem backend |

---

## 📋 Changelog

| Versão | Principais mudanças |
|--------|-------------------|
| v30 | Chart.js inline, linha branca corrigida, foto de perfil |
| v29 | Recuperação de senha, modo visitante, foto de perfil |
| v28 | Partículas no header, favicon FIN, botão voltar ao topo, pizza por Multi-Contas |
| v27 | Filtros multi-seleção no extrato |
| v26 | Cartão de Débito, Crypto, edição de contas com modal |
| v25 | Gestão Multi-Contas com exclusão segura |
| v24 | Filtro do extrato por tipo de conta agrupado |
| v23 | Padronização Config, totais no extrato |
| v22 | Nova categoria inline no modal de lançamento |
| v21 | Gestão de contas melhorada, bug acumulado corrigido |
| v20 | Drill-down anual com subtotais mensais e total por despesa |
| v19 | Filtros de extrato, notificações inteligentes |
| v18 | Parcelamentos com editar/excluir futuros |

---

## 👤 Autor

**Willians Martins**  
📧 willbrasilia@gmail.com  
🔗 [github.com/Martinswillians](https://github.com/Martinswillians)

---

## 📄 Licença

MIT © 2026 Willians Martins

---

> 💡 **Dica:** Para backup dos seus dados, use a opção **Exportar Backup JSON** em Configurações → Sistema. Guarde o arquivo em local seguro.

> Aplicação web mobile-first para gestão financeira pessoal completa. Funciona 100% offline, sem backend, sem dependências externas — basta abrir o arquivo HTML no navegador.

![Version](https://img.shields.io/badge/versão-v30-blue)
![Tech](https://img.shields.io/badge/tech-HTML%20%7C%20CSS%20%7C%20JS-orange)
![Status](https://img.shields.io/badge/status-ativo-green)
![License](https://img.shields.io/badge/licença-MIT-lightgrey)

---

## 📱 Demonstração

| Dashboard | Extrato | Metas | Configurações |
|-----------|---------|-------|---------------|
| Receitas, despesas, saldo e previsão | Filtros multi-conta e categoria | Acumulado anual detalhado | Multi-contas e categorias |

---

## ✨ Funcionalidades

### 🔐 Autenticação
- Login e cadastro com senha criptografada (hash local)
- Sessão persistente via `localStorage`
- **Recuperação de senha** com código temporário de 6 dígitos e timer de 10 minutos
- **Modo visitante** — acesso sem cadastro, dados não persistidos
- **Foto de perfil** — upload, preview e remoção

### 📊 Dashboard
- Cards de Receita, Despesa, Saldo e Economia %
- Card de Investimentos do mês com rentabilidade
- Previsão para o fim do mês com gasto médio/dia
- **Gráfico de pizza por Categoria e Multi-Contas** (abas alternáveis)
- Gráfico de Evolução Anual (receitas vs despesas)
- Partículas financeiras animadas no header

### 📜 Extrato Detalhado
- Busca por descrição ou categoria
- **Filtros multi-seleção**: tipo (Receita/Despesa), contas e categorias simultaneamente
- Chips visuais dos filtros ativos
- Totalizador dinâmico: Receitas | Despesas | Saldo
- Total geral dos lançamentos com hint informativo

### 🎯 Metas
- Metas mensais por categoria com barra de progresso
- Acumulado do Ano com **detalhamento mensal** e **total por despesa**
- Subtotais por mês dentro de cada categoria
- Total por item (ex: "Purificador Consul — 6× R$ 80,00 → R$ 480,00")

### ➕ Lançamentos
- Despesas e Receitas com conta vinculada
- **Parcelamentos**: geração automática de parcelas mensais
  - Hint explicativo ao marcar "Parcelado"
  - Editar "Apenas este mês" ou "Este e todos os futuros"
  - Excluir "Apenas este mês" ou "Este e todos os futuros"
- **Nova categoria inline** — sem precisar ir às configurações
- Categorias salvas automaticamente

### 🏦 Multi-Contas
- Cadastro de contas com nome, tipo e cor automática
- Tipos: C. Corrente, C. Poupança, Cartão de Crédito, Cartão de Débito, Carteira, Investimento, Crypto
- Edição e exclusão com aviso de lançamentos vinculados
- Filtro do extrato por tipo de conta ou conta específica

### 📈 Investimentos
- Registro de aportes mensais com rentabilidade
- Metas de investimento com progresso

### 🏠 Bens & Patrimônio
- Registro de bens com valor e categoria

### 🔁 Fixas
- Despesas e receitas recorrentes
- Geração automática de lançamentos

### ⚙️ Configurações
- **Gestão Multi-Contas** — adicionar, editar, excluir contas
- **Gestão de Categorias** — adicionar e remover categorias de Receita e Despesa
- **Sistema** — exportar backup JSON, exportar CSV, exportar PDF, importar backup
- Alternância de tema claro/escuro

### 🌙 UX & Visual
- Design mobile-first (iOS-inspired)
- Tema dark/light com persistência
- Toasts de notificação com badge no sino
- Alertas inteligentes (apenas no primeiro acesso, badge nos demais)
- Partículas financeiras no header (`$`, `%`, `↑`, `R$`)
- Favicon "FIN" SVG inline
- Botão Voltar ao Topo com fade suave
- Meta tags SEO e Open Graph completos

---

## 🚀 Como Usar

### Opção 1 — Direto no Navegador
```bash
# Baixe o arquivo
git clone https://github.com/seu-usuario/financeiro-pro.git

# Abra no navegador
open Planilha_Financeira_Mobile_IOS_v30.html
# ou arraste o arquivo para o Chrome/Firefox/Edge
```

### Opção 2 — Como PWA (mobile)
1. Abra o arquivo no Chrome mobile
2. Menu → "Adicionar à tela inicial"
3. Use como app nativo

> **Não requer servidor, Node.js, banco de dados ou internet.**  
> Todos os dados são salvos no `localStorage` do navegador.

---

## 🗃️ Estrutura dos Dados

Todos os dados ficam no `localStorage` com as seguintes chaves:

| Chave | Conteúdo |
|-------|----------|
| `will_users_v1` | Lista de usuários cadastrados |
| `will_dados_{uid}` | Lançamentos, metas, contas, categorias por usuário |
| `will_sessao` | Sessão ativa (id + timestamp) |
| `will_dark` | Preferência de tema |
| `will_foto_{uid}` | Foto de perfil em base64 |

---

## 🛠️ Tecnologias

| Tecnologia | Uso |
|-----------|-----|
| HTML5 | Estrutura e canvas de partículas |
| CSS3 | Design mobile-first, variáveis, dark mode |
| JavaScript ES6+ | Toda a lógica da aplicação |
| Chart.js v4.5.1 | Gráficos de pizza e linha (embutido inline) |
| localStorage | Persistência de dados sem backend |

---

## 📋 Changelog

| Versão | Principais mudanças |
|--------|-------------------|
| v30 | Chart.js inline, linha branca corrigida, foto de perfil |
| v29 | Recuperação de senha, modo visitante, foto de perfil |
| v28 | Partículas no header, favicon FIN, botão voltar ao topo, pizza por Multi-Contas |
| v27 | Filtros multi-seleção no extrato |
| v26 | Cartão de Débito, Crypto, edição de contas com modal |
| v25 | Gestão Multi-Contas com exclusão segura |
| v24 | Filtro do extrato por tipo de conta agrupado |
| v23 | Padronização Config, totais no extrato |
| v22 | Nova categoria inline no modal de lançamento |
| v21 | Gestão de contas melhorada, bug acumulado corrigido |
| v20 | Drill-down anual com subtotais mensais e total por despesa |
| v19 | Filtros de extrato, notificações inteligentes |
| v18 | Parcelamentos com editar/excluir futuros |

---

## 👤 Autor

**Willians Martins**  
📧 willbrasilia@gmail.com  
🔗 [GitHub](https://github.com/seu-usuario)

---

## 📄 Licença

MIT © 2026 Willians Martins

---

> 💡 **Dica:** Para backup dos seus dados, use a opção **Exportar Backup JSON** em Configurações → Sistema. Guarde o arquivo em local seguro.
