<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sabrina Brisola | Portfólio BI</title>
  <link rel="icon" type="image/png" href="imagens/s-icon.png">
  <style>
    body {
      font-family: "Poppins", sans-serif;
      margin: 0;
      background-color: #1a0033;
      color: white;
    }

    header {
      text-align: center;
      padding: 2rem 1rem;
    }

    header h1 {
      font-size: 2rem;
      margin-bottom: 0.3rem;
      color: #e6b3ff;
    }

    header p {
      font-size: 1rem;
      color: #c7a4ff;
    }

    nav {
      display: flex;
      justify-content: center;
      background-color: #2e0854;
      padding: 0.8rem;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 1.5rem;
      font-weight: 500;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #d580ff;
    }

    main {
      padding: 2rem;
      max-width: 900px;
      margin: auto;
    }

    section {
      margin-bottom: 3rem;
    }

    h2 {
      color: #d580ff;
      border-bottom: 1px solid #5e3370;
      padding-bottom: 0.5rem;
      margin-bottom: 1rem;
    }

    .projetos {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }

    .projeto {
      background-color: #2e0854;
      border-radius: 12px;
      overflow: hidden;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .projeto:hover {
      transform: translateY(-5px);
      box-shadow: 0 4px 10px rgba(213, 128, 255, 0.4);
    }

    .projeto img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }

    .projeto h3 {
      margin: 1rem;
      color: #e6b3ff;
    }

    .projeto p {
      margin: 0 1rem 1rem;
      font-size: 0.9rem;
      color: #d1b3ff;
    }

    footer {
      text-align: center;
      padding: 1.5rem;
      background-color: #2e0854;
      color: #c7a4ff;
      font-size: 0.9rem;
    }

    .foto-perfil {
      display: block;
      margin: 0 auto 1rem;
      width: 130px;
      height: 130px;
      border-radius: 50%;
      object-fit: cover;
      border: 2px solid #d580ff;
    }
  </style>
</head>

<body>
  <header>
    <img src="imagens/3f36e098-3654-4b41-82ba-f1e8ab6e89e5.png" alt="Sabrina Brisola" class="foto-perfil">
    <h1>Sabrina Brisola</h1>
    <p>Portfólio de Business Intelligence • Power BI • SQL • DAX</p>
  </header>

  <nav>
    <a href="#sobre">Sobre mim</a>
    <a href="#projetos">Projetos</a>
    <a href="#contato">Contato</a>
  </nav>

  <main>
    <section id="sobre">
      <h2>Sobre mim</h2>
      <p>
        Sou estudante de Gestão de TI e analista com foco em Governança de Dados e Business Intelligence. 
        Tenho experiência com análise de chamados e suporte técnico, utilizando ferramentas como Power BI, SQL, Active Directory e Salesforce.
        Busco aprimorar a tomada de decisões estratégicas por meio da integração e análise inteligente de dados.
      </p>
    </section>

    <section id="projetos">
      <h2>Projetos</h2>
      <div class="projetos">
        <div class="projeto">
          <img src="imagens/projeto1.png" alt="Dashboard de Vendas">
          <h3>Dashboard de Vendas</h3>
          <p>Criei um dashboard no Power BI integrando dados de vendas e produtividade para análise de desempenho comercial.</p>
        </div>

        <div class="projeto">
          <img src="imagens/projeto2.png" alt="Análise de Custos">
          <h3>Análise de Custos e Processos</h3>
          <p>Estruturei indicadores financeiros e de processos, otimizando a visualização dos custos e resultados operacionais.</p>
        </div>

        <div class="projeto">
          <img src="imagens/projeto3.png" alt="Governança de Dados">
          <h3>Governança de Dados</h3>
          <p>Desenvolvi estrutura de controle e relatórios técnicos voltados à qualidade e confiabilidade das informações corporativas.</p>
        </div>
      </div>
    </section>

    <section id="contato">
      <h2>Contato</h2>
      <p>
        💼 <strong>Email:</strong> sabrinabrisola.s@gmail.com<br>
        🔗 <strong>LinkedIn:</strong> 
        <a href="https://www.linkedin.com/in/sabrinabrisola" target="_blank" style="color:#e6b3ff; text-decoration:none;">
          linkedin.com/in/sabrinabrisola
        </a>
      </p>
    </section>
  </main>

  <footer>
    <p>© 2025 Sabrina Brisola | Portfólio BI</p>
  </footer>
</body>
</html>
