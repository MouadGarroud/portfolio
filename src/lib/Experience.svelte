<section class="section" id="experience">
    <h2 class="section-title">Expériences</h2>
    <div class="timeline">
        <!-- Carrefour Market -->
        <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-date">Janvier 2026</div>
            <div class="timeline-content card">
                <h3>Merchandiser | Carrefour Market</h3>
                <p class="location">Sala El Jadida</p>
                <p>
                    Gestion opérationnelle du département PGC : mise à jour des
                    prix, affiches et étiquetage. Contrôle rigoureux de la
                    présentation en rayon.
                </p>
                <div class="tech-stack">
                    <span>PDA</span> <span>Excel</span>
                </div>
            </div>
        </div>

        <!-- Ministère de la Culture -->
        <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-date">Mai – Juin 2025</div>
            <div class="timeline-content card">
                <h3>
                    Développeur Full Stack | Ministère de la jeunesse de la
                    Culture et de la Communication - Département de la Culture
                </h3>
                <p class="location">Rabat — Stage ( PFE - Hybride )</p>
                <p>
                    Développement d'une plateforme de gestion des inscriptions
                    pour une école de musique. Gestion des données personnelles,
                    validation et suivi des dossiers.
                </p>
                <div class="tech-stack">
                    <span>Laravel</span> <span>MySQL</span>
                    <span>Bootstrap 5</span> <span>HTML5/CSS3</span>
                    <span>JavaScript</span> <span>PHP</span>
                </div>
            </div>
        </div>

        <!-- Zatec -->
        <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-date">Mai – Juin 2025</div>
            <div class="timeline-content card">
                <h3>Développeur Full Stack | Zatec</h3>
                <p class="location">Rabat — Stage Présentiel </p>
                <p>
                    Conception et développement d'un système d'authentification
                    sécurisé pour un site e-commerce (Inscription, Connexion,
                    Profil).
                </p>
                <div class="tech-stack">
                    <span>Laravel</span> <span>MySQL</span>
                    <span>Bootstrap 5</span> <span>HTML5/CSS3</span>
                    <span>JavaScript</span> <span>PHP</span>
                </div>
            </div>
        </div>

        <!-- Société Abdelouaret -->
        <div class="timeline-item">
            <div class="timeline-dot"></div>
            <div class="timeline-date">Juin 2024</div>
            <div class="timeline-content card">
                <h3>Assistant Informatique | Abdelouaret d’Électricité</h3>
                <p class="location">Salé — Stage (1 mois)</p>
                <p>
                    Support utilisateur de proximité : installation,
                    configuration et dépannage matériel et logiciel (Maintenance
                    parc informatique).
                </p>
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

    .location {
        font-size: 0.85rem;
        color: #64748b;
        margin-bottom: 12px;
        font-weight: 500;
    }

    .tech-stack {
        margin-top: 15px;
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
    }

    .tech-stack span {
        background: rgba(52, 152, 219, 0.1);
        color: var(--primary);
        padding: 3px 12px;
        border-radius: 20px;
        font-size: 0.7rem;
        font-weight: bold;
        border: 1px solid var(--primary);
    }

    .timeline-content.card {
        transition:
            transform 0.3s ease,
            box-shadow 0.3s ease;
    }

    .timeline-content.card:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    }
</style>
