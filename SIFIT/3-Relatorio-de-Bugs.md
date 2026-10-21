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

---

### 🐞 **Bug 12: Não é possível cadastrar objetivo de treino**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-012    | Ao cadastrar um objetivo com o nome "Hipertrofia", o sistema exibe "Erro ao salvar objetivo" e nada é gravado. A tela de Objetivos Treino continua com "Nenhum objetivo cadastrado". Na consulta ao banco (DESCRIBE objetivos_treino), a coluna id não tem auto_increment nem valor padrão, o que pode ser a causa do erro. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Objetivos Treino" |
| 2. Clicar em "Novo Objetivo" |
| 3. Preencher "Hipertrofia" no campo Nome |
| 4. Clicar em "Salvar" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O objetivo deve ser salvo e exibido na lista. | É exibido "Erro ao salvar objetivo" e a lista continua vazia. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Objetivos de Treino         | C17-CT01: Adicionar novo objetivo com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/11966eaa-46d6-4084-9b42-2e2bcc6ee551) (0:28 a 0:35) |

---

### 🐞 **Bug 13: Não é possível criar ficha de treino porque a lista de objetivos vem vazia**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-013    | Ao cadastrar uma ficha com aluno, personal e datas preenchidos, o sistema exibe apenas "Erro ao salvar Ficha". O campo Objetivo não tem nenhuma opção além de "Selecione", pois não há objetivos cadastrados e o cadastro de objetivos também falha (BUG-012). Assim, nenhuma ficha de treino pode ser criada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Ficha de Treino" e clicar em "Cadastrar Ficha" |
| 2. Selecionar o aluno "Hendreu Teste", o personal e as datas |
| 3. Abrir o campo Objetivo e verificar que não há opções |
| 4. Clicar em "Criar Nova Ficha" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A ficha deve ser criada ou o sistema deve informar que é preciso cadastrar um objetivo antes. | É exibido apenas "Erro ao salvar Ficha", sem indicar o motivo. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Fichas de Treino         | C07-CT01: Cadastrar ficha de treino com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/27b40cdf-4229-4b0a-adb0-cecc0c053d8a) (0:31 a 0:33) |
| [Vídeo](https://jam.dev/c/11966eaa-46d6-4084-9b42-2e2bcc6ee551) (0:12 a 0:13, listas de fichas e objetivos vazias) |

---

### 🐞 **Bug 14: Sistema aceita turma com horário inicial igual ao horário final**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-014    | Ao cadastrar a turma "Turma Hendreu" com Hora Inicial 08:00 e Hora Final 08:00, o sistema salva normalmente e a turma aparece na lista com o horário "08:00:00 - 08:00:00". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Turmas" e clicar em "Cadastrar Turma" |
| 2. Preencher nome, plano e dias da semana |
| 3. Informar 08:00 em Hora Inicial e 08:00 em Hora Final |
| 4. Clicar em "Salvar" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve impedir o cadastro e informar que a hora final deve ser maior que a inicial. | A turma é salva com horário "08:00:00 - 08:00:00". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Turmas         | C08-CT02: Cadastrar turma com horário inválido |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/824d0d2e-0223-4c8e-b5c3-f4f7d4181fdc) (0:10 a 0:12 e 0:35 a 0:37) |

---

