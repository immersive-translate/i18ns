# Como implementar a tradução do Gemini no Immersive Translate

## Ativação do Gemini

1. **Configurações do Desenvolvedor:**
   - Acesse as [Configurações do Desenvolvedor](https://dash.immersivetranslate.com/#developer) no Immersive Translate.
   - Expanda a seção "Edit Full User Config", e procure ou adicione a seguinte linha:

     ```json
     "gemini": {
      "provider": "pro",
      "visible": false
     ```

   - Mude o valor de `"visible"` para `true` para exibir o serviço Gemini.

## Obtenção da Chave de API

1. **Makersuite:**

   - Acesse o site [Google AI Studio](https://aistudio.google.com/).
   - Faça login com sua conta Google.
   - Clique em `Get API key` (Obter chave de API) > `Criar chave de API`.
   - Aceite os termos e politicas de uso.
   - E selecione o botão `Criar uma chave de API em um novo projeto`.
   - Após a chave ser gerada, copie e salve-a em um local seguro.

2. **Configuração no Immersive Translate:**
   - Insira a chave de API na seção de configuração do Gemini no plugin.

## Precauções

- **Restrição de IP:** O serviço Gemini atualmente não suporta IPs de Hong Kong. Verifique as [Regiões suportadas](https://ai.google.dev/available_regions).

- **Risco de Bloqueio:** O uso do Gemini com IPs compartilhados ou com alto uso de banda pode ser considerado abuso pelo Google Cloud, resultando na desativação da chave de API ou da conta Google Cloud. Utilize com cautela e considere usar uma conta secundária para evitar problemas.
