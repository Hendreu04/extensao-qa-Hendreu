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
| BUG-004    | Ao pesquisar um cliente pelo nome, a lista mostra 1 resultado, mas a paginação continua exibindo as páginas 1, 2 e 3 e o botão "Próxima". O mesmo acontece na busca de Colaboradores. |

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
| [Vídeo](https://jam.dev/c/64d30fb2-224f-4f30-848f-cb7adca31a22) (1:13, o mesmo ocorre em Colaboradores: 1 resultado e páginas 1 e 2) |

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

---

### 🐞 **Bug 22: "Erro no servidor" ao salvar colaborador com campos obrigatórios vazios**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-022    | Ao clicar em "Salvar" no cadastro de colaborador com o Nome em branco, o sistema exibe "Erro no servidor – Erro interno inesperado." em vez de indicar o campo obrigatório. O mesmo erro aparece com o Nome preenchido e os demais campos (Status, Sexo, Data de Nascimento) vazios. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Colaboradores" e clicar em "Novo Colaborador" |
| 2. Deixar o campo Nome em branco |
| 3. Clicar em "Salvar" |
| 4. Preencher apenas o Nome e clicar em "Salvar" novamente |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve indicar quais campos obrigatórios não foram preenchidos, sem chegar a gerar erro no servidor. | É exibido "Erro no servidor – Erro interno inesperado." nas duas tentativas. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Colaboradores         | C11-CT02: Tentar adicionar colaborador sem nome |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/64d30fb2-224f-4f30-848f-cb7adca31a22) (0:06 a 0:09 e 0:21 a 0:22) |

---

### 🐞 **Bug 23: Cadastro de colaborador aceita CPF inválido**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-023    | O colaborador "Hendreu Colaborador" foi salvo com o CPF 123.456.789-88, que tem os dígitos verificadores errados (o correto para 123.456.789 seria -09). O sistema não validou o CPF. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Colaboradores" e clicar em "Novo Colaborador" |
| 2. Preencher Nome, Status, Sexo e Data de Nascimento |
| 3. Informar o CPF 123.456.789-88 |
| 4. Clicar em "Salvar" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve recusar o CPF e informar que ele é inválido. | O colaborador é salvo normalmente com o CPF inválido. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Colaboradores         | C11-CT01: Adicionar novo colaborador com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/64d30fb2-224f-4f30-848f-cb7adca31a22) (0:52 a 1:00 e 1:13) |

---

### 🐞 **Bug 24: Sistema permite cadastrar colaborador com login já usado por outro colaborador**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-024    | Ao cadastrar o colaborador "Hendreu Colaborador" (#57), o campo Login foi salvo como "marcelo_zandonadi", que já pertence ao colaborador #11. Na tabela login do banco existem agora dois registros com o mesmo login (id 118 do funcionário 11 e id 180 do funcionário 57). O sistema não avisou que o login já existe. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Colaboradores" e clicar em "Novo Colaborador"      |
| 2. Preencher os dados obrigatórios                             |
| 3. Em "Cadastro de Login", informar um login que já existe (ex.: marcelo_zandonadi) e uma senha |
| 4. Clicar em "Salvar"                                          |
| 5. Consultar no banco: SELECT id, funcionario_id, login FROM login WHERE login = 'marcelo_zandonadi'; |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve recusar o cadastro e informar que o login já está em uso. | O colaborador é salvo e o banco passa a ter dois logins iguais para colaboradores diferentes. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|       Colaboradores        | C11-CT01: Adicionar novo colaborador com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/64d30fb2-224f-4f30-848f-cb7adca31a22) (0:11 a 1:00, campo Login com "marcelo_zandonadi" ao salvar) |
| Consulta no banco: tabela login com os registros 118 (funcionário 11) e 180 (funcionário 57), ambos "marcelo_zandonadi" |

---

### 🐞 **Bug 25: Erro genérico ao salvar fornecedor preenchendo apenas o campo obrigatório**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-025    | No cadastro de fornecedor, apenas o campo Nome está marcado como obrigatório (*). Ao salvar com o Nome "Fornecedor Hendreu" preenchido e os demais campos vazios, o sistema exibe apenas "Erro ao salvar fornecedor", sem indicar qual informação está faltando. Depois de preencher CNPJ e endereço, o cadastro é salvo normalmente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Fornecedores" e clicar em "Novo Fornecedor" |
| 2. Preencher apenas o campo Nome |
| 3. Clicar em "Salvar" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O fornecedor deve ser salvo, ou o sistema deve marcar como obrigatórios e indicar os campos que faltam. | É exibido "Erro ao salvar fornecedor", sem indicar o campo com problema. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Fornecedores         | C13-CT01: Adicionar novo fornecedor com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/c76b43da-ac66-4235-9348-40a66add58cd) (0:14 a 0:17) |

---

