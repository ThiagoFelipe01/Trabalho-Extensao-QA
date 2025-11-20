Link da pasta cadastro transportadora: https://drive.google.com/drive/folders/1G6uMrls4-Zovk2tzQpeHFMi0NWRwT9vt?usp=drive_link

## Cenário 09: Gestão de transportadora

### Caso de Teste 01: Cadastrar novas transportadoras.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C09-CT01 | O sistema deve permitir o cadastro de novas transportadoras            |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo Cadastro transportadoras .  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Cadastro de transportadoras ”  |
| **E** clica no botão “Novo”                                       |
| **E** preenche todos os campos necessários                        |
| **QUANDO** clicar no botão “Salvar”                               |
| **ENTÃO** a transportadora deve ser cadastrado com sucesso        |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A transportadora deve aparecer corretamente na lista.           |
| [Video](https://drive.google.com/file/d/1PSyRPQWG3Bj95WDRTfO5sUYYBKMZV1pm/view?usp=drive_link) |

---

### Caso de Teste 02: Tentar cadastrar transportadora com campos obrigatórios vazios.

| ID       | Descrição                                                                       |
| :------- | :-------------------------------------------------------------------------------|
| C09-CT02 | Sistema deve impedir o cadastro de transportadora sem preencher campos obrigatórios.  |  

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Usuário com acesso à tela de cadastro.                        |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador clica em “Novo”                           |
| **E** deixa um ou mais campos obrigatórios em branco              |
| **QUANDO** clicar em “Salvar”                                     |
| **ENTÃO** o sistema deve exibir mensagens de erro indicando os campos faltantes |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema NÃO deve salvar a transportadora. |
| [Video](https://drive.google.com/file/d/1gGIaysPS5oPms9tejBFIAW3Vs8T46M3-/view?usp=drive_link) |

---

### Caso de Teste 03: Editar transportadora.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C09-CT03 | O sistema deve permitir a edição de transportadoras                  |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo cadastro de transportadoras. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Cadastro de transportadoras"  |
| **E** clica no botão “Editar”                                     |
| **E** alterar o nome da transportadora                            |
| **QUANDO** clicar no botão “Salvar”                               |
| **ENTÃO** os dados da transportadora deve ser alterado com sucesso  |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A transportadora deve aparecer com os dados alterados.             |
| [Video](https://drive.google.com/file/d/1vhnRfQ6jqJ_XmB2k9HdpPxWI29TWfAeO/view?usp=drive_link) |

---

### Caso de Teste 04: Excluir transportadora

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C09-CT03 | O sistema deve permitir a exclusão transportadoras                   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo cadastro de transportadoras. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “gestão de ransportadoras”  |
| **QUANDO** clicar no botão “excluir”                              |
| **E** clicar pra confirmar a exclusão                              |
| **ENTÃO** a transportadora deve ser deletado com sucesso             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A transportadora deve ser deletado com sucesso                  |
| [Video](https://drive.google.com/file/d/1B9cWvie4BjKxbcY-oV6ZpczeOMivFH8j/view?usp=drive_link) |
