## 📦 **Requisitos Funcionais Detalhados para Testes Manuais**



### 🔐 **RF01 - Autenticação de Usuário**

  * O sistema deve permitir que o usuário realize login com login e senha válidos.

  * O sistema deve exibir mensagens de erro em caso de login inválido.

  * O sistema deve manter o usuário conectado quando a opção "Manter conectado" estiver marcada.

---

### 🏠 **RF02 - Página Inicial**

**Descrição**: Após o login, o sistema deve exibir o resumo da academia com indicadores.

* **Funcionalidades esperadas**:

  * Saudação com o nome do usuário e a data atual.
  * Filtro de período para os indicadores.
  * Cards de: Clientes Ativos, Clientes Ausentes, Sem Matrículas, Personais, Matrículas e Desistências no período.
  * Navegação funcional pelo menu lateral.

---

### 👤 **RF03 - Gestão de Clientes**

**Descrição**: O sistema deve permitir o cadastro e a consulta dos alunos da academia.

* **Funcionalidades esperadas**:

  * Listagem de todos os clientes cadastrados.
  * Filtros de busca por código, nome, status, situação, plano e personal.
  * Botão "Novo Cliente" para cadastrar um cliente.
  * Campos obrigatórios: Nome, Status, Sexo e Data de Nascimento.
  * Opção de visualizar o perfil do cliente.

---

### 📝 **RF04 - Matrículas**

**Descrição**: O sistema deve permitir matricular um cliente em um plano.

* **Funcionalidades esperadas**:

  * Listagem das matrículas com cliente, plano e status.
  * Busca por código e nome.
  * Cadastro de matrícula com cliente, modalidade, datas, tipo de pagamento e valores.
  * Cálculo do valor total.

---

### 💳 **RF05 - Planos**

**Descrição**: O sistema deve permitir o cadastro dos planos da academia.

* **Funcionalidades esperadas**:

  * Listagem dos planos com valor, periodicidade e quantidade de alunos.
  * Filtro por código, nome e status.
  * Botão "Novo Plano" para cadastrar um plano.
  * Ranking dos planos com mais alunos.

---

### 📏 **RF06 - Avaliações Físicas**

**Descrição**: O sistema deve permitir agendar avaliações físicas dos alunos.

* **Funcionalidades esperadas**:

  * Listagem das avaliações com aluno, data, personal e status (Pendente/Realizado).
  * Filtro por código, nome e status.
  * Cadastro de avaliação com aluno, personal, data e hora.

---

### 🏋️ **RF07 - Fichas de Treino**

**Descrição**: O sistema deve permitir montar fichas de treino para os alunos.

* **Funcionalidades esperadas**:

  * Listagem das fichas com filtro por aluno e status.
  * Cadastro de ficha com aluno, personal, datas e objetivo.
  * Biblioteca de exercícios separada por grupo muscular.

---

### 👥 **RF08 - Turmas e Check-in**

**Descrição**: O sistema deve permitir organizar turmas e controlar a presença dos alunos.

* **Funcionalidades esperadas**:

  * Listagem das turmas com horário, dias da semana e status.
  * Cadastro de turma com nome, horário e dias.
  * Check-in manual pelo código do cliente.
  * Consulta de presenças por período.

---

### 💰 **RF09 - Financeiro**

**Descrição**: O sistema deve controlar as contas a receber e a pagar da academia.

* **Funcionalidades esperadas**:

  * Filtro de contas por data e status (Pendente, Recebido/Pago, Vencido, Cancelado).
  * Cadastro de conta a receber e de conta a pagar.
  * Cards com os totais do período.

---

### 📈 **RF10 - Relatórios**

**Descrição**: O sistema deve permitir a geração de relatórios em PDF.

* **Funcionalidades esperadas**:

  * Selecionar tipo de relatório (Ex: Clientes, Matrículas, Contas a Receber).
  * Definir data de início e fim.
  * Gerar e visualizar relatório.

---

### 🧑‍💼 **RF11 - Colaboradores**

**Descrição**: O sistema deve permitir o cadastro da equipe da academia.

* **Funcionalidades esperadas**:

  * Listagem dos colaboradores com código, nome e status.
  * Busca por código e nome.
  * Cards de colaboradores cadastrados, ativos e personais.
  * Botão "Novo Colaborador" para cadastrar um colaborador.

---

### 🏷️ **RF12 - Funções**

**Descrição**: O sistema deve permitir o cadastro das funções dos colaboradores.

* **Funcionalidades esperadas**:

  * Listagem das funções com tipo (Interno/Externo), se é personal e se é avaliador.
  * Filtro por código, nome e tipo.
  * Botão "Nova Função" para cadastrar uma função.

---

### 🚚 **RF13 - Fornecedores**

**Descrição**: O sistema deve permitir o cadastro dos fornecedores da academia.

* **Funcionalidades esperadas**:

  * Listagem dos fornecedores com código, nome e status.
  * Busca por código e nome.
  * Botão "Novo Fornecedor" para cadastrar um fornecedor.

