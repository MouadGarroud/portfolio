<script>
  import profileImage from '../images/profile.jpg';
</script>

<header class="hero">
    <div class="hero-content">
      <img
        src={profileImage}
        alt="Mouad Garroud"
        class="profile-pic"
        width="140"
        height="140"
        loading="eager"
        decoding="async"
        fetchpriority="high"
      >
      <h1>Mouad Garroud</h1>
      <p>Développeur Web • Créateur d'expériences web modernes</p>
      <a href="#about" class="btn">En savoir plus</a>
    </div>

    <div class="hero-bg">
      <svg viewBox="0 0 800 200" preserveAspectRatio="none" class="water-svg">
        <path class="water-back">
          <animate attributeName="d" dur="10s" repeatCount="indefinite" values="M0,100 Q200,70 400,100 T800,100 L800,200 L0,200 Z;
                    M0,100 Q200,130 400,100 T800,100 L800,200 L0,200 Z;
                    M0,100 Q200,70 400,100 T800,100 L800,200 L0,200 Z" />
        </path>
        <path class="water">
          <animate attributeName="d" dur="7s" repeatCount="indefinite" values="M0,120 Q200,100 400,120 T800,120 L800,200 L0,200 Z;
                    M0,120 Q200,140 400,110 T800,130 L800,200 L0,200 Z;
                    M0,120 Q200,100 400,120 T800,120 L800,200 L0,200 Z" />
        </path>
      </svg>
    </div>
  </header>

  <!-- Inside lib/Header.svelte -->
<style>
  .hero {
    position: relative;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    overflow: hidden;
    background: linear-gradient(135deg, #0f172a, #1e293b);
  }

  :global(body.light) .hero {
    background: linear-gradient(135deg, #e2e8f0, #f8fafc);
  }

  .hero-content {
    position: relative;
    z-index: 10;
    animation: fadeInUp 1s ease;
    width: 90%;
  }

  .profile-pic {
    width: 140px;
    height: 140px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 20px;
    border: 3px solid rgba(255, 255, 255, 0.2);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
    transition: 0.3s ease;
  }

  .profile-pic:hover {
    transform: scale(1.05);
  }

  .hero h1 {
    font-size: clamp(2.5rem, 8vw, 4.5rem);
    color: var(--text-main);
    font-weight: 700;
    margin-bottom: 10px;
  }

  .hero-bg {
    position: absolute;
    bottom: -2px;
    left: 0;
    width: 100%;
    height: 25vh;
    z-index: 5;
    pointer-events: none;
  }

  .water-svg {
    width: 100%;
    height: 100%;
    display: block;
  }

  .water {
    fill: rgba(59, 130, 246, 0.5);
  }

  .water-back {
    fill: rgba(59, 130, 246, 0.2);
  }

  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>