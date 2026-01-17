<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfólio Profissional | Fabricio Porto Rocha</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
    
    <style>
        :root {
            /* Paleta de Cores Premium */
            --bg-body: #0f172a;
            --primary: #3b82f6; /* Azul moderno */
            --primary-dark: #1d4ed8;
            --accent: #0ea5e9; /* Ciano para detalhes */
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --card-bg: rgba(30, 41, 59, 0.7);
            --card-border: rgba(255, 255, 255, 0.1);
            --glass-shine: rgba(255, 255, 255, 0.05);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-body);
            background-image: 
                radial-gradient(circle at 10% 20%, rgba(59, 130, 246, 0.15) 0%, transparent 20%),
                radial-gradient(circle at 90% 80%, rgba(14, 165, 233, 0.15) 0%, transparent 20%);
            color: var(--text-main);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* --- Tipografia e Elementos Globais --- */
        h1, h2, h3 {
            font-weight: 800;
            letter-spacing: -0.5px;
        }

        .section-header {
            text-align: center;
            margin-bottom: 4rem;
        }

    .section-header h2 {
    font-size: 2.5rem;
    background: linear-gradient(to right, #ffffff, #94a3b8);
    background-clip: text;              /* padrão */
    -webkit-background-clip: text;      /* WebKit */
    color: transparent;                 /* padrão */
    -webkit-text-fill-color: transparent; /* WebKit */
    margin-bottom: 1rem;
}


        .section-header p {
            color: var(--text-muted);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- Header Fixo --- */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 1.2rem 0;
            background: rgba(15, 23, 42, 0.85);
            backdrop-filter: blur(12px);
            z-index: 1000;
            border-bottom: 1px solid var(--card-border);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--text-main);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i { color: var(--primary); }

        .nav-menu {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-menu a {
            color: var(--text-muted);
            text-decoration: none;
            font-weight: 500;
            transition: 0.3s;
            position: relative;
        }

        .nav-menu a:hover, .nav-menu a.active {
            color: var(--text-main);
        }

        .nav-menu a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: var(--primary);
            transition: 0.3s;
        }

        .nav-menu a:hover::after { width: 100%; }

        /* --- Hero Section --- */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 80px;
            position: relative;
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 4rem;
            align-items: center;
        }

        /* --- ESTILO ADICIONADO PARA A FOTO DE PERFIL --- */
        .profile-photo {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--primary);
            box-shadow: 0 0 25px rgba(59, 130, 246, 0.4);
            margin-bottom: 2rem;
            display: block;
        }

        .hero-text h1 {
            font-size: 4rem;
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero-text .highlight {
            color: var(--primary);
            background: linear-gradient(120deg, rgba(59, 130, 246, 0.2) 0%, transparent 100%);
            padding: 0 10px;
            border-radius: 8px;
        }

        .hero-role {
            font-size: 1.5rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
            font-weight: 600;
            display: inline-block;
            background: rgba(14, 165, 233, 0.1);
            padding: 5px 15px;
            border-radius: 50px;
            border: 1px solid rgba(14, 165, 233, 0.2);
        }

        .hero-desc {
            font-size: 1.1rem;
            color: var(--text-muted);
            margin-bottom: 2.5rem;
            max-width: 90%;
        }

        .cta-group {
            display: flex;
            gap: 1rem;
        }

        .btn {
            padding: 12px 30px;
            border-radius: 8px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
            box-shadow: 0 4px 15px rgba(59, 130, 246, 0.4);
        }

        .btn-primary:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
        }

        .btn-outline {
            border: 1px solid var(--card-border);
            color: var(--text-main);
            background: rgba(255,255,255,0.05);
        }

        .btn-outline:hover {
            border-color: var(--text-main);
            background: rgba(255,255,255,0.1);
        }

        /* Stats Card (Hero Visual) */
        .hero-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
        }

        .stat-card {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            padding: 2rem;
            border-radius: 16px;
            text-align: center;
            backdrop-filter: blur(10px);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 0.5rem;
            display: block;
        }

        .stat-label {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* --- Timeline (Experiência) --- */
        #experience { padding: 6rem 0; }

        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 2px;
            background: linear-gradient(to bottom, var(--primary), transparent);
        }

        .timeline-item {
            margin-left: 2rem;
            margin-bottom: 3rem;
            position: relative;
        }

        .timeline-dot {
            position: absolute;
            left: -2.6rem;
            top: 0.5rem;
            width: 20px;
            height: 20px;
            background: var(--bg-body);
            border: 4px solid var(--primary);
            border-radius: 50%;
            box-shadow: 0 0 10px rgba(59, 130, 246, 0.5);
        }

        .job-card {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            padding: 2rem;
            border-radius: 12px;
            transition: 0.3s;
        }

        .job-card:hover {
            transform: translateX(10px);
            border-color: var(--primary);
        }

        .job-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1rem;
            flex-wrap: wrap;
            gap: 10px;
        }

        .job-title { color: var(--text-main); font-size: 1.25rem; }
        .job-company { color: var(--accent); font-weight: 600; }
        .job-date { 
            background: rgba(255,255,255,0.1); 
            padding: 4px 10px; 
            border-radius: 4px; 
            font-size: 0.8rem; 
        }

        /* --- Certifications Grid --- */
        #certifications { padding: 6rem 0; background: rgba(0,0,0,0.2); }

        .cert-filters {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 3rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            background: transparent;
            border: 1px solid var(--card-border);
            color: var(--text-muted);
            padding: 8px 20px;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.3s;
        }

        .filter-btn:hover, .filter-btn.active {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .cert-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 20px;
        }

        .cert-card {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            padding: 1.5rem;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            height: 100%;
        }

        .cert-card::before {
            content: '';
            position: absolute;
            top: 0; left: 0; width: 100%; height: 4px;
            background: var(--card-border);
            transition: 0.3s;
        }

        .cert-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            border-color: rgba(255,255,255,0.2);
        }

        .cert-card.data:hover::before { background: var(--primary); }
        .cert-card.corp:hover::before { background: #10b981; }
        .cert-card.tech:hover::before { background: #f59e0b; }
        .cert-card.ops:hover::before { background: #8b5cf6; }

        .cert-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--text-muted);
        }

        .cert-title {
            font-size: 1.1rem;
            margin-bottom: 0.5rem;
            font-weight: 700;
        }

        .cert-issuer {
            font-size: 0.9rem;
            color: var(--text-muted);
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .cert-tag {
            font-size: 0.75rem;
            padding: 4px 8px;
            border-radius: 4px;
            margin-top: 1rem;
            align-self: flex-start;
            background: rgba(255,255,255,0.05);
            color: var(--text-muted);
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* --- Footer --- */
        footer {
            padding: 4rem 0 2rem;
            text-align: center;
            border-top: 1px solid var(--card-border);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .social-links a {
            color: var(--text-muted);
            font-size: 1.5rem;
            transition: 0.3s;
        }

        .social-links a:hover {
            color: var(--primary);
            transform: scale(1.1);
        }

        /* --- Responsivo --- */
        @media (max-width: 968px) {
            .hero-grid { grid-template-columns: 1fr; text-align: center; }
            
            /* Ajuste para centralizar a foto no mobile */
            .profile-photo { margin: 0 auto 2rem auto; }
            
            .hero-text h1 { font-size: 3rem; }
            .hero-stats { display: none; }
            .cta-group { justify-content: center; }
            .timeline::before { left: -10px; }
            .timeline-item { margin-left: 1rem; }
            .timeline-dot { left: -1.45rem; width: 15px; height: 15px; }
            .nav-menu { display: none; } /* Mobile menu simplified */
        }
    </style>
</head>
<body>

    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <i class="fas fa-chart-network"></i> Fabricio P. Rocha
                </div>
                <ul class="nav-menu">
                    <li><a href="#home" class="active">Início</a></li>
                    <li><a href="#skills">Habilidades</a></li>
                    <li><a href="#experience">Experiência</a></li>
                    <li><a href="#certifications">Certificados</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="container hero-grid">
            <div class="hero-text">
                
                <img src="Imagens/Eu.jpg" alt="Fabricio Porto Rocha" class="profile-photo">

                <span class="hero-role">Analista de Planejamento</span>
                <h1>Transformando dados em <span class="highlight">estratégia</span></h1>
                <p class="hero-desc">
                    Profissional com sólida trajetória no Grupo Casas Bahia. Especialista em Power BI, Excel Intermediário e gestão de processos, conectando a operação logística à inteligência de negócios.
                </p>
                <div class="cta-group">
                    <a href="#experience" class="btn btn-primary">Ver Trajetória</a>
                    <a href="https://www.linkedin.com/in/fabr%C3%ADcio-porto-356a87130/" target="_blank" class="btn btn-outline">
                        <i class="fab fa-linkedin"></i> LinkedIn
                    </a>
                </div>
            </div>
            
            <div class="hero-stats">
                <div class="stat-card">
                    <span class="stat-number">15+</span>
                    <span class="stat-label">Anos de Experiência</span>
                </div>
                <div class="stat-card">
                    <span class="stat-number">13</span>
                    <span class="stat-label">Certificações</span>
                </div>
                <div class="stat-card">
                    <span class="stat-number">BI</span>
                    <span class="stat-label">Especialista</span>
                </div>
                <div class="stat-card">
                    <span class="stat-number">SP</span>
                    <span class="stat-label">Jundiaí - Base</span>
                </div>
            </div>
        </div>
    </section>

    <section id="skills" style="padding: 4rem 0;">
        <div class="container">
            <div class="section-header">
                <h2>Competências Técnicas</h2>
            </div>
            <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px;">
                <span style="background: rgba(59,130,246,0.1); color: #60a5fa; padding: 10px 20px; border-radius: 50px; font-weight: 600;">Power BI</span>
                <span style="background: rgba(59,130,246,0.1); color: #60a5fa; padding: 10px 20px; border-radius: 50px; font-weight: 600;">Excel Intermediário</span>
                <span style="background: rgba(59,130,246,0.1); color: #60a5fa; padding: 10px 20px; border-radius: 50px; font-weight: 600;">DAX</span>
                <span style="background: rgba(59,130,246,0.1); color: #60a5fa; padding: 10px 20px; border-radius: 50px; font-weight: 600;">Sharepoint</span>
                <span style="background: rgba(255,255,255,0.05); color: #94a3b8; padding: 10px 20px; border-radius: 50px;">Logística Reversa</span>
                <span style="background: rgba(255,255,255,0.05); color: #94a3b8; padding: 10px 20px; border-radius: 50px;">Gestão de Equipe</span>
                <span style="background: rgba(255,255,255,0.05); color: #94a3b8; padding: 10px 20px; border-radius: 50px;">Análise de Avarias</span>
            </div>
        </div>
    </section>

    <section id="experience">
        <div class="container">
            <div class="section-header">
                <h2>Minha Jornada</h2>
                <p>Uma história de crescimento contínuo e dedicação.</p>
            </div>
            
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="job-card">
                        <div class="job-header">
                            <div>
                                <h3 class="job-title">Analista de Planejamento</h3>
                                <span class="job-company">Grupo Casas Bahia</span>
                            </div>
                            <span class="job-date">Mai 2024 - Presente</span>
                        </div>
                        <p style="color: var(--text-muted)">Foco estratégico em análise de dados, planejamento operacional e suporte à tomada de decisão utilizando BI.</p>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="job-card">
                        <div class="job-header">
                            <div>
                                <h3 class="job-title">Inspetor de Mercadorias</h3>
                                <span class="job-company">Grupo Casas Bahia (Via Varejo)</span>
                            </div>
                            <span class="job-date">Jan 2018 - Mai 2024</span>
                        </div>
                        <p style="color: var(--text-muted)">6 anos de experiência em Pós-Vendas (Linha Branca), desenvolvendo análise técnica e liderança de equipe.</p>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="job-card">
                        <div class="job-header">
                            <div>
                                <h3 class="job-title">Ajudante Interno</h3>
                                <span class="job-company">Grupo Casas Bahia</span>
                            </div>
                            <span class="job-date">Ago 2014 - Out 2017</span>
                        </div>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="job-card">
                        <div class="job-header">
                            <div>
                                <h3 class="job-title">Ajudante de Cozinha</h3>
                                <span class="job-company">Setor Alimentício</span>
                            </div>
                            <span class="job-date">Set 2011 - Ago 2014</span>
                        </div>
                        <p style="color: var(--text-muted)">Experiência em preparação e organização em ambiente de cozinha, desenvolvendo disciplina e trabalho em equipe.</p>
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <div class="job-card">
                        <div class="job-header">
                            <div>
                                <h3 class="job-title">Operador de Caixa</h3>
                                <span class="job-company">Barra Doce</span>
                            </div>
                            <span class="job-date">Jan 2008 - Fev 2010</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="certifications">
        <div class="container">
            <div class="section-header">
                <h2>Certificações & Cursos</h2>
                <p>Aprendizado contínuo para entregar melhores resultados.</p>
            </div>

            <div class="cert-filters">
                <button class="filter-btn active">Todos</button>
                <button class="filter-btn">Dados & BI</button>
                <button class="filter-btn">Gestão & Ética</button>
                <button class="filter-btn">Operacional</button>
            </div>

            <div class="cert-grid">
                
                <div class="cert-card data">
                    <div>
                        <i class="fas fa-database cert-icon" style="color: #f59e0b;"></i>
                        <h3 class="cert-title">Microsoft Power BI para Business Intelligence e Data Science</h3>
                        <div class="cert-issuer"><i class="fas fa-university"></i> Data Science Academy</div>
                    </div>
                    <span class="cert-tag">Out 2024</span>
                </div>

                <div class="cert-card data">
                    <div>
                        <i class="fas fa-chart-pie cert-icon" style="color: #f59e0b;"></i>
                        <h3 class="cert-title">Master Power BI De A à Z</h3>
                        <div class="cert-issuer"><i class="fas fa-laptop-code"></i> Udemy</div>
                    </div>
                    <span class="cert-tag">Completo</span>
                </div>

                <div class="cert-card data">
                    <div>
                        <i class="fas fa-bolt cert-icon" style="color: #f59e0b;"></i>
                        <h3 class="cert-title">Minicurso de Power BI</h3>
                        <div class="cert-issuer"><i class="fas fa-building"></i> Xperiun | Data Analytics</div>
                    </div>
                    <span class="cert-tag">Dez 2023</span>
                </div>

                <div class="cert-card data">
                    <div>
                        <i class="fas fa-chart-line cert-icon" style="color: #0ea5e9;"></i>
                        <h3 class="cert-title">Power BI - Do Básico ao Avançado</h3>
                        <div class="cert-issuer"><i class="fas fa-building"></i> Grupo Casas Bahia</div>
                    </div>
                    <span class="cert-tag">Jun 2022</span>
                </div>

                <div class="cert-card data">
                    <div>
                        <i class="fas fa-file-excel cert-icon" style="color: #10b981;"></i>
                        <h3 class="cert-title">Excel 2013 Intermediário</h3>
                        <div class="cert-issuer"><i class="fas fa-university"></i> Fundação Bradesco</div>
                    </div>
                    <span class="cert-tag">Set 2019</span>
                </div>

                <div class="cert-card tech">
                    <div>
                        <i class="fab fa-microsoft cert-icon" style="color: #0ea5e9;"></i>
                        <h3 class="cert-title">Sharepoint</h3>
                        <div class="cert-issuer"><i class="fas fa-university"></i> Fundação Bradesco</div>
                    </div>
                    <span class="cert-tag">Jul 2022</span>
                </div>

                <div class="cert-card tech">
                    <div>
                        <i class="fas fa-shopping-cart cert-icon" style="color: #8b5cf6;"></i>
                        <h3 class="cert-title">Como construir uma loja virtual</h3>
                        <div class="cert-issuer"><i class="fas fa-building"></i> Sebrae</div>
                    </div>
                    <span class="cert-tag">E-commerce</span>
                </div>

                <div class="cert-card tech">
                    <div>
                        <i class="fas fa-video cert-icon" style="color: #ef4444;"></i>
                        <h3 class="cert-title">Curso em Vídeo</h3>
                        <div class="cert-issuer"><i class="fas fa-building"></i> Digirati Informática</div>
                    </div>
                    <span class="cert-tag">Jan 2022</span>
                </div>

                <div class="cert-card ops">
                    <div>
                        <i class="fas fa-truck-loading cert-icon" style="color: #f97316;"></i>
                        <h3 class="cert-title">Logística Reversa</h3>
                        <div class="cert-issuer"><i class="fas fa-university"></i> Faculdade Sul Mineira</div>
                    </div>
                    <span class="cert-tag">Logística</span>
                </div>

                <div class="cert-card ops">
                    <div>
                        <i class="fas fa-box-open cert-icon" style="color: #f97316;"></i>
                        <h3 class="cert-title">Avarias</h3>
                        <div class="cert-issuer"><i class="fas fa-building"></i> CrossKnowledge</div>
                    </div>
                    <span class="cert-tag">Fev 2019</span>
                </div>

                <div class="cert-card corp">
                    <div>
                        <i class="fas fa-comments cert-icon" style="color: #ec4899;"></i>
                        <h3 class="cert-title">Técnicas de Feedback</h3>
                        <div class="cert-issuer"><i class="fas fa-building"></i> CrossKnowledge</div>
                    </div>
                    <span class="cert-tag">Jul 2019</span>
                </div>

                <div class="cert-card corp">
                    <div>
                        <i class="fas fa-balance-scale cert-icon" style="color: #94a3b8;"></i>
                        <h3 class="cert-title">Código de Conduta Ética</h3>
                        <div class="cert-issuer"><i class="fas fa-building"></i> Grupo Casas Bahia</div>
                    </div>
                    <span class="cert-tag">Compliance</span>
                </div>
                
                 <div class="cert-card corp">
                    <div>
                        <i class="fas fa-user-shield cert-icon" style="color: #94a3b8;"></i>
                        <h3 class="cert-title">Código de Conduta Ética</h3>
                        <div class="cert-issuer"><i class="fas fa-building"></i> CrossKnowledge</div>
                    </div>
                    <span class="cert-tag">Compliance</span>
                </div>

            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="social-links">
                <a href="https://www.linkedin.com/in/fabr%C3%ADcio-porto-356a87130/" target="_blank"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fas fa-envelope"></i></a>
                <a href="#"><i class="fab fa-whatsapp"></i></a>
            </div>
            <p>&copy; 2026 Fabricio Porto Rocha. Todos os direitos reservados.</p>
        </div>
    </footer>

    <script>
        // Script simples para revelar elementos ao rolar (Scroll Reveal)
        window.addEventListener('scroll', reveal);

        function reveal(){
            var reveals = document.querySelectorAll('.timeline-item, .cert-card');

            for(var i = 0; i < reveals.length; i++){
                var windowheight = window.innerHeight;
                var revealtop = reveals[i].getBoundingClientRect().top;
                var revealpoint = 100;

                if(revealtop < windowheight - revealpoint){
                    reveals[i].style.opacity = "1";
                    reveals[i].style.transform = "translateY(0)";
                }
            }
        }
        
        // Inicializar estilos para animação
        document.querySelectorAll('.timeline-item, .cert-card').forEach(el => {
            el.style.opacity = "0";
            el.style.transform = "translateY(30px)";
            el.style.transition = "all 0.6s ease";
        });
        
        // Rodar uma vez no load
        reveal();
    </script>
</body>
</html>
