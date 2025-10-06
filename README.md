<!--
Single-file responsive website (index.html)
Instructions:
1) Preview locally: Save this file as `index.html` and open it in your browser.
2) Edit text/images: Search for the "/* EDIT HERE */" markers in the file and replace content.
3) Host for free:
   - GitHub Pages: create a repository, upload index.html to the repo root, enable Pages from the main branch. Your site will appear at https://<username>.github.io/<repo>/ (or the root repo if named <username>.github.io).
   - Netlify: drag & drop this file into Netlify Drop (or connect your GitHub repo) to publish instantly.
   - Vercel: sign in, import a Git repo containing this file and deploy.
4) Assets: This single-file uses SVG and base64 icons only; for photos swap the placeholder images (data-uris) with your own URLs or local image files when hosting.

Want custom colors, fonts, or content? Reply and tell me what to change — I'll update the file in the canvas.
-->

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Your Free Website</title>
  <meta name="description" content="A simple, free single-file website you can edit and host instantly.">
  <style>
    /* --------------- Simple CSS Reset --------------- */
    *,*::before,*::after{box-sizing:border-box}
    html,body{height:100%}
    body{margin:0;font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;line-height:1.4;color:#0f172a;background:#f8fafc}

    /* --------------- Layout & Utilities --------------- */
    .container{max-width:1100px;margin:0 auto;padding:28px}
    .row{display:flex;gap:24px;flex-wrap:wrap}
    .card{background:#fff;border-radius:12px;padding:18px;box-shadow:0 6px 18px rgba(7,11,27,0.06)}
    h1,h2,h3{margin:0 0 12px 0}
    p{margin:0 0 12px 0}
    a{color:inherit}

    /* --------------- Header --------------- */
    header{background:linear-gradient(90deg,#0ea5a4 0%,#2563eb 100%);color:#fff;padding:18px 0;border-radius:12px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:44px;height:44px;border-radius:8px;background:rgba(255,255,255,0.12);display:inline-grid;place-items:center;font-weight:700}
    nav{margin-left:auto}
    .nav-links{display:flex;gap:14px;align-items:center}
    .btn{padding:8px 12px;border-radius:8px;background:#fff;color:#0f172a;text-decoration:none;font-weight:600}

    /* --------------- Hero --------------- */
    .hero{display:flex;align-items:center;gap:28px;padding:28px 0}
    .hero-left{flex:1}
    .hero-right{flex:1;display:grid;place-items:center}
    .hero-cta{display:inline-flex;gap:10px;align-items:center}

    /* --------------- Features --------------- */
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px}

    /* --------------- Footer --------------- */
    footer{margin-top:28px;padding:14px 0;text-align:center;color:#475569}

    /* --------------- Responsive --------------- */
    @media (max-width:860px){
      .hero{flex-direction:column}
      nav{order:3;width:100%}
      .nav-links{justify-content:space-between}
    }

    /* --------------- Simple components --------------- */
    .badge{display:inline-block;padding:6px 10px;border-radius:999px;background:rgba(15,23,42,0.06);font-weight:700}
    .muted{color:#64748b}
    .feature-icon{width:40px;height:40px;border-radius:8px;background:#eef2ff;display:inline-grid;place-items:center;font-weight:700}

    /* --------------- Contact form --------------- */
    form{display:grid;gap:8px}
    input,textarea{padding:10px;border-radius:8px;border:1px solid #e2e8f0;font-size:14px}
    button[type="submit"]{padding:10px 14px;border-radius:8px;border:0;background:#0ea5a4;color:#fff;font-weight:700}

    /* --------------- Small helpers --------------- */
    .center{text-align:center}
    .small{font-size:13px}

    /* --------------- Code block (for demo) --------------- */
    pre{background:#0f172a;color:#f8fafc;padding:12px;border-radius:8px;overflow:auto}

    /* --------------- Minimal focus styles --------------- */
    a:focus,input:focus,button:focus,textarea:focus{outline:3px solid rgba(37,99,235,0.18);outline-offset:3px}

  </style>
</head>
<body>
  <div class="container">
    <header class="card row" style="align-items:center">
      <div class="brand">
        <div class="logo">YW</div>
        <div>
          <div style="font-weight:800">Your Website</div>
          <div class="small muted">Simple • Fast • Free</div>
        </div>
      </div>

      <nav>
        <div class="nav-links">
          <a href="#features" class="small muted">Features</a>
          <a href="#about" class="small muted">About</a>
          <a href="#contact" class="small muted">Contact</a>
          <a href="#" class="btn">Get started</a>
        </div>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="hero-left">
          <div class="badge">NEW</div>
          <h1>Launch your free website — one file, zero setup</h1>
          <p class="muted">Editable HTML file with styles and minimal JavaScript. Perfect for portfolios, small businesses, or a quick landing page.</p>
          <div class="hero-cta" style="margin-top:14px">
            <a class="btn" href="#contact">Customize it</a>
            <a class="small muted" href="#hosting" style="align-self:center">Hosting tips ↓</a>
          </div>
        </div>
        <div class="hero-right card center">
          <!-- Simple screenshot placeholder (SVG) -->
          <svg width="280" height="180" viewBox="0 0 280 180" fill="none" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="screenshot">
            <rect width="280" height="180" rx="12" fill="#f8fafc" stroke="#e2e8f0"/>
            <rect x="16" y="20" width="248" height="18" rx="6" fill="#e6eefc"/>
            <rect x="16" y="46" width="120" height="14" rx="6" fill="#eef2ff"/>
            <rect x="16" y="70" width="248" height="74" rx="8" fill="#fff" stroke="#e6eefc"/>
          </svg>
          <div class="muted small" style="margin-top:10px">Preview — replace this with your own image</div>
        </div>
      </section>

      <section id="features" style="margin-top:18px">
        <h2>Features</h2>
        <div class="grid" style="margin-top:12px">
          <div class="card">
            <div class="row" style="align-items:center">
              <div class="feature-icon">⚡</div>
              <div>
                <div style="font-weight:700">No dependencies</div>
                <div class="muted small">Single HTML file — easy to edit.</div>
              </div>
            </div>
          </div>

          <div class="card">
            <div class="row" style="align-items:center">
              <div class="feature-icon">🎨</div>
              <div>
                <div style="font-weight:700">Customizable</div>
                <div class="muted small">Colors, text, and images are easy to update.</div>
              </div>
            </div>
          </div>

          <div class="card">
            <div class="row" style="align-items:center">
              <div class="feature-icon">🔒</div>
              <div>
                <div style="font-weight:700">Secure</div>
                <div class="muted small">Works on HTTPS when hosted on GitHub/Netlify/Vercel.</div>
              </div>
            </div>
          </div>

          <div class="card">
            <div class="row" style="align-items:center">
              <div class="feature-icon">💾</div>
              <div>
                <div style="font-weight:700">Small footprint</div>
                <div class="muted small">Fast load times and low bandwidth usage.</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="about" style="margin-top:18px">
        <h2>About this template</h2>
        <div class="card">
          <p class="muted">This single file contains simple HTML, CSS, and a touch of JavaScript. No frameworks. You can fork it, edit it, or drop it into any static host.</p>

          <h3>How to edit</h3>
          <ul class="muted small">
            <li>Open the file in a text editor (VS Code, Sublime, Notepad++)</li>
            <li>Find the comment markers "/* EDIT HERE */" to change headings, text, and contact info</li>
            <li>Replace placeholder images with your own by updating &lt;svg&gt; or &lt;img&gt; src attributes</li>
          </ul>
        </div>
      </section>

      <section id="contact" style="margin-top:18px">
        <h2>Contact</h2>
        <div class="row">
          <div class="card" style="flex:1;min-width:260px">
            <form id="contactForm">
              <label class="small">Name</label>
              <input name="name" placeholder="Your name" required>
              <label class="small">Email</label>
              <input name="email" type="email" placeholder="you@example.com" required>
              <label class="small">Message</label>
              <textarea name="message" rows="4" placeholder="Say hi"></textarea>
              <button type="submit">Send message</button>
              <div id="formStatus" class="small muted" style="margin-top:8px"></div>
            </form>
          </div>

          <div class="card" style="flex:1;min-width:260px">
            <h3>Quick info</h3>
            <p class="muted small">Email: <a href="mailto:hello@example.com">hello@example.com</a></p>
            <p class="muted small">Location: Anywhere</p>
            <p class="muted small">Want this hosted for free? Try GitHub Pages, Netlify, or Vercel.</p>
          </div>
        </div>
      </section>

      <section id="hosting" style="margin-top:18px">
        <h2>Hosting tips</h2>
        <div class="card">
          <ol class="muted small">
            <li><strong>GitHub Pages</strong>: Create a repo, upload index.html to the root, go to Settings → Pages → publish from main branch.</li>
            <li><strong>Netlify Drop</strong>: Visit Netlify, drag & drop this file into the Drop area to publish instantly.</li>
            <li><strong>Vercel</strong>: Connect your Git repo and deploy with one click.</li>
          </ol>
        </div>
      </section>

      <section style="margin-top:18px">
        <h2>Example code snippet</h2>
        <div class="card">
          <pre>&lt;!-- Paste this file into index.html and edit --&gt;</pre>
        </div>
      </section>

    </main>

    <footer>
      <div class="small muted">Made with ♥ — Edit and host for free</div>
    </footer>
  </div>

  <script>
    // Simple contact form handling (client-side only)
    document.getElementById('contactForm').addEventListener('submit', function(e){
      e.preventDefault();
      const form = e.target;
      const status = document.getElementById('formStatus');
      const data = new FormData(form);
      const name = data.get('name');
      const email = data.get('email');
      const message = data.get('message');

      // Basic validation
      if(!name || !email){
        status.textContent = 'Please fill name and email.';
        return;
      }

      // This demo does not send messages to a server. To receive messages live,
      // connect this form to Formspree, Getform, Netlify Forms, or a backend.
      status.textContent = 'Thanks — this demo does not send email. To enable, connect to Formspree or Netlify Forms.';
      form.reset();
    });
  </script>
</body>
</html>
