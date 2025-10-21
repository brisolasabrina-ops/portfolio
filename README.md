<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sabrina Brisola | Portfólio BI</title>
  <!-- Google Fonts: Inter (Otimizada para BI/Data) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
      margin: 0;
      background: linear-gradient(to right, #050009, #1c0034);
      color: #fff;
      line-height: 1.6;
      font-weight: 400;
      font-feature-settings: "calt" 1, "liga" 1;
    }

    /* Cabeçalhos usam peso mais bold para contraste */
    h1, h2, h3 {
      font-weight: 600;
      letter-spacing: -0.02em;
      font-feature-settings: "calt" 1, "liga" 1, "ss01" 1;
    }

    header {
      background: linear-gradient(to bottom, rgba(56, 0, 98, 0.52), rgba(0, 0, 0, 0));
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 40px;
      position: sticky;
      top: 0;
      z-index: 100;
      opacity: 0;
      animation: fadeIn 1s ease-out forwards;
      transition: box-shadow 0.3s ease;
      font-family: "Inter", sans-serif;
    }

    header:hover {
      cursor: pointer;
    }

    header h1 {
        color: ;
      font-size: clamp(1.5em, 4vw, 2em);
      letter-spacing: -0.025em;
      font-weight: 700;
      transform: translateX(-20px);
      opacity: 0;
      animation: slideInLeft 0.8s ease-out 0.2s forwards;
      transition: color 0.3s ease, transform 0.3s ease;
    }

    header h1:hover {
      color: #b278ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 2rem;
      margin: 0;
      padding: 0;
    }

    nav a {
      color: #e0c7ff;
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s ease, transform 0.3s ease;
      opacity: 0;
      animation: fadeIn 0.8s ease-out forwards;
      animation-delay: calc(0.3s + 0.1s * var(--i));
      font-feature-settings: "calt" 1;
    }

    nav a:hover {
      color: #b278ff;
      transform: translateY(-2px);
      cursor: pointer;
    }
    
    .container {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      max-width: 1200px;
      margin: 50px auto;
      padding: 0 20px;
      gap: 50px;
    }

    .profile {
      flex: 1 1 300px;
      text-align: center;
    }

    .profile img {
      width: 450px;
      border-radius: 12px;
      margin-bottom: 20px;
      opacity: 0;
      transform: scale(0.95);
      animation: fadeInScale 1s ease-out 0.4s forwards;
      transition: transform 0.3s ease,
    }

    .profile img:hover {
      transform: scale(1.02);
      cursor: pointer;
    }

    .profile h1 {
      margin: 0;
      font-size: clamp(2em, 5vw, 2.5em);
      font-weight: 700;
      transform: translateX(-20px);
      opacity: 0;
      animation: slideInLeft 0.8s ease-out 0.6s forwards;
      transition: color 0.3s ease, transform 0.3s ease;
      letter-spacing: -0.025em;
    }

    .profile h1:hover {
      color: #b278ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    .profile p {
      margin: 5px 0 0 0;
      color: #ccc;
      font-size: 1.1em;
      font-weight: 400;
      opacity: 0;
      animation: fadeIn 0.8s ease-out forwards;
      animation-delay: calc(0.7s + 0.2s * var(--i));
      transition: color 0.3s ease, transform 0.3s ease;
      line-height: 1.7;
      display: flex;
      flex-direction: column;
    }

    .profile p:hover {
      color: #e0c7ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    .about {
      flex: 2 1 500px;
    }

    .about h2 {
      font-size: clamp(2.5em, 6vw, 3.5em);
      font-weight: 700;
      display: flex;
      flex-direction: column;
      padding-bottom: 5px;
      margin-bottom: 10px;
      transform: translateX(-20px);
      opacity: 0;
      animation: slideInLeft 0.8s ease-out 0.8s forwards;
      transition: color 0.3s ease, transform 0.3s ease;
      letter-spacing: -0.03em;
    }

    .about h2:hover {
      color: #b278ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    .about p {
      font-size: 1.1em;
      color: #eee;
      font-weight: 400;
      display: flex;
      flex-direction: column;
      opacity: 0;
      animation: fadeIn 0.8s ease-out forwards;
      animation-delay: calc(0.9s + 0.2s * var(--i));
      transition: color 0.3s ease, transform 0.3s ease;
      line-height: 1.75;
    }

    .about p:hover {
      color: #e0c7ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    .en {
      font-size: 0.85em;
      color: #b8a8d9;
      font-weight: 400;
      display: inline;
      margin-top: 5px;
      transition: color 0.3s ease, transform 0.3s ease;
      line-height: 1.6;
    }

    .en:hover {
      color: #e0c7ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    .projects-section {
      max-width: 1200px;
      margin: 50px auto;
      padding: 0 20px;
    }

    .projects-section h2 {
      font-size: clamp(2.5em, 6vw, 3.5em);
      font-weight: 700;
      display: flex;
      flex-direction: column;
      padding-bottom: 5px;
      margin-bottom: 10px;
      transform: translateX(-20px);
      opacity: 0;
      animation: slideInLeft 0.8s ease-out 0.2s forwards;
      transition: color 0.3s ease, transform 0.3s ease;
      letter-spacing: -0.03em;
    }

    .projects-section h2:hover {
      color: #b278ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    .project {
      display: flex;
      align-items: center;
      gap: 50px;
      margin-bottom: 40px;
      opacity: 0;
      animation: fadeInUp 1s ease-out forwards;
      animation-delay: calc(0.4s + 0.3s * var(--i));
      border-radius: 12px;
      padding: 20px;
    }

    .project.reverse {
      flex-direction: row-reverse;
    }

    .project-thumbnail {
      flex: 1 1 400px;
    }

    .project-thumbnail img {
      box-shadow: 0 0 20px #a942fd81;
      width: 100%;
      border-radius: 8px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .project-thumbnail img:hover {
      transform: scale(1.02);
      box-shadow: 0 0 30px #a942fd;
      cursor: pointer;
    }

    .project-description {
      flex: 2 1 500px;
    }

    .project-description h3 {
      margin-top: 0;
      margin-bottom: 10px;
      font-size: clamp(1.5em, 3vw, 1.9em);
      font-weight: 600;
      color: #d1adff;
      transform: translateX(-20px);
      opacity: 0;
      animation: slideInLeft 0.8s ease-out forwards;
      animation-delay: calc(0.5s + 0.3s * var(--i));
      transition: color 0.3s ease, transform 0.3s ease;
      letter-spacing: -0.02em;
    }

    .project-description h3:hover {
      color: #e0c7ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    .project-description p {
      margin: 0 0 10px 0;
      font-size: 1.05em;
      color: #eee;
      font-weight: 400;
      line-height: 1.75;
      transition: color 0.3s ease, transform 0.3s ease;
      display: flex;
      flex-direction: column;
    }

    .project-description p:hover {
      color: #e0c7ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    .divider {
      width: 100%;
      height: 1px;
      background: linear-gradient(90deg, transparent, rgba(178, 120, 255, 0.6), transparent);
      margin: 25px 0;
      transition: all 0.3s ease;
    }

    .divider:hover {
      background: linear-gradient(90deg, transparent, #b278ff, transparent);
      height: 2px;
      cursor: pointer;
    }

    footer {
      text-align: center;
      padding: 30px;
      background-color: #2d0052;
      color: #ccc;
      font-size: 0.95em;
      opacity: 0;
      animation: fadeIn 1s ease-out 1.2s forwards;
      border-radius: 12px;
      margin: 0 20px;
    }

    footer p {
      opacity: 0;
      animation: fadeIn 0.8s ease-out forwards;
      animation-delay: calc(1.3s + 0.2s * var(--i));
      transition: color 0.3s ease, transform 0.3s ease;
      font-weight: 400;
      line-height: 1.6;
      display: flex;
      flex-direction: column;
    }

    footer p:hover {
      color: #e0c7ff;
      transform: translateY(-2px);
      cursor: pointer;
    }

    a {
      color: #6c34c0;
      text-decoration: none;
      font-weight: 500;
      transition: all 0.3s ease;
    }

    a:hover {
      text-decoration: underline;
      color: #b278ff;
      transform: translateY(-1px);
      cursor: pointer;
    }

    /* Animações */
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes slideInLeft {
      from {
        opacity: 0;
        transform: translateX(-20px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    @keyframes fadeInScale {
      from {
        opacity: 0;
        transform: scale(0.95);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    /* Contador para animações escalonadas */
    .profile p:nth-child(1) { --i: 1; }
    .profile p:nth-child(2) { --i: 2; }
    .about p:nth-child(2) { --i: 1; }
    .about p:nth-child(3) { --i: 2; }
    .about p:nth-child(4) { --i: 3; }
    .project:nth-child(2) { --i: 1; }
    .project:nth-child(3) { --i: 2; }
    .project:nth-child(4) { --i: 3; }
    nav li:nth-child(1) a { --i: 1; }
    nav li:nth-child(2) a { --i: 2; }
    nav li:nth-child(3) a { --i: 3; }
    footer p:nth-child(1) { --i: 1; }
    footer p:nth-child(2) { --i: 2; }

    @media (max-width: 900px) {
      header {
        flex-direction: column;
        gap: 10px;
        padding: 15px 20px;
      }

      nav ul {
        flex-wrap: wrap;
        justify-content: center;
        gap: 1.5rem;
      }

      .container {
        flex-direction: column;
        align-items: center;
        gap: 3rem;
      }

      .about {
        text-align: center;
      }

      .project {
        flex-direction: column;
        gap: 2rem;
        padding: 1.5rem;
      }

      .project.reverse {
        flex-direction: column;
      }

      footer {
        margin: 0 10px;
        padding: 2rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Sabrina Brisola</h1>
    <nav>
      <ul>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#projetos">Projetos</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>
  </header>

  <div class="container" id="sobre">
    <div class="profile">
      <img src="Imagens/3f36e098-3654-4b41-82ba-f1e8ab6e89e5.png" alt="Sabrina Brisola">
      <h1>Sabrina Brisola</h1>
      <p>Analista de BI e Governança de Dados <span class="en">BI & Data Governance Analyst</span></p>
    </div>

    <div class="about">
      <h2>Sobre mim <span class="en">(About Me)</span></h2>
      <p>Sou uma profissional de TI dedicada à governança de dados, business intelligence e análise avançada, com foco em gerar valor por meio de insights precisos e conformidade regulatória. Com experiência prática em ambientes corporativos dinâmicos, como suporte computacional na SGS do Brasil, domino ferramentas como Power BI (incluindo DAX avançado), SQL, ETL e integrações com sistemas como Salesforce, SAP e Active Directory. Certificada em Google Data Analytics e fundamentos de BI, priorizo soluções inovadoras que otimizem processos, garantam qualidade de dados e atendam à LGPD, sempre em contextos colaborativos e multiculturais. <span class="en">I am an IT professional dedicated to data governance, business intelligence, and advanced analytics, focused on creating value through accurate insights and regulatory compliance. With hands-on experience in dynamic corporate environments, such as IT support at SGS Brazil, I master tools like Power BI (including advanced DAX), SQL, ETL, and integrations with systems such as Salesforce, SAP, and Active Directory. Certified in Google Data Analytics and BI fundamentals, I prioritize innovative solutions that optimize processes, ensure data quality, and comply with LGPD regulations, always in collaborative and multicultural contexts.</span></p>
      <div class="divider"></div>
    </div>
  </div>

  <section class="projects-section" id="projetos">
    <h2>Projetos <span class="en">(Projects)</span></h2>

    <div class="project">
      <div class="project-thumbnail">
        <a href="#"><img src="Imagens/Projetos.jpg" alt="Miniatura do Dashboard Executivo de Incidentes"></a>
      </div>
      <div class="project-description">
        <h3>Consolidação de Dados e Otimização de Processos</h3>
        <p>Desenvolvi um projeto de integração de dados provenientes de diferentes fontes, como ERP, CRM e planilhas, para gerar insights sobre processos, produtividade e vendas. Estruturei os dados de forma organizada e criei dashboards no Power BI, permitindo análises mais rápidas e decisões estratégicas fundamentadas em dados confiáveis.
 <span class="en">I developed a project integrating data from different sources, such as ERP, CRM, and spreadsheets, to generate insights on processes, productivity, and sales. I structured the data in an organized way and created dashboards in Power BI, enabling faster analysis and strategic decision-making based on reliable data.
</span></p>
        <div class="divider"></div>
      </div>
    </div>

    <div class="project reverse">
      <div class="project-thumbnail">
        <a href="#"><img src="Imagens/Projetos.jpg" alt="Miniatura da Otimização de Dados Sensíveis"></a>
      </div>
      <div class="project-description">
        <h3>Dashboard de Qualidade de Dados</h3>
        <p>Criei dashboards para identificar inconsistências, duplicidades e informações incompletas em conjuntos de dados. O projeto permitiu monitorar a qualidade das informações e fornecer indicadores que apoiam a tomada de decisão, reforçando boas práticas de governança de dados.
 <span class="en">I created dashboards to identify inconsistencies, duplicates, and incomplete information within datasets. The project enabled monitoring data quality and providing indicators that support decision-making, reinforcing best practices in data governance.
</span></p>
        <div class="divider"></div>
      </div>
    </div>

    <div class="project">
      <div class="project-thumbnail">
        <a href="#"><img src="Imagens/Projetos.jpg" alt="Miniatura da Análise de Conformidade e Riscos de Dados"></a>
      </div>
      <div class="project-description">
        <h3>Análise de Conformidade de Dados (LGPD/Compliance)</h3>
        <p>Realizei uma análise detalhada de dados para identificar informações sensíveis e avaliar a aderência às normas de compliance e LGPD. Utilizei SQL para checar inconsistências e criei relatórios executivos que transformam dados complexos em insights estratégicos, garantindo a segurança e integridade das informações.
<span class="en">I conducted a detailed data analysis to identify sensitive information and assess adherence to compliance standards and LGPD. I used SQL to check for inconsistencies and created executive reports that transform complex data into strategic insights, ensuring the security and integrity of information.</span></p>
        <div class="divider"></div>
      </div>
    </div>
  </section>

  <footer id="contato">
    <p>Contato: <a href="mailto:brisola.sabrina@gmail.com">brisola.sabrina@gmail.com</a> | Celular: +55 (11) 94313-7543 <span class="en">Contact: <a href="mailto:brisola.sabrina@gmail.com">brisola.sabrina@gmail.com</a> | Phone: +55 (11) 94313-7543</span></p>
    <div class="divider"></div>
  </footer>
</body>
</html>