### 🐞 **Bug 26: Cadastro de fornecedor aceita CNPJ inválido**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-026    | O fornecedor "Fornecedor Hendreu" (#415) foi salvo com o CNPJ 22.456.325/6622-56, que tem os dígitos verificadores errados (o correto para 22.456.325/6622 seria -59). O sistema não validou o CNPJ. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Fornecedores" e clicar em "Novo Fornecedor" |
| 2. Preencher o Nome e o CNPJ 22.456.325/6622-56 |
| 3. Preencher o endereço |
| 4. Clicar em "Salvar" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve recusar o CNPJ e informar que ele é inválido. | O fornecedor é salvo normalmente com o CNPJ inválido. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Fornecedores         | C13-CT01: Adicionar novo fornecedor com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/c76b43da-ac66-4235-9348-40a66add58cd) (0:22 a 0:26 e 0:50 a 1:06) |

---

### 🐞 **Bug 27: Produto do tipo "Venda" é salvo sem preço**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-027    | O produto "Garrafa Hendreu" (#9), do tipo "Venda", foi salvo com o campo Preço vazio. Na lista, a coluna Valor/Pontos aparece sem valor, e o produto é contado no card "Para venda". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Produtos" e clicar em "Novo"                |
| 2. Preencher o Nome "Garrafa Hendreu" e manter o Tipo "Venda"  |
| 3. Deixar o campo Preço em branco                              |
| 4. Clicar em "Salvar"                                          |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve exigir o preço para produtos do tipo Venda.              | O produto é salvo sem preço e aparece na lista como disponível para venda. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|          Produtos          | C15-CT01: Adicionar novo produto com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/52b224b2-eb8f-40bf-a669-3f096c2decdd) (0:12 a 0:19) |

---

### 🐞 **Bug 28: Sistema permite cadastrar produto sem nome**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-028    | Ao salvar um produto com o campo Nome em branco, o sistema não exibe mensagem de erro e o produto é cadastrado. Na lista aparecem produtos sem nome e sem preço (#7, #8, #10 e #11), todos como "Venda" e "Ativo", e eles são contados nos cards "Total de produtos" e "Para venda". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Produtos" e clicar em "Novo"                |
| 2. Deixar o campo Nome em branco                               |
| 3. Clicar em "Salvar"                                          |
| 4. Observar a lista de produtos                                |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve impedir o cadastro e exibir uma mensagem de erro no campo Nome. | O produto é salvo sem nome e aparece na lista como ativo e disponível para venda. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|          Produtos          | C15-CT02: Tentar adicionar produto sem nome        |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f236c5ea-20d1-4ab5-9880-f846f4b57fe9) |
| [Vídeo](https://jam.dev/c/52b224b2-eb8f-40bf-a669-3f096c2decdd) (0:03, produtos #7 e #8 sem nome na lista) |

---

### 🐞 **Bug 29: Total de grupos musculares não bate com a soma por tipo de membro**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-029    | O card "Grupos cadastrados" mostra 12, mas a soma dos cards Superiores (7), Inferiores (2) e Aeróbio (1) é 10. Na lista existe o grupo #8 "SAA" sem tipo de membro (exibido como "-"), o que indica que o sistema permite salvar grupo sem tipo e não o conta em nenhum card. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Grupos Musculares" |
| 2. Somar os cards Superiores, Inferiores e Aeróbio |
| 3. Comparar com o card "Grupos cadastrados" |
| 4. Observar a coluna Tipo Membro do grupo #8 |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O total deve ser igual à soma dos tipos, e todo grupo deve ter um tipo de membro. | O total é 12 e a soma é 10. O grupo #8 aparece sem tipo de membro. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Grupos Musculares         | C16-CT03: Verificar total de grupos cadastrados |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/738864f2-1b23-4d4a-8edb-c5cb52a5e503) (0:03 a 0:10) |

---

### 🐞 **Bug 30: Imagens dos grupos musculares aparecem quebradas**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-030    | Na lista de Grupos Musculares, os grupos Bicpes, Pernas, Teste 2, Cielo, Peitoral e Abdomen exibem o ícone de imagem quebrada na coluna Imagem. Os grupos sem imagem exibem corretamente o ícone padrão. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Baixa            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Grupos Musculares" |
| 2. Observar a coluna Imagem da lista |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A imagem cadastrada deve ser exibida, ou o ícone padrão quando não houver imagem. | É exibido o ícone de imagem quebrada. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Grupos Musculares         | C16-CT01: Visualizar lista de grupos musculares |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/738864f2-1b23-4d4a-8edb-c5cb52a5e503) (0:03 a 0:10 e 0:17) |

---

### 🐞 **Bug 31: Não é possível criar modelo de ficha de treino**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-031    | Ao abrir a tela Modelos de Ficha, o sistema exibe "Falha de conexão – Não foi possível conectar ao servidor". Ao criar o modelo "Modelo Hendreu", aparece "Erro ao salvar modelo" ou a janela fecha sem salvar, e a lista continua vazia. O Jam registra respostas com erro 500 do servidor. Na consulta ao banco não existe nenhuma tabela de modelo de ficha de treino (SHOW TABLES LIKE '%modelo%' e '%ficha%'), o que indica a causa provável. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Modelo Ficha"                               |
| 2. Clicar no botão "+" para criar um modelo                    |
| 3. Preencher "Modelo Hendreu" no Nome do Modelo e selecionar o personal "Santhago" |
| 4. Clicar em "Criar Modelo"                                    |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O modelo deve ser salvo e exibido na lista de modelos.                  | É exibido "Erro ao salvar modelo" ou a janela fecha, e nenhum modelo é cadastrado. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|      Modelos de Ficha      | C18-CT02: Pesquisar modelo de ficha por título     |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/42cd2169-d05d-4486-9ca0-74e544443ed1) (0:06, 0:27 e 0:31) |
| Consulta no banco: SHOW TABLES LIKE '%ficha%' retorna apenas exercicio_ficha, ficha_anamnese, ficha_treino, objetivo_ficha e pergunta_ficha |

