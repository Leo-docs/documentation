---
sidebar_position: 4
---

# Utilizando a Ferramenta

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