---

### 📞 **RF14 - Prospecção**

**Descrição**: O sistema deve permitir acompanhar os interessados (leads) em se matricular.

* **Funcionalidades esperadas**:

  * Listagem dos leads com data e estágio.
  * Busca por nome e filtro por estágio (Novo Contato, Interessado, Fez Aula Experimental, Proposta, Fechado).
  * Botão "Adicionar Lead" para cadastrar um lead.

---

### 🛒 **RF15 - Produtos**

**Descrição**: O sistema deve permitir o cadastro de produtos para venda ou para troca por pontos.

* **Funcionalidades esperadas**:

  * Listagem dos produtos com tipo (Venda/Pontuação) e status.
  * Filtro por código, nome, status e tipo.
  * Botão "Novo" para cadastrar um produto.

---

### 💪 **RF16 - Grupos Musculares**

**Descrição**: O sistema deve permitir organizar os exercícios por grupo muscular.

* **Funcionalidades esperadas**:

  * Listagem dos grupos com o tipo de membro (Superiores, Inferiores, Aeróbio).
  * Filtro por código, nome e tipo de membro.
  * Paginação da lista.

---

### 🎯 **RF17 - Objetivos de Treino**

**Descrição**: O sistema deve permitir o cadastro dos objetivos usados nas fichas de treino.

* **Funcionalidades esperadas**:

  * Listagem dos objetivos cadastrados.
  * Busca por código e nome.
  * Botão "Novo Objetivo" para cadastrar um objetivo.

---

### 📄 **RF18 - Modelos de Ficha**

**Descrição**: O sistema deve permitir consultar os modelos de ficha de treino.

* **Funcionalidades esperadas**:

  * Listagem dos modelos com título e criador.
  * Cards de modelos, criadores e modelos sem criador.
  * Uso do modelo ao cadastrar uma ficha de treino.

---

### 🗂️ **RF19 - Grupos de Planos**

**Descrição**: O sistema deve permitir agrupar os planos da academia.

* **Funcionalidades esperadas**:

  * Listagem dos grupos com descrição, status, exibição na home e tipo de caixa.
  * Filtro por código, nome, status e tipo de caixa (Interno/Externo).

---

### 📑 **RF20 - Modelos de Contrato**

**Descrição**: O sistema deve permitir o cadastro dos modelos de contrato da academia.

* **Funcionalidades esperadas**:

  * Listagem dos modelos com código, nome e status.
  * Botão "Adicionar Modelo Contrato" para cadastrar um modelo.

---

### 🧾 **RF21 - Despesas Fixas**

**Descrição**: O sistema deve permitir o cadastro das despesas que se repetem.

* **Funcionalidades esperadas**:

  * Listagem das despesas com valor, recorrência e status.
  * Filtro por código, nome, status e recorrência.
  * Card com o valor total listado.

---

### 💵 **RF22 - Tipos de Pagamento**

**Descrição**: O sistema deve permitir o cadastro das formas de pagamento aceitas.

* **Funcionalidades esperadas**:

  * Listagem dos tipos com tipo (Débito/Crédito) e status.
  * Filtro por código, nome, status e tipo.
  * Botão "Novo" para cadastrar um tipo de pagamento.

---

### 💳 **RF23 - Bandeiras de Cartão**

**Descrição**: O sistema deve permitir o cadastro das bandeiras de cartão aceitas.

* **Funcionalidades esperadas**:

  * Listagem das bandeiras com código e nome.
  * Botão "Nova Bandeira" para cadastrar uma bandeira.

---

### 📎 **RF24 - Tipos de Documentos**

**Descrição**: O sistema deve permitir o cadastro dos tipos de documento usados em contas e colaboradores.

* **Funcionalidades esperadas**:

  * Listagem dos tipos com a aplicação (Conta/Fornecedor ou Colaborador).
  * Filtro por código, nome e aplicação.
  * Botão "Novo Tipo" para cadastrar um tipo de documento.

---

### 🏦 **RF25 - Caixas**

**Descrição**: O sistema deve permitir abrir e fechar o caixa da academia.

* **Funcionalidades esperadas**:

  * Listagem dos caixas com data inicial, data final e status (Aberto/Fechado).
  * Filtro por data inicial, data final e status.
  * Botão "Abrir Caixa".
  * Paginação da lista.

---

### 💰 **RF26 - Pagar.me**

**Descrição**: O sistema deve exibir os recebimentos feitos pela integração com a Pagar.me.

* **Funcionalidades esperadas**:

  * Saldo disponível para saque, em processamento e recebíveis futuros.
  * Gráfico de recebimentos e divisão por meio de pagamento.
  * Lista de transações recentes e repasses.

---

### 🏃 **RF27 - Atividades**

**Descrição**: O sistema deve permitir o cadastro de atividades que valem pontos para os alunos.

* **Funcionalidades esperadas**:

  * Listagem das atividades com descrição e pontuação.
  * Busca por código e nome.
  * Botão "Nova Atividade" para cadastrar uma atividade.

