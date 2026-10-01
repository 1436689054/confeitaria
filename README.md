# confeitaria<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Maison Douceur | Confeitaria Artesanal</title>

  <meta name="description"
        content="Confeitaria artesanal especializada em bolos, doces e experiências únicas.">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Montserrat:wght@300;400;500;600;700&display=swap"
        rel="stylesheet">

  <style>
    :root {
      --creme: #f8f0df;
      --creme-claro: #fffaf0;
      --marrom: #4a2c20;
      --marrom-escuro: #2e1a13;
      --caramelo: #a66a42;
      --dourado: #c89b63;
      --texto: #50382e;
      --branco: #ffffff;
      --sombra: 0 15px 40px rgba(74, 44, 32, 0.12);
      --transicao: 0.3s ease;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Montserrat", sans-serif;
      color: var(--texto);
      background: var(--creme-claro);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button {
      font-family: inherit;
    }

    /* =========================
       HEADER
    ========================= */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(255, 250, 240, 0.94);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(74, 44, 32, 0.08);
    }

    .navbar {
      max-width: 1200px;
      height: 78px;
      margin: auto;
      padding: 0 25px;

      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-family: "Cormorant Garamond", serif;
      font-size: 30px;
      font-weight: 700;
      color: var(--marrom);
    }

    .logo span {
      color: var(--caramelo);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 32px;
      list-style: none;
    }

    .nav-links a {
      position: relative;
      font-size: 13px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: var(--transicao);
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -7px;
      width: 0;
      height: 2px;
      background: var(--caramelo);
      transition: var(--transicao);
    }

    .nav-links a:hover {
      color: var(--caramelo);
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .menu-btn {
      display: none;
      border: 0;
      background: none;
      color: var(--marrom);
      font-size: 28px;
      cursor: pointer;
    }

    /* =========================
       HERO
    ========================= */

    .hero {
      min-height: 100vh;
      padding: 130px 7% 70px;

      display: flex;
      align-items: center;

      background:
        radial-gradient(circle at 85% 20%, rgba(200,155,99,.22), transparent 28%),
        linear-gradient(120deg, #fffaf0 0%, #f5ead5 100%);
    }

    .hero-content {
      width: 100%;
      max-width: 1200px;
      margin: auto;

      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      gap: 70px;
    }

    .hero-text {
      animation: aparecer 1s ease forwards;
    }

    .tag {
      display: inline-block;
      margin-bottom: 18px;
      padding: 8px 15px;

      border: 1px solid rgba(166,106,66,.4);
      border-radius: 30px;

      color: var(--caramelo);
      font-size: 11px;
      font-weight: 700;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .hero h1 {
      max-width: 650px;

      font-family: "Cormorant Garamond", serif;
      font-size: clamp(55px, 7vw, 92px);
      line-height: .9;
      color: var(--marrom-escuro);
      margin-bottom: 28px;
    }

    .hero h1 span {
      color: var(--caramelo);
      font-style: italic;
    }

    .hero p {
      max-width: 550px;
      margin-bottom: 35px;
      font-size: 16px;
      color: #76584a;
    }

    .buttons {
      display: flex;
      align-items: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      justify-content: center;
      align-items: center;

      padding: 15px 27px;
      border-radius: 3px;

      border: 1px solid var(--marrom);
      cursor: pointer;

      font-size: 12px;
      font-weight: 700;
      letter-spacing: 1px;
      text-transform: uppercase;

      transition: var(--transicao);
    }

    .btn-primary {
      background: var(--marrom);
      color: white;
    }

    .btn-primary:hover {
      background: var(--caramelo);
      border-color: var(--caramelo);
      transform: translateY(-3px);
    }

    .btn-outline {
      color: var(--marrom);
      background: transparent;
    }

    .btn-outline:hover {
      background: var(--marrom);
      color: white;
    }

    .hero-image {
      position: relative;
      min-height: 550px;

      display: flex;
      justify-content: center;
      align-items: center;
    }

    .cake-circle {
      width: min(470px, 80vw);
      aspect-ratio: 1;

      border-radius: 50%;

      background:
        linear-gradient(
          135deg,
          rgba(255,255,255,.3),
          rgba(255,255,255,0)
        ),
        #d7ad83;

      box-shadow:
        0 30px 70px rgba(74,44,32,.25),
        inset 0 0 0 15px rgba(255,255,255,.18);

      display: flex;
      align-items: center;
      justify-content: center;

      font-size: 150px;

      animation: flutuar 5s ease-in-out infinite;
    }

    .floating-card {
      position: absolute;
      bottom: 35px;
      left: 15px;

      padding: 18px 22px;

      background: rgba(255,250,240,.94);
      box-shadow: var(--sombra);

      border-left: 3px solid var(--caramelo);
    }

    .floating-card strong {
      display: block;
      font-family: "Cormorant Garamond", serif;
      font-size: 25px;
      color: var(--marrom);
    }

    .floating-card small {
      color: #866a5b;
      font-size: 11px;
      letter-spacing: 1px;
      text-transform: uppercase;
    }

    /* =========================
       SEÇÕES
    ========================= */

    section {
      padding: 100px 7%;
    }

    .section-header {
      max-width: 700px;
      margin: 0 auto 55px;
      text-align: center;
    }

    .section-header span {
      color: var(--caramelo);
      font-size: 11px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 3px;
    }

    .section-header h2 {
      margin: 10px 0 15px;

      font-family: "Cormorant Garamond", serif;
      font-size: clamp(42px, 5vw, 62px);
      line-height: 1;
      color: var(--marrom);
    }

    .section-header p {
      color: #80685c;
      font-size: 14px;
    }

    /* =========================
       PRODUTOS
    ========================= */

    .products {
      background: var(--creme);
    }

    .product-grid {
      max-width: 1200px;
      margin: auto;

      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .product {
      overflow: hidden;
      background: var(--creme-claro);
      box-shadow: 0 8px 30px rgba(74,44,32,.07);
      transition: var(--transicao);
    }

    .product:hover {
      transform: translateY(-8px);
      box-shadow: var(--sombra);
    }

    .product-image {
      height: 260px;

      display: flex;
      align-items: center;
      justify-content: center;

      font-size: 100px;

      background:
        linear-gradient(135deg, rgba(255,255,255,.25), transparent),
        #dfc09f;
    }

    .product:nth-child(2) .product-image {
      background-color: #c9a27e;
    }

    .product:nth-child(3) .product-image {
      background-color: #ead7bd;
    }

    .product-info {
      padding: 25px;
    }

    .product-info h3 {
      margin-bottom: 8px;

      font-family: "Cormorant Garamond", serif;
      font-size: 30px;
      color: var(--marrom);
    }

    .product-info p {
      margin-bottom: 18px;
      color: #80685c;
      font-size: 13px;
    }

    .price {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .price strong {
      color: var(--caramelo);
      font-size: 18px;
    }

    .order-btn {
      border: 0;
      padding: 10px 15px;

      color: white;
      background: var(--marrom);

      cursor: pointer;
      transition: var(--transicao);
    }

    .order-btn:hover {
      background: var(--caramelo);
    }

    /* =========================
       SOBRE
    ========================= */

    .about {
      max-width: 1200px;
      margin: auto;

      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 80px;
      align-items: center;
    }

    .about-image {
      min-height: 500px;

      display: flex;
      align-items: center;
      justify-content: center;

      background:
        linear-gradient(rgba(74,44,32,.15), rgba(74,44,32,.15)),
        #b88760;

      font-size: 130px;
    }

    .about-text span {
      color: var(--caramelo);
      font-size: 11px;
      font-weight: 700;
      letter-spacing: 3px;
      text-transform: uppercase;
    }

    .about-text h2 {
      margin: 12px 0 20px;

      font-family: "Cormorant Garamond", serif;
      font-size: 58px;
      line-height: 1;
      color: var(--marrom);
    }

    .about-text p {
      margin-bottom: 18px;
      color: #76584a;
      font-size: 15px;
    }

    .signature {
      margin-top: 25px;

      font-family: "Cormorant Garamond", serif;
      font-size: 32px;
      font-style: italic;
      color: var(--caramelo);
    }

    /* =========================
       DIFERENCIAIS
    ========================= */

    .features {
      background: var(--marrom);
      color: var(--creme);
    }

    .features .section-header h2,
    .features .section-header p {
      color: var(--creme);
    }

    .feature-grid {
      max-width: 1000px;
      margin: auto;

      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 25px;
    }

    .feature {
      padding: 35px 25px;
      text-align: center;

      border: 1px solid rgba(255,255,255,.12);

      transition: var(--transicao);
    }

    .feature:hover {
      background: rgba(255,255,255,.06);
      transform: translateY(-5px);
    }

    .feature-icon {
      font-size: 38px;
      margin-bottom: 15px;
    }

    .feature h3 {
      margin-bottom: 10px;

      font-family: "Cormorant Garamond", serif;
      font-size: 27px;
    }

    .feature p {
      color: #d9c7b5;
      font-size: 13px;
    }

    /* =========================
       CONTATO
    ========================= */

    .contact {
      background: #fffaf0;
    }

    .contact-container {
      max-width: 900px;
      margin: auto;

      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 50px;
    }

    .contact-info h3 {
      margin-bottom: 15px;

      font-family: "Cormorant Garamond", serif;
      font-size: 38px;
      color: var(--marrom);
    }

    .contact-info p {
      margin-bottom: 22px;
      color: #80685c;
      font-size: 14px;
    }

    .contact-item {
      margin-bottom: 15px;
      font-size: 14px;
    }

    .contact-item strong {
      display: block;
      color: var(--marrom);
      margin-bottom: 3px;
    }

    form {
      display: grid;
      gap: 15px;
    }

    input,
    textarea {
      width: 100%;
      padding: 15px;

      border: 1px solid #dfcdb9;
      outline: none;

      background: #fffdf8;
      color: var(--texto);

      font-family: inherit;
      transition: var(--transicao);
    }

    textarea {
      min-height: 130px;
      resize: vertical;
    }

    input:focus,
    textarea:focus {
      border-color: var(--caramelo);
      box-shadow: 0 0 0 3px rgba(166,106,66,.08);
    }

    /* =========================
       FOOTER
    ========================= */

    footer {
      padding: 35px 7%;
      background: var(--marrom-escuro);
      color: #d8c5b1;
      text-align: center;
    }

    footer .logo {
      justify-content: center;
      color: var(--creme);
      margin-bottom: 10px;
    }

    footer p {
      font-size: 12px;
    }

    /* =========================
       MODAL
    ========================= */

    .modal {
      position: fixed;
      inset: 0;
      z-index: 2000;

      display: none;
      align-items: center;
      justify-content: center;

      padding: 20px;

      background: rgba(46,26,19,.65);
      backdrop-filter: blur(5px);
    }

    .modal.active {
      display: flex;
    }

    .modal-content {
      width: 100%;
      max-width: 450px;
      padding: 35px;

      background: var(--creme-claro);
      box-shadow: var(--sombra);

      animation: aparecer .3s ease;
    }

    .modal-content h3 {
      margin-bottom: 8px;

      font-family: "Cormorant Garamond", serif;
      font-size: 38px;
      color: var(--marrom);
    }

    .modal-content p {
      margin-bottom: 20px;
      color: #80685c;
      font-size: 13px;
    }

    .close-modal {
      float: right;

      border: 0;
      background: none;

      color: var(--marrom);
      font-size: 25px;
      cursor: pointer;
    }

    /* =========================
       ANIMAÇÕES
    ========================= */

    @keyframes aparecer {
      from {
        opacity: 0;
        transform: translateY(20px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes flutuar {
      0%, 100% {
        transform: translateY(0);
      }

      50% {
        transform: translateY(-15px);
      }
    }

    /* =========================
       RESPONSIVO
    ========================= */

    @media (max-width: 900px) {

      .nav-links {
        position: absolute;
        top: 78px;
        left: 0;

        width: 100%;
        padding: 25px;

        flex-direction: column;
        gap: 22px;

        background: var(--creme-claro);

        transform: translateY(-150%);
        transition: var(--transicao);
      }

      .nav-links.active {
        transform: translateY(0);
      }

      .menu-btn {
        display: block;
      }

      .hero-content,
      .about,
      .contact-container {
        grid-template-columns: 1fr;
      }

      .hero {
        text-align: center;
      }

      .hero p {
        margin-left: auto;
        margin-right: auto;
      }

      .buttons {
        justify-content: center;
      }

      .hero-image {
        min-height: 400px;
      }

      .about {
        gap: 40px;
      }

      .about-text {
        text-align: center;
      }
    }

    @media (max-width: 700px) {

      section {
        padding: 75px 5%;
      }

      .product-grid,
      .feature-grid {
        grid-template-columns: 1fr;
      }

      .product-image {
        height: 220px;
      }

      .about-image {
        min-height: 350px;
      }

      .hero h1 {
        font-size: 60px;
      }

      .floating-card {
        left: 0;
        bottom: 5px;
      }
    }
  </style>
</head>

<body>

  <!-- =========================
       HEADER
  ========================= -->

  <header>
    <nav class="navbar">

      <a href="#inicio" class="logo">
        Maison <span>Douceur</span>
      </a>

      <ul class="nav-links" id="navLinks">
        <li><a href="#inicio">Início</a></li>
        <li><a href="#produtos">Delícias</a></li>
        <li><a href="#sobre">Nossa História</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>

      <button class="menu-btn" id="menuBtn" aria-label="Abrir menu">
        ☰
      </button>

    </nav>
  </header>


  <!-- =========================
       HERO
  ========================= -->

  <main>

    <section class="hero" id="inicio">

      <div class="hero-content">

        <div class="hero-text">

          <span class="tag">Confeitaria Artesanal</span>

          <h1>
            Feito com<br>
            <span>amor</span> e sabor.
          </h1>

          <p>
            Bolos, doces e sobremesas preparados artesanalmente
            para transformar momentos especiais em memórias
            deliciosas.
          </p>

          <div class="buttons">
            <a href="#produtos" class="btn btn-primary">
              Conheça nossas delícias
            </a>

            <a href="#contato" class="btn btn-outline">
              Fazer encomenda
            </a>
          </div>

        </div>

        <div class="hero-image">

          <div class="cake-circle">
            🎂
          </div>

          <div class="floating-card">
            <strong>100% artesanal</strong>
            <small>Produzido com carinho</small>
          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         PRODUTOS
    ========================= -->

    <section class="products" id="produtos">

      <div class="section-header">
        <span>Nosso cardápio</span>

        <h2>Pequenos prazeres</h2>

        <p>
          Uma seleção especial preparada para adoçar
          os seus melhores momentos.
        </p>
      </div>

      <div class="product-grid">

        <article class="product">

          <div class="product-image">
            🍰
          </div>

          <div class="product-info">

            <h3>Bolo Artesanal</h3>

            <p>
              Massa fofinha, recheio cremoso e acabamento
              delicado feito à mão.
            </p>

            <div class="price">
              <strong>A partir de R$ 65</strong>

              <button
                class="order-btn"
                data-product="Bolo Artesanal">
                Encomendar
              </button>
            </div>

          </div>

        </article>


        <article class="product">

          <div class="product-image">
            🧁
          </div>

          <div class="product-info">

            <h3>Cupcakes</h3>

            <p>
              Pequenos bolinhos decorados com sabores
              irresistíveis.
            </p>

            <div class="price">
              <strong>A partir de R$ 8</strong>

              <button
                class="order-btn"
                data-product="Cupcakes">
                Encomendar
              </button>
            </div>

          </div>

        </article>


        <article class="product">

          <div class="product-image">
            🍫
          </div>

          <div class="product-info">

            <h3>Doces Finos</h3>

            <p>
              Brigadeiros, trufas e doces especiais
              para festas e celebrações.
            </p>

            <div class="price">
              <strong>A partir de R$ 4</strong>

              <button
                class="order-btn"
                data-product="Doces Finos">
                Encomendar
              </button>
            </div>

          </div>

        </article>

      </div>

    </section>


    <!-- =========================
         SOBRE
    ========================= -->

    <section id="sobre">

      <div class="about">

        <div class="about-image">
          👩🏻‍🍳
        </div>

        <div class="about-text">

          <span>Quem somos</span>

          <h2>
            Uma história<br>
            feita de afeto.
          </h2>

          <p>
            A Maison Douceur nasceu do amor pela confeitaria
            e pelo desejo de transformar ingredientes simples
            em experiências inesquecíveis.
          </p>

          <p>
            Cada receita é preparada em pequenos lotes,
            valorizando ingredientes selecionados, técnicas
            artesanais e aquele sabor que lembra momentos
            especiais.
          </p>

          <div class="signature">
            Com carinho, Maison Douceur ♡
          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         DIFERENCIAIS
    ========================= -->

    <section class="features">

      <div class="section-header">

        <span>Por que escolher a gente?</span>

        <h2>Feito para encantar</h2>

        <p>
          Mais do que doces, criamos experiências.
        </p>

      </div>

      <div class="feature-grid">

        <div class="feature">

          <div class="feature-icon">
            🌿
          </div>

          <h3>Ingredientes selecionados</h3>

          <p>
            Escolhemos cuidadosamente cada ingrediente
            utilizado em nossas receitas.
          </p>

        </div>


        <div class="feature">

          <div class="feature-icon">
            🤎
          </div>

          <h3>Produção artesanal</h3>

          <p>
            Tudo é preparado com atenção aos detalhes
            e muito carinho.
          </p>

        </div>


        <div class="feature">

          <div class="feature-icon">
            ✨
          </div>

          <h3>Feito para você</h3>

          <p>
            Personalizamos pedidos para tornar sua
            celebração ainda mais especial.
          </p>

        </div>

      </div>

    </section>


    <!-- =========================
         CONTATO
    ========================= -->

    <section class="contact" id="contato">

      <div class="section-header">

        <span>Vamos conversar</span>

        <h2>Faça sua encomenda</h2>

        <p>
          Conte para nós o que você está imaginando.
        </p>

      </div>

      <div class="contact-container">

        <div class="contact-info">

          <h3>Entre em contato</h3>

          <p>
            Estamos prontas para transformar sua ideia
            em uma deliciosa realidade.
          </p>

          <div class="contact-item">
            <strong>WhatsApp</strong>
            (83) 99999-9999
          </div>

          <div class="contact-item">
            <strong>Instagram</strong>
            @maisondouceur
          </div>

          <div class="contact-item">
            <strong>Atendimento</strong>
            Segunda a sábado · 09h às 18h
          </div>

        </div>


        <form id="contactForm">

          <input
            type="text"
            id="nome"
            placeholder="Seu nome"
            required>

          <input
            type="email"
            id="email"
            placeholder="Seu melhor e-mail"
            required>

          <input
            type="text"
            id="pedido"
            placeholder="O que você gostaria de encomendar?"
            required>

          <textarea
            id="mensagem"
            placeholder="Conte mais sobre sua encomenda..."
            required></textarea>

          <button class="btn btn-primary" type="submit">
            Enviar pedido
          </button>

        </form>

      </div>

    </section>

  </main>


  <!-- =========================
       FOOTER
  ========================= -->

  <footer>

    <div class="logo">
      Maison <span>Douceur</span>
    </div>

    <p>
      © <span id="year"></span> Maison Douceur.
      Todos os direitos reservados.
    </p>

  </footer>


  <!-- =========================
       MODAL
  ========================= -->

  <div class="modal" id="modal">

    <div class="modal-content">

      <button class="close-modal" id="closeModal">
        ×
      </button>

      <h3>Vamos adoçar seu dia!</h3>

      <p id="modalText">
        Preencha seus dados para solicitar sua encomenda.
      </p>

      <form id="modalForm">

        <input
          type="text"
          placeholder="Seu nome"
          required>

        <input
          type="tel"
          placeholder="Seu WhatsApp"
          required>

        <button class="btn btn-primary" type="submit">
          Solicitar orçamento
        </button>

      </form>

    </div>

  </div>


  <!-- =========================
       JAVASCRIPT
  ========================= -->

  <script>

    // Ano automático
    document.getElementById("year").textContent =
      new Date().getFullYear();


    // Menu mobile
    const menuBtn = document.getElementById("menuBtn");
    const navLinks = document.getElementById("navLinks");

    menuBtn.addEventListener("click", () => {
      navLinks.classList.toggle("active");

      menuBtn.textContent =
        navLinks.classList.contains("active")
          ? "×"
          : "☰";
    });


    // Fechar menu ao clicar em um link
    document.querySelectorAll(".nav-links a").forEach(link => {

      link.addEventListener("click", () => {

        navLinks.classList.remove("active");

        menuBtn.textContent = "☰";

      });

    });


    // Modal de encomenda
    const modal = document.getElementById("modal");
    const closeModal = document.getElementById("closeModal");
    const modalText = document.getElementById("modalText");

    document.querySelectorAll(".order-btn").forEach(button => {

      button.addEventListener("click", () => {

        const product =
          button.getAttribute("data-product");

        modalText.textContent =
          `Você escolheu: ${product}. Preencha seus dados para solicitar um orçamento.`;

        modal.classList.add("active");

      });

    });


    // Fechar modal
    closeModal.addEventListener("click", () => {
      modal.classList.remove("active");
    });


    // Fechar clicando fora
    modal.addEventListener("click", event => {

      if (event.target === modal) {
        modal.classList.remove("active");
      }

    });


    // Formulário do modal
    document.getElementById("modalForm")
      .addEventListener("submit", event => {

        event.preventDefault();

        alert(
          "Obrigada! Seu pedido foi recebido. Em breve entraremos em contato."
        );

        modal.classList.remove("active");

        event.target.reset();

      });


    // Formulário principal
    document.getElementById("contactForm")
      .addEventListener("submit", event => {

        event.preventDefault();

        const nome =
          document.getElementById("nome").value;

        alert(
          `Obrigada, ${nome}! Recebemos sua mensagem e entraremos em contato.`
        );

        event.target.reset();

      });


    // Animação suave dos elementos ao aparecerem
    const observer = new IntersectionObserver(
      entries => {

        entries.forEach(entry => {

          if (entry.isIntersecting) {

            entry.target.style.opacity = "1";
            entry.target.style.transform = "translateY(0)";

          }

        });

      },
      {
        threshold: 0.12
      }
    );


    document
      .querySelectorAll(".product, .feature, .about-text")
      .forEach(element => {

        element.style.opacity = "0";
        element.style.transform = "translateY(25px)";
        element.style.transition =
          "opacity .7s ease, transform .7s ease";

        observer.observe(element);

      });

  </script>

</body>
</html>
Claro. Vou alterar o formulário para que o pedido seja **montado automaticamente e enviado pelo WhatsApp** para **(81) 89181-775**.

 No seu HTML, substitua os dois tratamentos de formulário pelo código abaixo:

```
<script>
  // =========================
  // WHATSAPP
  // =========================

  const whatsapp = "558189181775";

  // Formulário principal
  document.getElementById("contactForm")
    .addEventListener("submit", function(event) {

      event.preventDefault();

      const nome = document.getElementById("nome").value;
      const email = document.getElementById("email").value;
      const pedido = document.getElementById("pedido").value;
      const mensagem = document.getElementById("mensagem").value;

      const texto = `
Olá! Gostaria de fazer uma encomenda na Maison Douceur. 🍰

*Nome:* ${nome}
*E-mail:* ${email}

*Pedido:* ${pedido}

*Detalhes:*
${mensagem}

Aguardo informações sobre valores e disponibilidade. 🤎
      `;

      const url =
        `https://wa.me/${whatsapp}?text=${encodeURIComponent(texto)}`;

      window.open(url, "_blank");

      this.reset();
    });

  // =========================
  // MODAL DE PRODUTOS
  // =========================

  const modal = document.getElementById("modal");
  const closeModal = document.getElementById("closeModal");
  const modalText = document.getElementById("modalText");

  let produtoSelecionado = "";

  document.querySelectorAll(".order-btn").forEach(button => {

    button.addEventListener("click", () => {

      produtoSelecionado =
        button.getAttribute("data-product");

      modalText.textContent =
        `Você escolheu: ${produtoSelecionado}. Preencha seus dados para solicitar um orçamento.`;

      modal.classList.add("active");

    });

  });

  // Fechar modal
  closeModal.addEventListener("click", () => {
    modal.classList.remove("active");
  });

  // Fechar clicando fora
  modal.addEventListener("click", event => {

    if (event.target === modal) {
      modal.classList.remove("active");
    }

  });

  // Enviar pedido do modal para WhatsApp
  document.getElementById("modalForm")
    .addEventListener("submit", function(event) {

      event.preventDefault();

      const nome = this.querySelector(
        'input[type="text"]'
      ).value;

      const telefone = this.querySelector(
        'input[type="tel"]'
      ).value;

      const texto = `
Olá! Gostaria de fazer uma encomenda. 🍰

*Produto:* ${produtoSelecionado}
*Nome:* ${nome}
*WhatsApp:* ${telefone}

Gostaria de receber informações sobre preço e disponibilidade. 🤎
      `;

      const url =
        `https://wa.me/${whatsapp}?text=${encodeURIComponent(texto)}`;

      window.open(url, "_blank");

      this.reset();
      modal.classList.remove("active");

    });

  // =========================
  // ANO AUTOMÁTICO
  // =========================

  document.getElementById("year").textContent =
    new Date().getFullYear();

  // =========================
  // MENU MOBILE
  // =========================

  const menuBtn = document.getElementById("menuBtn");
  const navLinks = document.getElementById("navLinks");

  menuBtn.addEventListener("click", () => {

    navLinks.classList.toggle("active");

    menuBtn.textContent =
      navLinks.classList.contains("active")
        ? "×"
        : "☰";

  });

  document.querySelectorAll(".nav-links a").forEach(link => {

    link.addEventListener("click", () => {

      navLinks.classList.remove("active");
      menuBtn.textContent = "☰";

    });

  });

  // =========================
  // ANIMAÇÃO
  // =========================

  const observer = new IntersectionObserver(
    entries => {

      entries.forEach(entry => {

        if (entry.isIntersecting) {

          entry.target.style.opacity = "1";
          entry.target.style.transform = "translateY(0)";

        }

      });

    },
    {
      threshold: 0.12
    }
  );

  document
    .querySelectorAll(".product, .feature, .about-text")
    .forEach(element => {

      element.style.opacity = "0";
      element.style.transform = "translateY(25px)";
      element.style.transition =
        "opacity .7s ease, transform .7s ease";

      observer.observe(element);

    });

</script>
```

 Agora, quando o cliente clicar em **“Encomendar”** ou enviar o formulário, o WhatsApp abrirá com a mensagem já preenchida e direcionada para **(81) 89181-775**.