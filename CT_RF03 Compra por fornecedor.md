-------------------------------------------
## CENÁRIO 03 – COMPRA POR FORNECEDOR
-------------------------------------------
### Caso de Teste 01: Compra concluída com sucesso
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C03-CT01	 | Compra lançada, estoque atualizado e caixa alimentado.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Fornecedor cadastrado.|
|Produto cadastrado.|

| **Passos**                                                        |
| :------------------------------------------------------------ |
DADO que o usuário cria nova compra
E adiciona produtos
QUANDO finalizar compra
ENTÃO estoque deve ser alimentado.

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Compra CONFIRMADA.|
| Teste evidenciado e aprovado|
|https://drive.google.com/file/d/12goFMYpFykL3UcFnHZIe8VMvuHLCSEye/view?usp=drive_link

### Caso de Teste 02: Fornecedor não infomado.
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C03-CT02	 | Deve impedir compra sem fornecedor.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Nenhuma.|

| **Passos**                                                        |
| :------------------------------------------------------------ |
DADO que usuário tenta criar compra sem fornecedor
QUANDO clicar em “Salvar”
ENTÃO sistema deve bloquear.

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Mensagem “Fornecedor obrigatório”.|
| Teste evidenciado e aprovado|
|https://drive.google.com/file/d/1H1LUw8G80Md4wN2MRO9aAmugPRmuGJgW/view?usp=drive_link

### Caso de Teste 03: Tipo de documento inválido para compra a prazo
| ID       | Descrição                                                        |
| :------- | :---------------------------------------------------------------- |
|C03-CT03	 | Sistema deve recusar documento que alimenta caixa.|

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
|Compra marcada como “A Prazo”.|

| **Passos**                                             |
| :------------------------------------------------------------ |
DADO que o usuário tenta inserir tipo de documento que alimenta caixa
QUANDO selecionar a opção proibida
ENTÃO deve exibir alerta.

| **Critérios de Aceitação**                                             |
| :------------------------------------------------------------ |
|Documento não deve ser aceito.|
| Teste realizado e evidenciado|
|https://drive.google.com/file/d/1L4Vy350RqYCL1-slHm4zNs35B1TieEVp/view?usp=drive_link
