## 🧪 **Plano de Testes - SIFIT**

### 📌 1. **Identificação**

* **Nome do Projeto**: SIFIT - Sistema para Academias
* **Versão Avaliada**: Ambiente de testes disponibilizado pelo professor
* **Ambiente de Testes**: [https://sifit.centrion.com.br](https://sifit.centrion.com.br)
* **Tipo de Teste**: Teste Funcional Manual
* **Data do Documento**: 02/10/2026
* **Responsável**: Hendreu Satoshi Zampieri Itami (240061)

---

### 🎯 2. **Objetivo**

Realizar a verificação manual dos principais requisitos funcionais do SIFIT com foco em validação dos fluxos críticos de uma academia, mensagens de erro, comportamento esperado e integridade das informações exibidas na interface web.

---

### 🧩 3. **Escopo**

**Incluído:**

* Autenticação de usuário
* Página inicial
* Gestão de clientes
* Matrículas
* Planos
* Avaliações físicas
* Fichas de treino
* Turmas e check-in
* Financeiro e relatórios
* Cadastros auxiliares (colaboradores, funções, fornecedores, produtos, tipos de pagamento etc.)
* Engajamento (atividades, pontuação, enquetes e aplicativo)
* Anamnese
* Inteligência e automação
* Configurações e SifitBox

**Excluído:**

* Pagamentos e saques reais pela Pagar.me
* Aplicativo do aluno (celular)
* Envio de mensagens reais por WhatsApp
* Testes de performance ou carga

---

### 🔧 4. **Ferramentas Utilizadas**

* Navegador Google Chrome
* Ferramentas de inspeção do navegador (DevTools)
* Jam (gravação dos vídeos de evidência)
* MySQL Workbench (conferência dos dados no banco)

---

### 🧪 5. **Técnicas de Teste**

* Particionamento de equivalência
* Análise de valor limite
* Caminho feliz (Happy Path)
* Testes negativos
* Testes exploratórios

---

### 📄 6. **Critérios de Aceitação**

* Todos os casos de teste devem passar com sucesso, conforme o resultado esperado.
* Nenhuma falha crítica deve estar presente em funcionalidades principais.
* Mensagens de erro e validações devem ser consistentes.

---

### 🚦 7. **Critérios de Saída (Exit Criteria)**

* Todos os testes do escopo foram executados.
* Falhas foram registradas, analisadas e reexecutadas se necessário.
* Documentação de evidências de sucesso e falhas está completa.

---

### ⏱️ 8. **Cronograma Estimado**

| Atividade                   | Data Início | Data Fim   |
| --------------------------- | ----------- | ---------- |
| Planejamento de Testes      | 30/09/2026  | 02/10/2026 |
| Criação de Casos de Teste   | 05/10/2026  | 16/10/2026 |
| Execução dos Testes Manuais | 19/10/2026  | 25/10/2026 |
| Registro e Report de Bugs   | 19/10/2026  | 27/10/2026 |
| Encerramento e Evidências   | 28/10/2026  | 30/10/2026 |

---

### 📋 9. **Módulos a Serem Testados**

| Código RF | Módulo                   | Prioridade |
| --------- | ------------------------ | ---------- |
| RF01      | Login                    | Alta       |
| RF02      | Página Inicial           | Média      |
| RF03      | Clientes                 | Alta       |
| RF04      | Matrículas               | Alta       |
| RF05      | Planos                   | Alta       |
| RF06      | Avaliações Físicas       | Média      |
| RF07      | Fichas de Treino         | Média      |
| RF08      | Turmas e Check-in        | Média      |
| RF09      | Financeiro               | Alta       |
| RF10      | Relatórios               | Baixa      |
| RF11      | Colaboradores            | Média      |
| RF12      | Funções                  | Baixa      |
| RF13      | Fornecedores             | Baixa      |
| RF14      | Prospecção               | Média      |
| RF15      | Produtos                 | Baixa      |
| RF16      | Grupos Musculares        | Baixa      |
| RF17      | Objetivos de Treino      | Baixa      |
| RF18      | Modelos de Ficha         | Baixa      |
| RF19      | Grupos de Planos         | Baixa      |
| RF20      | Modelos de Contrato      | Baixa      |
| RF21      | Despesas Fixas           | Média      |
| RF22      | Tipos de Pagamento       | Média      |
| RF23      | Bandeiras de Cartão      | Baixa      |
| RF24      | Tipos de Documentos      | Baixa      |
| RF25      | Caixas                   | Alta       |
| RF26      | Pagar.me                 | Média      |
| RF27      | Atividades               | Baixa      |
| RF28      | Pontuação                | Baixa      |
| RF29      | Enquetes                 | Baixa      |
| RF30      | Fichas de Anamnese       | Média      |
| RF31      | Modelos de Anamnese      | Baixa      |
| RF32      | Categorias de Anamnese   | Baixa      |
| RF33      | Perguntas de Anamnese    | Baixa      |
| RF34      | Inteligência e Automação | Média      |
| RF35      | Resultados da Inteligência | Média      |
| RF36      | Aplicativo               | Média      |
| RF37      | Configurações            | Média      |
| RF38      | SifitBox (Crossfit)      | Baixa      |
| RF39      | Dashboard                | Média      |
| RF40      | Perfil do Cliente        | Alta       |

---

### 🐞 10. **Gestão de Defeitos**

* Bugs serão documentados com:

  * Título
  * Descrição
  * Passos para reproduzir
  * Evidência (vídeo gravado no Jam)
  * Gravidade (Crítica, Alta, Média, Baixa)
* Ferramenta sugerida: Jam

---

### 📌 11. **Riscos Identificados**

| Risco                                       | Impacto | Mitigação                                     |
| ------------------------------------------- | ------- | --------------------------------------------- |
| Sistema fora do ar                          | Alto    | Tentar novamente após intervalo               |
| Outros alunos alterando dados do ambiente   | Médio   | Usar nomes próprios nos cadastros de teste    |
| Testes limitados a um único usuário         | Médio   | Documentar esse limite no escopo              |

---

### 📁 12. **Entregáveis**

* Plano de Testes (.md)
* Casos de Teste (.md)
* Evidências de Execução (vídeos no Jam)
* Registro de Bugs (se houver)
* Registro de Melhoria (se houver)
* Relatório Final de Execução
