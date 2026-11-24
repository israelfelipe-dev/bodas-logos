# Site da 7ª Viagem das Bodas (Logos Tour)

Site estático de uma página, sem build. HTML, CSS e JS ficam no `index.html`.

- `img/` fotos em .webp (800 e 1600 px; recortes em 700 px e no tamanho original)
- `media/` vídeo da hero (webm e mp4, sem áudio)
- `vendor/` GSAP 3.12.5 + ScrollTrigger e Lenis 1.1.20, servidos pelo próprio site
- `og-image.jpg` preview do link no WhatsApp (1200x630)

## Rodar localmente

```
npx serve .
```
ou
```
python -m http.server 8000
```
e abra http://localhost:8000

## Publicar

1. GitHub: `repositório: github.com/israelfelipe-dev/bodas-logos`
2. Vercel: Add New > Project > importar o repositório. Framework Preset: Other, Build Command vazio, Output Directory `./`.
3. Cada push em `main` publica sozinho. Ao ter a URL final, troque `https://bodas-logos.vercel.app/` no `index.html` (canonical, og:url, og:image, twitter:image e o JSON-LD).

## Onde mudar

- Data da contagem regressiva: `TARGET` no script (`2027-07-30T02:00:00-03:00`).
- WhatsApp e mensagem pronta: `WA` e `BASE` no script.
- Horários do all inclusive (relógio): array `SVC` no script.