### 🐞 **Bug 15: Check-in confirmado no banco aparece como "Pendente" e não conta como presente**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-015    | O check-in do cliente 413 (Hendreu Teste) está gravado na tabela checkins com status CONFIRMADO, mas a tela de Check-ins exibe o cliente com status "Pendente" e o card "Presentes agora" mostra 0. Ao fazer uma nova entrada rápida com o mesmo código, o campo é limpo, nenhum registro novo é gravado e nenhuma mensagem é exibida. O botão "Registrar entrada" da linha do cliente também não altera nada ao ser clicado. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta         |           Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Check-in" |
| 2. Digitar o código 413 em "Entrada rápida" e clicar em "Realizar check-in" |
| 3. Observar o status do cliente na lista e o card "Presentes agora" |
| 4. Clicar em "Registrar entrada" na linha do cliente |
| 5. Consultar a tabela checkins no banco: SELECT * FROM checkins WHERE cliente_id = 413; |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O status da tela deve ser igual ao do banco e o cliente deve aparecer em "Presentes agora". Uma nova tentativa deve exibir uma mensagem (sucesso ou check-in já realizado). | A tela mostra "Pendente" e "Presentes agora (0)", enquanto o banco mostra CONFIRMADO. A nova tentativa não grava nada e não exibe mensagem. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Check-in         | C08-CT03: Realizar check-in de cliente |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/824d0d2e-0223-4c8e-b5c3-f4f7d4181fdc) (0:40 a 0:48) |
| [Vídeo](https://jam.dev/c/0f0778fe-246a-4fd1-bbca-2151b866fc2d) (0:04 a 0:10, botão "Registrar entrada" sem efeito) |
| Consulta no banco: registro id 13 da tabela checkins com status CONFIRMADO |

---

### 🐞 **Bug 16: Horário de entrada do check-in exibido 3 horas adiantado**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-016    | Na tela de Check-ins, o relógio do topo mostra 19:44, mas a entrada do cliente Hendreu Teste aparece às 22:43. No banco, o registro foi gravado como 2026-10-21 22:43:30. O sistema exibe o horário em UTC, sem converter para o horário de Brasília (UTC-3). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Realizar o check-in de um cliente |
| 2. Comparar o horário da coluna "Entrada" com o relógio no topo da tela de Check-ins |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O horário de entrada deve ser exibido no horário local (Brasília). | A entrada aparece 3 horas à frente do horário real. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Check-in         | C08-CT03: Realizar check-in de cliente |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/824d0d2e-0223-4c8e-b5c3-f4f7d4181fdc) (0:40, entrada 22:43 com relógio 19:44) |
| Consulta no banco: created_at 2026-10-21 22:43:30 |

---

### 🐞 **Bug 17: Conta a receber em dinheiro pede bandeira de cartão e a lista de bandeiras vem vazia**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-017    | Ao cadastrar uma conta a receber com status "Recebido" e escolher o Tipo de Pagamento "Dinheiro", o sistema abre a janela "Escolher Bandeira", que é usada para cartão. A lista de bandeiras vem vazia. Ao clicar em "Fechar", o Tipo de Pagamento volta para "Selecione", e sem tipo de pagamento o sistema não salva a conta. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Contas a Receber" e clicar em "Nova Conta"  |
| 2. Selecionar o cliente "Hendreu Teste" e informar o valor 50,00 |
| 3. Manter o status "Recebido"                                  |
| 4. Selecionar "Dinheiro" no campo Tipo de Pagamento            |
| 5. Observar a janela "Escolher Bandeira"                       |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| Pagamento em dinheiro não deve pedir bandeira de cartão, e a conta deve ser salva. | A janela "Escolher Bandeira" abre com a lista vazia e, ao fechar, o tipo de pagamento é apagado. Não é possível salvar a conta como recebida em dinheiro. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|      Contas a Receber      | C09-CT01: Cadastrar conta a receber com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/21676c18-6d62-4959-aa27-99c1c41ab74a) (0:31 a 0:55) |

---

### 🐞 **Bug 18: Card "Total a Pagar" mostra 0 com conta pendente de R$ 200,00 na lista**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-018    | Na tela de Contas a Pagar, com o filtro Status "Pendente", a lista mostra 2 contas pendentes (R$ 200,00 e R$ 0,00), mas os cards "Total a Pagar" e "Valor Pendente" exibem 0. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Contas a Pagar"                             |
| 2. Selecionar o Status "Pendente" e clicar em "Buscar"         |
| 3. Somar a coluna "Valor Pagar" das contas listadas            |
| 4. Comparar com os cards "Total a Pagar" e "Valor Pendente"    |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| Os cards devem mostrar R$ 200,00, que é a soma das contas pendentes listadas. | Os cards "Total a Pagar" e "Valor Pendente" mostram 0, enquanto "Contas Listadas" mostra 2. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|       Contas a Pagar       | C09-CT03: Conferir total das contas a pagar pendentes |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/3bdb4808-fb6f-452a-800f-50733c073b37) (0:45 a 0:50) |

