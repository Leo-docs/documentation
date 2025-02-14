---
sidebar_position: 2
---

# Como Instalar a Biblioteca

## Instalar via Biblioteca

Para utilizar a biblioteca **LeoDocs** no seu projeto do Google Apps Script, siga os passos abaixo:

### 1 - Adicionando a Biblioteca

1. Acesse o **Editor de Scripts** no Google Sheets (`Extensões` > `Apps Script`).
2. No menu lateral esquerdo, selecione **Editor (`<>`)**
3. Clique no **mais (`+`),** em frente à **Bibliotecas**.
4. No campo `Código do script *`, insira o seguinte código:

   ```
   1t1YE6J3bX5c3lWpFHCQoG4YESw-roKItWQy2UrXDlMQ8v4NW3aD_2Fjc
   ```

5. Clique em **Pesquisar**.
6. Na versão, selecione a versão mais recente disponível para garantir o funcionamento correto da ferramenta.
7. No Identificador adicione o seguinte nome

   ```
   LeoDocs
   ```

8. Clique em **Adicionar.**

### 2 - Adicionando as Funções no Script

Após adicionar a biblioteca, copie e cole o código abaixo no editor de scripts para registrar as funções principais do **LeoDocs**:

```jsx
function onOpen(...args){ LeoDocs.onOpen(...args);}
function onChange(...args) { LeoDocs.onChange(...args); }
function criarDocumentos(...args){ LeoDocs.criarDocumentos(...args);}
function abrirModalMensagemEmail(...args){ LeoDocs.abrirModalMensagemEmail(...args);}
function abrirConfiguracoesGerais(...args) { LeoDocs.abrirConfiguracoesGerais(...args);}
function abrirMapeamento(...args){ LeoDocs.abrirMapeamento(...args);}
function abrirDocumentacao(...args){ LeoDocs.abrirDocumentacao(...args);}
function hoje(...args) { return LeoDocs.hoje(...args);}
function obterCabecalhos(...args) { return LeoDocs.obterCabecalhos(...args);}
function salvarConfiguracoes(...args){ LeoDocs.salvarConfiguracoes(...args);}
function salvarMensagemEmail(mensagem){ return LeoDocs.salvarMensagemEmail(mensagem);}
function resetarConfiguracoes(...args) { LeoDocs.resetarConfiguracoes(...args);}
function salvarMapeamento(mapeamento) { LeoDocs.salvarMapeamento(mapeamento);}
function removeVariabelMap(...args){ LeoDocs.removeVariabelMap(...args);}
function teste(...args){ LeoDocs.teste(...args);}
```

1. Clique em **Salvar (CTRL + S)** e feche o editor.
2. Agora a biblioteca está pronta para ser utilizada no Google Sheets!

---

## Instalar via Add-on

Atualmente, a ferramenta ainda não está disponível como um Add-on

---
