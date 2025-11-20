Link da pasta Roteiro 04: https://drive.google.com/drive/folders/1zN9IOScKdN2Um4QztDwjb7z7EZ_7Mkze?usp=drive_link

## Cenário 06: Gestão de Clientes

### Caso de Teste 01: Cadastrar novos clientes (PF e PJ).

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C06-CT01 | O sistema deve permitir o cadastro de novos clientes Pessoa Física e Pessoa Jurídica. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo Cadastro de Clientes.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Cadastro de Clientes”      |
| **E** clica no botão “Novo”                                       |
| **E** preenche todos os campos necessários (PF ou PJ)             |
| **QUANDO** clicar no botão “Salvar”                               |
| **ENTÃO** o cliente deve ser cadastrado com sucesso               |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O cliente deve aparecer corretamente na lista.                  |
| [Video](https://drive.google.com/file/d/1Ro0UNYa4PVTYnZ6WFNf4mY9wMsph235H/view?usp=drive_link) |

---

### Caso de Teste 02: Tentar cadastrar cliente com campos obrigatórios vazios.

| ID       | Descrição                                                                       |
| :------- | :-------------------------------------------------------------------------------|
| C06-CT02 | Sistema deve impedir o cadastro de cliente sem preencher campos obrigatórios.   |  

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
| O sistema NÃO deve salvar o cliente. |
| [Video](https://drive.google.com/file/d/1DjwfrkB1brsQRqnwS_cvOsF0Lo5NavmJ/view?usp=drive_link) |

---

### Caso de Teste 03: Habilitar limite de crédito para cliente.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C06-CT03 | O sistema deve permitir habilitar e configurar limite de crédito para clientes. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Cliente cadastrado no sistema.                                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador abre a tela “Cadastro de Clientes”        |
| **E** clica em “Novo” ou em “Alterar” para editar um cliente existente  |
| **E** acessa a aba “Dados Financeiros”                            |
| **E** informa um limite de crédito e condiçãoe                    |
| **QUANDO** clicar em “Salvar”                                     |
| **ENTÃO** o limite deve ser registrado corretamente               |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O limite de crédito deve aparecer na aba Dados Financeiros após salvar.  |
| [Video](https://drive.google.com/file/d/16yHRdAYLMb3xLgXtda8BtL4Cx1wD2dfx/view?usp=drive_link) |

---

### Caso de Teste 04: Informar limite de crédito inválido.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C06-CT04 | Sistema deve impedir salvar limite de crédito com valores inválidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Cliente cadastrado no sistema.                                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa a aba “Dados Financeiros”          |
| **E** informa um valor de limite negativo ou não numérico          |
| **QUANDO** clicar em “Salvar”                                     |
| **ENTÃO** o sistema deve exibir erro e impedir o salvamento       |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Deve existir mensagem clara orientando o usuário.               |
| [Video](https://drive.google.com/file/d/1xUxynOaDpFCniSsMWBQICZ2VR71PTPx8/view?usp=drive_link) |

---

### Caso de Teste 05: Adicionar dependentes a clientes.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C06-CT05 | Sistema deve permitir adicionar dependentes ao cliente.        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Cliente cadastrado no sistema.                                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador abre o cliente e clica em “Dependentes”   |
| **E** clica no botão “Novo”                                       |
| **E** preenche os dados do dependente                             |
| **QUANDO** clicar em “Salvar”                                     |
| **ENTÃO** o dependente deve ser exibido na lista de dependentes do cliente  |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Dependente deve aparecer corretamente vinculado ao cliente.     |
| [Video](https://drive.google.com/file/d/1X4bTvLtmhCl9QnGhVGd8WUQYAkOGWRDn/view?usp=drive_link) |

---

### Caso de Teste 06: Registrar vendas para os clientes.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C06-CT06 | Sistema deve permitir registrar vendas para clientes           |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Clientes e produtos cadastrado no sistema.                                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Venda”                     |
| **E** clica no botão “Novo”                                       |
| **E** informa o cliente                                           |
| **E** adiciona um produto                                         |
| **QUANDO** clicar em “Salvar”                                     |
| **ENTÃO** a venda deve ser registrada corretamente                |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A venda deve ser registrada corretamente.                       |
| [Video](https://drive.google.com/file/d/1cXbpJPIg27pbua0iMOHJWdaFxY60opBn/view?usp=drive_link) |

---

### Caso de Teste 07: Venda dentro do limite de crédito.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C06-CT07 | Sistema deve permitir venda dentro do limite de crédito        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Clientes e produtos cadastrado no sistema.                                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o cliente possui limite de crédito                   |
| **E** a soma da compra dentro do limite                           |
| **QUANDO** CLica pra finalizar a venda                            |
| **ENTÃO** a venda deve ser registrada corretamente                |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A venda deve ser registrada corretamente                        |
| [Video](https://drive.google.com/file/d/14t2DvZOdtyE_aff3_4qv-O0ig_6FS7ak/view?usp=drive_link) |

---

### Caso de Teste 08: Atualizar limite de crédito.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C06-CT08 | SSistema deve permitir alterar o limite de crédito de um cliente  |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Cliente existente com limite cadastrado.                      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o cadastro do cliente              |
| **E** clica em “Alterar”                                          |
| **E** altera o limite de crédito                                  |
| **QUANDO** Caltera o limite de crédito                            |
| **ENTÃO** o novo limite deve ser atualizado                       |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |  
| O valor atualizado deve ser exibido corretamente na aba financeira.  |                                               
| [Video](https://drive.google.com/file/d/1hHsY-CdSgNGnkkfQ2CzfZXmZ8dK4hrnn/view?usp=drive_link) |

---

### Caso de Teste 09: Editar cliente.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C09-CT09 | O sistema deve permitir a edição de clientes                         |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo cadastro de transportadoras. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Cadastro de cliente"       |
| **E** clica no botão “Editar”                                     |
| **E** alterar o nome do cliente                                   |
| **QUANDO** clicar no botão “Salvar”                               |
| **ENTÃO** os dados do cliente deve ser alterado com sucesso       |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O cliente deve aparecer com os dados alterados.                 |
| [Video](https://drive.google.com/file/d/1xJUoyVCiTKEPWl8C9JVJFg-KtT-2bcAv/view?usp=drive_link) |

---

### Caso de Teste 10: Excluir cliente

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C09-CT10 | O sistema deve permitir a exclusão clientes                   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao módulo cadastro de clientes. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “gestão de cliente”         |
| **QUANDO** clicar no botão “excluir”                              |
| **E** clicar pra confirmar a exclusão                             |
| **ENTÃO** o cliente deve ser deletado com sucesso                 |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O cliente deve ser deletado com sucesso                         |
| [Video](https://drive.google.com/file/d/1HwZc4_3Zqd7Wve24U08H5exbVBp5vhMy/view?usp=drive_link) |