---

### 🐞 **Bug 19: Mensagem genérica ao salvar matrícula com dia de vencimento anterior à data inicial**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-019    | Ao salvar uma matrícula com Data Inicial 31/10/2026 e Dia Vencimento 01/10/2026, o sistema exibe "Não foi possível concluir – Erro ao Cadastrar com Assinatura". A matrícula não é gravada (confirmado no banco), mas a mensagem não informa qual campo está errado. Além disso, a Data Final digitada antes de escolher o plano é descartada sem aviso. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Matrículas" e clicar em "Cadastrar Matrícula"      |
| 2. Informar Data Inicial 31/10/2026 e Data Final 01/10/2026    |
| 3. Selecionar o cliente "Hendreu Teste", o plano e o tipo de pagamento "Dinheiro" |
| 4. Informar 01/10/2026 em Dia Vencimento                       |
| 5. Clicar em "Salvar"                                          |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve informar que o vencimento não pode ser anterior à data inicial. | É exibido "Erro ao Cadastrar com Assinatura", sem indicar o problema. |

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
| [Vídeo](https://jam.dev/c/a8950630-7a17-4426-a570-4c9b4a76e827) (0:09 a 0:15 e 0:43 a 0:59) |
| Consulta no banco: só a matrícula #238 existe para o cliente 413 |

---

### 🐞 **Bug 20: Relatório é gerado com data final anterior à data inicial**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-020    | Ao gerar o relatório de Matrículas com Data Início 31/10/2026 e Data Fim 01/10/2026, o sistema não exibe mensagem de erro e baixa um PDF com "Data Inicial: 31/10/2026", "Data Final: 01/10/2026" e "Quantidade de registros: 0". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Relatórios" |
| 2. Selecionar o tipo "Matrículas" |
| 3. Informar Data Início 31/10/2026 e Data Fim 01/10/2026 |
| 4. Clicar em "Gerar Relatório" |
| 5. Abrir o PDF baixado |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve impedir a geração e informar que a data final deve ser maior que a inicial. | O PDF é gerado com o período invertido e 0 registros, sem aviso de período inválido. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Relatórios         | C10-CT02: Gerar relatório com período inválido |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/be9e953b-120a-4b46-be9d-f5ce0f0e07fb) (0:04 a 0:11) |
| [Vídeo](https://jam.dev/c/c0aad349-ea7d-48d8-9e2b-92eb157d216d) (0:04 a 0:07, PDF gerado) |

---

### 🐞 **Bug 21: Relatório de Clientes é baixado corrompido e não abre**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-021    | Ao gerar o relatório de Clientes com o período 01/01/2026 a 31/10/2026, o arquivo "relatorio (2).pdf" é baixado com 0 bytes. Ao abrir, o Chrome exibe "Erro – Falha ao carregar documento PDF". A tela de Relatórios não informa que o arquivo foi gerado com erro. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta         |           Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Relatórios" |
| 2. Selecionar o tipo "Clientes" |
| 3. Informar Data Início 01/01/2026 e Data Fim 31/10/2026 |
| 4. Clicar em "Gerar Relatório" |
| 5. Abrir o PDF baixado |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O PDF deve abrir com a lista de clientes cadastrados no período, incluindo o "Hendreu Teste". | O arquivo baixado está vazio (0 bytes) e não abre. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Relatórios         | C10-CT01: Gerar relatório de clientes |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/be9e953b-120a-4b46-be9d-f5ce0f0e07fb) (0:58 a 1:04) |
| [Vídeo](https://jam.dev/c/c0aad349-ea7d-48d8-9e2b-92eb157d216d) (0:02 e 0:19 a 0:22, arquivo com 0 bytes e erro ao abrir) |
