# Relatório de Bugs

**Software:** SIFIT - Sistema para Academias

**QA responsável:** Hendreu Satoshi Zampieri Itami (240061)

**Data:** 17.10.26

---

### 🐞 **Bug 01: Opção "Manter conectado" não mantém o usuário logado**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-001    | Mesmo com a opção "Manter conectado" marcada no login, ao fechar a aba e acessar o sistema novamente o usuário é levado de volta para a tela de login. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar a página de login do SIFIT                          |
| 2. Preencher login e senha válidos                             |
| 3. Marcar a opção "Manter conectado"                           |
| 4. Clicar em "Entrar"                                          |
| 5. Fechar a aba do sistema                                     |
| 6. Abrir uma nova aba e acessar sifit.centrion.com.br          |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve abrir a Página Inicial sem pedir o login novamente.      | O sistema exibe a tela de login e a opção "Manter conectado" aparece desmarcada. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|           Login            | C01-CT03: Login com a opção manter conectado       |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/5f641348-c322-4dde-9193-8ab76ba8e770) |

---

### 🐞 **Bug 02: Quantidade de clientes ausentes diferente entre a Página Inicial e a tela de Clientes**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-002    | A Página Inicial informa 6 clientes ausentes, enquanto a tela de Clientes informa 0 ausentes no mesmo momento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Realizar login no SIFIT                                     |
| 2. Observar o card "Clientes Ausentes" na Página Inicial       |
| 3. Acessar o menu "Clientes"                                   |
| 4. Observar o card "Ausentes"                                  |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A quantidade de clientes ausentes deve ser a mesma nas duas telas.      | A Página Inicial mostra 6 ausentes e a tela de Clientes mostra 0.      |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|  Página Inicial / Clientes | C02-CT01: Acesso à Página Inicial após login bem-sucedido |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/86c798a0-5b72-4fb2-bc0a-7f134f79ff58) (0:01 e 0:29) |

---

### 🐞 **Bug 03: Valor em aberto aparece zerado mesmo com mensalidade vencida**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-003    | A Página Inicial mostra "R$ 0,00 em aberto" e "Total em aberto R$ 0,00", mas lista uma mensalidade vencida em 12/05/2026. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Realizar login no SIFIT                                     |
| 2. Observar o card "em aberto" no topo da Página Inicial       |
| 3. Observar o quadro "Mensalidades pendentes" à direita        |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O total em aberto deve somar o valor das mensalidades vencidas.         | O total aparece R$ 0,00 enquanto uma mensalidade vencida é listada.    |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|  Página Inicial / Financeiro | C02-CT01: Acesso à Página Inicial após login bem-sucedido |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/86c798a0-5b72-4fb2-bc0a-7f134f79ff58) (0:20) |

---

### 🐞 **Bug 04: Paginação exibe 3 páginas quando a busca retorna apenas 1 cliente**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-004    | Ao pesquisar um cliente pelo nome, a lista mostra 1 resultado, mas a paginação continua exibindo as páginas 1, 2 e 3 e o botão "Próxima". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Baixa            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Clientes"                                   |
| 2. Digitar "Hendreu Teste" no campo Nome                       |
| 3. Clicar em "Buscar"                                          |
| 4. Observar a paginação abaixo do resultado                    |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| Com 1 resultado, deve existir apenas a página 1.                        | São exibidas as páginas 1, 2 e 3 e o botão "Próxima".                  |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|          Clientes          | C03-CT03: Pesquisar cliente já cadastrado          |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/7e8be00d-94a9-4a63-93e8-88c9c38faab4) (1:01) |

---

### 🐞 **Bug 05: Filtros da tela de Clientes vêm preenchidos e não correspondem à lista exibida**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-005    | Ao abrir a tela de Clientes, os filtros já aparecem com Plano "Aba" e Personal "Marcelo Longo Zandonadi", mas a lista mostra clientes sem matrícula e de outros planos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Clientes"                                   |
| 2. Observar os filtros Plano e Personal                        |
| 3. Comparar com a coluna Plano da lista                        |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| Os filtros devem vir vazios ou a lista deve respeitar os filtros exibidos. | Os filtros mostram Plano "Aba", mas a lista traz clientes "Sem Matrícula". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|          Clientes          | C03-CT03: Pesquisar cliente já cadastrado          |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/7e8be00d-94a9-4a63-93e8-88c9c38faab4) (0:51) |

---

