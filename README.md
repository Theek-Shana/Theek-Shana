import { useState, useEffect } from "react";

const skills = [
  { name: "HTML", icon: "🌐" },
  { name: "CSS", icon: "🎨" },
  { name: "JavaScript", icon: "⚡" },
  { name: "TypeScript", icon: "🔷" },
  { name: "React", icon: "⚛️" },
  { name: "Node.js", icon: "🟢" },
  { name: "Express", icon: "🚂" },
  { name: "Python", icon: "🐍" },
  { name: "Java", icon: "☕" },
  { name: "PHP", icon: "🐘" },
  { name: "MySQL", icon: "🗄️" },
  { name: "MongoDB", icon: "🍃" },
];

const projects = [
  {
    emoji: "👁️",
    title: "Eye-Tracking Assistive System",
    desc: "Real-time hands-free computer control using gaze detection and computer vision for accessibility.",
    tags: ["Python", "OpenCV", "MediaPipe", "React"],
    color: "#6366f1",
  },
  {
    emoji: "📚",
    title: "Online Book Store",
    desc: "Full-stack bookstore with authentication, book management, and SQL database integration.",
    tags: ["Java", "Servlets", "MySQL", "CSS"],
    color: "#8b5cf6",
  },
  {
    emoji: "🌡️",
    title: "Temperature Prediction",
    desc: "Machine learning model predicting minimum temperature using historical data and regression.",
    tags: ["Python", "Scikit-learn", "Pandas"],
    color: "#a78bfa",
  },
];

