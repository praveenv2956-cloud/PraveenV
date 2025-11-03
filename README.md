<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Praveen — Cybersecurity Portfolio</title>
<meta name="description" content="Praveen — B.E. Cybersecurity student at Mahendra Engineering College. Portfolio showcasing skills, projects and certificates." />
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&family=Roboto+Mono:wght@400;700&display=swap" rel="stylesheet">



<style>
  :root{
    --bg:#071017;              /* deep background */
    --card: rgba(255,255,255,0.03);
    --glass: rgba(255,255,255,0.04);
    --muted: #91a1ab;
    --text: #e8f6f2;
    --neon: #00ff88;           /* green neon */
    --neon-2: #00d18f;
    --accent-glow: 0 10px 35px rgba(0,255,136,0.08);
    --maxw: 1150px;
    --radius:12px;
    --mono: 'Roboto Mono', monospace;
    --ui: 'Poppins', system-ui, sans-serif;
  }

  *{box-sizing:border-box}
  html,body{height:100%}
  body{
    margin:0;
    font-family:var(--ui);
    background:
      radial-gradient(800px 400px at 10% 10%, rgba(0,255,136,0.03), transparent 8%),
      radial-gradient(600px 300px at 95% 85%, rgba(0,209,143,0.02), transparent 6%),
      var(--bg);
    color:var(--text);
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    padding:28px 18px;
    display:flex;
    justify-content:center;
  }

  .wrap{width:100%;max-width:var(--maxw)}
  header{
    display:flex;align-items:center;justify-content:space-between;gap:14px;
    margin-bottom:18px;
  }

  /* Brand */
  .brand{display:flex;gap:14px;align-items:center}
  .logo{
    width:54px;height:54px;border-radius:12px;
    background:linear-gradient(135deg,var(--neon),var(--neon-2));
    display:flex;align-items:center;justify-content:center;font-weight:800;color:#05221a;font-family:var(--mono);
    box-shadow:var(--accent-glow);
  }
  .brand .title{line-height:1}
  .brand .title .name{font-weight:700;font-size:18px}
  .brand .title .meta{font-size:12px;color:var(--muted)}

  nav{display:flex;gap:12px;align-items:center}
  nav a{
    color:var(--muted);text-decoration:none;padding:8px 10px;border-radius:8px;font-weight:600;font-size:14px;
    transition:all .18s ease;
  }
  nav a:hover{color:var(--text);background:rgba(255,255,255,0.02)}
  nav a.active{color:var(--neon);box-shadow:0 6px 20px rgba(0,255,136,0.06);background:linear-gradient(90deg,rgba(0,255,136,0.04),transparent)}

  .cta{display:flex;gap:10px;align-items:center}
  .btn{
    background:linear-gradient(90deg,var(--neon),var(--neon-2));
    color:#05221a;padding:10px 14px;border-radius:10px;border:none;font-weight:700;cursor:pointer;text-decoration:none;
    box-shadow:var(--accent-glow);
  }
  .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--text);box-shadow:none}

  /* HERO */
  .hero{
    display:grid;grid-template-columns:1fr 360px;gap:24px;padding:22px;background:linear-gradient(180deg,var(--glass),rgba(255,255,255,0.02));
    border-radius:var(--radius);backdrop-filter:blur(6px);box-shadow:0 10px 40px rgba(0,0,0,0.6);
  }
  .hero h1{font-size:30px;margin:0}
  .hero p{color:var(--muted);margin:10px 0 0}
  .hero .chips{display:flex;gap:8px;margin-top:14px;flex-wrap:wrap}
  .chip{padding:6px 10px;border-radius:999px;background:rgba(0,0,0,0.35);color:var(--muted);font-weight:700;font-size:13px}

  /* Profile card with neon ring */
  .profile{
    padding:16px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.015), rgba(255,255,255,0.01));
    display:flex;flex-direction:column;align-items:center;gap:12px;
  }
  .avatar{
    width:160px;height:160px;border-radius:999px;padding:6px;background:linear-gradient(90deg, rgba(0,255,136,0.08), rgba(0,209,143,0.06));box-shadow:0 10px 30px rgba(0,255,136,0.06);
    display:flex;align-items:center;justify-content:center;
  }
  .avatar img{width:100%;height:100%;object-fit:cover;border-radius:999px;border:4px solid rgba(0,0,0,0.35)}
  .badge{padding:6px 10px;border-radius:999px;background:rgba(0,0,0,0.45);color:var(--neon);font-weight:700}

  main{margin-top:18px;display:grid;gap:18px}
  section{padding:18px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));}

  .grid-2{display:grid;grid-template-columns:1fr 340px;gap:18px}
  .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:14px;border-radius:10px;border:1px solid rgba(255,255,255,0.02);transition:transform .18s ease}
  .card:hover{transform:translateY(-6px)}

  /* Skills */
  .skills{display:flex;flex-wrap:wrap;gap:10px}
  .skill{background:rgba(0,0,0,0.35);padding:8px 12px;border-radius:10px;font-weight:700;color:var(--muted)}

  /* Projects */
  .projects-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:12px}

  .project .title{font-weight:700}
  .tags{display:flex;gap:8px;flex-wrap:wrap;margin-top:10px}

  /* Certificates gallery */
  .certs{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:14px;align-items:start}
  .cert{
    border-radius:10px;overflow:hidden;position:relative;border:1px solid rgba(255,255,255,0.03);
    background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.005));
  }
  .cert-thumb{width:100%;height:160px;object-fit:cover;display:block;background:#061018}
  .cert-body{padding:10px}
  .cert-title{font-weight:700}
  .cert-meta{color:var(--muted);font-size:13px;margin-top:6px}
  .cert-actions{display:flex;gap:8px;margin-top:10px}
  .small-btn{padding:8px 10px;border-radius:8px;background:rgba(255,255,255,0.02);color:var(--muted);border:1px solid rgba(255,255,255,0.02);cursor:pointer;font-weight:700}

  /* Modal (fullscreen) for certificate images */
  .modal{
    position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:linear-gradient(rgba(2,8,10,0.7),rgba(2,8,10,0.85));
    z-index:1400;padding:20px;
  }
  .modal.open{display:flex}
  .modal-content{max-width:1000px;width:100%;max-height:90vh;border-radius:10px;overflow:hidden;box-shadow:0 30px 80px rgba(0,0,0,0.7)}
  .modal-img{width:100%;height:100%;object-fit:contain;background:#000}
  .modal-close{position:absolute;top:18px;right:18px;background:rgba(0,0,0,0.6);color:var(--neon);border:1px solid rgba(0,255,136,0.08);padding:8px 10px;border-radius:8px;font-weight:700;cursor:pointer}

  /* Footer */
  footer{margin-top:10px;text-align:center;color:var(--muted);padding:14px}

  /* small screens */
  @media (max-width:980px){
    .hero{grid-template-columns:1fr}
    .grid-2{grid-template-columns:1fr}
    nav{display:none}
  }

  /* subtle animations */
  .fade-up{transform:translateY(6px);opacity:0;transition:all .5s cubic-bezier(.2,.9,.2,1)}
  .fade-up.in{transform:none;opacity:1}
</style>
</head>
<body>
  <div class="wrap" id="page">
    <header>
      <div class="brand">
        <div class="logo">PV</div>
        <div class="title">
          <div class="name">Praveen</div>
          <div class="meta">B.E. Cybersecurity — Mahendra Engineering College</div>
        </div>
      </div>

      <nav aria-label="Primary">
        <a href="#home" class="nav-link active">Home</a>
        <a href="#about" class="nav-link">About</a>
        <a href="#skills" class="nav-link">Skills</a>
        <a href="#projects" class="nav-link">Projects</a>
        <a href="#certs" class="nav-link">Certificates</a>
        <a href="#contact" class="nav-link">Contact</a>
      </nav>

      <div class="cta">
        <a class="btn" href="#contact">Hire / Intern</a>
        <a class="btn ghost" href="resume.pdf" download>Download Resume</a>
      </div>
    </header>

    <!-- HERO -->
    <main>
      <section id="home" class="hero" aria-labelledby="hero-heading">
        <div>
          <h1 id="hero-heading">Hi — I’m <span style="color:var(--neon)">Praveen</span></h1>
          <p class="muted">Cybersecurity student focused on network & application security, ethical hacking and digital forensics. Building labs and CTF writeups — open to internships.</p>

          <div class="chips" style="margin-top:12px">
            <div class="chip">B.E. Cybersecurity</div>
            <div class="chip">Mahendra Engineering College</div>
            <div class="chip">Open to internships</div>
          </div>

          <div style="margin-top:16px;display:flex;gap:10px;">
            <a class="btn" href="#projects">View Work</a>
            <a class="btn ghost" href="#certs">Certificates</a>
          </div>

          <div style="margin-top:16px">
            <div class="card terminal" style="font-family:var(--mono);color:var(--neon);padding:10px">
              $ degree: B.E. Cybersecurity &nbsp;&nbsp;|&nbsp;&nbsp; $ college: Mahendra Engineering College
            </div>
          </div>
        </div>

        <!-- Profile card -->
        <aside class="profile" aria-label="Profile">
          <div class="avatar" aria-hidden="false">
            <!-- EDIT: Replace profile.jpg with your image file in same folder -->
            <img src=" alt="Praveen — Cybersecurity student"
                 onerror="this.src='data:image/svg+xml;utf8,<svg xmlns=\\'http://www.w3.org/2000/svg\\' width=400 height=400><rect width=\\'100%\\' height=\\'100%\\' fill=\\'%23060d12\\' /><text x=50% y=50% fill=\\'%2300ff88\\' font-size=28 text-anchor=middle dominant-baseline=central font-family=Roboto+Mono>Praveen</text></svg>'">
          </div>
          <div class="badge">B.E. Cybersecurity</div>
          <div style="text-align:center;color:var(--muted);font-size:14px">Mahendra Engineering College</div>
          <div style="display:flex;gap:8px;margin-top:10px">
            <a class="btn" href="#contact">Contact</a>
            <a class="btn ghost" href="resume.pdf" download>Resume</a>
          </div>
        </aside>
      </section>

      <!-- ABOUT -->
      <section id="about" class="fade-up" aria-labelledby="about-heading">
        <h2 id="about-heading">About</h2>
        <div class="grid-2" style="margin-top:12px">
          <div>
            <p class="muted">Student</p>
            <p>I am a B.E. Cybersecurity student at Mahendra Engineering College. I focus on hands-on labs: penetration testing, network analysis, and digital forensics. I take part in CTFs and security workshops to refine practical skills.</p>

            <div style="margin-top:12px" class="card">
              <strong>Education</strong>
              <div class="muted" style="margin-top:6px">B.E. in Cybersecurity — Mahendra Engineering College<br>Graduation: [YYYY]</div>
            </div>

            <div style="margin-top:10px" class="card">
              <strong>Experience</strong>
              <div class="muted" style="margin-top:6px">Student projects, labs, and CTFs. Open to internships and research opportunities.</div>
            </div>
          </div>

          <aside>
            <div class="card">
              <strong>Contact</strong>
              <div class="muted" style="margin-top:6px">Email: <a style="color:var(--neon)" href="mailto:your.email@example.com">your.email@example.com</a></div>
              <div class="muted" style="margin-top:6px">Social: <a style="color:var(--muted)" href="#">GitHub</a> • <a style="color:var(--muted)" href="#">LinkedIn</a></div>
            </div>

            <div style="margin-top:12px" class="card">
              <strong>Quick Skills</strong>
              <div class="skills" style="margin-top:8px">
                <span class="skill">Network Security</span>
                <span class="skill">Ethical Hacking</span>
                <span class="skill">Penetration Testing</span>
                <span class="skill">Forensics</span>
                <span class="skill">Linux</span>
                <span class="skill">Python</span>
              </div>
            </div>
          </aside>
        </div>
      </section>

      <!-- SKILLS -->
      <section id="skills" class="fade-up">
        <h2>Skills & Tools</h2>
        <div style="margin-top:12px" class="card">
          <div style="display:flex;gap:18px;flex-wrap:wrap;align-items:flex-start">
            <div style="flex:1;min-width:220px">
              <h4 style="margin:0 0 8px">Core</h4>
              <ul class="muted">
                <li>Network Security & Monitoring (Wireshark, tcpdump)</li>
                <li>Penetration Testing (Burp Suite, Metasploit)</li>
                <li>Web App Security (OWASP Top 10)</li>
                <li>Digital Forensics & IR</li>
                <li>Linux & Scripting (Bash, Python)</li>
              </ul>
            </div>
            <div style="min-width:220px">
              <h4 style="margin:0 0 8px">Proficiency</h4>
              <div style="display:flex;flex-direction:column;gap:10px">
                <div><strong>Penetration Testing</strong>
                  <div style="height:10px;background:rgba(255,255,255,0.04);border-radius:8px;margin-top:6px"><div style="width:65%;height:100%;background:linear-gradient(90deg,var(--neon),var(--neon-2));border-radius:8px"></div></div>
                </div>
                <div><strong>Network Security</strong>
                  <div style="height:10px;background:rgba(255,255,255,0.04);border-radius:8px;margin-top:6px"><div style="width:60%;height:100%;background:linear-gradient(90deg,var(--neon),var(--neon-2));border-radius:8px"></div></div>
                </div>
                <div><strong>Forensics</strong>
                  <div style="height:10px;background:rgba(255,255,255,0.04);border-radius:8px;margin-top:6px"><div style="width:45%;height:100%;background:linear-gradient(90deg,var(--neon),var(--neon-2));border-radius:8px"></div></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- PROJECTS -->
      <section id="projects" class="fade-up">
        <h2>Projects</h2>
        <div style="margin-top:12px" class="projects-grid">
          <article class="card project">
            <div class="title">Web App Pentest — Lab</div>
            <div class="muted">Lab-based pentest of vulnerable app: found SQLi & XSS, produced remediation report.</div>
            <div class="tags"><span class="small muted">OWASP</span><span class="small muted">Report</span></div>
          </article>

          <article class="card project">
            <div class="title">Network Packet Forensics</div>
            <div class="muted">Analyzed PCAPs to detect suspicious connections and exfiltration patterns.</div>
            <div class="tags"><span class="small muted">Wireshark</span></div>
          </article>
          <!-- ADD more project cards here -->
        </div>
      </section>

      <!-- CERTIFICATES -->
      <section id="certs" class="fade-up" aria-labelledby="certs-heading">
        <h2 id="certs-heading">Certificates</h2>
        <p class="muted">Click any certificate image to view it in full-screen. Replace cert1.jpg with your real image file (same folder).</p>

        <div style="margin-top:12px" class="certs" id="certGallery">
          <!-- CERT 1: Uses image (EDIT: replace cert1.jpg with your file) -->
          <div class="cert card" tabindex="0">
            <img src="index.html/IMG-20251103-WA0040.jpg" alt="" class="cert-thumb" onerror="this.style.filter='grayscale(1)';this.nextElementSibling.querySelector('.cert-title').textContent='Red Hat Certificate (preview)';">
            <div class="cert-body">
              <div class="cert-title"></div>
              <div class="cert-meta">Praveen V — Issued: October 14, 2025</div>
              <div class="cert-actions">
                <button class="small-btn" data-preview-src="cert1.jpg" aria-label="Open certificate 1">View</button>
                <!-- Fallback if you prefer opening the uploaded PDF -->
                <a class="small-btn" href="aeae7ed0-b962-40a2-89d5-94d124cfd238.pdf" target="_blank" rel="noopener">Open PDF</a>
              </div>
            </div>
          </div>

          <!-- CERT 2:Uses image (EDIT: replace cert1.jpg with your file) -->
          <div class="cert card" tabindex="0">
            <img src="index.html/IMG-20251103-WA0041.jpg" alt="" class="cert-thumb" onerror="this.style.filter='grayscale(1)';this.nextElementSibling.querySelector('.cert-title').textContent='Red Hat Certificate (preview)';">
            <div class="cert-body">
              <div class="cert-title"></div>
              <div class="cert-meta">Praveen V — Issued: October 14, 2025</div>
              <div class="cert-actions">
                <button class="small-btn" data-preview-src="cert1.jpg" aria-label="Open certificate 1">View</button>
                <!-- Fallback if you prefer opening the uploaded PDF -->
                <a class="small-btn" href="aeae7ed0-b962-40a2-89d5-94d124cfd238.pdf" target="_blank" rel="noopener">Open PDF</a>
              </div>
            </div>
          </div>
          <!-- CERT 3:Uses image (EDIT: replace cert1.jpg with your file) -->
          <div class="cert card" tabindex="0">
            <img src="index.html/IMG-20251103-WA0042.jpg" alt="" class="cert-thumb" onerror="this.style.filter='grayscale(1)';this.nextElementSibling.querySelector('.cert-title').textContent='Red Hat Certificate (preview)';">
            <div class="cert-body">
              <div class="cert-title"></div>
              <div class="cert-meta">Praveen V — Issued: October 14, 2025</div>
              <div class="cert-actions">
                <button class="small-btn" data-preview-src="cert1.jpg" aria-label="Open certificate 1">View</button>
                <!-- Fallback if you prefer opening the uploaded PDF -->
                <a class="small-btn" href="aeae7ed0-b962-40a2-89d5-94d124cfd238.pdf" target="_blank" rel="noopener">Open PDF</a>
              </div>
            </div>
          </div>
          <!-- CERT 4:Uses image (EDIT: replace cert1.jpg with your file) -->
          <div class="cert card" tabindex="0">
            <img src="index.html/IMG-20251103-WA0043.jpg" alt="" class="cert-thumb" onerror="this.style.filter='grayscale(1)';this.nextElementSibling.querySelector('.cert-title').textContent='Red Hat Certificate (preview)';">
            <div class="cert-body">
              <div class="cert-title"></div>
              <div class="cert-meta">Praveen V — Issued: October 14, 2025</div>
              <div class="cert-actions">
                <button class="small-btn" data-preview-src="cert1.jpg" aria-label="Open certificate 1">View</button>
                <!-- Fallback if you prefer opening the uploaded PDF -->
                <a class="small-btn" href="aeae7ed0-b962-40a2-89d5-94d124cfd238.pdf" target="_blank" rel="noopener">Open PDF</a>
              </div>
            </div>
          </div>


      <!-- CONTACT -->
      <section id="contact" class="fade-up">
        <h2>Contact</h2>
        <div class="grid-2" style="margin-top:12px">
          <div>
            <form id="contactForm" onsubmit="return false" class="card" style="display:flex;flex-direction:column;gap:10px">
              <input id="name" aria-label="Your name" placeholder="Your name" required />
              <input id="email" aria-label="Your email" type="email" placeholder="you@example.com" required />
              <input id="subject" placeholder="Subject (optional)" />
              <textarea id="message" rows="5" placeholder="Message..." required></textarea>
              <div style="display:flex;gap:10px;justify-content:flex-start">
                <button class="btn" id="sendBtn">Send Message</button>
                <button class="btn ghost" id="clearBtn" type="button">Clear</button>
              </div>
              <div id="formMsg" class="muted small" aria-live="polite"></div>
            </form>
          </div>

          <aside>
            <div class="card">
              <strong>Alternate</strong>
              <div class="muted" style="margin-top:6px">Email: <a href="praveenv2956@gmail.com" style="color:var(--neon)">your.email@example.com</a></div>
              <div class="muted" style="margin-top:6px">Phone: +91-7904869119</div>
              <div class="muted" style="margin-top:6px">Links: <a href="#" style="color:var(--muted)">GitHub</a>, <a href="#" style="color:var(--muted)">LinkedIn</a></div>
            </div>
          </aside>
        </div>
      </section>

      <footer>
        © <span id="year"></span> Praveen — Built with ♥
      </footer>
    </main>
  </div>

  <!-- Modal for certificate preview -->
  <div id="modal" class="modal" role="dialog" aria-modal="true" aria-label="Certificate preview">
    <button id="modalClose" class="modal-close" aria-label="Close preview">Close</button>
    <div class="modal-content" role="document">
      <img id="modalImg" class="modal-img" src="" alt="Certificate preview">
    </div>
  </div>

<script>
/* JavaScript: navigation highlight, scroll, modal preview, contact form validation, small animations */

/* Utilities */
const qs = s => document.querySelector(s);
const qsa = s => Array.from(document.querySelectorAll(s));

/* Insert year */
document.getElementById('year').textContent = new Date().getFullYear();

/* Smooth scroll + active nav */
qsa('.nav-link').forEach(a=>{
  a.addEventListener('click', e=>{
    e.preventDefault();
    const id = a.getAttribute('href');
    document.querySelector(id).scrollIntoView({behavior:'smooth',block:'start'});
  });
});

const sections = qsa('main section');
function onScroll(){
  const y = window.scrollY + 120;
  let active = null;
  sections.forEach(sec=>{
    const top = sec.offsetTop;
    if(top <= y) active = sec;
  });
  if(active){
    qsa('nav a').forEach(a=>a.classList.remove('active'));
    const id = '#'+active.id;
    const link = qsa(`nav a[href="${id}"]`)[0];
    if(link) link.classList.add('active');
  }
}
window.addEventListener('scroll', onScroll);
onScroll();

/* Fade-up entrance animations */
function revealOnScroll(){
  qsa('.fade-up').forEach(el=>{
    const rect = el.getBoundingClientRect();
    if(rect.top < window.innerHeight - 60) el.classList.add('in');
  });
}
window.addEventListener('scroll', revealOnScroll);
revealOnScroll();

/* Modal logic for certificates (image popup) */
const modal = qs('#modal');
const modalImg = qs('#modalImg');
const modalClose = qs('#modalClose');

function openModal(src, altText = 'Certificate preview'){
  modalImg.src = src;
  modalImg.alt = altText;
  modal.classList.add('open');
  document.body.style.overflow = 'hidden';
  modalClose.focus();
}
function closeModal(){
  modal.classList.remove('open');
  modalImg.src = '';
  document.body.style.overflow = '';
}
modalClose.addEventListener('click', closeModal);
modal.addEventListener('click', (e)=>{
  if(e.target === modal) closeModal();
});
window.addEventListener('keydown', (e)=>{
  if(e.key === 'Escape' && modal.classList.contains('open')) closeModal();
});

/* Attach click handlers to "View" buttons */
qsa('.small-btn[data-preview-src]').forEach(btn=>{
  btn.addEventListener('click', ()=>{
    const src = btn.getAttribute('data-preview-src');
    // If image file not found, it may still open (browser fallback)
    openModal(src, 'Certificate preview');
  });
});

/* Allow Enter key on cert card to open preview (accessibility) */
qsa('.cert[tabindex]').forEach(card=>{
  card.addEventListener('keydown', (e)=>{
    if(e.key === 'Enter'){
      const btn = card.querySelector('.small-btn[data-preview-src]');
      if(btn){
        btn.click();
      } else {
        const link = card.querySelector('a[href$=".pdf"], a[href$=".jpg"], a[href$=".png"]');
        if(link) link.click();
      }
    }
  });
});

/* Contact form validation (client-side) */
const sendBtn = qs('#sendBtn');
const clearBtn = qs('#clearBtn');
const formMsg = qs('#formMsg');
sendBtn && sendBtn.addEventListener('click', ()=>{
  const name = qs('#name').value.trim();
  const email = qs('#email').value.trim();
  const message = qs('#message').value.trim();
  if(!name || !email || !message){
    formMsg.textContent = 'Please fill name, email and message.';
    return;
  }
  const re = /^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$/;
  if(!re.test(email)){
    formMsg.textContent = 'Please enter a valid email address.';
    return;
  }
  formMsg.textContent = 'Message validated locally. To send messages, configure a backend endpoint.';
});

/* Clear form */
clearBtn && clearBtn.addEventListener('click', ()=>{
  qs('#contactForm').reset();
  formMsg.textContent = '';
});

/* Keyboard accessibility: allow tab trapping when modal open (basic) */
modal.addEventListener('keydown', (e)=>{
  if(e.key === 'Tab'){
    // keep focus inside modal close button and possible next elements (simple approach)
    e.preventDefault();
    modalClose.focus();
  }
});

/* Optional: preload certificate thumbnails for snappier modal */
['cert1.jpg','cert2.jpg'].forEach(src=>{
  const img = new Image();
  img.src = src;
});
</script>
</body>
</html>


