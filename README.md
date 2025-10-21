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
... (440 linhas)