---

### 🐞 **Bug 32: Lista de Modelos Contrato aparece vazia mesmo com modelos cadastrados**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-032    | Após salvar o modelo "Contrato Hendreu", o sistema volta para a tela Modelos Contrato, que exibe apenas o cabeçalho da tabela, sem nenhum registro, sem mensagem de sucesso e sem mensagem de lista vazia. No banco, a tabela modelos_contrato tem o "Contrato Hendreu" (id 14) e outros modelos (ids 10 a 13). O Jam registra uma resposta 403 (acesso negado) do servidor. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta         |           Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Modelos Contrato" |
| 2. Clicar em "Adicionar Modelo Contrato" |
| 3. Preencher o título "Contrato Hendreu" e o texto do contrato |
| 4. Clicar em "Salvar modelo" |
| 5. Observar a lista de modelos |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O modelo salvo e os demais modelos cadastrados devem aparecer na lista. | A lista aparece vazia, embora o banco tenha 5 modelos, incluindo o "Contrato Hendreu". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Modelos de Contrato         | C20-CT01: Adicionar novo modelo de contrato |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/ba72c986-89c6-4e48-8d0f-12602f40d271) (0:26 a 0:37) |
| Consulta no banco: modelos_contrato com os ids 10 a 14, sendo o 14 "Contrato Hendreu" ATIVO |

---

### 🐞 **Bug 33: Horário de criação é gravado no formato de 12 horas**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-033    | A coluna created_at grava a hora sem distinguir manhã e tarde. O modelo "Contrato Hendreu" foi criado às 14:47 (UTC) e ficou gravado como 02:47:18. O login do colaborador #57 foi criado às 13:12 (UTC) e ficou gravado como 01:12:11. Com isso, os registros feitos à tarde aparecem como se tivessem sido criados de madrugada. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Cadastrar um registro à tarde (ex.: um modelo de contrato) |
| 2. Consultar no banco: SELECT id, nome, created_at FROM modelos_contrato ORDER BY id DESC LIMIT 1; |
| 3. Comparar a hora gravada com a hora do cadastro |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A hora deve ser gravada no formato de 24 horas (14:47). | A hora é gravada como 02:47, 12 horas a menos. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Banco de dados (vários módulos)         | C20-CT01: Adicionar novo modelo de contrato |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/ba72c986-89c6-4e48-8d0f-12602f40d271) (gravado às 11:47 de Brasília, 14:47 UTC) |
| Consulta no banco: modelos_contrato id 14, created_at 2026-10-23 02:47:18 |
| Consulta no banco: bandeiras ids 30 e 31, criadas às 15:49 UTC e gravadas como 2026-10-23 03:49 |
| [Vídeo](https://jam.dev/c/64d30fb2-224f-4f30-848f-cb7adca31a22) (gravado às 13:12 UTC) e consulta no banco: login id 180, created_at 2026-10-22 01:12:11 |

---

### 🐞 **Bug 34: Sistema permite cadastrar tipo de pagamento sem nome**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-034    | Ao clicar em "Salvar" no cadastro de tipo de pagamento com o campo Nome em branco, o sistema não exibe mensagem de erro e o registro é criado. O total passa de 12 para 13 e aparece o código #14 sem nome na lista (já existia o #13, também sem nome). No banco, a coluna nome da tabela tipo_pagamentos aceita valor vazio (Null = YES). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Tipos de Pagamento" e clicar em "Novo" |
| 2. Deixar o campo Nome em branco |
| 3. Clicar em "Salvar" |
| 4. Observar a lista e o card "Total" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve impedir o cadastro e exibir uma mensagem de erro no campo Nome. | O tipo de pagamento é salvo sem nome. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Tipos de Pagamento         | C22-CT02: Tentar adicionar tipo de pagamento sem nome |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/4db1abb7-f50e-43e4-bcf2-cf768b968898) (0:10 a 0:16) |

---

