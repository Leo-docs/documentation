---
sidebar_position: 1
---

# Guia de Uso da Ferramenta de Automação de Documentos e E-mails

## Visão Geral

Bem-vindo à documentação da ferramenta de Automação de Documentos e E-mails! Esta ferramenta automatiza a geração de documentos personalizados e o envio de e-mails usando dados do Google Sheets. É ideal para equipes que precisam criar documentos e enviar e-mails personalizados de forma eficiente.

---

## 💬 Envie seu Feedback!

Sua opinião é muito importante para melhorarmos o **LeoDocs**!

- **Encontrou um problema?** Relate um bug.
- **Tem sugestões?** Queremos ouvir suas ideias!
- **Gostou da ferramenta?** Deixe um comentário.
- **Envie seu feedback aqui:** [[**CLIQUE AQUI**]](https://forms.gle/H2D7BnJ7biR7GYkW9)

## Funcionalidades Principais

### 1. Mapeamento de Variáveis

Associe variáveis do documento às colunas da sua planilha. As informações são inseridas automaticamente no documento, economizando tempo e trabalho manual.

### 2. Edição de Mensagens de E-mail

Personalize mensagens para acompanhar os documentos gerados. Insira variáveis que serão preenchidas com dados da planilha no envio.

### 3. Registro e Monitoramento de Erros

A ferramenta registra erros durante a execução e gera “logs” automáticos para facilitar a depuração e análise.

### 4. Estilização de Texto

As variáveis inseridas no texto podem conter formatações especificas para cada ocasião.

### 5. Automação Completa

Todo o processo ocorre dentro do Google Sheets. Não é necessário interagir com código, tornando a ferramenta simples e acessível.

---

## Como Usar a Ferramenta

### 1. Configuração Inicial

Antes de começar, o administrador ou usuário responsável deve garantir que:

- O Google Sheets esteja preparado com as colunas necessárias.
- O documento modelo do Google Docs tenha as variáveis configuradas no formato `{{variavel}}`.
- O add-on ou biblioteca esteja instalado com as permissões necessárias.

### 2. Mapeamento de Variáveis

Para mapear variáveis, siga estes passos:

1. No Google Sheets, acesse o menu da ferramenta e selecione **"Mapeamento de Variáveis"**.
2. A ferramenta identificará as variáveis do documento modelo e as colunas da planilha.
3. Selecione a coluna correspondente para cada variável. Defina também um estilo, como **"Título"**, **"Comentário"** ou **"Parágrafo"**.
4. Clique em **Salvar** para armazenar o mapeamento.

### Exemplo de Mapeamento de Variáveis

Se seu documento modelo contém a variável `{{nome}}`, você pode mapeá-la para a coluna **"Nome Completo"** da planilha. O estilo pode ser configurado como **"Parágrafo"**.

### 3. Personalização da Mensagem de E-mail

1. Acesse **"Personalizar Mensagem de E-mail"** no menu.
2. No editor, insira as variáveis desejadas da lista disponível.
3. Inclua `{{link do documento}}`, que será substituído pelo link do documento gerado.
4. Clique em **Salvar** ao terminar.

### Exemplo de Mensagem de E-mail

```
Olá {{nome do usuario}},

Seu documento foi gerado com sucesso! Para acessá-lo, clique no link abaixo:

{{link do documento}}

Atenciosamente,
Equipe
```

### 4. Geração de Documentos e Envio de E-mails

Com as configurações prontas, a ferramenta gera automaticamente os documentos e envia e-mails personalizados para cada destinatário.

1. **Geração de Documento**: Para cada linha da planilha, a ferramenta cria um documento personalizado com as variáveis substituídas.
2. **Envio de E-mail**: Em seguida, envia um e-mail ao destinatário com o link do documento gerado.

---

## Exemplos de Uso

### 1. Gerar Documentos Contratuais Personalizados

Para uma planilha com dados de clientes que precisam de contratos personalizados:

1. Insira variáveis como `{{nome_cliente}}`, `{{data_assinatura}}`, `{{valor_contrato}}` no modelo.
2. Crie as colunas correspondentes no Google Sheets.
3. Configure o mapeamento e a mensagem de e-mail para gerar e enviar contratos automaticamente.

### 2. Enviar Relatórios de Vendas Personalizados

Para enviar relatórios personalizados de vendas à equipe:

1. Use variáveis como `{{nome_vendedor}}`, `{{total_vendas}}`, `{{data_periodo}}` no modelo.
2. Mapeie as colunas e personalize o e-mail incluindo `{{total_vendas}}`.
3. A ferramenta gerará e enviará os relatórios automaticamente.

---

## Instalar via Biblioteca

Para utilizar a biblioteca **LeoDocs** no seu projeto do Google Apps Script, siga os passos abaixo:

### 1 - Adicionando a Biblioteca

1. Acesse o **Editor de Scripts** no Google Sheets (`Extensões` > `Apps Script`).
2. No menu lateral esquerdo, selecione **Editor (`<>`)**
3. Clique no **mais (`+`),** em frente à **Bibliotecas**.
4. No campo `Código do script *`, insira o seguinte código:

   ```
   1qN6aIa-2Q8eXPL0c3GmLXk7kpovULf5tN8dWPO2F_YVbq_jk-84gUs1M
   ```

5. Clique em **Pesquisar**.
6. Na versão, selecione a versão mais recente disponível para garantir o funcionamento correto da ferramenta.
7. No Identificador adicione o seguinte nome

   ```
   LeoDocsFree
   ```

8. Clique em **Adicionar.**

### 2 - Adicionando as Funções no Script

Após adicionar a biblioteca, copie e cole o código abaixo no editor de scripts para registrar as funções principais do **LeoDocs**:

```jsx
function onOpen() {
  LeoDocsFree.onOpen();
}
function onChange(e) {
  LeoDocsFree.onChange(e);
}
function criarDocumentos() {
  LeoDocsFree.criarDocumentos();
}
function abrirModalMensagemEmail() {
  LeoDocsFree.abrirModalMensagemEmail();
}
function abrirConfiguracoesGerais() {
  LeoDocsFree.abrirConfiguracoesGerais();
}
function abrirMapeamento() {
  LeoDocsFree.abrirMapeamento();
}
function abrirDocumentacao() {
  LeoDocsFree.abrirDocumentacao();
}
function hoje() {
  return LeoDocsFree.hoje();
}
function obterCabecalhos(a) {
  return LeoDocsFree.obterCabecalhos(a);
}
function salvarConfiguracoes(config) {
  LeoDocsFree.salvarConfiguracoes(config);
}
function salvarMensagemEmail(mensagem) {
  return LeoDocsFree.salvarMensagemEmail(mensagem);
}
function resetarConfiguracoes() {
  LeoDocsFree.resetarConfiguracoes();
}
function salvarMapeamento(mapeamento) {
  LeoDocsFree.salvarMapeamento(mapeamento);
}
```

1. Clique em **Salvar (CTRL + S)** e feche o editor.
2. Agora a biblioteca está pronta para ser utilizada no Google Sheets!

---

## Instalar via Add-on

Atualmente, a ferramenta ainda não está disponível como um Add-on

---

## Roadmap

[Funcionalidades](https://www.notion.so/191a5b06d13580968ea8e18296e50c2d?pvs=21)

---

## Como Rodar o Programa Automaticamente

Para que o processo seja automatico, é necessário adicionar um acionador `onChange`, que executa automaticamente uma função quando ocorre uma mudança na planilha. Isso permite que a ferramenta LeoDocs atualize seu comportamento e execute ações específicas sempre que um valor for alterado.

### Passo a Passo para Adicionar o Acionador `onChange`

1. Acesse o Editor de Scripts
   - No Google Planilhas, clique em **Extensões** > **Apps Script** para abrir o editor de scripts.
2. Crie a Função `onChange`

   - No editor de scripts, crie ou edite a função `onChange` para realizar a ação desejada. O Google Apps Script chama automaticamente esta função sempre que houver uma alteração na planilha.

   Exemplo de função `onChange`:

   ```jsx
   function onChange(e) {
     LeoDocsFree.onChange(e);
   }
   ```

3. Adicionar um Acionador para `onChange`
   - Para configurar o acionador, no editor de scripts, clique em **Acionadores** no menu lateral (ícone de relógio).
   - Clique em **Adicionar acionador** no canto inferior direito da página.
   - Selecione a função `onChange` no menu suspenso.
   - Escolha o tipo de evento. Para o **Ao editar** ou **Ao alterar**.
   - Clique em **Salvar**.
4. Testar o Acionador
   - Após salvar o acionador, qualquer alteração feita na planilha automaticamente acionará a função `onChange`, onde criará os arquivos e enviará o e-mail sempre que houver alguma edição/alteração na planilha. Você pode visualizar logs e verificar o comportamento no Editor de Scripts.

---

## Perguntas Frequentes (FAQ)

### 1. Como a ferramenta encontra as variáveis no documento?

As variáveis devem estar no formato `{{nome_da_variavel}}` no documento modelo. A ferramenta as identifica automaticamente.

### 2. Onde são armazenadas as configurações da ferramenta?

As configurações ficam no serviço de propriedades do Google Apps Script, garantindo acesso seguro aos dados.

### 3. O que fazer se uma variável não for substituída corretamente?

Verifique se o nome da variável no modelo corresponde ao mapeamento e se a coluna da planilha contém dados válidos. Não inclua caracteres especiais nas variáveis, como ponto de interrogação, exclamação, etc.

### 4. Como posso verificar se um documento foi gerado com sucesso?

Consulte as colunas de status na planilha, que mostram quais documentos foram gerados e e-mails enviados.

### 5. E se ocorrer um erro durante o processo?

A ferramenta registra erros em um arquivo de log. Consulte-o para detalhes do erro. A função `registrarErro` captura as informações para depuração.

---

## Solução de Problemas

### Verificação de Logs e Depuração

Se ocorrer um erro inesperado, a ferramenta gera automaticamente um log no Google Apps Script. Para acessá-lo:

1. Abra o **Editor de Scripts** no Google Sheets (`Extensões` > `Apps Script`).
2. No menu lateral esquerdo, clique em **Registros da Execução**.
3. Analise as mensagens de erro para identificar o problema e sua solução.

Exemplo de erro nos registros:

```
"Erro: Variável {{nome}} não encontrada no modelo de documento"
```

### 1. Erro ao gerar o documento

- **Possível Causa**: Mapeamento incorreto de variáveis no modelo.
- **Solução**: Verifique se todas as variáveis estão corretamente mapeadas às colunas da planilha e verifique se não possui caracteres especiais na variável.

### 2. O e-mail não está sendo enviado

- **Possível Causa**: Endereço de e-mail inválido na planilha.
- **Solução**: Confirme se a coluna de e-mail contém endereços válidos.
