Link pasta Roteiro 01: https://drive.google.com/drive/folders/1wYvFLuQzzIpqJltKPqZmvL4wriRot8WT?usp=drive_link

## Cenário 03:Importação de produtos via xml..

### Caso de Teste 01: Adicionar novos produtos via importação XML.

| ID       | Descrição                                                          |
| :------- | :----------------------------------------------------------------- |
| C03-CT01 | O sistema deve permitir o cadastro de novos produtos via importação XML. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso tela de importar XML da compra.       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela de importar XML da compra    |
| **E** O operador deve clicar no menu “Pedido”                     |
| **E** depois em “Importar XML da Compra”                          |
| **E** Na janela que se abre, clicar no campo “CFOP” Entrada       |
| **E** digitar o código e selecionar o “Grupo”                     |
| **E** clicar no campo “ST Entrada”                                |
| **E** digitar o código e clicar no botão “Importar XML”.          |
| **E** Selecionar o arquivo XML e clicar no botão “Abrir”.         |
| **E** Após a listagem dos produtos, clique no botão “Gerar Compra”|
| **E** na janela que aparecer clicar no botão “Sim”.               |
| **E** olhar pro “Número de Itens” e “Quantidade Total”.           |
| **E** Na tela Confirmar Compra, o operador deve selecionar o “Status”|
| **E** deve clicar no ícone “Folha” e selecionar o tipo de pagamento|
| **E**  clicar no botão “salvar” na tela de pagamento              |
| **QUANDO** logo após clicar no botão “salvar” na tela de compra.  |
| **ENTÃO** A importação via XML deve salvar os produtos corretamente|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os Itens da compra via XML deverão aparecer na tela             |
| [Video]([https://drive.google.com/file/d/1aScQfCCg5eT9okYJSxXrELBdlD3NW_2l/view?usp=sharing]()) |

---

### Caso de Teste 02: Tentar importar XML sem preencher campos obrigatórios (CFOP / Grupo / ST Entrada )

| ID       | Descrição                                                                  |
| :------- | :------------------------------------------------------------------------- |
| C03-CT02 | O sistema deve exibir erros ao tentar importar XML sem preencher os campos obrigatórios. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso à tela “Importar XML da Compra”.|

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela de Importar XML              |
| **E** não preenche o campo “CFOP Entrada”                         |
| **E** não preenche o campo “ST Entrada”                           |
| **E** não preenche o campo “Grupo”                           |
| **QUANDO** clicar no botão “Importar XML”                         |
| **ENTÃO** o sistema deve exibir mensagens de erro indicando que os campos não foram preenchidos. |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os campos obrigatórios devem exibir mensagens de validação.     |
| [Video]([https://drive.google.com/file/d/1CZZPOShJGRlRlSZXi_wjMv7syb4e6LW-/view?usp=sharing]()) |

---

### Caso de Teste 03: Tentar importar um arquivo XML vazio

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C03-CT03 | O sistema deve identificar XML inválido e impedir a importação |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve possuir um arquivo XML vazio.                 |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário seleciona um arquivo XML vazio             |
| **QUANDO** clicar em “Abrir”                                      |
| **ENTÃO** o sistema deve exibir mensagem informando que o arquivo XMl é inválido.|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema não deve avançar para a listagem de produtos.         |
| [Video]([https://drive.google.com/file/d/1xozMKgCaVMUs5cCvWfkwVyHz8DjhSGU5/view?usp=sharing]()) |

---

### Caso de Teste 04: Tentar finalizar compra sem definir tipo de pagamento

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C03-CT04 | O sistema deve bloquear a tentativa de finalizar compra sem informar forma de pagamento. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O XML foi importado e a compra gerada.                        |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela de importar XML da compra    |
| **E** O operador deve clicar no menu “Pedido”                     |
| **E** depois em “Importar XML da Compra”                          |
| **E** Na janela que se abre, clicar no campo “CFOP” Entrada       |
| **E** digitar o código e selecionar o “Grupo”                     |
| **E** clicar no campo “ST Entrada”                                |
| **E** digitar o código e clicar no botão “Importar XML”.          |
| **E** Selecionar o arquivo XML e clicar no botão “Abrir”.         |
| **E** Após a listagem dos produtos, clique no botão “Gerar Compra”|
| **E** na tela Confirmar Compra                                    |
| **E** não clicou no ícone “Folha” para cadastrar o tipo de pagamento |
| **QUANDO** tentar clicar em “Salvar” na tela da compra            |
| **ENTÃO** o sistema deve alertar que o tipo de pagamento difere do total do pedido.|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve bloquear o salvamento.                           |
| [Video]([https://drive.google.com/file/d/1Eeak_4Iwa99DF1KKz5dBUuEyPv3a1NGG/view?usp=drive_link]()) |

---

### Caso de Teste 05: Tentar finalizar compra com pagamento Parcial

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C03-CT05 | O sistema deve impedir finalizar compra quando o total dos pagamentos não bater com o total da nota. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Compra com itens correta e tela de pagamento aberta.          |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO**que o usuário adiciona um tipo de pagamento               |
| **E** informa um valor menor do que o total da nota               |
| **QUANDO** tentar clicar em “Salvar” na tela da compra            |
| **ENTÃO** o sistema deve alertar que o tipo de pagamento difere do total do pedido.|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve bloquear o salvamento.                           |
| [Video]([https://drive.google.com/file/d/1C6mQ7IW3xRCwyX7s41GPXiiOIBcspyw3/view?usp=sharing]()) |

---

### Caso de Teste 06: Relatório de produtos

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C03-CT06 | O sistema deve impedir finalizar compra quando o total dos pagamentos não bater com o total da nota. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Compra com itens correta e tela de pagamento aberta.          |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** O operador clica está no menu principal.                 |
| **E** no clica no menu “Consultas”                                |
| **E** depois clica em "Produtos"                                  |
| **E** depois clica em "Estoque"                                   |
| **QUANDO** na tela de consultar estoque, consultar todos clicar em "execultar"  |
| **ENTÃO** o sistema deve listar todos os produtos em estoque      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema exibe a lista de produtos                             |
| [Video]([https://drive.google.com/file/d/1ybIiPPOTaBssnooTbyVIKxx2sdaWCbuI/view?usp=drive_link]()) |
