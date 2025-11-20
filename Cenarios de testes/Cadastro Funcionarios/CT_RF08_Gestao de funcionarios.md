Link da pasta cadastro Funcinários: https://drive.google.com/drive/folders/11u5dgmnu2xJTU27OJhNdza9XhCGX2Dz7?usp=drive_link

## Cenário 08: Gestão de funcionarios

### Caso de Teste 01: Cadastrar novos funcionarios.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C08-CT01 | O sistema deve permitir o cadastro de novos funcionarios             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo Cadastro defuncionarios.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Cadastro de funcionarios”  |
| **E** clica no botão “Novo”                                       |
| **E** preenche todos os campos necessários                        |
| **QUANDO** clicar no botão “Salvar”                               |
| **ENTÃO** o funcionario deve ser cadastrado com sucesso           |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O funcionario deve aparecer corretamente na lista.                  |
| [Video]([https://drive.google.com/file/d/1bRz6GA21f-tfoEQINp6_Hdo6EFdTXcGS/view?usp=drive_link]()) |

---

### Caso de Teste 02: Tentar cadastrar funcionário com campos obrigatórios vazios.

| ID       | Descrição                                                                       |
| :------- | :-------------------------------------------------------------------------------|
| C08-CT02 | Sistema deve impedir o cadastro de funcionário sem preencher campos obrigatórios.   |  

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
| O sistema NÃO deve salvar o funcionário. |
| [Video]([https://drive.google.com/file/d/1jxecLQFDOi82sqHhplq_9BHdzqlhur_v/view?usp=drive_link]()) |

---

### Caso de Teste 03: Editar funcionario.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C08-CT03 | O sistema deve permitir a edição funcionarios                        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo cadastro de funcionarios.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Cadastro de funcionarios”  |
| **E** clica no botão “Editar”                                     |
| **E** alterar o nome do funcionário                               |
| **QUANDO** clicar no botão “Salvar”                               |
| **ENTÃO** os dados do funcionario deve ser alterado com sucesso   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O funcionario deve aparecer com os dados alterados.             |
| [Video]([https://drive.google.com/file/d/11jkkg9O2qwMD2uKcxUlK-kIQdbjhgQQ5/view?usp=drive_link]()) |

---

### Caso de Teste 04: Excluir funcionario.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C08-CT03 | O sistema deve permitir a exclusão funcionarios                      |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo cadastro de funcionarios.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Cadastro de funcionarios”  |
| **QUANDO** clicar no botão “excluir”                              |
| **E** clicar pra confirmar a exclusão                             |
| **ENTÃO** o funcionário deve ser deletado com sucesso             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O funcionario deve ser deletado com sucesso                     |
| [Video]([https://drive.google.com/file/d/16aSwoM-ilhMWro8DNCAiQsgNYQl6BP9U/view?usp=drive_link]()) |