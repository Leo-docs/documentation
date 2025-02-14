---
sidebar_position: 3
---

# Como Rodar o Programa Automaticamente

## Configurando `onChange`

Para que o processo seja automatico, é necessário adicionar um acionador `onChange`, que executa automaticamente uma função quando ocorre uma mudança na planilha. Isso permite que a ferramenta LeoDocs atualize seu comportamento e execute ações específicas sempre que um valor for alterado.

### Passo a Passo para Adicionar o Acionador `onChange`

1. Acesse o Editor de Scripts
   - No Google Planilhas, clique em **Extensões** > **Apps Script** para abrir o editor de scripts.
2. Crie a Função `onChange`

   - No editor de scripts, crie ou edite a função `onChange` para realizar a ação desejada. O Google Apps Script chama automaticamente esta função sempre que houver uma alteração na planilha.

   Exemplo de função `onChange`:

   ```jsx
   function onChange(e) {
     LeoDocs.onChange(e);
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
