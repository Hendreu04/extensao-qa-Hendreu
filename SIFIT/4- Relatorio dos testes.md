# ✅ **Relatório Final de Execução de Testes - SIFIT**

**Sistema testado:** SIFIT - Sistema para Academias (ambiente de testes)
**Responsável:** Hendreu Satoshi Zampieri Itami (240061)
**Data de execução:** 18/10/2026 a 23/10/2026
**Ambiente:** Ambiente de testes disponibilizado pelo professor

* Sistema operacional: Windows 11
* Navegador: Chrome 155.0.8059.85
* URL: [https://sifit.centrion.com.br](https://sifit.centrion.com.br)
* Banco de dados consultado: MySQL (somente consultas `SELECT`, `SHOW` e `DESCRIBE`)

---

## 📊 **Resumo da Execução**

| Total de Casos de Teste | Casos Passaram | Casos Falharam | Casos Bloqueados | Bugs Registrados |
| ----------------------- | -------------- | -------------- | ---------------- | ---------------- |
| 120                     | 87 (22 com ressalva) | 30             | 3                | 58               |

> **Passou com ressalva:** o caso atingiu o resultado esperado, mas foi observado algum problema na tela (mensagem genérica, informação incoerente etc.).
> **Bloqueado:** o caso não pôde ser executado por causa de outro defeito.

---

## 🔍 **Cobertura por Módulo**

| Código RF | Módulo                   | Casos Testados | Casos Passaram | Bugs encontrados | Bug(s) Associado(s) |
| --------- | ------------------------ | -------------- | -------------- | ---------------- | ------------------- |
| RF01      | Login                    | 3              | 2              | 1                | BUG-001 |
| RF02      | Página Inicial           | 3              | 3              | 2                | BUG-002, BUG-003 |
| RF03      | Clientes                 | 3              | 3              | 2                | BUG-004, BUG-005 |
| RF04      | Matrículas               | 3              | 3              | 4                | BUG-009, BUG-010, BUG-011, BUG-019 |
| RF05      | Planos                   | 3              | 1              | 3                | BUG-006, BUG-007, BUG-008 |
| RF06      | Avaliações Físicas       | 3              | 3              | 0                | - |
| RF07      | Fichas de Treino         | 3              | 2              | 1                | BUG-013 |
| RF08      | Turmas e Check-in        | 3              | 1              | 3                | BUG-014, BUG-015, BUG-016 |
| RF09      | Financeiro               | 3              | 2              | 2                | BUG-017, BUG-018 |
| RF10      | Relatórios               | 3              | 1              | 2                | BUG-020, BUG-021 |
| RF11      | Colaboradores            | 3              | 2              | 3                | BUG-022, BUG-023, BUG-024 |
| RF12      | Funções                  | 3              | 3              | 0                | - |
| RF13      | Fornecedores             | 3              | 3              | 2                | BUG-025, BUG-026 |
| RF14      | Prospecção               | 3              | 3              | 0                | - |
| RF15      | Produtos                 | 3              | 2              | 2                | BUG-027, BUG-028 |
| RF16      | Grupos Musculares        | 3              | 2              | 2                | BUG-029, BUG-030 |
| RF17      | Objetivos de Treino      | 2 (1 bloqueado) | 1              | 1                | BUG-012 |
| RF18      | Modelos de Ficha         | 1 (2 bloqueados) | 1              | 1                | BUG-031 |
| RF19      | Grupos de Planos         | 3              | 3              | 0                | - |
| RF20      | Modelos de Contrato      | 3              | 1              | 2                | BUG-032, BUG-033 |
| RF21      | Despesas Fixas           | 3              | 3              | 0                | - |
| RF22      | Tipos de Pagamento       | 3              | 0              | 3                | BUG-034, BUG-035, BUG-036 |
| RF23      | Bandeiras de Cartão      | 3              | 1              | 1                | BUG-037 |
| RF24      | Tipos de Documentos      | 3              | 3              | 0                | - |
| RF25      | Caixas                   | 3              | 3              | 2                | BUG-038, BUG-039 |
| RF26      | Pagar.me                 | 3              | 2              | 1                | BUG-040 |
| RF27      | Atividades               | 3              | 2              | 1                | BUG-041 |
| RF28      | Pontuação                | 3              | 3              | 1                | BUG-042 |
| RF29      | Enquetes                 | 3              | 2              | 1                | BUG-043 |
| RF30      | Fichas de Anamnese       | 3              | 1              | 3                | BUG-044, BUG-045, BUG-046 |
| RF31      | Modelos de Anamnese      | 3              | 2              | 2                | BUG-047, BUG-048 |
| RF32      | Categorias de Anamnese   | 3              | 3              | 1                | BUG-049 |
| RF33      | Perguntas de Anamnese    | 3              | 2              | 2                | BUG-050, BUG-051 |
| RF34      | Inteligência e Automação | 3              | 3              | 0                | - |
| RF35      | Resultados da Inteligência | 3              | 2              | 2                | BUG-052, BUG-053 |
| RF36      | Aplicativo               | 3              | 3              | 0                | - |
| RF37      | Configurações            | 3              | 3              | 2                | BUG-054, BUG-055 |
| RF38      | SifitBox (Crossfit)      | 3              | 2              | 1                | BUG-056 |
| RF39      | Dashboard                | 3              | 2              | 1                | BUG-057 |
| RF40      | Perfil do Cliente        | 3              | 3              | 1                | BUG-058 |

---

## 🐞 **Resumo dos Bugs Reportados**

| ID      | Título | Severidade | Status |
| ------- | ------ | ---------- | ------ |
| BUG-001 | Opção "Manter conectado" não mantém o usuário logado | Média | Aberto |
| BUG-002 | Quantidade de clientes ausentes diferente entre a Página Inicial e a tela de Clientes | Média | Aberto |
| BUG-003 | Valor em aberto aparece zerado mesmo com mensalidade vencida | Alta | Aberto |
| BUG-004 | Paginação exibe 3 páginas quando a busca retorna apenas 1 cliente | Baixa | Aberto |
| BUG-005 | Filtros da tela de Clientes vêm preenchidos e não correspondem à lista exibida | Média | Aberto |
| BUG-006 | Erro genérico ao salvar plano sem grupo selecionado | Média | Aberto |
| BUG-007 | Quantidade de alunos do plano diferente entre o ranking e a lista de planos | Média | Aberto |
| BUG-008 | Mensalidade e Receita Estimada aparecem zeradas em plano com valor e aluno | Média | Aberto |
| BUG-009 | Mensagem "Selecione o Tipo de Pagamento" continua na tela após selecionar o tipo | Baixa | Aberto |
| BUG-010 | Tela de pagamento da matrícula abre com tipo de pagamento vazio e título repetido | Baixa | Aberto |
| BUG-011 | Card "Cadastradas este Mês" mostra 0 com matrícula cadastrada no mês | Média | Aberto |
| BUG-012 | Não é possível cadastrar objetivo de treino | Alta | Aberto |
| BUG-013 | Não é possível criar ficha de treino porque a lista de objetivos vem vazia | Alta | Aberto |
| BUG-014 | Sistema aceita turma com horário inicial igual ao horário final | Média | Aberto |
| BUG-015 | Check-in confirmado no banco aparece como "Pendente" e não conta como presente | Alta | Aberto |
| BUG-016 | Horário de entrada do check-in exibido 3 horas adiantado | Média | Aberto |
| BUG-017 | Conta a receber em dinheiro pede bandeira de cartão e a lista de bandeiras vem vazia | Alta | Aberto |
| BUG-018 | Card "Total a Pagar" mostra 0 com conta pendente de R$ 200,00 na lista | Alta | Aberto |
| BUG-019 | Mensagem genérica ao salvar matrícula com dia de vencimento anterior à data inicial | Baixa | Aberto |
| BUG-020 | Relatório é gerado com data final anterior à data inicial | Baixa | Aberto |
| BUG-021 | Relatório de Clientes é baixado corrompido e não abre | Alta | Aberto |
| BUG-022 | "Erro no servidor" ao salvar colaborador com campos obrigatórios vazios | Média | Aberto |
| BUG-023 | Cadastro de colaborador aceita CPF inválido | Média | Aberto |
| BUG-024 | Sistema permite cadastrar colaborador com login já usado por outro colaborador | Alta | Aberto |
| BUG-025 | Erro genérico ao salvar fornecedor preenchendo apenas o campo obrigatório | Média | Aberto |
| BUG-026 | Cadastro de fornecedor aceita CNPJ inválido | Média | Aberto |
| BUG-027 | Produto do tipo "Venda" é salvo sem preço | Média | Aberto |
| BUG-028 | Sistema permite cadastrar produto sem nome | Média | Aberto |
| BUG-029 | Total de grupos musculares não bate com a soma por tipo de membro | Média | Aberto |
| BUG-030 | Imagens dos grupos musculares aparecem quebradas | Baixa | Aberto |
| BUG-031 | Não é possível criar modelo de ficha de treino | Alta | Aberto |
| BUG-032 | Lista de Modelos Contrato aparece vazia mesmo com modelos cadastrados | Alta | Aberto |
| BUG-033 | Horário de criação é gravado no formato de 12 horas | Média | Aberto |
| BUG-034 | Sistema permite cadastrar tipo de pagamento sem nome | Média | Aberto |
| BUG-035 | Tipo de pagamento cadastrado como "Ativo" aparece como "Inativo" | Alta | Aberto |
| BUG-036 | Filtro de status em Tipos de Pagamento não retorna nenhum registro | Média | Aberto |
| BUG-037 | Lista de Bandeiras de Cartão aparece vazia mesmo com bandeiras cadastradas | Alta | Aberto |
| BUG-038 | Tela de Caixas abre ignorando o período exibido nos filtros | Média | Aberto |
| BUG-039 | "Erro no servidor" ao abrir caixa sem selecionar o local | Média | Aberto |
| BUG-040 | Painel Pagar.me mostra R$ 38.420,00 em recebimentos sem nenhuma transação | Alta | Aberto |
| BUG-041 | Sistema permite cadastrar atividade sem nome | Média | Aberto |
| BUG-042 | Pontuação sem datas é salva com período "0000-00-00 — 0000-00-00" | Baixa | Aberto |
| BUG-043 | Não é possível cadastrar enquete | Alta | Aberto |
| BUG-044 | Anamnese pode ser aplicada sem selecionar aluno e termina com "Erro no servidor" | Média | Aberto |
| BUG-045 | Modelo de anamnese informa 2 perguntas, mas exibe apenas 1 e a revisão mostra outra pergunta | Média | Aberto |
| BUG-046 | Anamnese aplicada ao aluno não é gravada | Alta | Aberto |
| BUG-047 | Preview do modelo de anamnese não mostra as perguntas cadastradas | Média | Aberto |
| BUG-048 | Modelo de anamnese mostra 3 aplicações, mas nenhuma ficha existe | Baixa | Aberto |
| BUG-049 | Card "Com perguntas" conta categoria recém-criada sem nenhuma pergunta | Baixa | Aberto |
| BUG-050 | Sistema permite cadastrar pergunta de anamnese sem nome e sem texto | Média | Aberto |
| BUG-051 | Cadastro de pergunta de anamnese não tem campo para escolher a categoria | Média | Aberto |
| BUG-052 | Resultados da Inteligência apontam 42 inadimplentes, mas a Página Inicial mostra R$ 0,00 em aberto | Alta | Aberto |
| BUG-053 | Filtro "Hoje" dos Resultados da Inteligência não atualiza todos os cards | Baixa | Aberto |
| BUG-054 | Campo "Dias para contar cliente como ausente" aceita valor negativo | Média | Aberto |
| BUG-055 | Senha do aparelho biométrico é exibida em texto aberto nas Configurações | Média | Aberto |
| BUG-056 | Botão "Gerar aulas" do SifitBox não gera aulas nem exibe mensagem | Alta | Aberto |
| BUG-057 | Tela Dashboard exibe o título "Despesas Fixas" | Baixa | Aberto |
| BUG-058 | Perfil do cliente mostra check-in registrado, mas "Últimas Presenças" aparece vazio | Média | Aberto |

---

## 📈 **Gráfico de Resultado (Texto Alternativo)**

**Casos por status:**

* ✅ Passaram: 65
* ⚠️ Passaram com ressalva: 22
* ❌ Falharam: 30
* ⛔ Bloqueados: 3

**Severidade dos bugs:**

* 🟥 Alta: 17
* 🟨 Média: 30
* 🟩 Baixa: 11

---

## 📁 **Evidências e Documentos**

* ✔️ [Análise de Requisitos](1-Analise%20de%20requisitos.md)
* ✔️ [Plano de Testes](2-plano%20de%20testes.md)
* ✔️ [Casos de Teste](Cenarios%20de%20testes)
* 🐛 [Relatório de Bugs com Evidências em Vídeo](3-Relatorio-de-Bugs.md)
* 📹 Evidências em vídeo hospedadas no [Jam.dev](https://jam.dev)

---

## 🎥 **Evidências por Caso de Teste**

Todos os casos foram gravados com o Jam. Quando o caso foi refeito (reteste), os dois vídeos estão listados.

| Caso | Título | Resultado | Bug(s) | Evidência(s) |
| ---- | ------ | --------- | ------ | ------------ |
| C01-CT01 | Login com as credenciais válidas | Passou | - | [Vídeo](https://jam.dev/c/66f6a577-62ca-43e5-af1e-d50b385b1762) |
| C01-CT02 | Tentativa de login com senha incorreta | Passou | - | [Vídeo](https://jam.dev/c/b70ac6e9-0cab-4b03-b165-84e7ab1bf0fd) |
| C01-CT03 | Login com a opção manter conectado | Falhou | BUG-001 | [Vídeo](https://jam.dev/c/5f641348-c322-4dde-9193-8ab76ba8e770) |
| C02-CT01 | Acesso à Página Inicial após login bem-sucedido | Passou | BUG-002, BUG-003 | [Vídeo](https://jam.dev/c/86c798a0-5b72-4fb2-bc0a-7f134f79ff58) |
| C02-CT02 | Atualizar a página em uma tela interna | Passou | - | [Vídeo](https://jam.dev/c/86c798a0-5b72-4fb2-bc0a-7f134f79ff58) |
| C02-CT03 | Navegação pelo menu lateral | Passou | - | [Vídeo](https://jam.dev/c/86c798a0-5b72-4fb2-bc0a-7f134f79ff58) |
| C03-CT01 | Adicionar novo cliente com dados válidos | Passou | - | [Vídeo](https://jam.dev/c/7e8be00d-94a9-4a63-93e8-88c9c38faab4) |
| C03-CT02 | Tentar adicionar cliente sem preencher campos obrigatórios | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/4a1e8f13-dd2c-49df-808c-32a938ad143b) |
| C03-CT03 | Pesquisar cliente já cadastrado | Passou | BUG-004, BUG-005 | [Vídeo](https://jam.dev/c/7e8be00d-94a9-4a63-93e8-88c9c38faab4) |
| C04-CT01 | Cadastrar matrícula com dados válidos | Passou | BUG-010, BUG-011 | [Vídeo 1](https://jam.dev/c/941b9966-edb4-4e75-9d37-31f95071a55d) [Vídeo 2](https://jam.dev/c/06e32ae4-06b8-4d29-937c-d7fee97cbf6c) |
| C04-CT02 | Tentar cadastrar matrícula sem selecionar cliente | Passou | - | [Vídeo](https://jam.dev/c/941b9966-edb4-4e75-9d37-31f95071a55d) |
| C04-CT03 | Tentar cadastrar matrícula sem tipo de pagamento | Passou | BUG-009, BUG-019 | [Vídeo 1](https://jam.dev/c/941b9966-edb4-4e75-9d37-31f95071a55d) [Vídeo 2](https://jam.dev/c/a8950630-7a17-4426-a570-4c9b4a76e827) |
| C05-CT01 | Adicionar novo plano com dados válidos | Falhou | BUG-006 | [Vídeo 1](https://jam.dev/c/516e542a-5e59-4187-9379-bed8d372a748) [Vídeo 2](https://jam.dev/c/707ed084-77ce-4631-8406-2103a828bb1c) |
| C05-CT02 | Tentar adicionar plano sem nome | Passou | - | [Vídeo](https://jam.dev/c/516e542a-5e59-4187-9379-bed8d372a748) |
| C05-CT03 | Verificar quantidade de alunos por plano | Falhou | BUG-007, BUG-008 | [Vídeo](https://jam.dev/c/191aafea-be89-4847-9fad-2483724ea9ba) |
| C06-CT01 | Agendar avaliação com dados válidos | Passou | - | [Vídeo](https://jam.dev/c/d18a3aed-419c-426e-b425-a8ff3984f321) |
| C06-CT02 | Tentar agendar avaliação sem selecionar aluno | Passou | - | [Vídeo](https://jam.dev/c/d18a3aed-419c-426e-b425-a8ff3984f321) |
| C06-CT03 | Filtrar avaliações por status | Passou | - | [Vídeo](https://jam.dev/c/d18a3aed-419c-426e-b425-a8ff3984f321) |
| C07-CT01 | Cadastrar ficha de treino com dados válidos | Falhou | BUG-013 | [Vídeo 1](https://jam.dev/c/27b40cdf-4229-4b0a-adb0-cecc0c053d8a) [Vídeo 2](https://jam.dev/c/11966eaa-46d6-4084-9b42-2e2bcc6ee551) |
| C07-CT02 | Tentar cadastrar ficha sem selecionar aluno | Passou | - | [Vídeo](https://jam.dev/c/27b40cdf-4229-4b0a-adb0-cecc0c053d8a) |
| C07-CT03 | Adicionar exercício em um grupo muscular | Passou | - | [Vídeo](https://jam.dev/c/db33cca9-c252-49fc-b8a8-ad2fc4cba372) |
| C08-CT01 | Cadastrar turma com dados válidos | Passou (com ressalva) | BUG-014 | [Vídeo](https://jam.dev/c/824d0d2e-0223-4c8e-b5c3-f4f7d4181fdc) |
| C08-CT02 | Tentar cadastrar turma com horário final igual ao inicial | Falhou | BUG-014 | [Vídeo](https://jam.dev/c/824d0d2e-0223-4c8e-b5c3-f4f7d4181fdc) |
| C08-CT03 | Realizar check-in manual do aluno | Falhou | BUG-015, BUG-016 | [Vídeo 1](https://jam.dev/c/824d0d2e-0223-4c8e-b5c3-f4f7d4181fdc) [Vídeo 2](https://jam.dev/c/0f0778fe-246a-4fd1-bbca-2151b866fc2d) |
| C09-CT01 | Cadastrar conta a receber com dados válidos | Passou | BUG-017 | [Vídeo 1](https://jam.dev/c/3bdb4808-fb6f-452a-800f-50733c073b37) [Vídeo 2](https://jam.dev/c/21676c18-6d62-4959-aa27-99c1c41ab74a) |
| C09-CT02 | Tentar cadastrar conta a receber sem valor | Passou | - | [Vídeo](https://jam.dev/c/3bdb4808-fb6f-452a-800f-50733c073b37) |
| C09-CT03 | Verificar total das contas a pagar | Falhou | BUG-018 | [Vídeo](https://jam.dev/c/3bdb4808-fb6f-452a-800f-50733c073b37) |
| C10-CT01 | Gerar relatório de clientes | Falhou | BUG-021 | [Vídeo 1](https://jam.dev/c/be9e953b-120a-4b46-be9d-f5ce0f0e07fb) [Vídeo 2](https://jam.dev/c/c0aad349-ea7d-48d8-9e2b-92eb157d216d) |
| C10-CT02 | Gerar relatório com data de início maior que a de fim | Falhou | BUG-020 | [Vídeo 1](https://jam.dev/c/be9e953b-120a-4b46-be9d-f5ce0f0e07fb) [Vídeo 2](https://jam.dev/c/c0aad349-ea7d-48d8-9e2b-92eb157d216d) |
| C10-CT03 | Gerar relatório sem registros no período | Passou (com ressalva) | - | [Vídeo 1](https://jam.dev/c/be9e953b-120a-4b46-be9d-f5ce0f0e07fb) [Vídeo 2](https://jam.dev/c/c0aad349-ea7d-48d8-9e2b-92eb157d216d) |
| C11-CT01 | Adicionar novo colaborador com dados válidos | Passou (com ressalva) | BUG-023, BUG-024 | [Vídeo](https://jam.dev/c/64d30fb2-224f-4f30-848f-cb7adca31a22) |
| C11-CT02 | Tentar adicionar colaborador sem nome | Falhou | BUG-022 | [Vídeo](https://jam.dev/c/64d30fb2-224f-4f30-848f-cb7adca31a22) |
| C11-CT03 | Pesquisar colaborador já cadastrado | Passou | BUG-004 | [Vídeo](https://jam.dev/c/64d30fb2-224f-4f30-848f-cb7adca31a22) |
| C12-CT01 | Adicionar nova função com dados válidos | Passou | - | [Vídeo](https://jam.dev/c/cb883c0c-2c99-463f-94ef-680f3edfad66) |
| C12-CT02 | Tentar adicionar função sem nome | Passou | - | [Vídeo](https://jam.dev/c/b84d215f-0669-4a11-b715-bf72284b9d4c) |
| C12-CT03 | Filtrar funções por tipo | Passou | - | [Vídeo](https://jam.dev/c/cb883c0c-2c99-463f-94ef-680f3edfad66) |
| C13-CT01 | Adicionar novo fornecedor com dados válidos | Passou (com ressalva) | BUG-025, BUG-026 | [Vídeo](https://jam.dev/c/c76b43da-ac66-4235-9348-40a66add58cd) |
| C13-CT02 | Tentar adicionar fornecedor sem nome | Passou | - | [Vídeo](https://jam.dev/c/c76b43da-ac66-4235-9348-40a66add58cd) |
| C13-CT03 | Pesquisar fornecedor já cadastrado | Passou | - | [Vídeo](https://jam.dev/c/c76b43da-ac66-4235-9348-40a66add58cd) |
| C14-CT01 | Adicionar novo lead com dados válidos | Passou | - | [Vídeo](https://jam.dev/c/be809a93-2318-46ae-9e4f-580531801773) |
| C14-CT02 | Tentar adicionar lead sem nome | Passou | - | [Vídeo](https://jam.dev/c/be809a93-2318-46ae-9e4f-580531801773) |
| C14-CT03 | Filtrar leads por estágio | Passou | - | [Vídeo](https://jam.dev/c/be809a93-2318-46ae-9e4f-580531801773) |
| C15-CT01 | Adicionar novo produto com dados válidos | Passou (com ressalva) | BUG-027 | [Vídeo](https://jam.dev/c/52b224b2-eb8f-40bf-a669-3f096c2decdd) |
| C15-CT02 | Tentar adicionar produto sem nome | Falhou | BUG-028 | [Vídeo](https://jam.dev/c/f236c5ea-20d1-4ab5-9880-f846f4b57fe9) |
| C15-CT03 | Filtrar produtos por tipo | Passou | - | [Vídeo](https://jam.dev/c/52b224b2-eb8f-40bf-a669-3f096c2decdd) |
| C16-CT01 | Visualizar lista de grupos musculares | Passou (com ressalva) | BUG-030 | [Vídeo](https://jam.dev/c/738864f2-1b23-4d4a-8edb-c5cb52a5e503) |
| C16-CT02 | Filtrar grupos por tipo de membro | Passou | - | [Vídeo](https://jam.dev/c/738864f2-1b23-4d4a-8edb-c5cb52a5e503) |
| C16-CT03 | Verificar total de grupos cadastrados | Falhou | BUG-029 | [Vídeo](https://jam.dev/c/738864f2-1b23-4d4a-8edb-c5cb52a5e503) |
| C17-CT01 | Adicionar novo objetivo com dados válidos | Falhou | BUG-012 | [Vídeo](https://jam.dev/c/11966eaa-46d6-4084-9b42-2e2bcc6ee551) |
| C17-CT02 | Tentar adicionar objetivo sem nome | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/11966eaa-46d6-4084-9b42-2e2bcc6ee551) |
| C17-CT03 | Pesquisar objetivo já cadastrado | Bloqueado | BUG-012 | Não executado (bloqueado) |
| C18-CT01 | Visualizar lista de modelos de ficha | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/42cd2169-d05d-4486-9ca0-74e544443ed1) |
| C18-CT02 | Pesquisar modelo de ficha por título | Bloqueado | BUG-031 | [Vídeo](https://jam.dev/c/42cd2169-d05d-4486-9ca0-74e544443ed1) |
| C18-CT03 | Usar modelo ao cadastrar ficha de treino | Bloqueado | BUG-013, BUG-031 | Não executado (bloqueado) |
| C19-CT01 | Visualizar lista de grupos | Passou | - | [Vídeo](https://jam.dev/c/04ac7241-4223-4ea6-98aa-e9c874e7d9ea) |
| C19-CT02 | Filtrar grupos por status | Passou | - | [Vídeo](https://jam.dev/c/04ac7241-4223-4ea6-98aa-e9c874e7d9ea) |
| C19-CT03 | Filtrar grupos por tipo de caixa | Passou | - | [Vídeo](https://jam.dev/c/04ac7241-4223-4ea6-98aa-e9c874e7d9ea) |
| C20-CT01 | Adicionar novo modelo de contrato | Falhou | BUG-032, BUG-033 | [Vídeo](https://jam.dev/c/ba72c986-89c6-4e48-8d0f-12602f40d271) |
| C20-CT02 | Tentar adicionar modelo de contrato sem nome | Passou | - | [Vídeo](https://jam.dev/c/ba72c986-89c6-4e48-8d0f-12602f40d271) |
| C20-CT03 | Visualizar lista sem modelos cadastrados | Falhou | BUG-032 | [Vídeo 1](https://jam.dev/c/ba72c986-89c6-4e48-8d0f-12602f40d271) [Vídeo 2](https://jam.dev/c/409101db-ba9a-4e77-a3cc-88a6685f2398) |
| C21-CT01 | Adicionar nova despesa fixa com dados válidos | Passou | - | [Vídeo](https://jam.dev/c/02c1a6da-c0a6-4eee-99c0-6535f87f7f19) |
| C21-CT02 | Filtrar despesas por recorrência | Passou | - | [Vídeo](https://jam.dev/c/02c1a6da-c0a6-4eee-99c0-6535f87f7f19) |
| C21-CT03 | Verificar valor total das despesas | Passou | - | [Vídeo](https://jam.dev/c/02c1a6da-c0a6-4eee-99c0-6535f87f7f19) |
| C22-CT01 | Adicionar novo tipo de pagamento | Falhou | BUG-035 | [Vídeo](https://jam.dev/c/4db1abb7-f50e-43e4-bcf2-cf768b968898) |
| C22-CT02 | Tentar adicionar tipo de pagamento sem nome | Falhou | BUG-034 | [Vídeo](https://jam.dev/c/4db1abb7-f50e-43e4-bcf2-cf768b968898) |
| C22-CT03 | Filtrar tipos de pagamento por status | Falhou | BUG-036 | [Vídeo](https://jam.dev/c/4db1abb7-f50e-43e4-bcf2-cf768b968898) |
| C23-CT01 | Adicionar nova bandeira com dados válidos | Falhou | BUG-033, BUG-037 | [Vídeo](https://jam.dev/c/3b9274a5-017d-49c6-a478-22969296701e) |
| C23-CT02 | Tentar adicionar bandeira sem nome | Passou | - | [Vídeo](https://jam.dev/c/3b9274a5-017d-49c6-a478-22969296701e) |
| C23-CT03 | Pesquisar bandeira já cadastrada | Falhou | BUG-037 | [Vídeo](https://jam.dev/c/3b9274a5-017d-49c6-a478-22969296701e) |
| C24-CT01 | Adicionar novo tipo de documento | Passou | - | [Vídeo](https://jam.dev/c/c29b1dca-6df4-40ce-a947-f00535387852) |
| C24-CT02 | Tentar adicionar tipo de documento sem nome | Passou | - | [Vídeo](https://jam.dev/c/c29b1dca-6df4-40ce-a947-f00535387852) |
| C24-CT03 | Filtrar tipos de documentos por aplicação | Passou | - | [Vídeo](https://jam.dev/c/c29b1dca-6df4-40ce-a947-f00535387852) |
| C25-CT01 | Abrir caixa com dados válidos | Passou (com ressalva) | BUG-039 | [Vídeo](https://jam.dev/c/358a7731-1720-44d4-a9e4-489a9d7aa977) |
| C25-CT02 | Filtrar caixas por status | Passou (com ressalva) | BUG-038 | [Vídeo](https://jam.dev/c/358a7731-1720-44d4-a9e4-489a9d7aa977) |
| C25-CT03 | Navegar entre as páginas da lista de caixas | Passou | - | [Vídeo](https://jam.dev/c/358a7731-1720-44d4-a9e4-489a9d7aa977) |
| C26-CT01 | Visualizar painel da Pagar.me | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/b0dd20aa-9807-4d90-8e89-d69506a338e6) |
| C26-CT02 | Verificar coerência dos valores de recebimento | Falhou | BUG-040 | [Vídeo](https://jam.dev/c/b0dd20aa-9807-4d90-8e89-d69506a338e6) |
| C26-CT03 | Visualizar transações recentes | Passou | - | [Vídeo](https://jam.dev/c/b0dd20aa-9807-4d90-8e89-d69506a338e6) |
| C27-CT01 | Adicionar nova atividade com dados válidos | Passou | - | [Vídeo](https://jam.dev/c/ed415e90-3014-48aa-a674-47e90cc67b41) |
| C27-CT02 | Tentar adicionar atividade sem nome | Falhou | BUG-041 | [Vídeo](https://jam.dev/c/ed415e90-3014-48aa-a674-47e90cc67b41) |
| C27-CT03 | Pesquisar atividade já cadastrada | Passou | - | [Vídeo](https://jam.dev/c/ed415e90-3014-48aa-a674-47e90cc67b41) |
| C28-CT01 | Adicionar nova pontuação com dados válidos | Passou (com ressalva) | BUG-042 | [Vídeo](https://jam.dev/c/f74dc437-c900-4899-be8d-6f7b75f109e6) |
| C28-CT02 | Tentar adicionar pontuação sem nome | Passou | - | [Vídeo](https://jam.dev/c/f74dc437-c900-4899-be8d-6f7b75f109e6) |
| C28-CT03 | Filtrar pontuações por status | Passou | - | [Vídeo](https://jam.dev/c/f74dc437-c900-4899-be8d-6f7b75f109e6) |
| C29-CT01 | Adicionar nova enquete com pergunta | Falhou | BUG-043 | [Vídeo](https://jam.dev/c/3017b60f-a6e0-4388-90f4-e669845a4e87) |
| C29-CT02 | Tentar ativar enquete sem pergunta | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/3017b60f-a6e0-4388-90f4-e669845a4e87) |
| C29-CT03 | Filtrar enquetes por status | Passou | - | [Vídeo](https://jam.dev/c/3017b60f-a6e0-4388-90f4-e669845a4e87) |
| C30-CT01 | Aplicar nova anamnese a um aluno | Falhou | BUG-045, BUG-046 | [Vídeo](https://jam.dev/c/b5f3781c-f45f-4920-a0de-b87f5422c2c7) |
| C30-CT02 | Tentar aplicar anamnese sem selecionar aluno | Falhou | BUG-044 | [Vídeo](https://jam.dev/c/3555370a-0ce3-49df-b4eb-33105bfebfdd) |
| C30-CT03 | Filtrar fichas por status | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/3555370a-0ce3-49df-b4eb-33105bfebfdd) |
| C31-CT01 | Adicionar novo modelo de anamnese | Passou | - | [Vídeo](https://jam.dev/c/5274fc54-e9cb-40c5-8aae-1c2a0ec85fe9) |
| C31-CT02 | Visualizar prévia do modelo | Falhou | BUG-047 | [Vídeo](https://jam.dev/c/5274fc54-e9cb-40c5-8aae-1c2a0ec85fe9) |
| C31-CT03 | Filtrar modelos por status | Passou | BUG-048 | [Vídeo](https://jam.dev/c/5274fc54-e9cb-40c5-8aae-1c2a0ec85fe9) |
| C32-CT01 | Adicionar nova categoria com dados válidos | Passou | BUG-049 | [Vídeo](https://jam.dev/c/f53f9550-0b7a-4e79-b236-1f6d05feb717) |
| C32-CT02 | Tentar adicionar categoria sem nome | Passou | - | [Vídeo](https://jam.dev/c/f53f9550-0b7a-4e79-b236-1f6d05feb717) |
| C32-CT03 | Filtrar categorias por status | Passou | - | [Vídeo](https://jam.dev/c/f53f9550-0b7a-4e79-b236-1f6d05feb717) |
| C33-CT01 | Adicionar nova pergunta com dados válidos | Passou (com ressalva) | BUG-051 | [Vídeo](https://jam.dev/c/f3ac1ddf-61d0-4eae-bf87-ecc0602b5dd2) |
| C33-CT02 | Tentar adicionar pergunta em branco | Falhou | BUG-050 | [Vídeo](https://jam.dev/c/f3ac1ddf-61d0-4eae-bf87-ecc0602b5dd2) |
| C33-CT03 | Pesquisar pergunta já cadastrada | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/f3ac1ddf-61d0-4eae-bf87-ecc0602b5dd2) |
| C34-CT01 | Visualizar automações ativas | Passou | - | [Vídeo](https://jam.dev/c/9795388c-9203-4112-a80f-6f99a98862a0) |
| C34-CT02 | Abrir os resultados de uma automação | Passou | - | [Vídeo](https://jam.dev/c/9795388c-9203-4112-a80f-6f99a98862a0) |
| C34-CT03 | Atualizar a central de automações | Passou | - | [Vídeo](https://jam.dev/c/9795388c-9203-4112-a80f-6f99a98862a0) |
| C35-CT01 | Visualizar resultados da inteligência | Passou | - | [Vídeo](https://jam.dev/c/3b7b3ec0-bd1f-43eb-99f3-72fa107f4b3f) |
| C35-CT02 | Filtrar resultados por período | Passou (com ressalva) | BUG-053 | [Vídeo](https://jam.dev/c/3b7b3ec0-bd1f-43eb-99f3-72fa107f4b3f) |
| C35-CT03 | Verificar quantidade de inadimplentes | Falhou | BUG-052 | [Vídeo](https://jam.dev/c/3b7b3ec0-bd1f-43eb-99f3-72fa107f4b3f) |
| C36-CT01 | Criar notificação para os alunos | Passou | - | [Vídeo](https://jam.dev/c/3c0aff6e-dd1d-4a22-9fe7-0f0344b1e877) |
| C36-CT02 | Tentar criar notificação sem mensagem | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/3c0aff6e-dd1d-4a22-9fe7-0f0344b1e877) |
| C36-CT03 | Filtrar postagens pendentes | Passou | - | [Vídeo](https://jam.dev/c/3c0aff6e-dd1d-4a22-9fe7-0f0344b1e877) |
| C37-CT01 | Visualizar configurações gerais | Passou | BUG-054 | [Vídeo](https://jam.dev/c/9c52920c-240b-49e1-8cac-e183cbf67b26) |
| C37-CT02 | Navegar entre as abas de configuração | Passou (com ressalva) | BUG-055 | [Vídeo](https://jam.dev/c/9c52920c-240b-49e1-8cac-e183cbf67b26) |
| C37-CT03 | Cancelar alteração de configuração | Passou | - | [Vídeo](https://jam.dev/c/9c52920c-240b-49e1-8cac-e183cbf67b26) |
| C38-CT01 | Visualizar menu do SifitBox | Passou | - | [Vídeo](https://jam.dev/c/2851a247-c28c-4af5-b678-18100c5083bd) |
| C38-CT02 | Buscar aulas do SifitBox | Passou | - | [Vídeo](https://jam.dev/c/2851a247-c28c-4af5-b678-18100c5083bd) |
| C38-CT03 | Gerar aulas do SifitBox | Falhou | BUG-056 | [Vídeo](https://jam.dev/c/2851a247-c28c-4af5-b678-18100c5083bd) |
| C39-CT01 | Acesso ao Dashboard pelo menu | Falhou | BUG-057 | [Vídeo](https://jam.dev/c/5ef4bb24-0b96-4099-ae8f-18d4a74f6314) |
| C39-CT02 | Verificação dos gráficos do Dashboard | Passou (com ressalva) | - | [Vídeo](https://jam.dev/c/5ef4bb24-0b96-4099-ae8f-18d4a74f6314) |
| C39-CT03 | Abrir a Inteligência pelo Dashboard | Passou | - | [Vídeo](https://jam.dev/c/5ef4bb24-0b96-4099-ae8f-18d4a74f6314) |
| C40-CT01 | Visualizar perfil do cliente | Passou (com ressalva) | BUG-058 | [Vídeo](https://jam.dev/c/a088a7ce-c852-4bbd-8747-1d230586d096) |
| C40-CT02 | Verificar matrícula atual no perfil | Passou | BUG-011 | [Vídeo](https://jam.dev/c/a088a7ce-c852-4bbd-8747-1d230586d096) |
| C40-CT03 | Agendar avaliação pelo perfil | Passou | - | [Vídeo](https://jam.dev/c/a088a7ce-c852-4bbd-8747-1d230586d096) |

---

## 🔍 **Identificação da Causa Raiz (Root Cause Analysis)**

Além de assistir ao comportamento na tela, parte dos bugs foi investigada no banco de dados com consultas de leitura. Isso permitiu separar os defeitos por origem:

| Causa raiz | Descrição | Bugs |
| ---------- | --------- | ---- |
| Estrutura do banco diferente do que a tela espera | A tabela `objetivos_treino` não tem `auto_increment` no `id`; não existe tabela para modelo de ficha de treino; `tipo_pagamentos` não tem coluna de status; as bandeiras estão com `status` vazio (NULL); `planos.grupo_id` é obrigatório no banco, mas não na tela. | BUG-006, BUG-012, BUG-013, BUG-017, BUG-031, BUG-035, BUG-036, BUG-037 |
| Falta de validação no servidor | O sistema salva registros sem nome, aceita CPF e CNPJ inválidos, valor negativo, login duplicado, horário inicial igual ao final e período invertido. | BUG-014, BUG-020, BUG-023, BUG-024, BUG-026, BUG-027, BUG-028, BUG-034, BUG-041, BUG-042, BUG-050, BUG-054 |
| Cards e totais calculados de forma diferente da lista | Os números dos cards não usam a mesma regra (ou o mesmo filtro) da listagem exibida logo abaixo. | BUG-002, BUG-003, BUG-007, BUG-008, BUG-011, BUG-018, BUG-029, BUG-038, BUG-040, BUG-048, BUG-049, BUG-052, BUG-053, BUG-058 |
| Tela não exibe o que foi gravado | O registro é salvo no banco, mas a listagem não mostra nada ou mostra outro status. | BUG-015, BUG-032, BUG-037 |
| Tratamento de erro genérico | Quando algo falha, o usuário vê apenas "Erro ao salvar" ou "Erro no servidor", sem indicar o campo com problema. | BUG-006, BUG-019, BUG-021, BUG-022, BUG-025, BUG-039, BUG-043, BUG-044, BUG-046, BUG-056 |
| Data e hora | O horário é exibido em UTC (3 horas adiantado) e gravado no formato de 12 horas. | BUG-016, BUG-033 |
| Segurança | Login duplicado entre colaboradores e senha do aparelho biométrico exibida em texto aberto. | BUG-024, BUG-055 |

**Exemplo com os 5 Porquês (BUG-013 – não é possível criar ficha de treino):**

1. Por que a ficha não é salva? Porque o campo Objetivo vem vazio e é obrigatório.
2. Por que o Objetivo vem vazio? Porque não existe nenhum objetivo cadastrado.
3. Por que não existe objetivo cadastrado? Porque o cadastro de objetivo sempre retorna "Erro ao salvar objetivo" (BUG-012).
4. Por que o cadastro de objetivo falha? Porque a coluna `id` da tabela `objetivos_treino` não tem `auto_increment` nem valor padrão.
5. Por que isso não foi percebido? Porque o sistema mostra uma mensagem genérica, que não aponta a origem do erro.

---

## ⚠️ **Riscos e Observações do Ambiente**

* **Limite de conexões do banco:** o usuário do banco tem limite de 500 conexões por hora (`max_connections_per_hour`). O limite foi atingido duas vezes em 22/10/2026. Nesse período o SIFIT exibiu "Erro no servidor" e "Erro ao salvar", que pareciam bugs. Os casos foram retestados com o banco disponível e os falsos positivos foram descartados (RF12 e RF20).
* **Ambiente compartilhado:** outros alunos cadastram e alteram dados ao mesmo tempo. Por isso, todos os cadastros de teste usaram o nome "Hendreu".
* **Comportamento que mudou durante os testes:** a navegação com F5 (achado exploratório) deixou de falhar, e o card "Cadastradas este Mês" (BUG-011) passou a mostrar 1 no dia 23/10/2026.

---

## 💡 **Sugestões de Melhoria**

* Mostrar todos os campos obrigatórios de uma vez, em vez de avisar um campo por vez.
* Exibir mensagens de erro que indiquem o campo com problema.
* Corrigir textos sem acento ("Codigo", "Aplicacao", "Acoes rapidas", "periodo", "Sem descricao cadastrada").
* Melhorar o contraste das telas com fundo branco e texto cinza claro (Tipos de Documentos, Box - Turmas, resultados da automação).
* Explicar quando um botão está desabilitado (Criar Categoria, Enviar aviso).
* Evitar que o navegador preencha automaticamente login e senha nos cadastros de cliente e colaborador.
* Pedir confirmação antes de salvar alterações nas Configurações, já que afetam a academia inteira.

**Pontos positivos:** as senhas de login e do aplicativo são armazenadas criptografadas (bcrypt), e várias validações funcionaram corretamente (cliente sem nome, matrícula sem cliente, avaliação sem aluno, filtros de status em Grupos, Pontuação e Enquetes).

---

## ✅ **Conclusão**

A execução dos testes manuais no SIFIT cobriu os **40 requisitos** levantados, com **120 casos de teste**. O sistema tem **boa navegação e muitos recursos**, mas apresentou **58 defeitos**, sendo **17 de severidade alta**. Os mais graves impedem o uso de funções inteiras: **fichas de treino, objetivos, modelos de ficha, enquetes, anamnese, check-in e geração de aulas do SifitBox**. Também foram encontradas várias **informações financeiras incoerentes** entre telas (valor em aberto, total a pagar, recebimentos da Pagar.me).

Grande parte dos problemas tem origem em **validações que não existem no servidor** e em **diferenças entre a estrutura do banco e o que a tela espera**. Corrigir essas duas causas resolveria boa parte dos bugs registrados.
