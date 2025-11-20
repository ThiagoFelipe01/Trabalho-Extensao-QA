Link pasta Roteiro 05: https://drive.google.com/drive/folders/18WiGBKG-oHI2wiuIbsFgcKXnC4srbc8Z?usp=drive_link

## Cenário 07: Fechamento de Caixa

### Caso de Teste 01: Gerar vendas filtrando por tipos de documentos

| ID       | Descrição                                                                  |
| :------- | :------------------------------------------------------------------------- |
| C07-CT01 | O sistema deve permitir consultar vendas por tipo de documento utilizando os filtros da tela de consultas.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve haver vendas confirmadas registradas no sistema.         |
| O caixa do dia deve ter sido aberto anteriormente.            |


| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Consultas” → “Pedidos” → “Vendas - Outras” → “Tipo de Documento” |
| **E** seleciona “Consulta por: Todas”                           |
| **E** seleciona “Status da Venda: Confirmada”                   |
| **E** seleciona “Tipo de Documento: Todos”                      |
| **E** marca “Filtrar por Data” informando a data de abertura do caixa |
| **E** seleciona “Condição de Venda: Todas”                      |
| **QUANDO** clicar em “Executar”                                 |
| **ENTÃO** o sistema deve listar todas as vendas confirmadas correspondentes ao filtro aplicado |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
|A lista deve conter todas as vendas do dia filtradas corretamente. |
|Os tipos de documentos devem ser exibidos corretamente na listagem.|
| [Video]([https://drive.google.com/file/d/1pIQSyWSkl-17Gpo6U0KU9DbjbywAxY4V/view?usp=drive_link]()) |

---

### Caso de Teste 02: Realizar retirada de valores.

| ID       | Descrição                                                                 |
| :------- | :------------------------------------------------------------------------ |
| C07-CT02 | O sistema deve permitir registrar uma retirada de valores no Livro Caixa. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Operador com permissão de movimentação financeira.            |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o ícone “Livro Caixa”              |
| **E** clica no botão “Retirar Valores”                            |
| **E** clica no botão “Novo”                                       |
| **E** informa o valor da retirada                                 |
| **E** preenche o campo “Histórico” com “Retirada de dinheiro”     |
| **QUANDO** clicar em “Salvar”                                     |
| **ENTÃO** A retirada deve aparecer imediatamente no movimento do caixa. |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A retirada deve aparecer imediatamente no movimento do caixa.   |
| [Video]([https://drive.google.com/file/d/1BxkSirMX49V42YqFQ9SqKN6k8bykhmt8/view?usp=drive_link]()) |

---

### Caso de Teste 03: Conciliar totais com relatórios de vendas.

| ID       | Descrição                                                              |
| :------- | :---------------------------------------------------------------------- |
| C07-CT03 | O sistema deve permitir conciliar os valores do fechamento do caixa com os relatórios de vendas do dia. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Relatórios devem possuir registros de vendas e retirada.      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o operador acessa o menu “Consultas” → “Pedidos” → “Vendas - Outras” → “Listar Totais”  |
| **E** em “Consulta por:” seleciona “Dia”                          |
| **E** ativa “Filtrar por Data” com a data de abertura do caixa    |
| **E** seleciona “Status da Venda: Confirmada”                     |
| **QUANDO** clicar em “Executar”                                   |
| **ENTÃO** o sistema deve exibir o total de vendas do dia          |
| **E** dado que o operador acessa novamente “Vendas - Outras” → “Tipo de Documento”  |
| **E** filtra por data, status Confirmada e tipo de documento Todos  |
| **QUANDO** clicar em “Executar”                                   |
| **ENTÃO** o relatório deve listar todas as vendas e exibir corretamente a retirada registrada no caixa  |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Relatório e fechamento do caixa devem apresentar totais, retirada e tipos de documentos de forma consistente. |
| [Video]([https://drive.google.com/file/d/1bGEIbUqr9anU5hObJZD0sXL4lwmZZoSx/view?usp=drive_link]()) |