# Vozescolarsp
Aplicativo para combater o bullying nas escolas
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>VozEscolar - Denúncias Anônimas e Seguras</title>
  <style>
    body { font-family: Arial, sans-serif; margin:0; padding:0; background:#f9f9f9; color:#333; }
    header { background:#2a6ebb; color:#fff; padding:15px 20px; display:flex; justify-content:space-between; align-items:center; }
    header h1 { margin:0; font-size:1.5em; }
    nav a { color:#fff; text-decoration:none; margin-left:20px; font-weight:bold; }
    nav a:hover { text-decoration:underline; }

    main { padding:20px; max-width:900px; margin:auto; }

    section { margin-bottom:50px; }

    h2 { color:#2a6ebb; margin-bottom:15px; border-bottom:2px solid #2a6ebb; padding-bottom:5px; }

    button { background:#2a6ebb; color:#fff; border:none; padding:12px 25px; font-size:1em; cursor:pointer; border-radius:5px; }
    button:hover { background:#1c4e87; }

    .highlight { background:#e8f0fe; padding:15px; border-left:5px solid #2a6ebb; margin-bottom:25px; }

    form label { display:block; margin-top:15px; font-weight:bold; }
    form input, form textarea { width:100%; padding:10px; margin-top:5px; border:1px solid #ccc; border-radius:4px; }
    form textarea { resize:vertical; height:100px; }

    footer { background:#222; color:#ccc; text-align:center; padding:20px; font-size:0.9em; }
    footer a { color:#ccc; text-decoration:none; margin:0 5px; }
  </style>
</head>
<body>

<header>
  <h1>VozEscolar</h1>
  <nav>
    <a href="#home">Início</a>
    <a href="#sobre">Sobre</a>
    <a href="#funciona">Como Funciona</a>
    <a href="#seguranca">Segurança</a>
    <a href="#contato">Contato</a>
  </nav>
</header>

<main>

  <section id="home">
    <h2>VozEscolar — Sua voz segura contra o bullying e abusos na escola</h2>
    <p class="highlight">Relate com anonimato, segurança e apoio confiável para proteger a comunidade escolar.</p>
    <button onclick="window.location.href='#contato'">Enviar um relato</button>
  </section>

  <section id="sobre">
    <h2>Sobre Nós</h2>
    <p><strong>Missão:</strong> Dar voz e proteção segura a estudantes e comunidade escolar para relatar violações e garantir responsabilidade.</p>
    <p><strong>Visão:</strong> Escolas mais seguras e justas, apoiadas por tecnologia, transparência e ação efetiva.</p>
  </section>

  <section id="funciona">
    <h2>Como Funciona</h2>
    <ul>
      <li><strong>Cadastro Seguro:</strong> Login via e-mail, telefone e documentação escolar com criptografia.</li>
      <li><strong>Envio de Relatos:</strong> Formulário simples para informar tipo do incidente, provas e testemunhas.</li>
      <li><strong>Triagem Inteligente:</strong> IA prioriza casos urgentes e equipe humana revisa os relatos.</li>
      <li><strong>Relatórios Oficiais:</strong> Consolidação para secretarias e autoridades com protocolo.</li>
      <li><strong>Acompanhamento:</strong> Token seguro para seguir o andamento do caso anonimamente.</li>
    </ul>
  </section>

  <section id="seguranca">
    <h2>Segurança e Privacidade</h2>
    <p>Anônimo e seguro com criptografia ponta a ponta. Proteção contra fraudes e conformidade com a LGPD para garantir a privacidade dos usuários.</p>
  </section>

  <section id="contato">
    <h2>Contato</h2>
    <form>
      <label for="nome">Nome</label>
      <input type="text" id="nome" name="nome" placeholder="Seu nome" />

      <label for="email">E-mail</label>
      <input type="email" id="email" name="email" placeholder="Seu e-mail" />

      <label for="mensagem">Mensagem</label>
      <textarea id="mensagem" name="mensagem" placeholder="Escreva sua mensagem aqui"></textarea>

      <button type="submit">Enviar</button>
    </form>
  </section>

</main>

<footer>
  <p>&copy; 2025 VozEscolar - Todos os direitos reservados.</p>
  <p><a href="#home">Início</a> | <a href="#sobre">Sobre</a> | <a href="#seguranca">Segurança</a> | <a href="#contato">Contato</a></p>
</footer>

</body>
</html>