### 🐞 **Bug 35: Tipo de pagamento cadastrado como "Ativo" aparece como "Inativo"**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-035    | O tipo "Pix Hendreu" foi cadastrado com o Status "Ativo", mas aparece na lista como INATIVO (#15). Todos os 14 tipos de pagamento aparecem como INATIVO e o card "Ativos" mostra 0, embora o tipo "Dinheiro" seja aceito normalmente no cadastro de matrícula. Na consulta ao banco (DESCRIBE tipo_pagamentos), a tabela não tem nenhuma coluna de status: o campo Status da tela não é gravado, e por isso todos os registros aparecem como inativos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta         |           Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Tipos de Pagamento" e clicar em "Novo" |
| 2. Preencher o Nome "Pix Hendreu", manter o Status "Ativo" e o Tipo "Débito" |
| 3. Clicar em "Salvar" |
| 4. Observar o status do registro na lista |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O tipo de pagamento deve aparecer com o status informado no cadastro (Ativo). | O registro aparece como INATIVO e o card "Ativos" continua 0. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Tipos de Pagamento         | C22-CT01: Adicionar novo tipo de pagamento |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/4db1abb7-f50e-43e4-bcf2-cf768b968898) (0:31 a 0:45) |
| Consulta no banco: DESCRIBE tipo_pagamentos sem coluna de status (id, empresa_id, nome, tipo, via_gateway, escolher_bandeira, created_at, updated_at) |

---

### 🐞 **Bug 36: Filtro de status em Tipos de Pagamento não retorna nenhum registro**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-036    | Na tela Tipos de Pagamento, ao filtrar por Status "Inativo" ou "Ativo", o sistema exibe "Nenhum tipo de pagamento encontrado", embora a lista sem filtro mostre 14 registros, todos como INATIVO. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Tipos de Pagamento" |
| 2. Selecionar "Inativo" no filtro Status e buscar |
| 3. Repetir com o Status "Ativo" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O filtro "Inativo" deve exibir os tipos inativos da lista. | Os dois filtros exibem "Nenhum tipo de pagamento encontrado". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Tipos de Pagamento         | C22-CT03: Filtrar tipos de pagamento por status |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/4db1abb7-f50e-43e4-bcf2-cf768b968898) (0:22 a 0:27 e 0:47 a 0:51) |

---

### 🐞 **Bug 37: Lista de Bandeiras de Cartão aparece vazia mesmo com bandeiras cadastradas**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-037    | Após salvar a bandeira "Visa", a tela Bandeiras de Cartão continua exibindo "Nenhuma bandeira encontrada", e a busca por "Visa" também não retorna nada. No banco, a tabela bandeiras tem a "Visa" (id 30) e outras bandeiras (ids 27 a 31), todas com a coluna status vazia (NULL). Isso também explica a janela "Escolher Bandeira" vazia do BUG-017. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Bandeiras" e clicar em "Nova Bandeira"      |
| 2. Preencher "Visa" no campo Nome                              |
| 3. Clicar em "Salvar"                                          |
| 4. Observar a lista e buscar por "Visa"                        |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A bandeira salva e as demais cadastradas devem aparecer na lista e na busca. | A lista e a busca mostram "Nenhuma bandeira encontrada", embora o banco tenha 5 bandeiras. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|    Bandeiras de Cartão     | C23-CT01: Adicionar nova bandeira com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/3b9274a5-017d-49c6-a478-22969296701e) (0:10 a 0:18 e 0:28 a 0:32) |
| Consulta no banco: bandeiras ids 27 a 31, sendo o 30 "Visa", com status NULL |

---

### 🐞 **Bug 38: Tela de Caixas abre ignorando o período exibido nos filtros**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-038    | Ao abrir a tela Caixas, os filtros já mostram o período de 01/10/2026 a 31/10/2026, mas a lista exibe 20 caixas de 2022 a 2026 e os cards mostram 18 caixas fechados e 20 registros no período. Depois de clicar em "Buscar" com os mesmos filtros, a lista passa a mostrar apenas 2 caixas e os cards mudam para 0 fechados e 2 registros. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Caixas" |
| 2. Observar o período nos filtros (01/10/2026 a 31/10/2026) |
| 3. Observar as datas dos caixas na lista e os cards |
| 4. Clicar em "Buscar" sem alterar os filtros |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A lista e os cards devem respeitar o período exibido desde a abertura da tela. | A lista inicial mostra caixas de 2022 a 2025 fora do período, e os números mudam ao clicar em "Buscar" com os mesmos filtros. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Caixas         | C25-CT02: Filtrar caixas por status |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/358a7731-1720-44d4-a9e4-489a9d7aa977) (0:03 a 0:21 e 0:27 a 0:34) |

---

### 🐞 **Bug 39: "Erro no servidor" ao abrir caixa sem selecionar o local**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-039    | Ao clicar em "Salvar" na janela Abrir Caixa sem selecionar o Local de Caixa, o sistema exibe "Erro no servidor – Erro interno inesperado." em vez de indicar o campo obrigatório. Com o local "Caixa Academia" selecionado, o caixa é aberto normalmente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Caixas" e clicar em "Abrir Caixa" |
| 2. Deixar o campo Local de Caixa vazio |
| 3. Clicar em "Salvar" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve informar que o Local de Caixa é obrigatório. | É exibido "Erro no servidor – Erro interno inesperado.". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Caixas         | C25-CT01: Abrir caixa com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/358a7731-1720-44d4-a9e4-489a9d7aa977) (0:38 a 0:41) |

---

