# 💰 Financeiro Pro — Controle Financeiro Pessoal

> Aplicação web mobile-first para gestão financeira pessoal completa. Funciona 100% offline, sem backend, sem dependências externas — basta abrir o arquivo HTML no navegador.

![Version](https://img.shields.io/badge/versão-v38-blue)
![Tech](https://img.shields.io/badge/tech-HTML%20%7C%20CSS%20%7C%20JS-orange)
![Status](https://img.shields.io/badge/status-ativo-green)
![License](https://img.shields.io/badge/licença-MIT-lightgrey)

---

## 📱 Demonstração

| Dashboard | Extrato | Metas | Por Item |
|-----------|---------|-------|----------|
| Receitas, despesas, saldo e previsão | Filtros multi-seleção com status pago/pendente | Acumulado anual detalhado | Agrupamento por parcelamento e repetição |

---

## ✨ Funcionalidades

### 🔐 Autenticação
- Login e cadastro com senha criptografada (hash local)
- Sessão persistente via `localStorage`
- **Recuperação de senha** com código temporário de 6 dígitos e timer de 10 minutos
- **Modo visitante** — acesso sem cadastro, dados não persistidos
- **Foto de perfil** — upload, preview e remoção
- Suporte a múltiplos usuários com dados completamente isolados

### 📊 Dashboard
- Cards de Receita, Despesa, Saldo e Economia %
- Card de Investimentos do mês com rentabilidade
- Previsão para o fim do mês com gasto médio/dia
- **Gráfico de pizza** com abas alternáveis: **por Categoria** e **por Multi-Contas**
- Gráfico de Evolução Anual (receitas vs despesas)
- Partículas financeiras animadas no header (`$`, `%`, `↑`, `R$`)

### 📜 Extrato — 3 abas

#### 📜 Mês
- Busca por descrição, categoria ou **tag**
- **Filtros multi-seleção**: Tipo, Status (✅ Pago / ⏳ Pendente), Contas e Categorias
- Chips visuais dos filtros ativos com badge no botão Filtros
- Totalizador dinâmico: Receitas | Despesas | Saldo
- Total geral dos lançamentos no rodapé
- **Toggle de status** em cada item — marcar como pago/pendente com um toque
- Item pago exibe descrição riscada e ícone ✅
- Exportação **📊 XLS** e **📄 PDF** respeitando filtros ativos

#### 📦 Por Item
- Visão consolidada de **todos os lançamentos** independente do mês
- Agrupamento inteligente: parcelamentos, repetições e recorrentes em um único card
- Total acumulado + valor por parcela + período completo
- **▼ Ver parcelas** para expandir e editar/excluir individualmente
- Ordenação por **📅 Data** ou **🔤 A-Z**
- Filtro por tipo e busca por nome/categoria/tag
- Exportação **📊 XLS** e **📄 PDF**

#### 🎁 Benefícios
- Exclusivo para Ticket Alimentação, Ticket Refeição e Cartão Benefícios
- Saldo disponível de cada benefício no mês
- Esses itens **não aparecem** no extrato comum nem nos totalizadores

### 🎯 Metas
- Metas mensais por categoria com barra de progresso
- Alerta visual quando ultrapassa 80% do limite
- **Acumulado do Ano** com drill-down:
  - Total por despesa (ex: "Purificador 6× R$ 80 = R$ 480")
  - Detalhamento mensal com subtotais por mês

### ➕ Lançamentos
- **Tipos**: Despesa, Receita e **↔️ Transferência entre contas**
- **Parcelamentos**: geração automática mensal com numeração (1/10)
  - Editar/excluir "Apenas este mês" ou "Este e todos os futuros"
- **Repetição personalizada**: Semanal, Quinzenal, Mensal ou Anual com preview de data final
- **🏷️ Tags** separadas por vírgula — pesquisáveis no extrato
- **📎 Comprovante** — anexe foto ou PDF; visualize clicando no ícone
- **Nova categoria inline** — sem sair do modal de lançamento
- Distinção visual de contas com mesmo nome (ex: `Nubank (C. Corrente)` vs `Nubank (Cartão de Crédito)`)

### 🏦 Multi-Contas
- Tipos disponíveis: C. Corrente, C. Poupança, Cartão de Crédito, Cartão de Débito, Carteira, Investimento, Crypto
- Edição com modal dedicado; exclusão com aviso de lançamentos vinculados
- Filtro do extrato por **tipo de conta** (agrupa todas do tipo) ou **conta específica**

### 📈 Investimentos
- Registro de aportes mensais com rentabilidade
- Metas de investimento com barra de progresso

### 🔁 Fixas (Recorrentes)
- Templates de despesas/receitas que se repetem mensalmente
- Confirmação mês a mês; alerta no sino quando há pendentes

### ⚙️ Configurações
- **Gestão Multi-Contas** — adicionar, editar, excluir
- **Gestão de Categorias** — Receita e Despesa separadas
- **Sistema** — Exportar Backup JSON, CSV, PDF, Importar Backup

### 📖 Manual Integrado
- Botão **❓** no header abre o manual completo dentro do app
- **15 tópicos** cobrindo todas as funcionalidades
- **Busca inteligente** por palavra-chave — filtra por título, tags e conteúdo
- Se só um resultado → abre automaticamente

### 🌙 UX & Visual
- Design mobile-first (iOS-inspired)
- Tema dark/light com persistência
- Toasts de notificação com badge no sino
- Alertas inteligentes (toasts no primeiro acesso, badge nos demais)
- Favicon "FIN" SVG inline
- Botão Voltar ao Topo com fade suave
- Meta tags SEO e Open Graph completos
- Seletores Mês/Ano no header funcionam no Safari/iOS

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
1. Abra o arquivo no Chrome (Android) ou Safari (iOS)
2. Menu → "Adicionar à tela inicial"
3. Use como app nativo

> **Não requer servidor, Node.js, banco de dados ou internet.**  
> Todos os dados são salvos no `localStorage` do navegador.

---

## 🗃️ Estrutura dos Dados

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
| CSS3 | Design mobile-first, variáveis CSS, dark mode |
| JavaScript ES6+ | Toda a lógica da aplicação (sem frameworks) |
| Chart.js v4.5.1 | Gráficos de pizza e linha (embutido inline) |
| localStorage | Persistência de dados sem backend |

---

## 📋 Changelog

| Versão | Principais mudanças |
|--------|-------------------|
| v38 | Status pago/pendente por lançamento, filtro por status |
| v37 | Manual integrado com busca, botão ❓ no header |
| v36 | Extrato por Item: agrupamento corrigido, ordenação A-Z/Data, exportação XLS/PDF |
| v35 | Extrato com 3 abas: Mês, Por Item e Benefícios |
| v34 | Bug de edição corrigido, modal para repetições, Safari fix |
| v33 | Benefícios movidos para aba do Extrato, separados do extrato comum |
| v32 | Busca por tags, exportação XLS/PDF no extrato |
| v31 | Transferência entre contas, tags, comprovante, repetição personalizada |
| v30 | Chart.js inline (sem CDN), linha branca corrigida, foto de perfil |
| v29 | Recuperação de senha, modo visitante |
| v28 | Partículas no header, favicon FIN, botão voltar ao topo, pizza por Multi-Contas |
| v27 | Filtros multi-seleção no extrato |
| v26 | Cartão de Débito, Crypto, edição de contas com modal |
| v25 | Gestão Multi-Contas com exclusão segura e aviso |
| v24 | Filtro do extrato por tipo de conta agrupado |
| v23 | Padronização Config, totais dinâmicos no extrato |
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

> 💡 **Dica:** Para backup dos seus dados, use **Configurações → Sistema → Exportar Backup JSON**. Guarde o arquivo em local seguro — limpar o cache do navegador apaga os dados.