export default function App() {
  const [scrolled, setScrolled] = useState(false);
  const [activeSection, setActiveSection] = useState("home");

  useEffect(() => {
    const onScroll = () => setScrolled(window.scrollY > 40);
    window.addEventListener("scroll", onScroll);
    return () => window.removeEventListener("scroll", onScroll);
  }, []);

  const scrollTo = (id) => {
    document.getElementById(id)?.scrollIntoView({ behavior: "smooth" });
  };

  return (
    <div style={styles.root}>
      <style>{css}</style>

      {/* NAV */}
      <nav style={{ ...styles.nav, ...(scrolled ? styles.navScrolled : {}) }}>
        <span style={styles.navLogo}>TV</span>
        <div style={styles.navLinks}>
          {["about", "skills", "projects", "contact"].map((s) => (
            <button key={s} style={styles.navBtn} onClick={() => scrollTo(s)}>
              {s}
            </button>
          ))}
        </div>
      </nav>

      {/* HERO */}
      <section style={styles.hero}>
        <div style={styles.heroGlow} />
        <div style={styles.heroDots} />
        <div style={styles.heroContent} className="fade-in">
          <div style={styles.badge}>Available for opportunities</div>
          <h1 style={styles.heroTitle}>
            Theekshana
            <br />
            <span style={styles.heroAccent}>Vidushan</span>
          </h1>
          <p style={styles.heroRole}>
            Software Engineer &nbsp;·&nbsp; Full-Stack Developer &nbsp;·&nbsp; Designer
          </p>
          <p style={styles.heroDesc}>
            Building modern, scalable applications and turning ideas into
            real-world solutions through clean code and creative thinking.
          </p>
          <div style={styles.heroCtas}>
            <button style={styles.ctaPrimary} onClick={() => scrollTo("projects")}>
              View Projects
            </button>
            <button style={styles.ctaSecondary} onClick={() => scrollTo("contact")}>
              Contact Me
            </button>
          </div>
        </div>
        <div style={styles.heroCard} className="fade-in-delay">
          <div style={styles.cardLine}>
            <span style={styles.cardDot} />
            <span style={styles.cardLabel}>Status</span>
            <span style={styles.cardValue}>Open to work</span>
          </div>
          <div style={styles.cardLine}>
            <span style={{ ...styles.cardDot, background: "#60a5fa" }} />
            <span style={styles.cardLabel}>Focus</span>
            <span style={styles.cardValue}>Full-Stack Dev</span>
          </div>
          <div style={styles.cardLine}>
            <span style={{ ...styles.cardDot, background: "#a78bfa" }} />
            <span style={styles.cardLabel}>Location</span>
            <span style={styles.cardValue}>Sri Lanka 🇱🇰</span>
          </div>
          <div style={styles.cardDivider} />
          <div style={styles.cardStat}>
            <div>
              <div style={styles.statNum}>3+</div>
              <div style={styles.statLabel}>Projects</div>
            </div>
            <div>
              <div style={styles.statNum}>12+</div>
              <div style={styles.statLabel}>Technologies</div>
            </div>
            <div>
              <div style={styles.statNum}>∞</div>
              <div style={styles.statLabel}>Curiosity</div>
            </div>
          </div>
        </div>
      </section>

      {/* ABOUT */}
      <section id="about" style={styles.section}>
        <div style={styles.sectionInner}>
          <div style={styles.sectionTag}>About</div>
          <h2 style={styles.sectionTitle}>Who I am</h2>
          <p style={styles.aboutText}>
            I'm a Software Engineering graduate with a passion for building impactful
            software solutions. I thrive on solving complex problems and crafting
            clean, user-friendly applications — from responsive frontends to
            robust backend systems.
          </p>
          <p style={styles.aboutText}>
            My focus areas span full-stack development, UI/UX design, and
            real-time systems. I believe that great software is both technically
            sound and genuinely delightful to use.
          </p>
        </div>
      </section>

      {/* SKILLS */}
      <section id="skills" style={{ ...styles.section, background: "rgba(99,102,241,0.04)" }}>
        <div style={styles.sectionInner}>
          <div style={styles.sectionTag}>Skills</div>
          <h2 style={styles.sectionTitle}>Tech Stack</h2>
          <div style={styles.skillsGrid}>
            {skills.map((s, i) => (
              <div key={i} style={styles.skillChip} className="skill-chip">
                <span>{s.icon}</span>
                <span>{s.name}</span>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* PROJECTS */}
      <section id="projects" style={styles.section}>
        <div style={styles.sectionInner}>
          <div style={styles.sectionTag}>Work</div>
          <h2 style={styles.sectionTitle}>Projects</h2>
          <div style={styles.projectsGrid}>
            {projects.map((p, i) => (
              <div key={i} style={styles.projectCard} className="project-card">
                <div style={{ ...styles.projectAccent, background: p.color }} />
                <div style={styles.projectEmoji}>{p.emoji}</div>
                <h3 style={styles.projectTitle}>{p.title}</h3>
                <p style={styles.projectDesc}>{p.desc}</p>
                <div style={styles.projectTags}>
                  {p.tags.map((t, j) => (
                    <span key={j} style={{ ...styles.tag, borderColor: p.color, color: p.color }}>
                      {t}
                    </span>
                  ))}
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* CONTACT */}
      <section id="contact" style={{ ...styles.section, background: "rgba(99,102,241,0.04)" }}>
        <div style={{ ...styles.sectionInner, textAlign: "center" }}>
          <div style={styles.sectionTag}>Contact</div>
          <h2 style={styles.sectionTitle}>Let's Connect</h2>
          <p style={{ color: "#94a3b8", marginBottom: 36, fontSize: 16 }}>
            Open to opportunities, collaborations, or just a good conversation.
          </p>
          <div style={styles.contactBtns}>
            <a href="#" style={{ ...styles.contactBtn, background: "#0077b5" }}>
              <span>in</span> LinkedIn
            </a>
            <a href="#" style={{ ...styles.contactBtn, background: "#1a1a2e", border: "1px solid #334155" }}>
              <span>⌥</span> GitHub
            </a>
            <a href="#" style={{ ...styles.contactBtn, background: "#ea4335" }}>
              <span>✉</span> Email
            </a>
          </div>
        </div>
      </section>

      {/* FOOTER */}
      <footer style={styles.footer}>
        <span>© 2026 Theekshana Vidushan</span>
        <span style={{ color: "#475569" }}>·</span>
        <span>Built with React 🚀</span>
      </footer>
    </div>
  );
}

const styles = {
  root: {
    background: "#080c14",
    color: "#e2e8f0",
    minHeight: "100vh",
    fontFamily: "'Georgia', serif",
    overflowX: "hidden",
  },
  nav: {
    position: "fixed",
    top: 0,
    left: 0,
    right: 0,
    zIndex: 100,
    display: "flex",
    alignItems: "center",
    justifyContent: "space-between",
    padding: "20px 48px",
    transition: "all 0.3s ease",
  },
  navScrolled: {
    background: "rgba(8,12,20,0.92)",
    backdropFilter: "blur(12px)",
    borderBottom: "1px solid rgba(99,102,241,0.15)",
    padding: "14px 48px",
  },
  navLogo: {
    fontWeight: "700",
    fontSize: 20,
    color: "#6366f1",
    letterSpacing: 2,
    fontFamily: "'Georgia', serif",
  },
  navLinks: { display: "flex", gap: 32 },
  navBtn: {
    background: "none",
    border: "none",
    color: "#94a3b8",
    fontSize: 13,
    cursor: "pointer",
    textTransform: "uppercase",
    letterSpacing: 2,
    fontFamily: "'Georgia', serif",
    transition: "color 0.2s",
    padding: 0,
  },
  hero: {
    minHeight: "100vh",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    padding: "100px 48px 60px",
    gap: 64,
    flexWrap: "wrap",
    position: "relative",
    overflow: "hidden",
  },
  heroGlow: {
    position: "absolute",
    width: 600,
    height: 600,
    borderRadius: "50%",
    background: "radial-gradient(circle, rgba(99,102,241,0.18) 0%, transparent 70%)",
    top: "50%",
    left: "50%",
    transform: "translate(-50%, -50%)",
    pointerEvents: "none",
  },
  heroDots: {
    position: "absolute",
    inset: 0,
    backgroundImage: "radial-gradient(rgba(99,102,241,0.12) 1px, transparent 1px)",
    backgroundSize: "40px 40px",
    pointerEvents: "none",
  },
  heroContent: {
    flex: "1 1 360px",
    maxWidth: 560,
    position: "relative",
    zIndex: 1,
  },
  badge: {
    display: "inline-flex",
    alignItems: "center",
    gap: 8,
    background: "rgba(99,102,241,0.12)",
    border: "1px solid rgba(99,102,241,0.3)",
    borderRadius: 99,
    padding: "6px 16px",
    fontSize: 12,
    color: "#a5b4fc",
    marginBottom: 28,
    letterSpacing: 0.5,
  },
  heroTitle: {
    fontSize: "clamp(44px, 6vw, 72px)",
    fontWeight: 700,
    lineHeight: 1.05,
    margin: "0 0 16px",
    letterSpacing: -1,
    color: "#f1f5f9",
  },
  heroAccent: {
    color: "#6366f1",
    fontStyle: "italic",
  },
  heroRole: {
    fontSize: 14,
    color: "#64748b",
    letterSpacing: 1.5,
    textTransform: "uppercase",
    marginBottom: 20,
  },
  heroDesc: {
    fontSize: 16,
    color: "#94a3b8",
    lineHeight: 1.8,
    marginBottom: 36,
    maxWidth: 480,
  },
  heroCtas: { display: "flex", gap: 16, flexWrap: "wrap" },
  ctaPrimary: {
    background: "#6366f1",
    color: "#fff",
    border: "none",
    borderRadius: 10,
    padding: "13px 28px",
    fontSize: 14,
    fontWeight: 600,
    cursor: "pointer",
    fontFamily: "'Georgia', serif",
    letterSpacing: 0.3,
    transition: "all 0.2s",
  },
  ctaSecondary: {
    background: "transparent",
    color: "#94a3b8",
    border: "1px solid #334155",
    borderRadius: 10,
    padding: "13px 28px",
    fontSize: 14,
    cursor: "pointer",
    fontFamily: "'Georgia', serif",
    transition: "all 0.2s",
  },
  heroCard: {
    flex: "0 0 260px",
    background: "rgba(15,20,35,0.9)",
    border: "1px solid rgba(99,102,241,0.2)",
    borderRadius: 20,
    padding: "28px 24px",
    backdropFilter: "blur(12px)",
    position: "relative",
    zIndex: 1,
  },
  cardLine: {
    display: "flex",
    alignItems: "center",
    gap: 10,
    marginBottom: 14,
  },
  cardDot: {
    width: 8,
    height: 8,
    borderRadius: "50%",
    background: "#4ade80",
    display: "block",
    boxShadow: "0 0 6px #4ade80",
  },
  cardLabel: { color: "#475569", fontSize: 12, flex: 1 },
  cardValue: { color: "#e2e8f0", fontSize: 13, fontWeight: 500 },
  cardDivider: {
    height: 1,
    background: "rgba(99,102,241,0.15)",
    margin: "18px 0",
  },
  cardStat: {
    display: "flex",
    justifyContent: "space-between",
    textAlign: "center",
  },
  statNum: {
    fontSize: 22,
    fontWeight: 700,
    color: "#6366f1",
    lineHeight: 1,
  },
  statLabel: { fontSize: 11, color: "#475569", marginTop: 4 },
  section: {
    padding: "96px 48px",
  },
  sectionInner: {
    maxWidth: 860,
    margin: "0 auto",
  },
  sectionTag: {
    fontSize: 11,
    letterSpacing: 3,
    textTransform: "uppercase",
    color: "#6366f1",
    marginBottom: 12,
    fontWeight: 600,
  },
  sectionTitle: {
    fontSize: "clamp(28px, 4vw, 42px)",
    fontWeight: 700,
    margin: "0 0 36px",
    color: "#f1f5f9",
    letterSpacing: -0.5,
  },
  aboutText: {
    fontSize: 16,
    color: "#94a3b8",
    lineHeight: 1.9,
    marginBottom: 18,
    maxWidth: 680,
  },
  skillsGrid: {
    display: "flex",
    flexWrap: "wrap",
    gap: 12,
  },
  skillChip: {
    display: "flex",
    alignItems: "center",
    gap: 8,
    background: "rgba(99,102,241,0.08)",
    border: "1px solid rgba(99,102,241,0.2)",
    borderRadius: 10,
    padding: "10px 18px",
    fontSize: 14,
    color: "#c7d2fe",
    cursor: "default",
    transition: "all 0.2s",
  },
  projectsGrid: {
    display: "grid",
    gridTemplateColumns: "repeat(auto-fill, minmax(260px, 1fr))",
    gap: 24,
  },
  projectCard: {
    background: "rgba(15,20,35,0.8)",
    border: "1px solid rgba(255,255,255,0.06)",
    borderRadius: 18,
    padding: "28px 24px",
    position: "relative",
    overflow: "hidden",
    transition: "all 0.25s ease",
  },
  projectAccent: {
    position: "absolute",
    top: 0,
    left: 0,
    right: 0,
    height: 3,
    borderRadius: "18px 18px 0 0",
  },
  projectEmoji: { fontSize: 28, marginBottom: 14, display: "block" },
  projectTitle: {
    fontSize: 17,
    fontWeight: 700,
    color: "#f1f5f9",
    margin: "0 0 10px",
    lineHeight: 1.3,
  },
  projectDesc: {
    fontSize: 14,
    color: "#64748b",
    lineHeight: 1.7,
    marginBottom: 18,
  },
  projectTags: { display: "flex", flexWrap: "wrap", gap: 8 },
  tag: {
    fontSize: 11,
    border: "1px solid",
    borderRadius: 6,
    padding: "3px 10px",
    letterSpacing: 0.3,
    fontWeight: 500,
  },
  contactBtns: {
    display: "flex",
    gap: 16,
    justifyContent: "center",
    flexWrap: "wrap",
  },
  contactBtn: {
    display: "flex",
    alignItems: "center",
    gap: 8,
    padding: "13px 28px",
    borderRadius: 12,
    fontSize: 14,
    fontWeight: 600,
    color: "#fff",
    textDecoration: "none",
    transition: "all 0.2s",
  },
  footer: {
    borderTop: "1px solid rgba(99,102,241,0.1)",
    padding: "28px 48px",
    display: "flex",
    justifyContent: "center",
    gap: 16,
    fontSize: 13,
    color: "#475569",
  },
};

const css = `
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .fade-in { animation: fadeIn 0.7s ease forwards; }
  .fade-in-delay { animation: fadeIn 0.7s ease 0.2s forwards; opacity: 0; }
  .skill-chip:hover {
    background: rgba(99,102,241,0.18) !important;
    border-color: rgba(99,102,241,0.5) !important;
    transform: translateY(-2px);
  }
  .project-card:hover {
    border-color: rgba(99,102,241,0.25) !important;
    transform: translateY(-4px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.3);
  }
  button:hover { opacity: 0.88; }
  a:hover { opacity: 0.85; transform: translateY(-1px); }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
`;