### 🐞 **Bug 40: Painel Pagar.me mostra R$ 38.420,00 em recebimentos sem nenhuma transação**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-040    | O painel Pagar.me exibe "Recebimentos R$ 38.420,00" nos últimos 30 dias (+18,6% vs período anterior), com gráfico e percentuais por meio de pagamento (Cartão 62%, PIX 23%, Boleto 10%, Recorrência 3%, Outros 2%). Porém os valores de cada meio de pagamento e todos os saldos aparecem como "R$ --", a lista de Transações recentes está vazia e "Ver todas as transações" informa "Nenhuma transação encontrada no período". Os números do gráfico não têm origem nas transações e parecem fixos (dados de exemplo). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Pagar.me"                                   |
| 2. Observar o total de Recebimentos e os Meios de pagamento    |
| 3. Observar os saldos e as Transações recentes                 |
| 4. Clicar em "Ver todas as transações"                         |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O total de recebimentos deve corresponder às transações do período e aos valores por meio de pagamento. | O total é R$ 38.420,00, mas não há nenhuma transação e os valores por meio de pagamento aparecem como "R$ --". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|          Pagar.me          | C26-CT02: Verificar coerência dos valores de recebimento |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/b0dd20aa-9807-4d90-8e89-d69506a338e6) (0:01 a 0:06 e 0:18 a 0:19) |

---

### 🐞 **Bug 41: Sistema permite cadastrar atividade sem nome**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-041    | Ao clicar em "Salvar" no cadastro de atividade com os campos Nome e Pontuação em branco, o sistema não exibe mensagem de erro e o registro é criado. O card "Total de atividades" passa de 5 para 6 (#7) e, em uma segunda tentativa, de 7 para 8 (#9), com linhas sem nome na lista. Já existia o #6 também sem nome. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Atividades" e clicar em "Nova Atividade"    |
| 2. Deixar os campos Nome e Pontuação em branco                 |
| 3. Clicar em "Salvar"                                          |
| 4. Observar a lista e o card "Total de atividades"             |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve impedir o cadastro e exibir uma mensagem de erro no campo Nome. | A atividade é salva sem nome e aparece na lista. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Atividades         | C27-CT02: Tentar adicionar atividade sem nome      |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/ed415e90-3014-48aa-a674-47e90cc67b41) (0:03 a 0:05 e 0:28 a 0:30) |

---

### 🐞 **Bug 42: Pontuação sem datas é salva com período "0000-00-00 — 0000-00-00"**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-042    | Ao cadastrar a pontuação "Desafio de Novembro" (tipo Mensal) sem preencher Data Inicial e Data Final, o sistema salva sem aviso e a lista exibe o período "0000-00-00 — 0000-00-00", uma data inválida. O mesmo ocorre com a pontuação #6. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Pontuação" e clicar em "Nova Pontuação"     |
| 2. Preencher o Nome e manter o Tipo "Mensal"                   |
| 3. Deixar Data Inicial e Data Final em branco                  |
| 4. Clicar em "Salvar" e observar a coluna Período              |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve exigir as datas ou exibir o período de forma válida (ex.: "Mensal" ou "-"). | O período aparece como "0000-00-00 — 0000-00-00". |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Pontuação          | C28-CT01: Adicionar nova pontuação com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f74dc437-c900-4899-be8d-6f7b75f109e6) (0:25 a 0:28) |

---

### 🐞 **Bug 43: Não é possível cadastrar enquete**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-043    | Ao salvar a enquete "Enquete Hendreu" com a pergunta "Voce gosta de treinos?" e as respostas "sim" e "nao", o sistema exibe "Erro ao salvar enquete" e nada é gravado. O erro ocorre com o status Ativo e Inativo, com uma ou duas respostas. As 30 enquetes da lista aparecem como "Sem pergunta cadastrada" e o card "Respostas" mostra 0. O banco estava respondendo no momento do teste (SELECT 1 executado com sucesso). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Enquetes" e clicar em "Nova Enquete"        |
| 2. Preencher o Nome "Enquete Hendreu" e a Pergunta "Voce gosta de treinos?" |
| 3. Preencher as respostas "sim" e "nao"                        |
| 4. Clicar em "Salvar"                                          |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A enquete deve ser salva e exibida na lista com a pergunta cadastrada.  | É exibido "Erro ao salvar enquete" e a enquete não é cadastrada.       |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|          Enquetes          | C29-CT01: Adicionar nova enquete com pergunta      |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/3017b60f-a6e0-4388-90f4-e669845a4e87) (0:47 a 1:05) |
| Consulta no banco: SELECT 1 respondeu às 15:57 (banco disponível) |

---

### 🐞 **Bug 44: Anamnese pode ser aplicada sem selecionar aluno e termina com "Erro no servidor"**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-044    | Na janela Aplicar Anamnese, o botão "Próxima" avança sem nenhum aluno selecionado, permitindo escolher o modelo, responder e revisar. Ao clicar em "Finalizar Anamnese", o sistema exibe "Erro no servidor – Erro interno inesperado." e, numa segunda tentativa, fica em "Salvando..." e volta sem salvar, sem nenhuma mensagem. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Fichas Anamnese" e clicar em "Nova Anamnese" |
| 2. Não informar nenhum aluno e clicar em "Próxima" |
| 3. Escolher o modelo "Triplet 2", clicar em "Iniciar" e depois em "Revisar" |
| 4. Clicar em "Finalizar Anamnese" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve impedir o avanço e informar que é preciso selecionar um aluno. | O fluxo avança sem aluno e termina com "Erro no servidor" ou sem resposta. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Fichas de Anamnese         | C30-CT02: Tentar aplicar anamnese sem selecionar aluno |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/3555370a-0ce3-49df-b4eb-33105bfebfdd) (0:07 a 0:17 e 0:28 a 0:40) |

