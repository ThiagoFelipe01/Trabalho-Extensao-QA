## Cenário 02: Acesso e visualização da tela principal.

### Caso de Teste 01: Acesso a tela principal após login bem-sucedido.

| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
| C02-CT01 | Verificar a exibição correta da tela principal após login com sucesso. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com credenciais válidas.     |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessou o sistema com sucesso              |
| **QUANDO** for redirecionado automaticamente após o login         |
| **ENTÃO** a tela principal deve ser exibida com os atalhos e widgets principais |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir corretamente a interface da tela principal.     |
| [Video](https://drive.google.com/file/d/1cZZxr_bb_fxc77R8PowaIfbuVtePOjGM/view?usp=drive_link)  |

---

### Caso de Teste 02: Verificação da exibição dos widgets do Dashboard.

| ID       | Descrição                                                 |
| :------- | :-------------------------------------------------------- |
| C02-CT02 | Os widgets padrão devem ser exibidos corretamente na tela principal. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar na tela principal após login.         |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está autenticado                          |
| **E** está visualizando a tela principal                         |
| **QUANDO** a página for carregada                                |
| **ENTÃO** widgets como \"venda\" e \"Compra\" devem ser exibidos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Todos os widgets principais devem ser visíveis e funcionais.     |
| [Video](https://drive.google.com/file/d/1EpROo6M3BH7gXETEwYepy3_lPF3ufoGk/view?usp=drive_link)  |


---

