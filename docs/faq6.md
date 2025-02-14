---
sidebar_position: 6
---

# Perguntas Frequentes (FAQ) e Soluções de problemas

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
