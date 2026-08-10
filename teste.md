<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Linha do Tempo — História dos Sistemas Operacionais</title>
<style>
  * { box-sizing: border-box; }
  body {
    margin: 0;
    min-height: 100vh;
    font-family: Georgia, "Times New Roman", serif;
    background: #ead1d3;
    color: #222;
    overflow-x: hidden;
  }

  .page {
    max-width: 1200px;
    margin: auto;
    padding: 38px 28px 60px;
  }

  h1 {
    text-align: center;
    font-size: clamp(32px, 5vw, 58px);
    margin: 0 0 45px;
    font-weight: 800;
  }

  .timeline-wrap {
    position: relative;
    padding: 115px 30px 125px;
  }

  .line {
    position: absolute;
    left: 6%;
    right: 6%;
    top: 50%;
    height: 18px;
    transform: translateY(-50%);
    border-radius: 20px;
    background: linear-gradient(90deg,
      #35a86b 0%,
      #35a86b 25%,
      #5967b8 25%,
      #5967b8 50%,
      #f2b51d 50%,
      #f2b51d 75%,
      #c93c34 75%,
      #c93c34 100%);
    box-shadow: 0 3px 3px rgba(0,0,0,.08);
  }

  .events {
    position: relative;
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 10px;
  }

  .event {
    position: relative;
    min-height: 260px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .event:nth-child(odd) .label { top: 5px; }
  .event:nth-child(even) .label { bottom: 5px; }

  .label {
    position: absolute;
    width: 190px;
    text-align: center;
    font-size: 23px;
    line-height: 1.15;
    font-weight: 700;
  }

  .connector {
    position: absolute;
    width: 5px;
    height: 62px;
    left: 50%;
    transform: translateX(-50%);
    background: currentColor;
  }

  .event:nth-child(odd) .connector { top: 66px; }
  .event:nth-child(even) .connector { bottom: 66px; }

  .dot {
    position: relative;
    z-index: 5;
    width: 64px;
    height: 64px;
    border-radius: 50%;
    background: #f8f7ef;
    border: 6px solid currentColor;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: Arial, sans-serif;
    font-size: 26px;
    font-weight: 800;
    cursor: pointer;
    transition: transform .2s, box-shadow .2s;
  }

  .dot:hover, .dot:focus {
    transform: scale(1.12);
    box-shadow: 0 0 0 8px rgba(255,255,255,.35);
    outline: none;
  }

  .green { color: #35a86b; }
  .blue { color: #5967b8; }
  .yellow { color: #f2b51d; }
  .red { color: #c93c34; }

  .info {
    margin: 5px auto 0;
    max-width: 920px;
    background: rgba(255,255,255,.92);
    border-radius: 22px;
    padding: 26px 30px;
    box-shadow: 0 10px 35px rgba(0,0,0,.12);
    display: none;
    animation: show .25s ease;
  }

  .info.active { display: block; }

  .info h2 {
    margin: 0 0 8px;
    font-size: 30px;
  }

  .info .period {
    font-family: Arial, sans-serif;
    font-weight: 700;
    margin-bottom: 14px;
    opacity: .75;
  }

  .info ul {
    margin: 10px 0 0 20px;
    padding: 0;
    font-family: Arial, sans-serif;
    line-height: 1.6;
  }

  .hint {
    text-align: center;
    font-family: Arial, sans-serif;
    margin-top: 12px;
    opacity: .7;
  }

  @keyframes show {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 800px) {
    .timeline-wrap { padding: 20px 10px; }
    .line {
      left: 40px;
      top: 0;
      bottom: 0;
      width: 14px;
      height: auto;
      transform: none;
      background: linear-gradient(180deg,
        #35a86b 0%, #35a86b 25%,
        #5967b8 25%, #5967b8 50%,
        #f2b51d 50%, #f2b51d 75%,
        #c93c34 75%, #c93c34 100%);
    }
    .events {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }
    .event {
      min-height: 115px;
      justify-content: flex-start;
      padding-left: 10px;
    }
    .dot {
      margin-left: 0;
    }
    .label {
      position: static !important;
      width: auto;
      text-align: left;
      margin-left: 28px;
      font-size: 20px;
    }
    .connector { display: none; }
  }
</style>
</head>
<body>
<div class="page">
  <h1>Divisão da História</h1>

  <div class="timeline-wrap">
    <div class="line"></div>

    <div class="events">
      <div class="event green">
        <div class="label">Primeira<br>Geração</div>
        <div class="connector"></div>
        <button class="dot" onclick="showInfo(0)" aria-label="Primeira geração">1</button>
      </div>

      <div class="event blue">
        <div class="label">Segunda<br>Geração</div>
        <div class="connector"></div>
        <button class="dot" onclick="showInfo(1)" aria-label="Segunda geração">2</button>
      </div>

      <div class="event yellow">
        <div class="label">Terceira<br>Geração</div>
        <div class="connector"></div>
        <button class="dot" onclick="showInfo(2)" aria-label="Terceira geração">3</button>
      </div>

      <div class="event red">
        <div class="label">Quarta<br>Geração</div>
        <div class="connector"></div>
        <button class="dot" onclick="showInfo(3)" aria-label="Quarta geração">4</button>
      </div>

      <div class="event red">
        <div class="label">Quinta<br>Geração</div>
        <div class="connector"></div>
        <button class="dot" onclick="showInfo(4)" aria-label="Quinta geração">5</button>
      </div>
    </div>
  </div>

  <div id="info" class="info active"></div>
  <div class="hint">Clique nos números para explorar cada geração.</div>
</div>

<script>
const data = [
  {
    title: "1 — Primeira geração",
    period: "1945–1955",
    items: [
      "Uso de válvulas.",
      "Computadores grandes, caros e pouco confiáveis.",
      "Não existiam sistemas operacionais.",
      "Programação diretamente em código de máquina.",
      "Uso de cartões perfurados.",
      "Computadores voltados principalmente para cálculos científicos."
    ]
  },
  {
    title: "2 — Segunda geração",
    period: "1955–1965",
    items: [
      "Uso de transistores, aumentando a confiabilidade.",
      "Surgimento dos computadores comerciais de grande porte.",
      "Processamento em lote (batch).",
      "GM-NAA I/O e outros sistemas iniciais.",
      "Programas preparados em cartões e executados em sequência.",
      "FMS e IBSYS são exemplos de sistemas da época."
    ]
  },
  {
    title: "3 — Terceira geração",
    period: "1965–1980",
    items: [
      "Uso de circuitos integrados.",
      "System/360 e OS/360.",
      "Multiprogramação.",
      "Spooling.",
      "Timesharing e CTSS.",
      "MULTICS influenciou o desenvolvimento do UNIX.",
      "UNIX surgiu nos Bell Labs e tornou-se multiusuário, multitarefa e portátil."
    ]
  },
  {
    title: "4 — Quarta geração",
    period: "1980–presente",
    items: [
      "Circuitos integrados em larga escala e microprocessadores.",
      "Popularização dos computadores pessoais.",
      "CP/M em microcomputadores.",
      "MS-DOS associado ao IBM PC.",
      "Macintosh popularizou interfaces gráficas.",
      "Windows evoluiu de ambiente gráfico para sistema operacional completo.",
      "Linux surgiu em 1991, inspirado no MINIX e influenciado pelo UNIX."
    ]
  },
  {
    title: "5 — Quinta geração",
    period: "1990–presente",
    items: [
      "Expansão da computação móvel.",
      "Smartphones combinam telefonia e computação.",
      "iPhone OS/iOS foi apresentado com o primeiro iPhone.",
      "Android é baseado no kernel Linux.",
      "Dispositivos móveis passaram a executar aplicativos, navegar na web e realizar diversas funções.",
      "A competição entre sistemas móveis tornou-se intensa."
    ]
  }
];

function showInfo(index) {
  const item = data[index];
  const info = document.getElementById("info");
  info.innerHTML = `
    <h2>${item.title}</h2>
    <div class="period">${item.period}</div>
    <ul>${item.items.map(x => `<li>${x}</li>`).join("")}</ul>
  `;
  info.classList.remove("active");
  void info.offsetWidth;
  info.classList.add("active");
}
showInfo(0);
</script>
</body>
</html>
