## Cenário 01: Login na plataforma.

### Caso de Teste 01: Login com as credenciais válidas.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C01-CT01 | O login será realizado com um login e uma senha válidos.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| As credenciais fornecidas (login e senha) devem ser válidas.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do SIFIT                  |
| **E** preenchemos o login de teste no campo "Login"               |
| **E** preenchemos a senha correta no campo "Senha"                |
| **QUANDO** clicarmos no botão "Entrar"                            |
| **ENTÃO** seremos redirecionados para a Página Inicial do sistema |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O redirecionamento para a Página Inicial deve ocorrer corretamente. |

---

### Caso de Teste 02: Tentativa de login com senha incorreta.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C01-CT02 | O login falhará quando a senha for inválida.               |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário de teste deve existir no sistema.                   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do SIFIT                  |
| **E** preenchemos o login de teste no campo "Login"               |
| **E** preenchemos "senhaerrada" no campo "Senha"                  |
| **QUANDO** clicarmos no botão "Entrar"                            |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A mensagem "O nome de usuário e senha não correspondem" deve ser exibida e o acesso não deve ser liberado. |

---

### Caso de Teste 03: Login com a opção manter conectado.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C01-CT03 | O usuário deve continuar logado ao reabrir o sistema.      |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| As credenciais fornecidas devem ser válidas.                  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página de login do SIFIT                  |
| **E** preenchemos login e senha válidos                           |
| **E** marcamos a opção "Manter conectado"                         |
| **QUANDO** fecharmos a aba e acessarmos o sistema novamente       |
| **ENTÃO** a Página Inicial deve ser exibida sem pedir login       |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A sessão deve ser mantida quando a opção estiver marcada.       |
