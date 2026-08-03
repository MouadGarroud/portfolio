<script lang="ts">
    import { onMount } from "svelte";

    function getProjectArt(label: string, accent: string) {
        const svg = `
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 420" role="img" aria-label="${label}">
                <defs>
                    <linearGradient id="g" x1="0" x2="1" y1="0" y2="1">
                        <stop offset="0%" stop-color="#0f172a"/>
                        <stop offset="100%" stop-color="${accent}"/>
                    </linearGradient>
                </defs>
                <rect width="800" height="420" fill="url(#g)"/>
                <rect x="34" y="34" width="732" height="352" rx="22" fill="rgba(255,255,255,0.06)" stroke="rgba(255,255,255,0.18)"/>
                <circle cx="130" cy="150" r="52" fill="rgba(255,255,255,0.08)"/>
                <circle cx="660" cy="120" r="72" fill="rgba(255,255,255,0.06)"/>
                <rect x="92" y="224" width="220" height="18" rx="9" fill="rgba(255,255,255,0.85)"/>
                <rect x="92" y="260" width="300" height="14" rx="7" fill="rgba(255,255,255,0.6)"/>
                <rect x="92" y="286" width="260" height="14" rx="7" fill="rgba(255,255,255,0.45)"/>
                <text x="92" y="170" fill="white" font-size="42" font-family="Segoe UI, Arial, sans-serif" font-weight="700">${label}</text>
            </svg>
        `;

        return `data:image/svg+xml;charset=UTF-8,${encodeURIComponent(svg)}`;
    }

    let cards: (HTMLElement | null)[] = [];
    let visibleCount = 0;
    let loadMoreBtn: HTMLElement | undefined;

    function updateCardVisibility() {
        cards.forEach((card, index) => {
            if (!card) return;
            card.classList.toggle("hidden", index >= visibleCount);
        });

        if (loadMoreBtn) {
            const hasMore = visibleCount < cards.length;
            loadMoreBtn.style.display = hasMore ? "inline-flex" : "none";
        }
    }

    function applyProjectVisibility() {
        const width = window.innerWidth;
        const initialVisible = width <= 600 ? 3 : width <= 1024 ? 4 : cards.length;
        visibleCount = initialVisible;
        updateCardVisibility();
    }

    function loadMoreProjects() {
        const width = window.innerWidth;
        const step = width <= 600 ? 3 : 4;
        visibleCount = Math.min(cards.length, visibleCount + step);
        updateCardVisibility();
    }

    onMount(() => {
        applyProjectVisibility();
        window.addEventListener("resize", applyProjectVisibility);

        return () => window.removeEventListener("resize", applyProjectVisibility);
    });
</script>

<section class="section" id="projects">
    <h2 class="section-title">Projets</h2>
    <div class="projects-grid">
        <!-- Kinesics (Nouveau) -->
        <div class="project-card" bind:this={cards[0]}>
            <img
                src={getProjectArt("Kinesics", "#3b82f6")}
                alt="Kinesics - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>Kinesics</h3>
                <p>
                    Application web d’apprentissage de la langue des signes
                    permettant aux utilisateurs d’apprendre l’alphabet anglais,
                    l’alphabet arabe et les signes de base grâce à des leçons
                    interactives et des illustrations de gestes.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/Kinesics"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>

        <!-- DBlocker -->
        <div class="project-card" bind:this={cards[1]}>
            <img
                src={getProjectArt("DBlocker", "#22c55e")}
                alt="DBlocker - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>DBlocker</h3>
                <p>
                    Extension Chrome légère et open source qui bloque
                    instantanément les domaines indésirables et ferme
                    automatiquement les onglets lorsqu'un site bloqué est
                    ouvert. Améliore la concentration et réduit les
                    distractions.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/DBlocker"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>

        <!-- PIP -->
        <div class="project-card" bind:this={cards[2]}>
            <img
                src={getProjectArt("PIP", "#a855f7")}
                alt="PIP - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>PIP</h3>
                <p>
                    Outil open source permettant le mode Picture-in-Picture
                    (PiP) pour n'importe quelle vidéo sur le web. Simple, rapide
                    et extensible — accélère les flux de travail de
                    développement.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/PIP"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>

        <!-- PicShot -->
        <div class="project-card" bind:this={cards[3]}>
            <img
                src={getProjectArt("PicShot", "#f59e0b")}
                alt="PicShot - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>PicShot</h3>
                <p>
                    Extension légère et facile à utiliser pour prendre des
                    captures d'écran plein écran ou d'une zone spécifique de
                    n'importe quelle page web, puis les télécharger
                    instantanément.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/PicShot"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>

        <!-- DID-You -->
        <div class="project-card" bind:this={cards[4]}>
            <img
                src={getProjectArt("DID-You", "#14b8a6")}
                alt="DID-You - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>DID-You</h3>
                <p>
                    Application simple de liste de tâches pour gérer la
                    progression des tâches avec recherche, filtres et gestion de
                    profil utilisateur. (Code en cours de refactorisation)
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/Did-You_fr"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">Frontend</a
                    >
                    <a
                        href="https://github.com/MouadGarroud/Did-you_bc"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">Backend</a
                    >
                </div>
            </div>
        </div>

        <!-- Convertix -->
        <div class="project-card" bind:this={cards[5]}>
            <img
                src={getProjectArt("Convertix", "#ef4444")}
                alt="Aperçu du projet PDF Converter sur GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>Convertix</h3>
                <p>
                    Outil léger et intuitif qui vous permet de convertir entre
                    les formats DOCX et PDF en un seul clic. Interface propre et
                    simple pour une conversion rapide de documents.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/Convertix"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>

        <!-- SPassword -->
        <div class="project-card" bind:this={cards[6]}>
            <img
                src={getProjectArt("SPassword", "#ec4899")}
                alt="SPassword - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>SPassword</h3>
                <p>
                    Générateur de mots de passe simple avec une interface
                    élégante. Créez des mots de passe robustes, copiez-les
                    facilement, avec des fonds en dégradé et des boutons
                    interactifs.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/SPassword"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>

        <!-- Downloader -->
        <div class="project-card" bind:this={cards[7]}>
            <img
                src={getProjectArt("Downloader", "#8b5cf6")}
                alt="Downloader - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>Downloader</h3>
                <p>
                    Outil conçu pour télécharger des vidéos et de l'audio depuis
                    de nombreuses plateformes aux formats MP3 ou MP4. Utilise
                    yt-dlp et moviepy pour une conversion fluide.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/Downloder"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>

        <!-- Encrypt -->
        <div class="project-card" bind:this={cards[8]}>
            <img
                src={getProjectArt("Encrypt", "#06b6d4")}
                alt="Encrypt - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>Encrypt</h3>
                <p>
                    Application sécurisée de cryptage et décryptage de fichiers
                    avec stéganographie. Cachez des sels cryptographiques au
                    sein d'images et protégez vos fichiers avec des clés basées
                    sur des mots de passe.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/Encrypt"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>

        <!-- Contact-Form -->
        <div class="project-card" bind:this={cards[9]}>
            <img
                src={getProjectArt("Contact Form", "#f97316")}
                alt="Contact-form - Aperçu GitHub"
                width="380"
                height="190"
                loading="lazy"
                decoding="async"
            />
            <div class="project-content">
                <h3>Contact-Form</h3>
                <p>
                    Formulaire de contact web avec popup et backend PHP/MySQL.
                    Inclut des validations, l'intégration d'une base de données
                    et une limite d'un message par heure.
                </p>
                <div class="project-buttons">
                    <a
                        href="https://github.com/MouadGarroud/Contact-form"
                        class="btn-outline"
                        target="_blank"
                        rel="noopener noreferrer">GitHub</a
                    >
                </div>
            </div>
        </div>
    </div>
    <div class="more-btn-container">
        <button
            id="loadMore"
            class="btn-outline"
            bind:this={loadMoreBtn}
            on:click={loadMoreProjects}
        >
            Plus
        </button>
    </div>
