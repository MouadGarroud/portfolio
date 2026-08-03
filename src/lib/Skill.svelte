<section class="section" id="technology">
  <h2 class="section-title">Stack Technique</h2>
  <div class="card">
    <!-- Core Stack / Front-end -->
    <div style="margin-bottom: 25px;">
      <h3
        style="color: var(--primary); margin-bottom: 12px; font-size: 1.2rem;"
      >
        🎨 Front-end
      </h3>
      <div class="skills-grid">
        <span class="skill-tag">TypeScript</span>
        <span class="skill-tag">JavaScript</span>
        <span class="skill-tag">Svelte</span>
        <span class="skill-tag">Angular</span>
        <span class="skill-tag">HTML5 / CSS3</span>
        <span class="skill-tag">Tailwind CSS</span>
        <span class="skill-tag">Bootstrap</span>
      </div>
    </div>

    <!-- Back-end & Architecture -->
    <div style="margin-bottom: 25px;">
      <h3
        style="color: var(--primary); margin-bottom: 12px; font-size: 1.2rem;"
      >
        ⚙️ Back-end
      </h3>
      <div class="skills-grid">
        <span class="skill-tag">Node.js</span>
        <span class="skill-tag">Express.js</span>
        <span class="skill-tag">PHP (Laravel)</span>
        <span class="skill-tag">Python</span>
        <span class="skill-tag">RESTful APIs</span>
      </div>
    </div>

    <!-- Databases & Caching -->
    <div style="margin-bottom: 25px;">
      <h3
        style="color: var(--primary); margin-bottom: 12px; font-size: 1.2rem;"
      >
        🗄️ Bases de données
      </h3>
      <div class="skills-grid">
        <span class="skill-tag">MySQL</span>
        <span class="skill-tag">MongoDB / Mongoose</span>
        <span class="skill-tag">Redis</span>
        <span class="skill-tag">SQL Server</span>
      </div>
    </div>

    <!-- Security, Testing & DevOps -->
    <div>
      <h3
        style="color: var(--primary); margin-bottom: 12px; font-size: 1.2rem;"
      >
        🛠️ DevOps, Sécurité & Outils
      </h3>
      <div class="skills-grid">
        <span class="skill-tag">Docker</span>
        <span class="skill-tag">Git / GitHub</span>
        <span class="skill-tag">CI/CD</span>
        <span class="skill-tag">JWT & Web Security</span>
        <span class="skill-tag">Unit Testing (Jest)</span>
        <span class="skill-tag">Postman</span>
        <span class="skill-tag">Vite</span>
        <span class="skill-tag">Figma / UML</span>
        <div class="libraries-list">
          <p>
            <strong>📦 Librairies & Utilitaires :</strong> Multer, Sharp, Nodemailer,
            Winston, Morgan, Helmet, CORS, Rate Limiting, Joi, Bcrypt, Inno Setup
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Inside lib/Skill.svelte -->
<style>
  .libraries-list {
    margin-top: 20px;
    padding-top: 15px;
    border-top: 1px dashed #333;
    font-size: 0.85rem;
    color: var(--text-dim);
  }
  .skills-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 20px;
  }

  .skill-tag {
    background: rgba(59, 130, 246, 0.1);
    border: 1px solid rgba(59, 130, 246, 0.3);
    padding: 8px 18px;
    border-radius: 10px;
    font-size: 0.9rem;
    color: var(--primary);
    font-weight: 600;
  }
</style>
