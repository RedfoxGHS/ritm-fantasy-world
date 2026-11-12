# Before the Kingdom Fades — Prólogo (PWA)

Jogo de ritmo de piano em um único `index.html` (áudio e fases embutidos), instalável como app e
funcionando offline depois da primeira visita. Jogue com o celular **deitado**.

## Como jogar
- **Toque** quando a nota encostar na linha de luz.
- **Segure** até o rastro acabar.
- **Deslize** o dedo por cima das notas em losango, sem soltar.
- Botões **−/+ Sincronia** no menu ajustam o atraso do áudio (útil com fone Bluetooth).

## Publicar (GitHub Pages)
1. Faça merge deste branch no `main`.
2. Em **Settings → Pages → Source**, escolha **GitHub Actions** (só na primeira vez).
3. O workflow `.github/workflows/pages.yml` publica sozinho em
   `https://<usuario>.github.io/<repositorio>/`.

## Instalar no celular
- Android (Chrome): menu ⋮ → "Instalar app" / "Adicionar à tela inicial".
- iPhone (Safari): Compartilhar → "Adicionar à Tela de Início".

## Desempenho
- Cenário, castelo, névoa e notas são pré-renderizados uma única vez; o quadro só desenha imagens prontas.
- **Resolução adaptativa:** se o FPS ficar abaixo de ~46 durante a partida, o jogo reduz a resolução
  (100% → 75% → 55%) sozinho e lembra a escolha. O contador de FPS fica no canto superior direito
  (mostra `· 75%` quando a qualidade foi reduzida). Para voltar a 100%: limpe os dados do site.
- Telas limitadas a 30 Hz (modo economia de bateria) são detectadas e não causam redução de qualidade.

## Atualizar o jogo
Ao trocar o `index.html`, mude também `CACHE` em `sw.js` (ex.: `kingdom-fades-v3`).
