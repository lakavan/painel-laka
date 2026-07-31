# Painel de Operação — Tráfego Direto / Infoproduto

App pessoal de controle da operação: tarefas, infraestrutura (BMs, contas de
anúncio), ofertas em teste, custos fixos, financeiro mês a mês (gasto,
faturamento, lucro, por gateway de pagamento), caixa da empresa e diário de
operação.

Os dados são salvos no Supabase (banco de dados próprio, fora do Claude) —
funcionam tanto no celular quanto no computador, sincronizados.

## Estrutura de arquivos

```
index.html        -> o app inteiro (interface + lógica)
manifest.json      -> configuração de "app" (ícone, tela cheia) pra celular
icons/              -> ícones do app (192px, 512px, apple-touch-icon)
.nojekyll           -> evita que o GitHub processe os arquivos como Jekyll
```

## Como publicar no GitHub Pages

1. Cria um repositório novo no GitHub.
2. Sobe TODOS os arquivos dessa pasta (index.html, manifest.json, a pasta
   icons/ inteira, e o .nojekyll) pra raiz do repositório.
3. Vai em **Settings > Pages > Source** e escolhe a branch **main**, pasta
   **/ (root)**.
4. Espera 1-2 minutos. O link fica:
   `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`
5. Abre esse link no celular e usa "Adicionar à Tela de Início" pra ele
   funcionar como um app instalado.

## Importante

Os dados ficam guardados no Supabase, vinculados a uma chave própria já
embutida no código. Não compartilhe o link desse app publicamente.


