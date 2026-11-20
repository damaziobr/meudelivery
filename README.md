# MeuDelivery

Sistema para restaurantes de delivery venderem pelo **próprio canal, sem comissão por pedido**: cardápio digital, atendente virtual no WhatsApp, gestor de pedidos, entregadores, cupons, cashback e relatórios.

> **Nome provisório.** Por enquanto existe só o **protótipo visual**: não há servidor, banco de dados nem pagamento de verdade. Todos os dados são fictícios e voltam ao início quando a página é recarregada.

---

## Como abrir o protótipo (passo a passo)

### Opção 1 — Baixar o ZIP (mais fácil, sem instalar nada)

1. Nesta página do GitHub, clique no botão verde **`<> Code`**.
2. Clique em **Download ZIP**.
3. Abra a pasta **Downloads** e extraia o arquivo `meudelivery-main.zip`. No Windows: botão direito → **Extrair tudo…** → **Extrair**.
4. Entre na pasta extraída e depois na pasta **`prototipo`**.
5. Dê **dois cliques** em **`index.html`**. Ele abre no navegador (Chrome, Edge ou Firefox).

Pronto, o protótipo funciona sem internet. Só a fonte das letras é baixada da internet; sem conexão, o navegador usa uma fonte parecida.

### Opção 2 — Usando o Git (para quem já usa)

```bash
git clone https://github.com/damaziobr/meudelivery.git
cd meudelivery/prototipo
```

Depois abra o arquivo `index.html` no navegador.

### Opção 3 — No celular

O jeito mais simples é abrir no computador e diminuir a janela: o layout se ajusta ao tamanho de celular.

Para abrir direto no celular, o protótipo precisa estar publicado como site, por exemplo pelo **GitHub Pages**: em **Settings → Pages**, escolha a branch `main` e a pasta `/ (root)`. O endereço fica assim:
`https://damaziobr.github.io/meudelivery/prototipo/`

---

## Roteiro para testar (1 minuto)

1. No menu da esquerda, abra **Cardápio digital**. Escolha um lanche, coloque na sacola, use o cupom `VOLTA10` e pague com **Pix** (clique em *Simular pagamento aprovado*).
2. Vá em **Pedidos**. O pedido chega com aviso sonoro. Clique em **Aceitar** → **Pronto** → **Despachar** e escolha um motoboy.
3. Volte ao **Cardápio digital** ou ao **WhatsApp do cliente**: o acompanhamento e as mensagens se atualizam a cada etapa.
4. Abra o **App do motoboy** e confirme a entrega.
5. No **WhatsApp do cliente**, clique em **Ver conversa de exemplo** para ver a atendente virtual anotar um pedido sozinha.
6. Em **Pedidos**, clique em **Simular pedidos chegando** para ver a loja em movimento.

Cupons que funcionam no teste: `VOLTA10` (10% de desconto), `FRETE0` (frete grátis acima de R$ 40) e `BEMVINDO` (R$ 10 de desconto acima de R$ 40).

---

## Telas do protótipo

| Lado | Tela | O que mostra |
|---|---|---|
| Apresentação | Início | Proposta do produto, roteiro de teste e planos (valores de exemplo) |
| Cliente | Cardápio digital | Produtos, adicionais, sacola, cupom, entrega ou retirada, Pix simulado e acompanhamento do pedido |
| Cliente | WhatsApp do cliente | Atendente virtual que anota o pedido conversando, avisa itens em falta, pede o comprovante e informa cada etapa |
| Restaurante | Pedidos | Quadro em tempo real, aceitar ou recusar, comanda da cozinha, despacho, pausar a loja e alta demanda |
| Restaurante | Atendimento | Todas as conversas do WhatsApp; a equipe assume a conversa da atendente virtual quando quiser |
| Restaurante | Editar cardápio | Preço, item em falta, item oculto, destaque, produto novo e banners |
| Restaurante | Entregas | Mapa simulado, motoboys e acerto do dia |
| Restaurante | Marketing | Cupons, cashback, clientes mais fiéis e campanhas no WhatsApp |
| Restaurante | Relatórios | Faturamento, origem dos pedidos, funil do cardápio, avaliações e margem por produto |
| Entregador | App do motoboy | Corridas, rota, valor a cobrar na entrega e confirmação |

---

## Estrutura

```
meudelivery/
├── README.md            ← este arquivo
└── prototipo/
    └── index.html       ← protótipo completo (HTML, CSS e JavaScript num arquivo só)
```

---

## Próximas fases (sistema de verdade)

1. **MVP:** cadastro da loja, editor de cardápio, cardápio público, pedidos em tempo real, Pix com divisão do pagamento (split) e impressão da comanda.
2. **Fidelização:** motoboys e app do entregador, cupons, cashback, cadastro de clientes e relatórios.
3. **WhatsApp oficial:** avisos de pedido e campanhas pela API oficial do WhatsApp.
4. **Atendente virtual:** pedidos pelo WhatsApp e recuperação de clientes que sumiram.
5. **Escala:** integrações com iFood e sistemas de caixa, nota fiscal (NFC-e), cobrança da mensalidade e painel administrativo.