### 🐞 **Bug 06: Erro genérico ao salvar plano sem grupo selecionado**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-006    | Ao salvar um plano com nome e valor preenchidos, mas sem selecionar o Grupo, o sistema exibe apenas "Erro ao salvar plano", sem indicar o campo com problema. O campo Grupo não aparece como obrigatório na tela, mas a coluna grupo_id da tabela planos não aceita valor vazio. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Alta             |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Planos"                                     |
| 2. Clicar em "Novo Plano"                                      |
| 3. Preencher "Plano Hendreu" no Nome e "99,90" no Valor Mensal |
| 4. Deixar o campo Grupo sem seleção                            |
| 5. Clicar em "Salvar Plano"                                    |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O campo Grupo deve ser marcado como obrigatório e o sistema deve avisar que ele precisa ser preenchido. | O plano não é salvo e aparece apenas a mensagem "Erro ao salvar plano". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|           Planos           | C05-CT01: Adicionar novo plano com dados válidos   |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/516e542a-5e59-4187-9379-bed8d372a748) (0:31 a 0:33) |
| [Vídeo de confirmação](https://jam.dev/c/707ed084-77ce-4631-8406-2103a828bb1c) (0:07 a 0:21): com o Grupo "Treino Livre" selecionado, o mesmo plano é salvo normalmente |

---

### 🐞 **Bug 07: Quantidade de alunos do plano diferente entre o ranking e a lista de planos**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-007    | O plano #56 "Teste Diaria QA Verify" aparece com 1 aluno no ranking "Planos com mais alunos", mas com 0 alunos na coluna Alunos da lista de planos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Planos"                                     |
| 2. Digitar "Teste Diaria QA Verify" no campo Nome e clicar em "Buscar" |
| 3. Comparar a quantidade de alunos do ranking com a coluna Alunos da lista |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A quantidade de alunos deve ser a mesma no ranking e na lista.          | O ranking mostra 1 aluno e a lista mostra 0.                           |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|           Planos           | C05-CT03: Verificar quantidade de alunos por plano |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/191aafea-be89-4847-9fad-2483724ea9ba) (0:05) |

---

### 🐞 **Bug 08: Mensalidade e Receita Estimada aparecem zeradas em plano com valor e aluno**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-008    | O plano #56 tem valor de R$ 25,00 e 1 aluno, mas o ranking exibe "Mensalidade R$ 0,00" e o card "Receita Estimada" exibe R$ 0,00. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Planos"                                     |
| 2. Observar o card "Receita Estimada" no topo da tela          |
| 3. Observar a "Mensalidade" no ranking "Planos com mais alunos" |
| 4. Comparar com a coluna Valor do plano na lista               |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A mensalidade e a receita estimada devem considerar o valor do plano e a quantidade de alunos. | Os dois valores aparecem como R$ 0,00, mesmo com o plano de R$ 25,00 e 1 aluno. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|           Planos           | C05-CT03: Verificar quantidade de alunos por plano |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/191aafea-be89-4847-9fad-2483724ea9ba) (0:05 a 0:09) |

---

### 🐞 **Bug 09: Mensagem "Selecione o Tipo de Pagamento" continua na tela após selecionar o tipo**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-009    | Ao salvar a matrícula sem tipo de pagamento, a mensagem "Selecione o Tipo de Pagamento" é exibida. Depois de selecionar "Dinheiro", a mensagem continua aparecendo abaixo do campo. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Baixa            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Matrículas" e clicar em "Cadastrar Matrícula" |
| 2. Selecionar o cliente e o plano |
| 3. Clicar em "Salvar" sem selecionar o Tipo Pagamento |
| 4. Selecionar "Dinheiro" no campo Tipo Pagamento |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A mensagem deve sumir assim que o tipo de pagamento for selecionado. | A mensagem continua exibida em vermelho com o campo já preenchido. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Matrículas         | C04-CT03: Tentar cadastrar matrícula sem tipo de pagamento |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/941b9966-edb4-4e75-9d37-31f95071a55d) (0:58 a 1:14) |

---

### 🐞 **Bug 10: Tela de pagamento da matrícula abre com tipo de pagamento vazio e título repetido**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-010    | Após salvar a matrícula e confirmar o pagamento, a tela "Cadastrar Conta a Receber" abre com o Tipo de Pagamento vazio, mesmo com "Dinheiro" escolhido na matrícula, e com o título "Plano Plano Hendreu". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Cadastrar uma matrícula com o tipo de pagamento "Dinheiro" |
| 2. Clicar em "Salvar" |
| 3. Clicar em "Confirmar" na mensagem "Deseja pagar a conta a receber agora?" |
| 4. Observar os campos Título e Tipo de Pagamento |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| Os campos devem vir com os dados informados na matrícula e o título sem palavras repetidas. | O Tipo de Pagamento vem vazio e o título aparece como "Plano Plano Hendreu". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Matrículas / Contas a Receber         | C04-CT01: Cadastrar matrícula com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/941b9966-edb4-4e75-9d37-31f95071a55d) (1:18 a 1:23) |

---

### 🐞 **Bug 11: Card "Cadastradas este Mês" mostra 0 com matrícula cadastrada no mês**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-011    | A matrícula #238 do cliente "Hendreu Teste" foi cadastrada em 18/10/2026 e aparece como ATIVO na lista, mas o card "Cadastradas este Mês" da tela de Matrículas continua exibindo 0. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Cadastrar uma matrícula com a data atual                    |
| 2. Acessar o menu "Matrículas"                                 |
| 3. Observar a matrícula na lista                               |
| 4. Observar o card "Cadastradas este Mês"                      |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O card deve contar as matrículas cadastradas no mês atual.              | O card exibe 0, mesmo com a matrícula #238 cadastrada no mês.          |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Matrículas         | C04-CT01: Cadastrar matrícula com dados válidos    |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Captura de tela](https://jam.dev/c/06e32ae4-06b8-4d29-937c-d7fee97cbf6c) |
