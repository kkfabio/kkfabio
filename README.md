<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fábio Nascimento - Backend Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0D1B2A 0%, #1B263B 100%);
            color: #E0E1E7;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #0D1B2A 0%, #162B45 50%, #1B263B 100%);
            overflow: hidden;
        }

        .header-background {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 1;
        }

        .blob {
            position: absolute;
            border-radius: 50%;
            opacity: 0.1;
            animation: float 8s ease-in-out infinite;
        }

        .blob-1 {
            width: 300px;
            height: 300px;
            background: #0096D6;
            top: -50px;
            right: -50px;
            animation-delay: 0s;
        }

        .blob-2 {
            width: 250px;
            height: 250px;
            background: #6DB33F;
            bottom: -30px;
            left: -30px;
            animation-delay: 2s;
        }

        .blob-3 {
            width: 200px;
            height: 200px;
            background: #FF6B6B;
            top: 50%;
            left: 50%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(30px); }
        }

        .header-content {
            position: relative;
            z-index: 2;
            text-align: center;
            animation: slideUp 0.8s ease-out;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .profile-icon {
            width: 120px;
            height: 120px;
            margin: 0 auto 40px;
            background: linear-gradient(135deg, #0096D6 0%, #6DB33F 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 60px;
            animation: pulse 3s ease-in-out infinite;
            box-shadow: 0 20px 60px rgba(0, 150, 214, 0.3);
        }

        @keyframes pulse {
            0%, 100% { box-shadow: 0 20px 60px rgba(0, 150, 214, 0.3); }
            50% { box-shadow: 0 20px 80px rgba(0, 150, 214, 0.5); }
        }

        h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #0096D6 0%, #FFFFFF 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 700;
            letter-spacing: -1px;
        }

        .subtitle {
            font-size: 1.4rem;
            color: #0096D6;
            margin-bottom: 15px;
            font-weight: 500;
        }

        .location {
            font-size: 1rem;
            color: #B0C4DE;
            margin-bottom: 40px;
        }

        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .btn {
            padding: 14px 32px;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .btn-primary {
            background: linear-gradient(135deg, #0096D6 0%, #0073A8 100%);
            color: white;
            box-shadow: 0 10px 30px rgba(0, 150, 214, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(0, 150, 214, 0.5);
        }

        .btn-secondary {
            background: transparent;
            color: #0096D6;
            border: 2px solid #0096D6;
        }

        .btn-secondary:hover {
            background: #0096D6;
            color: #0D1B2A;
            transform: translateY(-3px);
        }

        section {
            padding: 80px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        section:last-of-type {
            border-bottom: none;
        }

        h2 {
            font-size: 2.5rem;
            margin-bottom: 50px;
            text-align: center;
            position: relative;
            display: inline-block;
            width: 100%;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, #0096D6 0%, #6DB33F 100%);
            border-radius: 2px;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
            margin-top: 50px;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #0096D6;
        }

        .about-text p {
            margin-bottom: 15px;
            color: #D0D1D7;
            line-height: 1.8;
        }

        .highlights {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
        }

        .highlight-item {
            background: rgba(0, 150, 214, 0.1);
            padding: 20px;
            border-radius: 8px;
            border-left: 4px solid #0096D6;
            transition: all 0.3s ease;
        }

        .highlight-item:hover {
            background: rgba(0, 150, 214, 0.15);
            transform: translateX(10px);
        }

        .highlight-item strong {
            color: #0096D6;
        }

        .tech-categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }

        .tech-category {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 12px;
            border: 1px solid rgba(0, 150, 214, 0.2);
            transition: all 0.3s ease;
        }

        .tech-category:hover {
            border-color: #0096D6;
            background: rgba(0, 150, 214, 0.1);
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 150, 214, 0.2);
        }

        .tech-category h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: #0096D6;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .tech-list {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .tech-tag {
            background: linear-gradient(135deg, #0096D6 0%, #0073A8 100%);
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s ease;
            cursor: default;
        }

        .tech-tag:hover {
            transform: scale(1.1);
            box-shadow: 0 5px 15px rgba(0, 150, 214, 0.4);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }

        .project-card {
            background: linear-gradient(135deg, rgba(13, 27, 42, 0.8) 0%, rgba(27, 38, 59, 0.8) 100%);
            border: 1px solid rgba(0, 150, 214, 0.2);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            border-color: #0096D6;
            box-shadow: 0 20px 50px rgba(0, 150, 214, 0.3);
            transform: translateY(-15px);
        }

        .project-header {
            background: linear-gradient(135deg, #0096D6 0%, #6DB33F 100%);
            padding: 20px;
            color: white;
        }

        .project-header h3 {
            font-size: 1.4rem;
            margin-bottom: 5px;
        }

        .project-tech {
            font-size: 0.85rem;
            opacity: 0.9;
        }

        .project-body {
            padding: 25px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .project-description {
            margin-bottom: 20px;
            color: #D0D1D7;
            font-size: 0.95rem;
            flex-grow: 1;
        }

        .project-features {
            list-style: none;
            margin-bottom: 20px;
        }

        .project-features li {
            padding: 8px 0;
            padding-left: 25px;
            position: relative;
            font-size: 0.9rem;
            color: #B0C4DE;
        }

        .project-features li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: #0096D6;
            font-weight: bold;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #0096D6;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            width: fit-content;
        }

        .project-link:hover {
            gap: 12px;
        }

        .learning-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
            margin-top: 50px;
        }

        .learning-item {
            background: rgba(0, 150, 214, 0.1);
            padding: 25px;
            border-radius: 8px;
            border: 1px solid rgba(0, 150, 214, 0.3);
            text-align: center;
            transition: all 0.3s ease;
        }

        .learning-item:hover {
            background: rgba(0, 150, 214, 0.2);
            border-color: #0096D6;
            transform: translateY(-10px);
        }

        .learning-item strong {
            display: block;
            color: #0096D6;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .learning-item p {
            font-size: 0.9rem;
            color: #B0C4DE;
        }

        .icon-small {
            width: 24px;
            height: 24px;
            display: inline-block;
        }

        footer {
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            background: rgba(13, 27, 42, 0.5);
        }

        .social-links {
            display: flex;
            gap: 25px;
            justify-content: center;
            margin-bottom: 30px;
        }

        .social-link {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, #0096D6 0%, #6DB33F 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            color: white;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 150, 214, 0.2);
        }

        .social-link:hover {
            transform: translateY(-5px) scale(1.1);
            box-shadow: 0 10px 25px rgba(0, 150, 214, 0.4);
        }

        .social-link svg {
            width: 24px;
            height: 24px;
        }

        .footer-text {
            color: #B0C4DE;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }

            .subtitle {
                font-size: 1.1rem;
            }

            .about-grid {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .highlights {
                grid-template-columns: 1fr;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .btn {
                width: 100%;
                justify-content: center;
            }

            section {
                padding: 50px 0;
            }

            h2 {
                font-size: 1.8rem;
            }

            .tech-categories {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="header-background">
            <div class="blob blob-1"></div>
            <div class="blob blob-2"></div>
            <div class="blob blob-3"></div>
        </div>
        <div class="header-content">
            <div class="profile-icon">
                <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg" style="width: 80px; height: 80px;">
                    <circle cx="50" cy="35" r="20" fill="white"/>
                    <path d="M 20 70 Q 20 55 50 55 Q 80 55 80 70 L 80 85 Q 80 90 75 90 L 25 90 Q 20 90 20 85 Z" fill="white"/>
                </svg>
            </div>
            <h1>FÁBIO NASCIMENTO</h1>
            <p class="subtitle">Backend Developer</p>
            <p class="location">Java • Spring Boot • PostgreSQL</p>
            <p class="location">Recife, PE • Brasil</p>
            <div class="cta-buttons">
                <a href="#projects" class="btn btn-primary">Ver Projetos</a>
                <a href="#contact" class="btn btn-secondary">Entre em Contato</a>
            </div>
        </div>
    </header>

    <section id="about">
        <div class="container">
            <h2>Sobre Mim</h2>
            <div class="about-grid">
                <div class="about-text">
                    <h3>Desenvolvedor Backend com Foco em Performance</h3>
                    <p>Sou estagiário em desenvolvimento de software na ADEERE Comunicações, com especialização em backend Java e Spring Boot. Trabalho no desenvolvimento de aplicações web robustas, APIs REST de alta performance e sistemas de automação de processos.</p>
                    <p>Minha abordagem combina excelência técnica com boas práticas de desenvolvimento, sempre buscando otimização e arquitetura escalável. Atualmente cursando Análise e Desenvolvimento de Sistemas (ADS) na FICR.</p>
                </div>
                <div class="highlights">
                    <div class="highlight-item">
                        <strong>Especialidade</strong>
                        <p>APIs REST • Backend • Otimização</p>
                    </div>
                    <div class="highlight-item">
                        <strong>Empresa</strong>
                        <p>ADEERE Comunicações</p>
                    </div>
                    <div class="highlight-item">
                        <strong>Estudo</strong>
                        <p>ADS • FICR (2025–2027)</p>
                    </div>
                    <div class="highlight-item">
                        <strong>Realização</strong>
                        <p>Melhoria de 40% em performance</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="tech">
        <div class="container">
            <h2>Stack Técnico</h2>
            <div class="tech-categories">
                <div class="tech-category">
                    <h3>
                        <svg class="icon-small" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon>
                        </svg>
                        Backend
                    </h3>
                    <div class="tech-list">
                        <span class="tech-tag">Java</span>
                        <span class="tech-tag">Spring Boot</span>
                        <span class="tech-tag">Spring Security</span>
                        <span class="tech-tag">JWT</span>
                        <span class="tech-tag">JPA/Hibernate</span>
                        <span class="tech-tag">REST APIs</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>
                        <svg class="icon-small" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm3.5-9c.83 0 1.5-.67 1.5-1.5S16.33 8 15.5 8 14 8.67 14 9.5s.67 1.5 1.5 1.5zm-7 0c.83 0 1.5-.67 1.5-1.5S9.33 8 8.5 8 7 8.67 7 9.5 7.67 11 8.5 11zm3.5 6.5c2.33 0 4.31-1.46 5.11-3.5H6.89c.8 2.04 2.78 3.5 5.11 3.5z"></path>
                        </svg>
                        Frontend
                    </h3>
                    <div class="tech-list">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">TypeScript</span>
                        <span class="tech-tag">JavaScript</span>
                        <span class="tech-tag">Tailwind CSS</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>
                        <svg class="icon-small" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <ellipse cx="12" cy="5" rx="9" ry="3"></ellipse>
                            <path d="M3 5v14a9 3 0 0 0 18 0V5"></path>
                            <path d="M3 12a9 3 0 0 0 18 0"></path>
                        </svg>
                        Data & Infrastructure
                    </h3>
                    <div class="tech-list">
                        <span class="tech-tag">PostgreSQL</span>
                        <span class="tech-tag">SQL Server</span>
                        <span class="tech-tag">Docker</span>
                        <span class="tech-tag">Git</span>
                        <span class="tech-tag">GitHub Actions</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <h2>Projetos em Destaque</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-header">
                        <h3>PedidoFácil</h3>
                        <p class="project-tech">Spring Boot • React • PostgreSQL</p>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Sistema de gestão de pedidos completo com autenticação JWT, modelagem relacional avançada e testes abrangentes. Aplicação fullstack em produção.</p>
                        <ul class="project-features">
                            <li>API REST com autenticação JWT</li>
                            <li>Design Patterns aplicados</li>
                            <li>Testes unitários (JUnit 5)</li>
                            <li>Autenticação e segurança</li>
                        </ul>
                        <a href="#" class="project-link">Acessar Repositório →</a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <h3>Universidade Heineken</h3>
                        <p class="project-tech">Spring Boot • Next.js • PostgreSQL</p>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Plataforma corporativa de e-learning com arquitetura fullstack, integração de conteúdos interativos e pipeline CI/CD automatizado.</p>
                        <ul class="project-features">
                            <li>Autenticação segura</li>
                            <li>CI/CD com GitHub Actions</li>
                            <li>Deploy em cloud</li>
                            <li>Design Patterns avançados</li>
                        </ul>
                        <a href="#" class="project-link">Acessar Repositório →</a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-header">
                        <h3>Meets Pageflow</h3>
                        <p class="project-tech">API REST • Arquitetura • Dados</p>
                    </div>
                    <div class="project-body">
                        <p class="project-description">Projeto acadêmico da Residência em Software e IA. Líder técnico da API, tratamento de falhas e definição de contratos de dados.</p>
                        <ul class="project-features">
                            <li>Arquitetura de software</li>
                            <li>Tratamento de erros</li>
                            <li>Contratos de API</li>
                            <li>Liderança técnica</li>
                        </ul>
                        <a href="#" class="project-link">Acessar Repositório →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="learning">
        <div class="container">
            <h2>Aprendizado Contínuo</h2>
            <div class="learning-grid">
                <div class="learning-item">
                    <strong>Arquitetura de Software</strong>
                    <p>Padrões e princípios de design avançados</p>
                </div>
                <div class="learning-item">
                    <strong>Otimização de Performance</strong>
                    <p>Análise de planos SQL e tunning</p>
                </div>
                <div class="learning-item">
                    <strong>Clean Code</strong>
                    <p>SOLID Principles e boas práticas</p>
                </div>
                <div class="learning-item">
                    <strong>Test-Driven Development</strong>
                    <p>Cobertura de testes e qualidade</p>
                </div>
                <div class="learning-item">
                    <strong>Containerização</strong>
                    <p>Docker e orquestração</p>
                </div>
                <div class="learning-item">
                    <strong>DevOps</strong>
                    <p>CI/CD e deploy automatizado</p>
                </div>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div class="container">
            <h2 style="margin-bottom: 40px;">Vamos nos Conectar</h2>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/fabio-nascimento-nunes/" class="social-link" title="LinkedIn">
                    <svg viewBox="0 0 24 24" fill="currentColor">
                        <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.475-2.236-1.986-2.236-1.081 0-1.722.722-2.002 1.413-.103.249-.129.597-.129.946v5.446h-3.554s.05-8.836 0-9.754h3.554v1.391c.433-.669 1.206-1.622 2.929-1.622 2.142 0 3.742 1.398 3.742 4.402v5.583zM5.337 9.432c-1.144 0-1.915-.759-1.915-1.71 0-.955.769-1.71 1.959-1.71 1.188 0 1.913.759 1.932 1.71 0 .951-.744 1.71-1.976 1.71zm1.581 11.02H3.757V9.678h3.161v10.774zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.225 0z"/>
                    </svg>
                </a>
                <a href="https://github.com/kkfabio" class="social-link" title="GitHub">
                    <svg viewBox="0 0 24 24" fill="currentColor">
                        <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v 3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                    </svg>
                </a>
                <a href="mailto:fabionascfilho@gmail.com" class="social-link" title="Email">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                        <rect x="2" y="4" width="20" height="16" rx="2"></rect>
                        <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"></path>
                    </svg>
                </a>
                <a href="https://wa.me/5581988177227" class="social-link" title="WhatsApp">
                    <svg viewBox="0 0 24 24" fill="currentColor">
                        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.67-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.076 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421-7.403h-.004a8.06 8.06 0 0 0-8.062 8.062c0 4.44 3.62 8.06 8.062 8.06h.031a8.062 8.062 0 0 0 8.062-8.062c0-4.44-3.622-8.06-8.062-8.06m0-1.053c4.527 0 8.236 3.71 8.236 8.262 0 4.55-3.709 8.262-8.236 8.262-4.528 0-8.236-3.712-8.236-8.262 0-4.552 3.708-8.262 8.236-8.262"/>
                    </svg>
                </a>
            </div>
            <p class="footer-text">Desenvolvido com excelência técnica • Recife, PE • 2026</p>
        </div>
    </footer>
</body>
</html>
