<footer class="footer">
    <div class="footer-content">
        <div class="footer-info">
            <p class="copyright">© 2026 <span>Mouad Garroud</span></p>
            <p class="footer-tagline">
                Développeur Web • Créateur de solutions numériques.
            </p>
        </div>

        <div class="footer-socials">
            <!-- Email (Nouveau) -->
            <a
                href="mailto:mouadgarroud@gmail.com"
                aria-label="Envoyer un e-mail"
            >
                <svg
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="footer-svg"
                >
                    <path
                        d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
                    ></path>
                    <polyline points="22,6 12,13 2,6"></polyline>
                </svg>
            </a>

            <!-- LinkedIn -->
            <a
                href="https://linkedin.com/in/mouadgarroud"
                target="_blank"
                aria-label="LinkedIn"
            >
                <svg
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="footer-svg"
                >
                    <path
                        d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"
                    ></path>
                    <rect x="2" y="9" width="4" height="12"></rect>
                    <circle cx="4" cy="4" r="2"></circle>
                </svg>
            </a>

            <!-- GitHub -->
            <a
                href="https://github.com/MouadGarroud"
                target="_blank"
                aria-label="GitHub"
            >
                <svg
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="footer-svg"
                >
                    <path
                        d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"
                    ></path>
                </svg>
            </a>
        </div>
    </div>
</footer>

<!-- Inside lib/Footer.svelte -->
<style>
    .footer {
        padding: 50px 0 30px;
        background: var(--bg-dark);
        border-top: 1px solid rgba(255, 255, 255, 0.05);
        margin-top: 100px;
    }

    .footer-content {
        max-width: 1100px;
        margin: 0 auto;
        padding: 0 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 20px;
    }

    .copyright {
        font-size: 1rem;
        margin: 0;
        color: var(--text-main);
        opacity: 1;
    }

    .copyright span {
        color: var(--text-main);
        font-weight: 700;
    }

    .footer-tagline {
        font-size: 0.85rem;
        color: var(--text-dim);
        opacity: 1;
        margin: 5px 0 0;
    }

    .footer-socials {
        display: flex;
        gap: 15px;
    }

    .footer-socials a {
        color: var(--text-main);
        opacity: 0.8;
        transition: all 0.3s ease;
        display: flex;
        align-items: center;
    }

    .footer-svg {
        width: 20px;
        height: 20px;
    }

    .footer-socials a:hover {
        color: var(--primary);
        opacity: 1;
        transform: translateY(-3px);
    }

    @media (max-width: 600px) {
        .footer-content {
            flex-direction: column;
            text-align: center;
        }

        .footer-socials {
            justify-content: center;
        }
    }
</style>
