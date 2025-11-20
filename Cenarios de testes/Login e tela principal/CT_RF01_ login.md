Link pasta Login e tela principal: https://drive.google.com/drive/folders/1CaSHCCimB0hGvGJE4Zdz0YKFung9Uq4W?usp=drive_link

## Cenário 01: Login na plataforma.

### Caso de Teste 01: Login com as credenciais válidas.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT01 | O login será realizado com um nome de usuário e uma senha válidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| As credenciais fornecidas (usuário e senha) devem ser válidas. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** Estamos na tela de login do Sistema Afa              |
| **E** preenchemos "GERENTE" no campo usuário                  |
| **E** preenchemos "afa" no campo senha                        |
| **QUANDO** Teclar Enter                                       |
| **ENTÃO** seremos redirecionados para a Tela principal do sistema    |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O redirecionamento para a tela principal deve ocorrer corretamente. |
| [Video]([https://drive.google.com/file/d/1FxPNN-mu3TMPK14-gHkH7_Z1sifKnJAl/view?usp=drive_link]()) |

---

### Caso de Teste 02: Tentativa de login com senha incorreta.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT02 | O login falhará quando a senha for inválida.             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário \"GERENTE\" deve existir no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de login do sistema afa              |
| **E** preenchemos "GERENTE" no campo usuário                      |
| **E** preenchemos "senhaerrada" no campo senha                    |
| **QUANDO** Teclar Enter                                           |
| **ENTÃO** uma mensagem de erro \"senha inválida\" será exibida |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A mensagem de erro \"senha inválida\" deve ser exibida.    |
| [Video]([https://drive.google.com/file/d/1LOPaBKUEnHeQC8QCExkWV1DGxaKSnqGv/view?usp=drive_link]()) | 

---

### Caso de Teste 03: Tentativa de login com campos em branco.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C01-CT03 | O login falhará quando os campos obrigatórios estiverem em branco. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Nenhuma. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela de login do sistema afa              |
| **E** deixamos os campos de usuário e senha em branco             |
| **QUANDO** teclar Enter                                           |
| **ENTÃO** deve ser exibida a mensagem em cada campo: o campor é obrigatório |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os campos obrigatórios devem exibir mensagens de validação.     |
| [Video]([https://drive.google.com/file/d/1djjcMxQ-gTE6gFQ3hF76oYK0MgJQ-b-Q/view?usp=drive_link]()) |