---

### 🏆 **RF28 - Pontuação**

**Descrição**: O sistema deve permitir criar campanhas de pontuação para os alunos.

* **Funcionalidades esperadas**:

  * Listagem das pontuações com tipo (Mensal/Período) e status.
  * Filtro por código, nome e status.
  * Botão "Nova Pontuação" para cadastrar uma campanha.

---

### 📊 **RF29 - Enquetes**

**Descrição**: O sistema deve permitir criar enquetes para os alunos responderem.

* **Funcionalidades esperadas**:

  * Listagem das enquetes com pergunta e status.
  * Filtro por código, nome e status.
  * Cards de enquetes, ativas, inativas e respostas.
  * Botão "Nova Enquete" para cadastrar uma enquete.

---

### 🩺 **RF30 - Fichas de Anamnese**

**Descrição**: O sistema deve permitir aplicar questionários de saúde aos alunos.

* **Funcionalidades esperadas**:

  * Listagem das fichas aplicadas com status (Concluído/Pendente).
  * Filtro por status.
  * Botão "Nova Anamnese" para aplicar uma ficha.

---

### 📋 **RF31 - Modelos de Anamnese**

**Descrição**: O sistema deve permitir montar modelos de questionário de anamnese.

* **Funcionalidades esperadas**:

  * Listagem dos modelos com quantidade de perguntas e aplicações.
  * Filtro por status.
  * Opções de editar e visualizar (Preview) o modelo.
  * Botão "Novo Modelo".

---

### 🗃️ **RF32 - Categorias de Anamnese**

**Descrição**: O sistema deve permitir organizar as perguntas de anamnese em categorias.

* **Funcionalidades esperadas**:

  * Listagem das categorias com status.
  * Filtro por status.
  * Botão "Nova Categoria".

---

### ❓ **RF33 - Perguntas de Anamnese**

**Descrição**: O sistema deve permitir o cadastro das perguntas usadas nos modelos de anamnese.

* **Funcionalidades esperadas**:

  * Listagem das perguntas com status.
  * Filtro por código, nome e status.
  * Botão "Nova Pergunta".

---

### 🤖 **RF34 - Inteligência e Automação**

**Descrição**: O sistema deve executar automações como a análise de risco de evasão e os aniversariantes.

* **Funcionalidades esperadas**:

  * Lista das automações ativas com frequência, canal, última execução e resultado.
  * Botões "Executar agora", "Configurar" e "Ver resultados".
  * Lista das automações em desenvolvimento.

---

### 📈 **RF35 - Resultados da Inteligência**

**Descrição**: O sistema deve exibir o que as automações identificaram na academia.

* **Funcionalidades esperadas**:

  * Filtro por período (Hoje, Últimos 7, 30 e 90 dias).
  * Cards de automações executadas, alunos em risco, aniversariantes, avaliações vencendo e inadimplentes.
  * Histórico do que foi identificado e ranking das automações.

---

### 📱 **RF36 - Aplicativo**

**Descrição**: O sistema deve permitir a comunicação com os alunos pelo aplicativo.

* **Funcionalidades esperadas**:

  * Cards de usuários do app e novos posts.
  * Criação e listagem de notificações para os alunos.
  * Moderação das postagens e das denúncias.

---

### ⚙️ **RF37 - Configurações**

**Descrição**: O sistema deve permitir configurar o funcionamento da academia.

* **Funcionalidades esperadas**:

  * Abas: Home, Biometria, Avaliação, Aniversário, Pagamento, Integrações e Design.
  * Configurações de presença, academia Box, turmas, dias de ausência, multa e juros.
  * Botões "Cancelar" e "Salvar Configurações".

---

### 📦 **RF38 - SifitBox (Crossfit)**

**Descrição**: O sistema deve permitir gerenciar as aulas de crossfit quando a academia for marcada como Box.

* **Funcionalidades esperadas**:

  * Telas de Aulas, Box - Turmas e Categorias Crossfit.
  * Busca de aulas por período e botão "Gerar aulas".
  * As telas aparecem no menu apenas com a configuração "Academia marcada como Box?" ativa.

---

### 📉 **RF39 - Dashboard**

**Descrição**: O sistema deve exibir gráficos gerenciais da academia.

* **Funcionalidades esperadas**:

  * Bloco da Inteligência Sifit com alunos em risco, aniversariantes, avaliações vencendo e frequência em queda.
  * Gráficos de clientes, matrículas, contas a receber, cancelamentos e avaliações.

---

### 🪪 **RF40 - Perfil do Cliente**

**Descrição**: O sistema deve exibir um resumo completo de cada cliente.

* **Funcionalidades esperadas**:

  * Dados pessoais, idade e data de cadastro.
  * Análise de risco, desempenho e frequência.
  * Matrícula atual, últimas presenças e situação financeira.
  * Ações rápidas: enviar mensagem, agendar avaliação, registrar pagamento e aplicar anamnese.
