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
