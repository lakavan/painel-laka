# Guia de publicação — Painel LAKA

## ⚠️ Antes de tudo: revogue o token antigo

O `.zip` que você me enviou tinha uma pasta `.git` com um **token de acesso do GitHub
já embutido** na URL do remote (`ghp_...`). Isso significa que esse token ficou
exposto neste chat. Recomendo fortemente:

1. Ir em GitHub → **Settings > Developer settings > Personal access tokens**
2. Revogar esse token específico
3. Gerar um novo, se precisar, e não deixar ele salvo dentro da pasta do projeto

Isso não afeta a publicação abaixo — só recomendo trocar o token por segurança.

## O que mudou nesta versão

- Mineração: layout voltou ao estilo de card (nome + nicho + anúncios ativos em
  destaque), com botão "✎ editar" pra abrir os campos e continuar editando tudo
  (agora incluindo **ticket do produto** e **checkout usado**), e histórico de
  anúncios continua igual.
- Financeiro: custos fixos agora ficam do lado da tabela (como na sua planilha),
  coluna de **ROAS** adicionada, e o detalhamento de gasto por conta de anúncio
  ficou mais simples (só "conta de anúncio" + valor, sem o campo de fonte que
  tava duplicando informação).
- Início: novo cabeçalho "Hoje" (gasto, faturamento, lucro, ROI do dia) e um
  resumo clicável de urgências / ofertas validando / escalando / infraestrutura
  no topo, antes do resto do painel.

## Atualização — repaginação visual + melhorias de operação

- **Nova identidade visual**: fim do roxo/lima, entrou preto/azul/verde, com
  cards, sombras, tipografia e navegação em abas redesenhados (visual "SaaS"
  mais tecnológico). Nenhuma funcionalidade ou dado foi removido — só a casca.
- **Mineração**: botão "✓ Concluir edição" ficou verde, grande, com ícone e
  pulso — impossível não ver. Adicionado **drag-and-drop** pra reordenar os
  cards manualmente (ordem fica salva).
- **Recuperação de vendas / Entrega do entregável**: cards de mensagem bem
  maiores (mais altura, menos aperto).
- **Financeiro**: clicar no faturamento do mês agora abre um **modal** de
  gateway (Hotmart, Kiwify, PerfectPay, Monetizze, Braip, + outros já
  cadastrados), com opção de cadastrar novos gateways.
- **Custos fixos**: agora aceita valor **fixo (R$)** ou **percentual (%)** —
  o percentual calcula automaticamente em cima do faturamento do mês. Total
  do mês ficou bem mais destacado visualmente.
- **Diário da operação**: registros antigos agora podem ser **editados**
  (texto e correções), mantendo a data original e marcando "editado".
- **Nova aba Ferramentas**: biblioteca pessoal (nome, categoria, descrição,
  pra que serve, observações).
- Responsividade revisada (mobile, tablet, desktop) — sem scroll horizontal,
  sem cards quebrando.

## Como publicar (atualizar o repositório já existente)

Você já tem o repositório `painel-laka` no GitHub. Pra atualizar:

1. Baixe os arquivos desse pacote (index.html, manifest.json, pasta icons/,
   README.md, .nojekyll).
2. Substitua os arquivos antigos na sua pasta local do projeto pelos novos
   (mantendo seu `.git` como está — só sobrescreva os arquivos de conteúdo).
3. Abra o PowerShell na pasta do projeto e rode:

```powershell
git add .
git commit -m "home redesenhada, mineracao com layout antigo + ticket/checkout, financeiro com custos ao lado e ROAS"
git push
```

4. Espera 1-2 minutos e o GitHub Pages atualiza sozinho no mesmo link de sempre.

## Se for subir do zero (novo repositório)

1. Cria um repositório novo no GitHub.
2. Sobe todos os arquivos desse pacote pra raiz do repositório.
3. Settings > Pages > Source > branch **main**, pasta **/ (root)**.
4. Link fica: `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`
