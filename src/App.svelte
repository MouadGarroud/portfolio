<script>
  import Header from "./lib/Header.svelte";
  import About from "./lib/About.svelte";
  import Project from "./lib/Project.svelte";
  import Skill from "./lib/Skill.svelte";
  import Experience from "./lib/Experience.svelte";
  import Education from "./lib/Education.svelte";
  import Certificat from "./lib/Certificat.svelte";
  import Contact from "./lib/Contact.svelte";
  import Footer from "./lib/Footer.svelte";

  // 1. Initialize state from the DOM (already configured by the script in <head>)
  let isLight = $state(
    typeof document !== "undefined" &&
      document.documentElement.classList.contains("light")
  );
  let isToggleHidden = $state(false);

  // 2. Toggle function with LocalStorage persistence
  function toggleMode() {
    isLight = !isLight;
    document.documentElement.classList.toggle("light", isLight);
    document.body.classList.toggle("light", isLight); // Keep body class if your CSS targets body
    localStorage.setItem("theme", isLight ? "light" : "dark");
  }

  $effect(() => {
    document.body.classList.toggle("light", isLight);

    const mediaQuery = window.matchMedia("(prefers-color-scheme: light)");
    // @ts-ignore
    const handleSystemThemeChange = (e) => {
      if (!localStorage.getItem("theme")) {
        isLight = e.matches;
        document.documentElement.classList.toggle("light", isLight);
        document.body.classList.toggle("light", isLight);
      }
    };

    mediaQuery.addEventListener("change", handleSystemThemeChange);

    const sectionObserver = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) entry.target.classList.add("visible");
        });
      },
      { threshold: 0.1 }
    );

    document
      .querySelectorAll(".section")
      .forEach((sec) => sectionObserver.observe(sec));

    const footerEl = document.querySelector("footer");
    // @ts-ignore
    let footerObserver;

    if (footerEl) {
      footerObserver = new IntersectionObserver(
        (entries) => {
          entries.forEach((entry) => {
            isToggleHidden = entry.isIntersecting;
          });
        },
        { threshold: 0 }
      );

      footerObserver.observe(footerEl);
    }

    return () => {
      mediaQuery.removeEventListener("change", handleSystemThemeChange);
      sectionObserver.disconnect();
      // @ts-ignore
      if (footerObserver) footerObserver.disconnect();
    };
  });
</script>

<header id="header">
  <Header />
</header>

<main class="container">
  <button
    class="toggle"
    class:hidden={isToggleHidden}
    onclick={toggleMode}
    aria-label="Toggle theme"
  >
    <span>{isLight ? "☀️" : "🌙"}</span>
  </button>

  <section id="about" class="section"><About /></section>
  <section id="project" class="section"><Project /></section>
  <section id="skill" class="section"><Skill /></section>
  <section id="experience" class="section"><Experience /></section>
  <section id="education" class="section"><Education /></section>
  <section id="certificat" class="section"><Certificat /></section>
  <section id="contact" class="section"><Contact /></section>
</main>

<footer id="footer">
  <Footer />
</footer>

<style>
  .container {
    width: 90%;
    max-width: 1200px;
    margin: 100px auto;
  }

  .section {
    margin-bottom: 80px;
    opacity: 0;
    transform: translateY(30px);
    transition: 0.8s ease-out;
  }

  :global(.section.visible) {
    opacity: 1;
    transform: translateY(0);
  }

  .toggle {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 55px;
    height: 55px;
    background: var(--primary);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    z-index: 100;
    font-size: 1.5rem;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
    border: none;
    color: white;
    transition: var(--transition);
  }

  .toggle.hidden {
    opacity: 0;
    transform: scale(0.8);
    visibility: hidden;
  }
</style>