# Daniel Bueno Moreira — página de apresentação

Página pessoal de desenvolvedor: quem sou, o que já construí, tecnologias e contatos. Serve de cartão
de visitas para quem chega pelo WhatsApp, pelo LinkedIn ou pelo GitHub.

**No ar:** https://danielbuenomoreira.github.io/QuemSouEu/

![Prévia do card de compartilhamento](img/og-image.jpg)

## Como é feita

Um único `index.html` e um `css/style.css`. Sem framework de JavaScript, sem build, sem dependência
instalada — só Bootstrap 5.3.3 e a fonte Poppins, ambos por CDN. O deploy é o próprio branch `main`
servido pelo GitHub Pages.

O que está por baixo:

- **Semântica e acessibilidade** — `header`, `main`, `nav` com `aria-labelledby`, `footer`; ícones
  decorativos com `alt=""`; aviso "(abre em nova aba)" oculto para leitores de tela; foco de teclado
  visível (`:focus-visible`) separado do hover; `prefers-reduced-motion` respeitado; a tecnologia
  principal é diferenciada por forma (estrela e preenchimento), não só por cor.
- **Compartilhamento** — Open Graph e Twitter Card com imagem 1200×630, `og:image:width/height` e
  `og:image:alt`, para o link virar card no WhatsApp, LinkedIn, Facebook e Telegram.
- **SEO** — `title`, `meta description`, `canonical`, `theme-color` e JSON-LD `Person` com `sameAs`
  ligando os perfis.
- **CSS** — tokens em `:root` (cores, raios, transição), hover só em dispositivos com mouse
  (`@media (hover: hover)`), ajustes para telas de 360–400 px, favicon em SVG.

## Estrutura

```
index.html                      página inteira
css/style.css                   estilos próprios (sobre o Bootstrap)
cv/daniel-bueno-moreira-cv.pdf  currículo linkado no botão "Currículo em PDF"
img/foto-perfil-DMoreira.jpg    foto de perfil (320×320, exibida a 160 px)
img/og-image.jpg                card de compartilhamento (1200×630)
img/favicon.svg                 ícone da aba
img/icone-*.png, img/email.png  ícones dos botões (60×60)
```

## Como atualizar

| O quê | Onde |
| --- | --- |
| Texto, projetos, tecnologias | seções marcadas com `<!-- ===== ... ===== -->` em `index.html` |
| Currículo | substituir `cv/daniel-bueno-moreira-cv.pdf` mantendo o nome |
| Foto de perfil | substituir `img/foto-perfil-DMoreira.jpg` (quadrada, 320×320 ou maior) |
| Card de compartilhamento | substituir `img/og-image.jpg` (1200×630, JPEG, abaixo de 600 KB) |
| Cores | variáveis no topo de `css/style.css` |

Depois de publicar uma mudança no card ou nas metas, limpe o cache dos scrapers — senão eles servem o
card antigo por dias: [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) (vale
para o WhatsApp) e [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/).

Para testar localmente basta abrir o `index.html` no navegador.

## Sobre mim

Desenvolvedor full stack em Porto Alegre/RS, com foco em PHP/Laravel e PostgreSQL. Hoje na
MB Advocacia, onde construí a plataforma de gestão processual do escritório; antes, único desenvolvedor
do DECOR, na Secretaria de Logística e Transportes do RS. A história completa está na
[página](https://danielbuenomoreira.github.io/QuemSouEu/) e no
[LinkedIn](https://www.linkedin.com/in/danielbuenomoreira/).

Outro projeto público: [Bíblia Sagrada Online](https://github.com/danielbuenomoreira/BibliaSagrada) —
leitura da Bíblia completa, gratuita e sem anúncios.

## Licença

[MIT](LICENSE). Os textos, a foto e as imagens são pessoais — use o código, não a identidade.