---

### 🐞 **Bug 45: Modelo de anamnese informa 2 perguntas, mas exibe apenas 1 e a revisão mostra outra pergunta**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-045    | O modelo "Triplet 2" aparece com "2 perguntas" na seleção, mas o questionário mostra "Pergunta 1 de 1" ("qual é o exercicio"). Na tela de revisão, a resposta aparece ligada a outra pergunta ("quais tipos"). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Fichas Anamnese" e clicar em "Nova Anamnese" |
| 2. Avançar até a escolha do modelo e selecionar "Triplet 2" |
| 3. Clicar em "Iniciar" e observar a quantidade de perguntas |
| 4. Responder e clicar em "Revisar" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O questionário deve exibir as 2 perguntas do modelo, e a revisão deve mostrar a mesma pergunta respondida. | Só 1 pergunta é exibida, e a revisão mostra uma pergunta diferente da respondida. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Fichas de Anamnese         | C30-CT01: Aplicar nova anamnese a um aluno |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/3555370a-0ce3-49df-b4eb-33105bfebfdd) (0:09 a 0:14 e 0:34 a 0:37) |

---

### 🐞 **Bug 46: Anamnese aplicada ao aluno não é gravada**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-046    | Ao aplicar o modelo "Triplet 2" ao aluno "Hendreu Teste", responder e clicar em "Finalizar Anamnese", a janela fecha sem mensagem de sucesso ou de erro. A lista continua com "Nenhuma ficha encontrada" e todos os cards em 0. No banco, a tabela ficha_anamnese não tem nenhum registro. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar "Fichas Anamnese" e clicar em "Nova Anamnese"       |
| 2. Buscar e selecionar o aluno "Hendreu Teste"                 |
| 3. Escolher o modelo "Triplet 2", clicar em "Iniciar", responder e clicar em "Revisar" |
| 4. Clicar em "Finalizar Anamnese"                              |
| 5. Consultar no banco: SELECT * FROM ficha_anamnese ORDER BY id DESC LIMIT 5; |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A ficha deve ser salva e exibida na lista com status Pendente ou Concluído. | A janela fecha sem aviso, a lista continua vazia e nada é gravado no banco. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|     Fichas de Anamnese     | C30-CT01: Aplicar nova anamnese a um aluno         |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/b5f3781c-f45f-4920-a0de-b87f5422c2c7) (0:04 a 0:19) |
| Consulta no banco: ficha_anamnese sem nenhum registro (0 rows) |

---

### 🐞 **Bug 47: Preview do modelo de anamnese não mostra as perguntas cadastradas**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-047    | Ao clicar em "Preview" no modelo "Triplet 2" (2 perguntas) e no "Modelo Hendreu" (1 pergunta), a janela exibe "Nenhuma pergunta adicionada ainda.", embora os cards dos modelos informem a quantidade de perguntas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Modelos" de Anamnese |
| 2. Clicar em "Preview" no modelo "Triplet 2" |
| 3. Repetir no "Modelo Hendreu" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O preview deve exibir as perguntas do modelo como o aluno verá. | É exibido "Nenhuma pergunta adicionada ainda." nos dois modelos. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Modelos de Anamnese         | C31-CT02: Visualizar prévia do modelo |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/5274fc54-e9cb-40c5-8aae-1c2a0ec85fe9) (0:11 a 0:16 e 0:36 a 0:38) |

---

### 🐞 **Bug 48: Modelo de anamnese mostra 3 aplicações, mas nenhuma ficha existe**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-048    | O card "Aplicações" e o modelo "Triplet 2" informam 3 aplicações, mas a tela Fichas de Anamnese mostra 0 fichas e a tabela ficha_anamnese do banco está vazia. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Baixa            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Modelos" de Anamnese e observar o card "Aplicações" e o modelo "Triplet 2" |
| 2. Acessar "Fichas Anamnese" e observar o total de fichas |
| 3. Consultar no banco: SELECT * FROM ficha_anamnese; |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A quantidade de aplicações deve ser igual à quantidade de fichas aplicadas. | O card mostra 3 aplicações, enquanto não existe nenhuma ficha. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Modelos de Anamnese         | C31-CT03: Filtrar modelos por status |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/5274fc54-e9cb-40c5-8aae-1c2a0ec85fe9) (0:05 e 0:35) |

---

