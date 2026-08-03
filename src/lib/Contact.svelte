<section class="section" id="contact">
    <h2 class="section-title">Me Contacter</h2>
    <div class="contact-container">
        <div class="card contact-card">
            <p class="contact-text">
                Vous avez un projet en tête ou une opportunité de collaboration
                ? N'hésitez pas à me contacter !
            </p>

            <div class="contact-grid">
                <!-- Email -->
                <a href="mailto:mouadgarroud@gmail.com" class="contact-item">
                    <div class="icon-box">
                        <svg
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        >
                            <path
                                d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"
                            ></path>
                            <polyline points="22,6 12,13 2,6"></polyline>
                        </svg>
                    </div>
                    <span>mouadgarroud@gmail.com</span>
                </a>
            </div>
        </div>
    </div>
</section>

<!-- Inside lib/Contact.svelte -->
<style>
  .contact-container {
    max-width: 700px;
    margin: 0 auto;
  }

  .contact-card {
    text-align: center;
    padding: 40px !important;
  }

  .contact-text {
    margin-bottom: 30px;
    opacity: 0.8;
    line-height: 1.6;
  }

  .contact-grid {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }

  .contact-item {
    display: flex;
    align-items: center;
    gap: 15px;
    padding: 15px 20px;
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(52, 152, 219, 0.1);
    border-radius: 12px;
    text-decoration: none;
    color: var(--text-main);
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    min-width: 0;
  }

  .icon-box {
    width: 40px;
    height: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: var(--primary);
    color: white;
    border-radius: 10px;
    transition: transform 0.3s ease;
  }

  .icon-box :global(svg) {
    width: 20px;
    height: 20px;
  }

  .contact-item span {
    font-weight: 500;
    font-size: 1.1rem;
    min-width: 0;
    overflow-wrap: anywhere;
  }

  .contact-item:hover {
    background: rgba(52, 152, 219, 0.1);
    border-color: var(--primary);
    transform: translateX(10px);
  }

  .contact-item:hover .icon-box {
    transform: scale(1.1) rotate(-5deg);
    box-shadow: 0 5px 15px rgba(52, 152, 219, 0.3);
  }

  @media (max-width: 600px) {
    .contact-item {
      flex-direction: row;
      align-items: center;
      justify-content: flex-start;
      gap: 12px;
      padding: 14px 16px;
    }

    .icon-box {
      width: 34px;
      height: 34px;
      border-radius: 9px;
      flex-shrink: 0;
    }

    .icon-box :global(svg) {
      width: 17px;
      height: 17px;
    }

    .contact-item span {
      font-size: 0.78rem;
      line-height: 1.2;
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
    }
  }
</style>