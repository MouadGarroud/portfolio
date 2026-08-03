<section class="section" id="education">
    <h2 class="section-title">Éducation & Formations</h2>
    <div class="timeline">
        <!-- Job In Tech -->
        <div class="timeline-item">
            <div class="timeline-dot edu-dot"></div>
            <div class="timeline-date">Juin – Décembre 2025</div>
            <div class="timeline-content card">
                <h3>Formation Développeur Full Stack</h3>
                <p>
                    <strong
                        >École High-Tech | Programme Job In Tech, Rabat</strong
                    >
                </p>
                <p>
                    Spécialisation intensive sur les technologies web modernes
                    et l'agilité logicielle.
                </p>
            </div>
        </div>

        <!-- Miage -->
        <div class="timeline-item">
            <div class="timeline-dot edu-dot"></div>
            <div class="timeline-date">2023 – 2025</div>
            <div class="timeline-content card">
                <h3>Technicien Spécialisé en Développement Informatique</h3>
                <p><strong>École Miage, Salé</strong></p>
            </div>
        </div>

        <!-- Université Mohammed V -->
        <div class="timeline-item">
            <div class="timeline-dot edu-dot"></div>
            <div class="timeline-date">2022 – 2023</div>
            <div class="timeline-content card">
                <h3>Physique Chimie (MPC)</h3>
                <p><strong>Université Mohammed V, Rabat</strong></p>
            </div>
        </div>

        <!-- Baccalauréat -->
        <div class="timeline-item">
            <div class="timeline-dot edu-dot"></div>
            <div class="timeline-date">2021 – 2022</div>
            <div class="timeline-content card">
                <h3>Baccalauréat Sciences de la Vie et de la Terre (SVT)</h3>
                <p><strong>Lycée Al Mander Al Jamil, Salé</strong></p>
            </div>
        </div>
    </div>
</section>

<!-- Inside lib/Experience.svelte & lib/Education.svelte -->
<style>
  .timeline {
    position: relative;
    max-width: 850px;
    margin: 30px auto;
    padding-left: 30px;
    border-left: 2px solid var(--primary);
  }

  .timeline-item {
    position: relative;
    margin-bottom: 40px;
  }

  .timeline-dot {
    position: absolute;
    left: -42px;
    top: 10px;
    width: 20px;
    height: 20px;
    background: var(--primary);
    border: 4px solid var(--bg-dark);
    border-radius: 50%;
  }

  .edu-dot {
    background: #f39c12;
  }

  .timeline-date {
    font-size: 0.85rem;
    font-weight: 600;
    color: var(--primary);
    margin-bottom: 5px;
    display: block;
  }

  .timeline-content h3 {
    margin: 0 0 5px 0;
    font-size: 1.15rem;
  }

  .timeline-content.card {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .timeline-content.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
  }
</style>