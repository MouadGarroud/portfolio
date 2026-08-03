<section class="section" id="certifications">
  <h2 class="section-title">Certifications</h2>
  <div class="certifications-grid">
    <!-- Certification Data Structures & Algorithms pour AI & Software (Nouveau) -->
    <div class="cert-card card">
      <div class="cert-icon-container">
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="cert-svg"
        >
          <path d="M12 15l-2 5l-1.5-1.5L6 20l2-5"></path>
          <path d="M12 15l2 5l1.5-1.5L18 20l-2-5"></path>
          <circle cx="12" cy="10" r="4"></circle>
          <path d="M8.5 13.5l1.5-1.5M15.5 13.5l-1.5-1.5"></path>
        </svg>
      </div>
      <div class="cert-info">
        <h3>Data Structures & Algorithms pour AI & Software</h3>
        <p class="issuer">Orange</p>
        <p class="cert-date">25 Juin 2026</p>
      </div>
    </div>

    <!-- Certification Rédiger des cahiers des charges avec l'IA -->
    <div class="cert-card card">
      <div class="cert-icon-container">
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="cert-svg"
        >
          <path d="M12 15l-2 5l-1.5-1.5L6 20l2-5"></path>
          <path d="M12 15l2 5l1.5-1.5L18 20l-2-5"></path>
          <circle cx="12" cy="10" r="4"></circle>
          <path d="M8.5 13.5l1.5-1.5M15.5 13.5l-1.5-1.5"></path>
        </svg>
      </div>
      <div class="cert-info">
        <h3>Rédiger des cahiers des charges avec l'IA</h3>
        <p class="issuer">Orange</p>
        <p class="cert-date">21 Mai 2026</p>
      </div>
    </div>

    <!-- Certification Booster Tailwind avec l’AI -->
    <div class="cert-card card">
      <div class="cert-icon-container">
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="cert-svg"
        >
          <path d="M12 15l-2 5l-1.5-1.5L6 20l2-5"></path>
          <path d="M12 15l2 5l1.5-1.5L18 20l-2-5"></path>
          <circle cx="12" cy="10" r="4"></circle>
          <path d="M8.5 13.5l1.5-1.5M15.5 13.5l-1.5-1.5"></path>
        </svg>
      </div>
      <div class="cert-info">
        <h3>Booster Tailwind avec l'IA</h3>
        <p class="issuer">Orange</p>
        <p class="cert-date">18 et 19 Mai 2026</p>
      </div>
    </div>

    <!-- Certification UI/UX Generative AI -->
    <div class="cert-card card">
      <div class="cert-icon-container">
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="cert-svg"
        >
          <path d="M12 15l-2 5l-1.5-1.5L6 20l2-5"></path>
          <path d="M12 15l2 5l1.5-1.5L18 20l-2-5"></path>
          <circle cx="12" cy="10" r="4"></circle>
          <path d="M8.5 13.5l1.5-1.5M15.5 13.5l-1.5-1.5"></path>
        </svg>
      </div>
      <div class="cert-info">
        <h3>UI/UX Generative AI</h3>
        <p class="issuer">Orange</p>
        <p class="cert-date">12 et 13 Mai 2026</p>
      </div>
    </div>

    <!-- Certification JavaScript -->
    <div class="cert-card card">
      <div class="cert-icon-container">
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="cert-svg"
        >
          <path d="M12 15l-2 5l-1.5-1.5L6 20l2-5"></path>
          <path d="M12 15l2 5l1.5-1.5L18 20l-2-5"></path>
          <circle cx="12" cy="10" r="4"></circle>
          <path d="M8.5 13.5l1.5-1.5M15.5 13.5l-1.5-1.5"></path>
        </svg>
      </div>
      <div class="cert-info">
        <h3>JavaScript</h3>
        <p class="issuer">Simplilearn</p>
        <p class="cert-date">25 Septembre 2025</p>
      </div>
    </div>

    <!-- Certification PHP -->
    <div class="cert-card card">
      <div class="cert-icon-container">
        <svg
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="1.5"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="cert-svg"
        >
          <path d="M12 15l-2 5l-1.5-1.5L6 20l2-5"></path>
          <path d="M12 15l2 5l1.5-1.5L18 20l-2-5"></path>
          <circle cx="12" cy="10" r="4"></circle>
          <path d="M8.5 13.5l1.5-1.5M15.5 13.5l-1.5-1.5"></path>
        </svg>
      </div>
      <div class="cert-info">
        <h3>PHP</h3>
        <p class="issuer">Orange</p>
        <p class="cert-date">25 et 26 Juin 2025</p>
      </div>
    </div>
  </div>
</section>

<!-- Inside lib/Certificat.svelte -->
<style>
  .certifications-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    margin-top: 30px;
  }

  .cert-card {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    padding: 25px;
    transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
    border: 1px solid transparent;
  }

  .cert-card:hover {
    transform: translateY(-5px);
    border-color: rgba(52, 152, 219, 0.3);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  }

  .cert-icon-container {
    flex-shrink: 0;
    width: 45px;
    height: 45px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(52, 152, 219, 0.1);
    border-radius: 12px;
    color: var(--primary);
    margin-top: 2px;
  }

  .cert-svg {
    width: 26px;
    height: 26px;
    transition: transform 0.3s ease;
  }

  .cert-card:hover .cert-svg {
    transform: scale(1.1) rotate(5deg);
  }

  .cert-info h3 {
    margin: 0;
    font-size: 1.15rem;
    font-weight: 600;
    line-height: 1.3;
  }

  .issuer {
    margin: 4px 0;
    font-weight: 500;
    color: var(--primary);
    font-size: 0.9rem;
  }

  .cert-date {
    margin: 0;
    font-size: 0.8rem;
    opacity: 0.7;
  }
</style>