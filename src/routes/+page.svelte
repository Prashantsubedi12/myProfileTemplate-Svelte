<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  :global(body) {
    font-family: 'Segoe UI', system-ui, sans-serif;
    background-color: #0A1024;
    color: #e2e8f0;
  }

  :global(a) {
    color: inherit;
    text-decoration: none;
  }
  /* ── AVATAR ── */
  .avatar-wrapper {
    position: relative;
    display: inline-block;
    margin-bottom: 1.5rem;
    cursor: pointer;
  }

  .avatar {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 3px solid rgba(0, 102, 255, 0.4);
    background: rgba(10, 16, 36, 0.6);
    object-fit: cover;
    transition: transform 0.3s, border-color 0.3s, opacity 0.3s;
  }

  .avatar-wrapper:hover .avatar {
    transform: scale(1.08);
    border-color: rgba(0, 102, 255, 0.9);
  }

  .greetings {
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%) translateY(-85%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.3rem;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.25s ease, transform 0.25s ease;
  }

  .greetings.visible {
    opacity: 1;
    transform: translateX(-50%) translateY(-100%);
  }

  .greetings span {
    background: rgba(10, 16, 36, 0.95);
    border: 1px solid rgba(0, 102, 255, 0.4);
    color: #4D94FF;
    font-size: 0.85rem;
    font-weight: 600;
    padding: 0.3rem 0.85rem;
    border-radius: 999px;
    white-space: nowrap;
  }

  /* ── HERO ── */
    .hero {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 2rem;
      background: radial-gradient(ellipse at center, #0D1A40 0%, #0A1024 70%);
    }

    .hero-badge {
      display: inline-block;
      background: rgba(0, 102, 255, 0.12);
      border: 1px solid rgba(0, 102, 255, 0.35);
      color: #4D94FF;
      font-size: 0.85rem;
      padding: 0.4rem 1rem;
      border-radius: 999px;
      margin-bottom: 1.5rem;
    }

    .hero h1 {
      font-size: clamp(2.5rem, 8vw, 5rem);
      font-weight: 800;
      color: #ffffff;
      line-height: 1.1;
      margin-bottom: 1rem;
      letter-spacing: -0.02em;
    }

    .hero h1 span {
      color: #0066FF;
    }

    .hero .subtitle {
      font-size: clamp(1rem, 3vw, 1.4rem);
      color: #94a3b8;
      font-weight: 300;
      margin-bottom: 1rem;
    }

    .hero .bio {
      max-width: 520px;
      color: #64748b;
      line-height: 1.7;
      margin-bottom: 2.5rem;
    }

    .hero-buttons {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
      justify-content: center;
    }

    .btn-primary {
      background: #0066FF;
      color: #fff;
      font-weight: 600;
      padding: 0.75rem 1.75rem;
      border-radius: 999px;
      transition: background 0.2s;
    }

    .btn-primary:hover {
      background: #0052CC;
    }

    .btn-outline {
      border: 1px solid rgba(0, 102, 255, 0.3);
      color: #94a3b8;
      font-weight: 600;
      padding: 0.75rem 1.75rem;
      border-radius: 999px;
      transition: border-color 0.2s, color 0.2s;
    }

    .btn-outline:hover {
      border-color: #0066FF;
      color: #4D94FF;
    }

    /* ── SECTIONS ── */
    section {
      padding: 5rem 1.5rem;
    }

    .section-inner {
      max-width: 900px;
      margin: 0 auto;
    }

    .section-header {
      text-align: center;
      margin-bottom: 3.5rem;
    }

    .section-header h2 {
      font-size: 2.2rem;
      font-weight: 700;
      color: #ffffff;
      margin-bottom: 0.5rem;
    }

    .section-header p {
      color: #64748b;
    }

    /* ── PROJECTS ── */
    #projects {
      background: #0A1024;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
    }

    .project-card {
      background: rgba(10, 20, 45, 0.6);
      border: 1px solid rgba(0, 60, 150, 0.3);
      border-radius: 1.25rem;
      padding: 2rem;
      transition: transform 0.25s, border-color 0.25s;
    }

    .project-card:hover {
      transform: translateY(-4px);
      border-color: rgba(0, 102, 255, 0.55);
    }

    .project-emoji {
      font-size: 3rem;
      margin-bottom: 1.25rem;
    }

    .project-card h3 {
      font-size: 1.15rem;
      font-weight: 700;
      color: #fff;
      margin-bottom: 0.75rem;
    }

    .project-card p {
      color: #94a3b8;
      font-size: 0.9rem;
      line-height: 1.65;
      margin-bottom: 1.25rem;
    }

    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 1.5rem;
    }

    .tag {
      background: rgba(0, 50, 150, 0.35);
      border: 1px solid rgba(0, 102, 255, 0.3);
      color: #4D94FF;
      font-size: 0.75rem;
      padding: 0.25rem 0.75rem;
      border-radius: 999px;
    }

    .first-badge {
      font-size: 0.65rem;
      font-weight: 600;
      background: rgba(0, 102, 255, 0.12);
      border: 1px solid rgba(0, 102, 255, 0.3);
      color: #4D94FF;
      padding: 0.15rem 0.55rem;
      border-radius: 999px;
      vertical-align: middle;
      margin-left: 0.4rem;
    }

    .project-link {
      color: #0066FF;
      font-size: 0.9rem;
      font-weight: 600;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      transition: color 0.2s;
    }

    .project-link:hover {
      color: #4D94FF;
    }

    .project-links {
      display: flex;
      gap: 1.25rem;
    }

    /* ── ABOUT ── */
    #about {
      background: #060C18;
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: start;
    }

    @media (max-width: 700px) {
      .about-grid {
        grid-template-columns: 1fr;
      }
    }

    .about-text p {
      color: #94a3b8;
      line-height: 1.8;
      margin-bottom: 1rem;
    }

    .about-text p span {
      color: #4D94FF;
      font-weight: 600;
    }

    .skills-title {
      font-size: 1rem;
      font-weight: 600;
      color: #fff;
      margin-bottom: 1rem;
    }

    .skills-list {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-bottom: 2rem;
    }

    .skill-chip {
      background: #0D1A3A;
      border: 1px solid #0F2555;
      color: #cbd5e1;
      padding: 0.45rem 1rem;
      border-radius: 0.75rem;
      font-size: 0.85rem;
      font-weight: 500;
      transition: border-color 0.2s, color 0.2s;
    }

    .skill-chip:hover {
      border-color: #0066FF;
      color: #4D94FF;
    }

    .focus-card {
      background: rgba(10, 20, 45, 0.5);
      border: 1px solid #0D1A3A;
      border-radius: 1rem;
      padding: 1.5rem;
    }

    .focus-card h4 {
      color: #fff;
      font-weight: 600;
      margin-bottom: 0.75rem;
    }

    .focus-card ul {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }

    .focus-card li {
      color: #94a3b8;
      font-size: 0.875rem;
      display: flex;
      gap: 0.5rem;
    }

    .focus-card li::before {
      content: '▸';
      color: #0066FF;
      flex-shrink: 0;
    }

    /* ── CONTACT ── */
    #contact {
      background: #0A1024;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 1.25rem;
      max-width: 640px;
      margin: 0 auto;
    }

    .contact-card {
      background: rgba(10, 20, 45, 0.6);
      border: 1px solid rgba(0, 60, 150, 0.3);
      border-radius: 1.25rem;
      padding: 1.75rem 1.25rem;
      text-align: center;
      transition: transform 0.2s, border-color 0.2s;
    }

    .contact-card:hover {
      transform: translateY(-3px);
    }

    .contact-card.email:hover  { border-color: rgba(0, 102, 255, 0.6); }
    .contact-card.insta:hover  { border-color: rgba(236, 72, 153, 0.6); }
    .contact-card.fb:hover     { border-color: rgba(59, 130, 246, 0.6); }
    .contact-card.gh:hover     { border-color: rgba(255, 255, 255, 0.4); }

    .contact-card .icon {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-bottom: 0.75rem;
    }

    .contact-card .icon svg {
      width: 2rem;
      height: 2rem;
    }

    .contact-card.email .icon svg  { color: #4D94FF; }
    .contact-card.insta .icon svg  { color: #f9a8d4; }
    .contact-card.fb .icon svg     { color: #93c5fd; }
    .contact-card.gh .icon svg     { color: #e2e8f0; }

    .contact-card .label {
      color: #64748b;
      font-size: 0.75rem;
      margin-bottom: 0.3rem;
    }

    .contact-card .value {
      color: #e2e8f0;
      font-size: 0.85rem;
      font-weight: 500;
      word-break: break-all;
    }

    .contact-card.email:hover .value  { color: #4D94FF; }
    .contact-card.insta:hover .value  { color: #f9a8d4; }
    .contact-card.fb:hover .value     { color: #93c5fd; }
    .contact-card.gh:hover .value     { color: #e2e8f0; }

    /* ── FOOTER ── */
    footer {
      background: #060C18;
      border-top: 1px solid #0D1A3A;
      text-align: center;
      padding: 2rem 1rem;
      color: #475569;
      font-size: 0.85rem;
    }

  
</style>

<script>
  let hovered = false;
</script>

<!-- paste ALL your HTML content here (hero, projects, about, contact, footer) -->
<section class="hero">
  <div class="hero-badge">👋 Welcome to my portfolio</div>

  <div
    class="avatar-wrapper"
    on:mouseenter={() => hovered = true}
    on:mouseleave={() => hovered = false}
  >
    <img
      src={hovered ? '/wakingavatar.png' : '/sleepingavatar.png'}
      alt="Prashant's memoji"
      class="avatar"
    />
    <div class="greetings" class:visible={hovered}>
      <span>Namaste 🙏</span>
      <span>こんにちは</span>
      <span>Hello 👋</span>
    </div>
  </div>

  <h1>Prashant <span>Subedi</span></h1>
  <p class="subtitle">Web Developer &amp; Engineering Student</p>
  <p class="bio">
    Second-year student at Industrial Technology Junior College, passionate about
    building software that solves real problems.
  </p>
  <div class="hero-buttons">
    <a href="#projects" class="btn-primary">View My Work</a>
    <a href="#contact" class="btn-outline">Contact Me</a>
  </div>
</section>

<!-- paste rest of your sections below... -->
 <!-- Projects -->
  <section id="projects">
    <div class="section-inner">
      <div class="section-header">
        <h2>My Projects</h2>
        <p>A collection of things I've built so far</p>
      </div>
      <div class="projects-grid">

        <div class="project-card">
          <div class="project-emoji">🎬</div>
          <h3>Movie Ranking <span class="first-badge">1st Project</span></h3>
          <p>My very first project — built when I had just started coding and only knew HTML. I wanted to put my new skills to use, so I made a ranked list of my top 3 all-time favourite movies: Interstellar, Avengers: Endgame, and Top Gun.</p>
          <div class="tags">
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
          </div>
          <a href="/movie-ranking.html" class="project-link">View Project →</a>
        </div>

        <div class="project-card">
          <div class="project-emoji">🎂</div>
          <h3>Birthday Invite <span class="first-badge">2nd Project</span></h3>
          <p>My second project, still early in my coding journey with just HTML knowledge. I challenged myself to build a birthday invitation page complete with event details, a wishlist, and a location link.</p>
          <div class="tags">
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
          </div>
          <a href="/birthday-invite.html" class="project-link">View Project →</a>
        </div>

        <div class="project-card">
          <div class="project-emoji">🚀</div>
          <h3>Space Game</h3>
          <p>A browser-based space game built during a mini hackathon with limited time. My first ever game — developed with AI tools, focused on fast delivery and fun gameplay.</p>
          <div class="tags">
            <span class="tag">HTML</span>
            <span class="tag">JavaScript</span>
            <span class="tag">CSS</span>
          </div>
          <div class="project-links">
            <a href="https://space-game-amber.vercel.app" target="_blank" rel="noopener" class="project-link">Live Demo →</a>
            <a href="https://github.com/Prashantsubedi12/Space-Game" target="_blank" rel="noopener" class="project-link">GitHub →</a>
          </div>
        </div>

        <div class="project-card">
          <div class="project-emoji">🌀</div>
          <h3>Maze Escape</h3>
          <p>A 2-player competitive maze game originally written in C for college. Ported to the browser — each player races through a randomly generated maze to reach the goal in the shortest time and fewest steps.</p>
          <div class="tags">
            <span class="tag">C Language</span>
            <span class="tag">JavaScript</span>
            <span class="tag">HTML</span>
          </div>
          <div class="project-links">
            <a href="/maze-escape.html" class="project-link">Play Game →</a>
            <a href="https://github.com/Prashantsubedi12/Maze-Escape-Game" target="_blank" rel="noopener" class="project-link">GitHub →</a>
          </div>
        </div>

        <div class="project-card">
          <div class="project-emoji">🎨</div>
          <h3>Mosaic Camera</h3>
          <p>A webcam interactive art tool built in Processing for 情報処理基礎実験. Ported to the browser — hold the mouse or press any key to shatter your live camera feed into mosaic blocks. Drag to control block size and color tone.</p>
          <div class="tags">
            <span class="tag">Processing</span>
            <span class="tag">JavaScript</span>
            <span class="tag">WebRTC</span>
          </div>
          <div class="project-links">
            <a href="/mosaic-cam.html" class="project-link">Try It →</a>
            <a href="https://github.com/Prashantsubedi12/Processing-mosaic-" target="_blank" rel="noopener" class="project-link">GitHub →</a>
          </div>
        </div>

        <div class="project-card">
          <div class="project-emoji">🔢</div>
          <h3>Binary Adventure</h3>
          <p>An interactive browser-based platform for learning binary numbers from scratch. Flip light bulbs, toggle magic boxes, play a prize guessing game, and watch an 8-bit counter machine — then test your knowledge with a 10-question quiz.</p>
          <div class="tags">
            <span class="tag">HTML</span>
            <span class="tag">JavaScript</span>
            <span class="tag">CSS</span>
          </div>
          <div class="project-links">
            <a href="/binary-adventure.html" class="project-link">Play →</a>
            <a href="https://github.com/Prashantsubedi12/binary-learning-project" target="_blank" rel="noopener" class="project-link">GitHub →</a>
          </div>
        </div>

        <div class="project-card">
          <div class="project-emoji">🐍</div>
          <h3>Python Adventure</h3>
          <p>A full interactive Python learning platform with 15 lessons, a live code playground, quiz arena, badge system, and XP progression. Includes 5 pro projects: Password Generator, Contact Book, Text Analyzer, Quiz Engine, and RPG Inventory.</p>
          <div class="tags">
            <span class="tag">HTML</span>
            <span class="tag">JavaScript</span>
            <span class="tag">CSS</span>
          </div>
          <div class="project-links">
            <a href="https://python-adventure-six.vercel.app" target="_blank" rel="noopener" class="project-link">Live Demo →</a>
            <a href="https://github.com/Prashantsubedi12/python-adventure" target="_blank" rel="noopener" class="project-link">GitHub →</a>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about">
    <div class="section-inner">
      <div class="section-header">
        <h2>About Me</h2>
        <p>A little about who I am</p>
      </div>
      <div class="about-grid">
        <div class="about-text">
          <p>
            I'm a second-year student majoring in
            <span>Information Processing Engineering</span>
            at Industrial Technology Junior College (産業技術短期大学).
          </p>
          <p>
            My curiosity drives me — from the low-level logic of C programming to the
            software engineering behind SpaceX's Falcon rocket landings.
          </p>
          <p>
            I'm also the founder of <span>Team Extra</span>, a programming club at my
            university dedicated to collaborative coding and exploring new tech stacks.
          </p>
        </div>
        <div>
          <p class="skills-title">Skills &amp; Interests</p>
          <div class="skills-list">
            <span class="skill-chip">C Language</span>
            <span class="skill-chip">HTML &amp; CSS</span>
            <span class="skill-chip">Web Development</span>
            <span class="skill-chip">Unity / Game Dev</span>
            <span class="skill-chip">JavaScript</span>
          </div>
          <div class="focus-card">
            <h4>Currently Focusing On</h4>
            <ul>
              <li>Preparing for the FE (Fundamental IT Engineer) Exam</li>
              <li>Game development with Unity</li>
              <li>Building more web projects</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <div class="section-inner">
      <div class="section-header">
        <h2>Get In Touch</h2>
        <p>I'm always open to new opportunities and conversations.</p>
      </div>
      <div class="contact-grid">
        <a href="mailto:prashantsubedi718@gmail.com" class="contact-card email">
          <div class="icon">
            <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
              <path d="M20 4H4C2.9 4 2 4.9 2 6v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4-8 5-8-5V6l8 5 8-5v2z"/>
            </svg>
          </div>
          <p class="label">Email</p>
          <p class="value">prashantsubedi718@gmail.com</p>
        </a>
        <a href="https://www.instagram.com/prashantsub12/" target="_blank" rel="noopener" class="contact-card insta">
          <div class="icon">
            <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
              <path d="M12 2.163c3.204 0 3.584.012 4.85.07 1.366.062 2.633.334 3.608 1.308.975.975 1.246 2.242 1.308 3.608.058 1.266.07 1.646.07 4.85s-.012 3.584-.07 4.85c-.062 1.366-.334 2.633-1.308 3.608-.975.975-2.242 1.246-3.608 1.308-1.266.058-1.646.07-4.85.07s-3.584-.012-4.85-.07c-1.366-.062-2.633-.334-3.608-1.308-.975-.975-1.246-2.242-1.308-3.608C2.175 15.584 2.163 15.204 2.163 12s.012-3.584.07-4.85c.062-1.366.334-2.633 1.308-3.608.975-.975 2.242-1.246 3.608-1.308C8.416 2.175 8.796 2.163 12 2.163zm0-2.163C8.741 0 8.332.013 7.052.072 5.197.157 3.355.673 2.014 2.014.673 3.355.157 5.197.072 7.052.013 8.332 0 8.741 0 12c0 3.259.013 3.668.072 4.948.085 1.855.601 3.697 1.942 5.038 1.341 1.341 3.183 1.857 5.038 1.942C8.332 23.987 8.741 24 12 24s3.668-.013 4.948-.072c1.855-.085 3.697-.601 5.038-1.942 1.341-1.341 1.857-3.183 1.942-5.038.059-1.28.072-1.689.072-4.948s-.013-3.668-.072-4.948c-.085-1.855-.601-3.697-1.942-5.038C20.645.673 18.803.157 16.948.072 15.668.013 15.259 0 12 0zm0 5.838a6.162 6.162 0 1 0 0 12.324A6.162 6.162 0 0 0 12 5.838zm0 10.162a4 4 0 1 1 0-8 4 4 0 0 1 0 8zm6.406-11.845a1.44 1.44 0 1 0 0 2.881 1.44 1.44 0 0 0 0-2.881z"/>
            </svg>
          </div>
          <p class="label">Instagram</p>
          <p class="value">@prashantsub12</p>
        </a>
        <a href="https://www.facebook.com/kshitij.subedi.12" target="_blank" rel="noopener" class="contact-card fb">
          <div class="icon">
            <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
              <path d="M24 12.073C24 5.405 18.627 0 12 0S0 5.405 0 12.073C0 18.1 4.388 23.094 10.125 24v-8.437H7.078v-3.49h3.047V9.41c0-3.025 1.792-4.697 4.532-4.697 1.312 0 2.686.236 2.686.236v2.97h-1.514c-1.491 0-1.956.93-1.956 1.886v2.267h3.328l-.532 3.49h-2.796V24C19.612 23.094 24 18.1 24 12.073z"/>
            </svg>
          </div>
          <p class="label">Facebook</p>
          <p class="value">Prashant Subedi</p>
        </a>
        <a href="https://github.com/Prashantsubedi12" target="_blank" rel="noopener" class="contact-card gh">
          <div class="icon">
            <svg viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
              <path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0 1 12 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/>
            </svg>
          </div>
          <p class="label">GitHub</p>
          <p class="value">Prashantsubedi12</p>
        </a>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    © 2025 Prashant Subedi · Built with HTML &amp; CSS
  </footer>