### 🐞 **Bug 49: Card "Com perguntas" conta categoria recém-criada sem nenhuma pergunta**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-049    | Após criar a categoria "Historico de Lesoes", sem nenhuma pergunta vinculada, o card "Com perguntas" passa de 3 para 4. O card acompanha o total de categorias em vez de contar apenas as que têm perguntas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Baixa            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Categorias" de Anamnese e observar o card "Com perguntas" |
| 2. Clicar em "Nova Categoria", preencher o nome e clicar em "Criar Categoria" |
| 3. Observar novamente o card "Com perguntas"                   |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O card deve continuar em 3, pois a nova categoria não tem perguntas.    | O card passa para 4, igual ao total de categorias.                     |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|  Categorias de Anamnese    | C32-CT01: Adicionar nova categoria com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f53f9550-0b7a-4e79-b236-1f6d05feb717) (0:01 e 0:27) |

---

### 🐞 **Bug 50: Sistema permite cadastrar pergunta de anamnese sem nome e sem texto**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-050    | Ao clicar em "Salvar" no cadastro de pergunta com os campos Nome e Pergunta em branco, o sistema salva sem mensagem de erro. O total passa de 2 para 3 (#7) e, numa segunda tentativa, para 4 (#8), com linhas vazias na lista. Essas perguntas não podem ser encontradas pela busca. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Perguntas" de Anamnese e clicar em "Nova Pergunta" |
| 2. Deixar os campos Nome e Pergunta em branco |
| 3. Clicar em "Salvar" |
| 4. Observar a lista e o card "Total de perguntas" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O sistema deve impedir o cadastro e informar que o texto da pergunta é obrigatório. | A pergunta é salva vazia e aparece na lista. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Perguntas de Anamnese         | C33-CT02: Tentar adicionar pergunta em branco |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f3ac1ddf-61d0-4eae-bf87-ecc0602b5dd2) (0:03 a 0:08) |

---

### 🐞 **Bug 51: Cadastro de pergunta de anamnese não tem campo para escolher a categoria**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-051    | O formulário "Pergunta Anamnese" tem apenas Código, Nome, Status, Pergunta, Número e Tipo Resposta. Não existe campo de categoria, então não é possível ligar a pergunta a uma das categorias cadastradas (ex.: "Historico de Lesoes"). As categorias continuam sem relação com as perguntas criadas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Perguntas" de Anamnese e clicar em "Nova Pergunta" |
| 2. Procurar um campo para escolher a categoria |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O formulário deve permitir escolher a categoria da pergunta. | Não há campo de categoria no formulário. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Perguntas de Anamnese         | C33-CT01: Adicionar nova pergunta com dados válidos |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/f3ac1ddf-61d0-4eae-bf87-ecc0602b5dd2) (0:09 a 0:23) |

---

### 🐞 **Bug 52: Resultados da Inteligência apontam 42 inadimplentes, mas a Página Inicial mostra R$ 0,00 em aberto**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-052    | Na tela Resultados da Inteligência, o card "Alunos inadimplentes monitorados" mostra 42 e o painel Inteligência Sifit informa "42 aluno(s) inadimplente(s) sendo monitorado(s)". Na Página Inicial, no mesmo momento, o card mostra "R$ 0,00 em aberto" e o "Total em aberto" das mensalidades pendentes também é R$ 0,00. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta         |           Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Resultados IA" e observar o card "Alunos inadimplentes monitorados" |
| 2. Acessar a "Página Inicial" e observar o card "em aberto" e o quadro "Mensalidades pendentes" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| As duas telas devem apresentar informações coerentes sobre a inadimplência. | A inteligência aponta 42 inadimplentes enquanto a Página Inicial mostra R$ 0,00 em aberto. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Resultados IA / Página Inicial         | C35-CT03: Verificar quantidade de inadimplentes |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/3b7b3ec0-bd1f-43eb-99f3-72fa107f4b3f) (0:01, 0:25 e 0:27 a 0:31) |

---

### 🐞 **Bug 53: Filtro "Hoje" dos Resultados da Inteligência não atualiza todos os cards**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-053    | Ao selecionar o período "Hoje", os cards de automações, relatórios, aniversariantes e avaliações vão a 0 e o histórico mostra "Ainda não há registros no período", mas os cards "Alunos em risco identificados" (1) e "Alunos inadimplentes monitorados" (42) e o painel Inteligência Sifit (7 alunos em risco) continuam iguais aos dos outros períodos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Baixa            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Resultados IA" |
| 2. Clicar em "Hoje" |
| 3. Comparar os cards com os de "Últimos 7 dias" e "Últimos 30 dias" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| Todos os cards devem respeitar o período selecionado, ou indicar que não dependem dele. | Parte dos cards zera e parte continua igual, mesmo sem registros no período. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Resultados IA         | C35-CT02: Filtrar resultados por período |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/3b7b3ec0-bd1f-43eb-99f3-72fa107f4b3f) (0:08 a 0:10) |

---