</section>

<!-- Inside lib/Project.svelte -->
<style>
    .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 30px;
    }

    @media (min-width: 1025px) {
        .projects-grid {
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        }
    }

    .project-card {
        background: var(--card-bg);
        border-radius: 18px;
        overflow: hidden;
        box-shadow: 0 15px 40px rgba(0, 0, 0, 0.25);
        transition: 0.3s ease;
        display: flex;
        flex-direction: column;
    }

    .project-card:hover {
        transform: translateY(-8px);
    }

    :global(.project-card.hidden) {
        display: none !important;
    }

    .project-card img {
        width: 100%;
        height: 140px;
        object-fit: cover;
    }

    .project-content {
        padding: 20px;
        display: flex;
        flex-direction: column;
        flex: 1;
    }

    .project-content h3 {
        margin-bottom: 10px;
        color: var(--text-main);
    }

    .project-content p {
        color: var(--text-dim);
        font-size: 0.95rem;
        flex: 1;
        line-height: 1.5;
    }

    .project-buttons {
        margin-top: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding-top: 15px;
        gap: 5px;
    }

    .project-buttons .btn-outline {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
        padding: 10px 24px;
        background: transparent;
        border: 1.5px solid var(--primary);
        color: var(--primary);
        border-radius: 10px;
        text-decoration: none;
        font-size: 0.9rem;
        font-weight: 700;
        transition: all 0.3s ease;
        cursor: pointer;
        min-width: 120px;
    }

    .project-buttons .btn-outline:hover {
        background: var(--primary);
        color: #f8fafc;
        transform: translateY(-2px);
        box-shadow: 0 5px 15px rgba(29, 78, 216, 0.28);
    }

    .project-buttons .btn-outline::before {
        content: "";
        display: inline-block;
        width: 16px;
        height: 16px;
        -webkit-mask-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12'/%3E%3C/svg%3E");
        mask-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12'/%3E%3C/svg%3E");
        -webkit-mask-repeat: no-repeat;
        mask-repeat: no-repeat;
        -webkit-mask-size: contain;
        mask-size: contain;
        background-color: #24292e;
        transition:
            transform 0.3s ease,
            background-color 0.3s ease;
    }

    .project-buttons .btn-outline:hover::before {
        transform: rotate(5deg);
    }

    .more-btn-container {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 50px;
        margin-bottom: 20px;
    }

    #loadMore {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
        padding: 12px 35px;
        background: transparent;
        border: 2px solid var(--primary);
        color: var(--primary);
        border-radius: 12px;
        text-decoration: none;
        font-size: 1rem;
        font-weight: 600;
        transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        cursor: pointer;
        outline: none;
    }

    #loadMore:hover {
        background: var(--primary);
        color: white;
        transform: translateY(-3px);
        box-shadow: 0 8px 20px rgba(59, 130, 246, 0.4);
    }

    #loadMore:active {
        transform: translateY(-1px);
    }
</style>
