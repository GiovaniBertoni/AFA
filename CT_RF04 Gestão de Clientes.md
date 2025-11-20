-------------------------------------------
## CENÁRIO 04 – GESTÃO DE CLIENTES
-------------------------------------------
### Caso de Teste 01: Cadastro de cliente PF com sucesso
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C04-CT01	 | Cadastro básico deve ser salvo corretamente.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Nenhuma.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que usuário clica em “Novo”
E preenche os campos obrigatórios
QUANDO clicar em Salvar
ENTÃO cliente deve aparecer na lista.

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Cadastro salvo.|
| Teste evidenciado e aprovado|
| https://drive.google.com/file/d/1dp-k4BgbfeZafhUxaMIbZ7OAvGauiYgo/view?usp=drive_link

### Caso de Teste 02: Tentativa de salvar cliente sem campos obrigatórios
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C04-CT02	 | Sistema deve impedir cadastro incompleto.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Nenhuma.|

| **Passos**                                                        |
| :------------------------------------------------------------ |
DADO que o usuário deixa Nome ou CEP vazio
QUANDO tentar salvar
ENTÃO deve exibir alerta.

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Cadastro bloqueado.|
|Teste evidenciado e aprovado|
|https://drive.google.com/file/d/1AZl_c-u1xAuntdTuoE-ymLpMVbYXHqFi/view?usp=drive_link

### Caso de Teste 03: Venda acima do limite de crédito
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C04-CT03	 | Sistema alerta e redireciona para Contas a Receber.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Cliente com limite de crédito.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o cliente tem limite de R$100
QUANDO a venda ultrapassar esse valor
ENTÃO sistema alerta e abre fluxo de contas a receber.

| **Critérios de Aceitação**                                             |
| :-------------
|----------------------------------------------- |
|Alerta exibido.|
|Venda permitida após confirmação.|
|Teste evidenciado e aprovado|
|https://drive.google.com/file/d/1t1yPC2fxsYl4PL8zYC7O3JXynN0ihQDQ/view?usp=drive_link

