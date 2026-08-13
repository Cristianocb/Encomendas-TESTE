# Reconhecimento de Encomendas (Teste IA)

Protótipo standalone para testar reconhecimento automático de etiquetas
de encomendas via IA (Gemini), separado do PortaLog.

## Como usar

1. Suba este `index.html` para um repositório novo no GitHub.
2. Conecte o repositório ao Vercel (mesmo processo do PortaLog).
3. Acesse o link gerado (`algumnome.vercel.app`) pelo **Chrome do celular**
   — não abra pelo link de preview do chat, pois a câmera não funciona
   direito dentro dele.
4. Gere uma API key gratuita em https://aistudio.google.com e cole na
   página (fica salva só no seu aparelho).
5. Toque em "Tirar foto da etiqueta" e teste com etiquetas reais.

## O que ele faz

- Comprime a foto antes de enviar (mais rápido, usa menos memória).
- Envia a imagem para a API do Gemini pedindo para extrair:
  - Nome do destinatário
  - Origem/transportadora (Mercado Livre, Shopee, Correios, Temu etc.)
  - Nível de confiança da leitura
- Se a página recarregar durante o uso da câmera, tenta retomar a
  análise sozinha (guarda a foto temporariamente no navegador).

## Próximos passos (se o teste for bem)

- Integrar esse reconhecimento como botão dentro do PortaLog.
- Mover a chamada à API para um backend (ex: função no Vercel) para
  não expor a API key no código do navegador.
