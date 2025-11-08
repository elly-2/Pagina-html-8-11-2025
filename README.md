# Pagina-html-8-11-2025
Uma pagina de currículo feito em html,css e js 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8"/>
  <meta name="viewport" content="width=device-width,initial-scale=1"/>
  <title>Currículo - Monyelly</title>
  
  <link rel="stylesheet" href="/Styles.css" />
</head>
<body>
  <div class="container">
    <div class="card" role="main">
      <aside class="left" aria-label="coluna lateral">
        <div class="profile">
          <div>
            <h1 id="name">Monyelly Rodrigues</h1>
            <div class="role" id="role">Estudante de ADS - Estagiária Suporte N1</div>
            
          </div>
        </div>

        <div class="section contact" id="contact">
          <h3>Contato</h3>
          <p id="email">monyellyrodrigues@gmail.com</p>
          <p id="phone">(83) 9 8841-2486</p>
          <p id="location">João Pessoa - PB</p>
        </div>

        <div class="section skills">
          <h3>Habilidades</h3>
          <div class="skill"><strong>Moodle</strong><div class="bar"><span style="width:90%"></span></div></div>
          <div class="skill"><strong>Suporte N1</strong><div class="bar"><span style="width:75%"></span></div></div>
          <div class="skill"><strong>HTML/CSS</strong><div class="bar"><span style="width:70%"></span></div></div>
        </div>

        <div class="section">
          <h3>Formação</h3>
          <p><strong>ADS</strong><br/><span class="muted">Sectras — início: 2024 a 2026</span></p>
        </div>
      </aside>

      <main class="right">
        <section class="summary">
          <h2>Resumo Profissional</h2>
          <p class="muted">Profissional proativa em início de carreira com foco em suporte técnico N1, administração de Moodle e desenvolvimento web. Gosto de transformar problemas técnicos em soluções práticas.</p>
        </section>

        <section class="section timeline" id="experiencia">
          <h3>Experiência</h3>

          <article class="job">
            <h4>Estagiária — Suporte N1</h4>
            <div class="meta">Empresa Techeduconnect • out.2025 – abr.2026</div>
            <p>Atendimento a usuários, triagem de chamados, suporte em plataformas de ensino (Moodle) e criação de tutoriais técnicos.</p>
          </article>

        </section>
      </main>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
/* styles.css */
/* Fonte: Playfair Display (títulos) + Poppins (texto) */
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Poppins:wght@300;400;600&display=swap');

:root{
  --bg: #fff5f7;      /* fundo geral rosa clarinho */
  --card: #fce4ec;    /* bloco dos cards */
  --accent: #f2a6b3;  /* rosa pêssego (destaques) */
  --text: #4a2c2a;    /* marrom quente (texto) */
  --muted: #8b6866;   /* texto secundário */
  --white-trans: rgba(255,255,255,0.9);
}

*{box-sizing:border-box}
html,body{height:100%}

/* página */
body{
  margin:0;
  font-family:'Poppins', sans-serif;
  background:var(--bg);
  color:var(--text);
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
}

/* container central */
.container{
  max-width:1000px;
  margin:2rem auto;
  padding:1rem;
}

/* card (colunas) */
.card{
  display:flex;
  background:var(--card);
  border-radius:18px;
  overflow:hidden;
  box-shadow:0 8px 30px rgba(234,197,201,0.35);
}

/* coluna esquerda (perfil) */
.left{
  width:320px;
  padding:2rem;
  background:linear-gradient(180deg, var(--accent), #ef9dac);
  color:#fff;
  display:flex;
  flex-direction:column;
  gap:1rem;
}

/* nome e função */
.profile h1{
  margin:0;
  font-family:'Playfair Display', serif;
  font-size:1.9rem;
  letter-spacing:0.4px;
}
.role{
  margin-top:6px;
  opacity:0.98;
  font-weight:500;
  font-size:0.95rem;
}

/* botões */
.actions{margin-top:12px;display:flex;gap:10px}
.btn{
  background:#fff;
  color:var(--accent);
  padding:8px 14px;
  border-radius:20px;
  text-decoration:none;
  font-weight:600;
  font-size:0.95rem;
}
.btn.ghost{ background:transparent; border:1px solid rgba(255,255,255,0.2); color:#fff; }

/* coluna direita (conteúdo) */
.right{flex:1;padding:2rem}

/* seção geral */
.section{margin-bottom:1.6rem}
.section h3{
  font-family:'Playfair Display', serif;
  color:var(--text);
  margin:0 0 0.6rem 0;
  font-size:1.05rem;
  border-bottom:2px solid rgba(242,166,179,0.25);
  padding-bottom:6px;
}
.muted{color:var(--muted);font-size:0.95rem;line-height:1.5}

/* skills */
.skills .skill{display:flex;align-items:center;gap:12px;margin:8px 0}
.bar{flex:1;height:10px;background:var(--white-trans);border-radius:20px;overflow:hidden}
.bar span{display:block;height:100%;background:#fff;border-radius:20px}

/* job (experiência) */
.job{
  padding:12px;border-radius:12px;background:rgba(255,255,255,0.6);border:1px solid rgba(74,44,42,0.05);margin-bottom:12px;
}
.job h4{margin:0;font-size:1rem;color:var(--text)}
.job .meta{color:var(--muted);font-size:0.9rem;margin-top:6px}

/* footer */
footer{ text-align:center;padding:1rem;color:var(--text);font-family:'Playfair Display', serif; }

/* responsividade */
@media (max-width:860px){
  .card{flex-direction:column}
  .left{width:100%}
  .container{padding:0.5rem}
}

// script.js
document.addEventListener('DOMContentLoaded', () => {
  console.log('Currículo de Monyelly carregado 💖');
  enableSmoothScroll();
  beautifySkillBars();
});

/* Smooth scroll simples para links internos */
function enableSmoothScroll() {
  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', function(e){
      const targetId = this.getAttribute('href').slice(1);
      const el = document.getElementById(targetId);
      if(el){
        e.preventDefault();
        el.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });
}

/* Ajusta visual das skill bars: lê o style="width:XX%" do span e aplica uma transição */
function beautifySkillBars(){
  const spans = document.querySelectorAll('.bar > span');
  spans.forEach(span => {
    const w = span.style.width || '0%';
    span.style.transition = 'width 900ms cubic-bezier(.2,.9,.2,1)';
    // força reflow para animação inicial:
    requestAnimationFrame(() => span.style.width = w);
    // garante contraste sutil: se muito claro, escurece levemente
    span.style.boxShadow = 'inset 0 -2px 6px rgba(0,0,0,0.06)';
  });
}

/* Função utilitária opcional para atualizar dados via console
   Exemplo:
   updateProfile({
     name: 'Monyelly Rodrigues',
     role: 'Estudante de ADS',
     email: 'meu@email.com',
     phone: '(83) 9 9999-9999',
     location: 'João Pessoa - PB'
   });
*/
function updateProfile(data){
  if(data.name) document.getElementById('name').textContent = data.name;
  if(data.role) document.getElementById('role').textContent = data.role;
  if(data.email) {
    const el = document.getElementById('email');
    if(el) el.textContent = data.email;
  }
  if(data.phone) {
    const el = document.getElementById('phone');
    if(el) el.textContent = data.phone;
  }
  if(data.location) {
    const el = document.getElementById('location');
    if(el) el.textContent = data.location;
  }
}
