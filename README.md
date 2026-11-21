<h1 align="center">Azevedo Filho</h1>

<p align="center">
  Desenvolvedor back-end no TCE · ferramentas para sim racing nas horas vagas
</p>

<p align="center">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black">
  <img alt="PHP" src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white">
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
  <img alt="Cloudflare Workers" src="https://img.shields.io/badge/Cloudflare_Workers-F38020?style=flat-square&logo=cloudflare&logoColor=white">
  <img alt="Windows" src="https://img.shields.io/badge/Windows_API-0078D4?style=flat-square&logo=windows&logoColor=white">
  <img alt="Git" src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
</p>

---

Trabalho com back-end no **TCE** e gosto de resolver problema com código simples, que dura. Fora do expediente, levo isso para o automobilismo virtual: construo ferramentas para o **iRacing** usadas por pilotos e por ligas, do overlay que roda junto com o jogo até a transmissão ao vivo.

## Projetos em destaque

### eSimControl
**Overlay do piloto e direção de prova para iRacing.** Produto comercial, para Windows, em português, espanhol e inglês.

- **Overlay do piloto:** 22 widgets (relative, standings, delta, combustível, radar, bandeiras e outros) desenhados de forma nativa, em processo próprio e sem navegador, para gastar o mínimo de CPU enquanto o jogo roda.
- **Delta com cronômetro próprio:** cada volta vira uma referência com o tempo a cada 0,1% da pista, conferida contra o tempo oficial do iRacing. Conferido em telemetria real: setores a menos de 1 ms do oficial.
- **Direção de prova:** torre ao vivo, detecção de incidentes, controle de replay e câmeras e relatório oficial em PDF para os comissários.
- **Licença e atualização:** chaves assinadas com Ed25519 e verificadas sem internet; atualização automática servida por Cloudflare Workers, com pacote assinado.

`Python` · `Win32 / GDI+` · `WebView2` · `Cloudflare Workers + KV` · `Ed25519` · `ReportLab`

<sub>Código privado.</sub>

### Central de transmissão iRacing
**Torre, câmeras e overlays para OBS,** usada nas transmissões ao vivo de uma liga brasileira de iRacing.

- Lê o estado da corrida direto do SDK do iRacing e publica por WebSocket para a mesa de direção e para os overlays do OBS.
- Gap entre carros recalculado a cada quadro, e não só na linha de chegada; setores de todos os carros calculados pela posição na pista.
- Temas, rodízio da torre, lower third com foto do piloto, tabela do campeonato e patrocinadores, tudo controlado ao vivo.

`Python` · `FastAPI` · `WebSocket` · `HTML/CSS` · `OBS`

<sub>Código privado.</sub>

---

<details>
<summary><b>English</b></summary>
<br>

Back-end developer at **TCE**. I like solving problems with simple code that lasts. In my spare time I build tools for **iRacing** sim racing, used by drivers and leagues:

- **eSimControl:** a commercial driver overlay and race control tool for Windows (Portuguese, Spanish and English). Native, low-CPU overlay widgets; a lap delta built on its own timing engine, verified against real telemetry to within 1 ms of official sector times; live race control with incident detection, replay control and official PDF reports; offline Ed25519 licensing and signed auto-updates served from Cloudflare Workers.
- **iRacing broadcast hub:** timing tower, camera control and OBS overlays used for a Brazilian iRacing league's live broadcasts, built with Python, FastAPI and WebSockets.

Both projects are closed source.

</details>