### 🐞 **Bug 54: Campo "Dias para contar cliente como ausente" aceita valor negativo**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-054    | Na aba Home das Configurações, o campo "Dias para contar cliente como ausente" está com o valor -120 e aceita ser salvo com -60. Um número negativo de dias não faz sentido para essa regra e pode explicar a divergência de clientes ausentes entre telas (BUG-002). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Configurações", aba "Home" |
| 2. Observar o campo "Dias para contar cliente como ausente" |
| 3. Informar -60 e clicar em "Salvar Configurações" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O campo deve aceitar apenas números positivos e recusar valores negativos. | O valor -120 está cadastrado e o sistema salva -60 sem aviso. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Configurações         | C37-CT03: Cancelar alteração de configuração |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/9c52920c-240b-49e1-8cac-e183cbf67b26) (0:01 e 0:45 a 0:53 (o valor original -120 foi restaurado aos 0:57)) |

---

### 🐞 **Bug 55: Senha do aparelho biométrico é exibida em texto aberto nas Configurações**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-055    | Na aba Biometria das Configurações, os campos Login e Senha do aparelho de catraca (Control ID) aparecem com o conteúdo visível, sem máscara. A senha visível é a padrão de fábrica. Qualquer usuário com acesso à tela pode ver a credencial do equipamento. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Configurações" |
| 2. Clicar na aba "Biometria" |
| 3. Observar os campos Login e Senha |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| A senha deve aparecer mascarada (••••), e o sistema deve recomendar a troca da senha padrão. | Login e senha aparecem em texto aberto. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Configurações / Biometria         | C37-CT02: Navegar entre as abas de configuração |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/9c52920c-240b-49e1-8cac-e183cbf67b26) (0:05 a 0:06) |

---

### 🐞 **Bug 56: Botão "Gerar aulas" do SifitBox não gera aulas nem exibe mensagem**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-056    | Na tela SifitBox - Aulas, com o período de 23/10/2026 a 30/10/2026 e turmas recorrentes cadastradas em "Box - Turmas", o botão "Gerar aulas" foi clicado várias vezes. Nenhuma aula foi criada, nenhuma mensagem de sucesso ou de erro foi exibida e a lista continuou com "Nenhuma aula encontrada no periodo." mesmo após clicar em "Buscar". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Alta          |            Alta            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Conferir em "Box - Turmas" que existem turmas recorrentes ativas |
| 2. Acessar o menu "SifitBox" com o período de 23/10/2026 a 30/10/2026 |
| 3. Clicar em "Gerar aulas"                                     |
| 4. Clicar em "Buscar"                                          |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| As aulas das turmas recorrentes devem ser geradas e exibidas, ou o sistema deve informar por que não gerou. | Nada acontece: nenhuma aula é gerada e nenhuma mensagem é exibida. |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|          SifitBox          | C38-CT03: Gerar aulas do SifitBox                  |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/2851a247-c28c-4af5-b678-18100c5083bd) (0:11 a 0:20 turmas cadastradas; 0:27 a 0:40 cliques em "Gerar aulas") |

---

### 🐞 **Bug 57: Tela Dashboard exibe o título "Despesas Fixas"**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-057    | Ao acessar o menu "Dashboard" (endereço /dash), o menu lateral marca "Dashboard", mas o título da página exibido no topo é "Despesas Fixas". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Baixa         |           Baixa            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Realizar login no SIFIT                                     |
| 2. Clicar no menu "Dashboard"                                  |
| 3. Observar o título no topo da página                         |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O título da página deve ser "Dashboard".                               | O título exibido é "Despesas Fixas".                                   |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|         Dashboard          | C39-CT01: Acesso ao Dashboard pelo menu            |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/5ef4bb24-0b96-4099-ae8f-18d4a74f6314) (0:00 e 0:37) |

---

### 🐞 **Bug 58: Perfil do cliente mostra check-in registrado, mas "Últimas Presenças" aparece vazio**

| **ID**     | **Descrição**                                                                                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| BUG-058    | No perfil do cliente "Hendreu Teste" (#413), o bloco Desempenho do aluno informa "Total de check-ins 1", "Este mês 1 check-in" e "Último registro 21/10/2026", mas o bloco "Últimas Presenças" exibe "Nenhuma presença registrada". |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :-------------------: | :------------------------: | :--------: |
|         Média         |           Média            |   Aberto   |

| **Passo a passo para simular o bug**                           |
| -------------------------------------------------------------- |
| 1. Acessar o menu "Clientes" e buscar "Hendreu Teste"          |
| 2. Clicar na lupa do cliente                                   |
| 3. Comparar o bloco "Desempenho do aluno" com o bloco "Últimas Presenças" |

|                        **Comportamento Esperado**                       |                        **Comportamento Obtido**                        |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| O check-in de 21/10/2026 deve aparecer em "Últimas Presenças".          | "Últimas Presenças" mostra "Nenhuma presença registrada".              |

| **Ambiente**             |
| ------------------------ |
| Ambiente de testes.      |
| Desktop com Windows 11.  |
| Chrome 155.0.8059.85     |
| SIFIT                    |

| **Funcionalidade Afetada** |           **Caso de Teste Relacionado**            |
| :------------------------: | :------------------------------------------------: |
|     Perfil do Cliente      | C40-CT01: Visualizar perfil do cliente             |

|                **Evidência(s)**               |
| :-------------------------------------------: |
| [Vídeo](https://jam.dev/c/a088a7ce-c852-4bbd-8747-1d230586d096) (0:32 a 0:36) |
