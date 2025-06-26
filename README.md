# Bncc<!DOCTYPE html><html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GeoIdeias BNCC</title>
  <style>
    body { font-family: Arial, sans-serif; background-color: #f0f0f5; padding: 20px; }
    h1 { color: #4b0082; }
    .container { background: #fff; border-radius: 10px; padding: 20px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    label { display: block; margin-top: 15px; font-weight: bold; }
    select, input[type=text] { width: 100%; padding: 10px; margin-top: 5px; border: 1px solid #ccc; border-radius: 5px; }
    button { margin-top: 20px; padding: 10px 20px; background-color: #6a0dad; color: white; border: none; border-radius: 5px; cursor: pointer; }
    button:hover { background-color: #5800a0; }
    .resultado { margin-top: 20px; background-color: #ece6ff; padding: 15px; border-radius: 10px; }
    .resultado h3 { color: #333; }
  </style>
</head>
<body>
  <div class="container">
    <h1>🌍 GeoIdeias BNCC</h1><label for="ano">Selecione o ano/série:</label>
<select id="ano">
  <option value="6ano">6º ano</option>
  <option value="7ano">7º ano</option>
  <option value="8ano">8º ano</option>
  <option value="9ano">9º ano</option>
  <option value="1em">1º EM</option>
  <option value="2em">2º EM</option>
  <option value="3em">3º EM</option>
</select>

<label for="tema">Digite um tema ou palavra-chave:</label>
<input type="text" id="tema" placeholder="Ex: água, migração, paisagem...">

<button onclick="mostrarSugestao()">Buscar sugestão</button>

<div id="resultado" class="resultado" style="display:none;"></div>

  </div>  <script>
    function mostrarSugestao() {
      const ano = document.getElementById('ano').value;
      const tema = document.getElementById('tema').value.toLowerCase();
      const resultado = document.getElementById('resultado');
      let sugestao = '';

      if (ano === '6ano' && tema.includes('água')) {
        sugestao = `
          <h3>Habilidade: EF06GE04</h3>
          <p><strong>Explicação:</strong> Estuda o ciclo da água e as diferenças de escoamento entre meios urbanos e rurais.</p>
          <p><strong>Atividades sugeridas:</strong></p>
          <ul>
            <li>Mini livro "A Jornada da Gota" para colorir</li>
            <li>Experimento com garrafa PET (simulação de escoamento)</li>
            <li>Mapa ilustrado da bacia hidrográfica da cidade</li>
          </ul>
        `;
      } else if (ano === '7ano' && tema.includes('território')) {
        sugestao = `
          <h3>Habilidade: EF07GE01</h3>
          <p><strong>Explicação:</strong> Estuda as territorialidades no Brasil e suas interações históricas e culturais.</p>
          <p><strong>Atividades sugeridas:</strong></p>
          <ul>
            <li>Comparação das ocupações territoriais por diferentes povos indígenas e colonizadores</li>
            <li>Debate sobre o direito à terra e demarcações de territórios</li>
            <li>Cartaz sobre a resistência de povos em diferentes territórios brasileiros</li>
          </ul>
        `;
      } else if (ano === '8ano' && tema.includes('migração')) {
        sugestao = `
          <h3>Habilidade: EF08GE04</h3>
          <p><strong>Explicação:</strong> Estuda os fluxos migratórios, suas causas e impactos na sociedade e no território.</p>
          <p><strong>Atividades sugeridas:</strong></p>
          <ul>
            <li>Mapas e gráficos de movimentos migratórios no Brasil e América Latina</li>
            <li>Histórias de imigrantes: criar relatos fictícios com base em dados históricos</li>
            <li>Debate sobre a migração forçada e os direitos humanos</li>
          </ul>
        `;
      } else if (ano === '9ano' && tema.includes('globalização')) {
        sugestao = `
          <h3>Habilidade: EF09GE05</h3>
          <p><strong>Explicação:</strong> Estuda a integração dos mercados e as influências culturais globais.</p>
          <p><strong>Atividades sugeridas:</strong></p>
          <ul>
            <li>Infográfico sobre a globalização econômica e seus efeitos nos países</li>
            <li>Simulação de uma negociação comercial internacional</li>
            <li>Debate sobre os impactos da globalização na diversidade cultural</li>
          </ul>
        `;
      } else if (ano === '1em' && tema.includes('territórios')) {
        sugestao = `
          <h3>Habilidade: EM13CHS201</h3>
          <p><strong>Explicação:</strong> Análise da formação e disputa de territórios em diferentes escalas.</p>
          <p><strong>Atividades sugeridas:</strong></p>
          <ul>
            <li>Debate sobre conflitos territoriais no Oriente Médio</li>
            <li>Estudo de caso sobre fronteiras e sua importância geopolítica</li>
            <li>Criação de mapas temáticos sobre o controle territorial global</li>
          </ul>
        `;
      } else if (ano === '2em' && tema.includes('meio ambiente')) {
        sugestao = `
          <h3>Habilidade: EM13CHS302</h3>
          <p><strong>Explicação:</strong> Análise dos impactos socioambientais e a relação das atividades humanas com a natureza.</p>
          <p><strong>Atividades sugeridas:</strong></p>
          <ul>
            <li>Discussão sobre os impactos da indústria no meio ambiente</li>
            <li>Proposta de soluções sustentáveis para empresas locais</li>
            <li>Mapa de poluição e conservação ambiental em uma cidade</li>
          </ul>
        `;
      } else if (ano === '3em' && tema.includes('trabalho')) {
        sugestao = `
          <h3>Habilidade: EM13CHS401</h3>
          <p><strong>Explicação:</strong> Análise das relações de produção, trabalho e transformação das sociedades em diferentes contextos.</p>
          <p><strong>Atividades sugeridas:</strong></p>
          <ul>
            <li>Comparação dos sistemas de trabalho industrial e agrícola ao longo da história</li>
            <li>Discussão sobre as transformações nas relações de trabalho com a Revolução Industrial</li>
            <li>Simulação de uma reunião de negociação entre empresas e trabalhadores</li>
          </ul>
        `;
      } else {
        sugestao = `<p>Nenhuma sugestão cadastrada para esse tema ainda. Tente outro termo ou selecione outra série.</p>`;
      }

      resultado.innerHTML = sugestao;
      resultado.style.display = 'block';
    }
  </script></body>
</html>
