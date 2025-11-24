import React, { useState } from "react";

function App() {
  const [user, setUser] = useState(null);
  const [emailInput, setEmailInput] = useState("");
  const [relatos, setRelatos] = useState([]);
  const [form, setForm] = useState({
    tipo: "",
    data: "",
    local: "",
    envolvidos: "",
    descricao: "",
  });

  function login() {
    if (emailInput.trim()) {
      setUser(emailInput.trim());
    } else {
      alert("Digite um e-mail válido");
    }
  }

  function logout() {
    setUser(null);
    setEmailInput("");
    setForm({
      tipo: "",
      data: "",
      local: "",
      envolvidos: "",
      descricao: "",
    });
  }

  function handleFormChange(e) {
    setForm({ ...form, [e.target.name]: e.target.value });
  }

  function enviarRelato() {
    if (
      form.tipo &&
      form.data &&
      form.local &&
      form.envolvidos &&
      form.descricao
    ) {
      setRelatos([...relatos, { ...form, id: Date.now() }]);
      alert("Relato enviado com sucesso!");
      setForm({
        tipo: "",
        data: "",
        local: "",
        envolvidos: "",
        descricao: "",
      });
    } else {
      alert("Preencha todos os campos do formulário.");
    }
  }

  if (!user) {
    return (
      <div style={{ padding: 20 }}>
        <h2>Login - VozEscolar</h2>
        <input
          type="email"
          value={emailInput}
          onChange={(e) => setEmailInput(e.target.value)}
          placeholder="Digite seu e-mail"
          style={{ padding: "8px", width: "250px" }}
        />
        <button onClick={login} style={{ marginLeft: 10, padding: "8px" }}>
          Entrar
        </button>
      </div>
    );
  }

  return (
    <div style={{ maxWidth: 600, margin: "20px auto", fontFamily: "Arial" }}>
      <header style={{ marginBottom: 20 }}>
        <h1>Bem-vindo, {user}</h1>
        <button onClick={logout}>Sair</button>
      </header>

      <section>
        <h2>Enviar Relato</h2>
        <div>
          <label>Tipo de Bullying:</label>
          <select name="tipo" value={form.tipo} onChange={handleFormChange}>
            <option value="">Selecione</option>
            <option value="Físico">Físico</option>
            <option value="Psicológico">Psicológico</option>
            <option value="Verbal">Verbal</option>
            <option value="Virtual">Virtual</option>
          </select>
        </div>

        <div>
          <label>Data e hora:</label>
          <input
            type="datetime-local"
            name="data"
            value={form.data}
            onChange={handleFormChange}
          />
        </div>

        <div>
          <label>Local:</label>
          <input
            type="text"
            name="local"
            value={form.local}
            onChange={handleFormChange}
          />
        </div>

        <div>
          <label>Pessoas envolvidas:</label>
          <input
            type="text"
            name="envolvidos"
            value={form.envolvidos}
            onChange={handleFormChange}
          />
        </div>

        <div>
          <label>Descrição:</label>
          <textarea
            name="descricao"
            value={form.descricao}
            onChange={handleFormChange}
          />
        </div>

        <button onClick={enviarRelato} style={{ marginTop: 10 }}>
          Enviar
        </button>
      </section>

      <section>
        <h2>Relatos enviados</h2>
        {relatos.length === 0 && <p>Nenhum relato enviado ainda.</p>}
        {relatos.map((r) => (
          <div key={r.id} style={{ border: "1px solid #ddd", marginTop: 10, padding: 10 }}>
            <strong>Tipo:</strong> {r.tipo} <br />
            <strong>Data:</strong> {r.data} <br />
            <strong>Local:</strong> {r.local} <br />
            <strong>Envolvidos:</strong> {r.envolvidos} <br />
            <strong>Descrição:</strong> {r.descricao}
          </div>
        ))}
      </section>
    </div>
  );
}

export default App;
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
