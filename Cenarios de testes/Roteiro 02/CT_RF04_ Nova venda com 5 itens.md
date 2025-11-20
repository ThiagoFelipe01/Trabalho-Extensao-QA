Link pasta Roteiro 02: https://drive.google.com/drive/folders/1C3aPMs0WxRVbBG1L9uOtpDVich8DkOtU?usp=drive_link

## Cenário 04: Nova venda com 5 itens

### Caso de Teste 01: Iniciar nova venda com 5 itens


| ID       | Descrição                                                          |
| :------- | :----------------------------------------------------------------- |
| C04-CT01 | O sistema deve permitir iniciar uma nova venda e adicionar 5 itens ao pedido. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O sistema deve permitir iniciar uma nova venda e adicionar 5 itens ao pedido.   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o módulo de venda clicando no ícone "Venda"  |
| **E** clica no botão "Novo" para iniciar uma nova venda                     |
| **E** informa o número do cliente no campo menor OU clica no campo maior para pesquisar pelo nome |
| **E** informa o número do funcionário no campo menor OU clica no campo maior para pesquisar pelo nome |
| **QUANDO** clicar em "Salvar" para confirmar cliente e funcionário          |
| **E** no campo “Produto” digitar o código ou clicar no campo maior para pesquisar pelo nome |
| **E** informar a quantidade no campo “Quant.” e clicar em "Salvar"          |
| **E** repetir o processo clicando em "Novo" até completar os 5 itens        |
| **ENTÃO** os 5 itens devem ser adicionados à venda corretamente.            |
| **E** Clica no botão finalizar venda                              |
| **E** clicar no ícone “Folha” para abrir a tela de tipo de documento  |
| **E** selecionar “Cartão” como tipo de documento                  |
| **E** informar o itpo de pagamento                                |
| **E** clicar em "Salvar"                                          |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A venda é confirmada com 5 itens no total                       |
| [Video]([https://drive.google.com/file/d/1hecx5nXODj2ypD30HkhsJkrPxgR4F9hh/view?usp=drive_link]()) |

---

### Caso de Teste 02: Finalizar venda com pagamento misto (Cartão 70% + Dinheiro 30%)

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C04-CT02 | O sistema deve permitir finalizar uma venda utilizando pagamento misto. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| A venda deve estar com todos os itens adicionados e pronta para finalização. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador clica em "novo"                           |
| **E** informa o cliente e o funcionário                           | 
| **E** clicar em "Salvar" para confirmar cliente e funcionário  |
| **E** no campo “Produto” digitar o código ou clicar no campo maior para pesquisar pelo nome |
| **E** informar a quantidade no campo “Quant.” e clicar em "Salvar"   |
| **E** Clica no botão finalizar venda                              |
| **E** clicar no ícone “Folha” para abrir a tela de tipo de documento  |
| **E** selecionar “Cartão” como tipo de documento                  |
| **E** informar 70% do valor total                                 |
| **E** clicar em "Salvar"                                          |
| **E** novamente clicar no ícone “Folha”                           |
| **E** selecionar “Dinheiro” como tipo de documento                |
| **E** informar o restante (30%)                                   |
| **E** clicar em "Salvar"                                          |
| **E** Na tela confirmar venda clicar em "Salvar"                  |
| **Então** a venda deve ser confirmada                             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A venda deve ser finalizada com os dois tipos de pagamento cadastrados |
| [Video]([https://drive.google.com/file/d/17TdWNG-tzY4WRf67xu0iZRKDwbK4nIUu/view?usp=sharing]()) |

---

### Caso de Teste 03: Tentar iniciar venda sem selecionar cliente e funcionário

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C04-CT03 | O sistema deve impedir iniciar uma venda sem selecionar um cliente e funcionário. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O operador deve estar logado no PDV.                          |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador clica em "Venda"                          |
| **E** clica em "Novo"                                             |
| **E** não informa cliente e funcionário nem pesquisa pelo nome    |
| **QUANDO** tentar clicar em "Salvar"                              |
| **ENTÃO** o sistema deve exibir mensagem informando que o campo nome cliente não foi preenchido |
| **Então** o sistema deve exibir mensagem informando que o campo nome funcionário não foi preenchido |


| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve impedir o avanço e exibir mensagem de validação destacando o campo do cliente, do Funcionário |
| [Video]([https://drive.google.com/file/d/1vj6yyI9FYRHHGg7nKbeRxn2N_p8ibIq5/view?usp=sharing]()) |

---

### Caso de Teste 04: Tentar finalizar venda sem cadastrar forma de pagamento

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C04-CT04 | O sistema deve impedir finalizar a venda caso nenhum tipo de pagamento seja informado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Venda com produtos já adicionados.                            |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador clica em "novo"                           |
| **E** informa o cliente e o funcionário                           | 
| **E** clicar em "Salvar" para confirmar cliente e funcionário     |
| **E** no campo “Produto” digitar o código ou clicar no campo maior para pesquisar pelo nome |
| **E** informar a quantidade no campo “Quant.” e clicar em "Salvar"   |
| **E** Clica no botão finalizar venda                              |
| **E** Prencha o status da venda                                   |
| **E** Deixa o tipo de pagamento vazio                             |
| **E** Clica em salvar                                             |
| **Então** o sistema deve exibir mensagem: tipo de documento difere com o total do pedido   |


| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir mensagem alertando o valor do tipo de documento difere com o total do pedido |
| [Video]([https://drive.google.com/file/d/1CCU_usCZjQQIEu0zpco0vMg3oQGvfgF_/view?usp=drive_link]()) |

---

### Caso de Teste 05: Tentar finalizar venda Com valor de pagamento parcial

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C04-CT05 | O sistema deve impedir conclusão da venda caso os valores dos documentos não totalizem 100%. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Venda em processo de finalização.                             |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador clica em "novo"                           |
| **E** informa o cliente e o funcionário                           | 
| **E** clicar em "Salvar" para confirmar cliente e funcionário     |
| **E** no campo “Produto” digitar o código ou clicar no campo maior para pesquisar pelo nome |
| **E** informar a quantidade no campo “Quant.” e clicar em "Salvar"   |
| **E** Clica no botão finalizar venda                              |
| **E** Prencha o status da venda                                   |
| **E** adiciona pagamento com valor parcial                        |
| **QUANDO** clicar em "Salvar"                                     |
| **Então** o sistema deve impedir a conclusão da venda informando que tipo de documento difere com o total do pedido |


| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve validar os valores e exigir que somem 100% do valor da venda. |
| [Video]([https://drive.google.com/file/d/1ZGl0eMJfKF1AKMXbtXj3f5kQqaQKoHe9/view?usp=sharing]()) |