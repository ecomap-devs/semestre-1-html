<p align="center">
  <img src="logo2.png" alt="EcoMapBrasil" width="96">
</p>

<h1 align="center">EcoMapBrasil · 1º semestre</h1>

<p align="center">
  <img alt="Semestre" src="https://img.shields.io/badge/semestre-1%C2%BA_%C2%B7_2025%2F1-5b6270">
  <img alt="HTML" src="https://img.shields.io/badge/HTML-puro-e34f26?logo=html5&logoColor=white">
  <img alt="Tailwind" src="https://img.shields.io/badge/Tailwind-CDN-38bdf8?logo=tailwindcss&logoColor=white">
  <img alt="Leaflet" src="https://img.shields.io/badge/mapa-Leaflet-199900?logo=leaflet&logoColor=white">
  <img alt="Arquivado" src="https://img.shields.io/badge/estado-entregue-199e70">
</p>

A primeira versão do **EcoMapBrasil**, entregue em junho de 2025 no Projeto Integrador do
1º semestre de Desenvolvimento de Software Multiplataforma da FATEC. Um site estático,
sem framework e sem backend: HTML, Tailwind por CDN e um mapa em Leaflet com os alertas
de desmatamento.

> [!NOTE]
> Esta é uma versão **congelada**, guardada como registro. O projeto continua nos
> semestres seguintes: veja a [página da organização](https://github.com/ecomap-devs).

## 🗺️ O que tem

| Página | O que mostra |
|---|---|
| `index.html` | A página inicial: mapa, espécies ameaçadas, dados, soluções e a equipe |
| `mapa.html` | Mapa com os biomas e a camada de áreas desmatadas (`meuarquivo4.json`) |
| `login.html` · `cadastro.html` | As telas de entrada, só a interface: os formulários não enviam para lugar nenhum, porque ainda não havia backend |
| `p.html` | Cópia idêntica da página inicial |

## 🚀 Como abrir

O mapa carrega o GeoJSON por `fetch`, e o navegador bloqueia isso em arquivo aberto
direto do disco. Sirva a pasta com qualquer servidor estático:

```bash
npx serve .
# ou
python -m http.server
```

<details>
<summary>O que não funciona mais, e por quê</summary>

- **Fotos da equipe:** vinham de links temporários do WhatsApp, que expiraram.
- **Camada de estados:** o `mapa.html` pede um `estados.json` que não estava entre os
  arquivos entregues.
- **`meuarquivo4.json`** (32 MB) foi adicionado a este repositório em 2026, a partir da
  cópia local do projeto, porque o mapa não abria sem ele.

</details>

## 📜 Histórico

Os commits vêm do repositório original da equipe (`EcoMapBrasil/EcoMapBrasil`), de 05/06
a 22/06/2025, com os autores originais. Os commits seguintes, de 2026, só organizam o
repositório: este README e o arquivo de dados do mapa.

## 👥 Equipe do 1º semestre

**Vinicius** · **Cesar** · **Bruno** · **João Flávio** · **Victor** · **Ana Carolina**

## 📄 Licença

[MIT](LICENSE) para o código da equipe. Projeto acadêmico, sem fins lucrativos. A licença não
cobre os dados de `meuarquivo4.json`, que não são da equipe, nem as bibliotecas carregadas por
CDN, que têm as próprias licenças.
