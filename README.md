import React from "react";

export default function App() {
  return (
    <div className="bg-gray-900 text-white min-h-screen font-sans">

      {/* HERO SECTION */}
      <section className="text-center py-16 px-4">
        <h1 className="text-4xl md:text-5xl font-bold text-indigo-400">
          🚀 Theekshana Vidushan
        </h1>
        <p className="mt-4 text-lg text-gray-300">
          Software Engineer | Full-Stack Developer | Designer
        </p>

        <p className="mt-6 max-w-xl mx-auto text-gray-400">
          Building modern, scalable applications and turning ideas into real-world solutions through clean code and creative thinking.
        </p>
      </section>

      {/* ABOUT */}
      <section className="py-12 px-6 max-w-4xl mx-auto">
        <h2 className="text-2xl font-semibold text-indigo-400 mb-4">💫 About Me</h2>
        <p className="text-gray-300 leading-relaxed">
          I am a Software Engineering graduate passionate about building impactful software solutions.
          I enjoy solving complex problems and creating clean, user-friendly applications.
          My focus areas include full-stack development, UI/UX design, and real-time systems.
        </p>
      </section>

      {/* TECH STACK */}
      <section className="py-12 px-6 bg-gray-800">
        <h2 className="text-2xl font-semibold text-indigo-400 mb-6 text-center">
          🛠️ Tech Stack
        </h2>

        <div className="grid grid-cols-2 md:grid-cols-4 gap-4 text-center">
          {[
            "HTML", "CSS", "JavaScript", "TypeScript",
            "React", "Node.js", "Express",
            "Python", "Java", "PHP",
            "MySQL", "MongoDB"
          ].map((tech, index) => (
            <div key={index} className="bg-gray-700 p-3 rounded-xl">
              {tech}
            </div>
          ))}
        </div>
      </section>

      {/* PROJECTS */}
      <section className="py-12 px-6 max-w-5xl mx-auto">
        <h2 className="text-2xl font-semibold text-indigo-400 mb-6">🌟 Projects</h2>

        <div className="grid md:grid-cols-2 gap-6">

          {/* Eye Tracking */}
          <div className="bg-gray-800 p-5 rounded-2xl shadow-lg">
            <h3 className="text-xl font-bold mb-2">👁️ Eye-Tracking Assistive System</h3>
            <p className="text-gray-400">
              Developed a real-time eye-tracking system for hands-free computer control using computer vision and gaze detection.
            </p>
            <p className="text-sm text-indigo-300 mt-2">
              Python • OpenCV • MediaPipe • React • APIs
            </p>
          </div>

          {/* Bookstore */}
          <div className="bg-gray-800 p-5 rounded-2xl shadow-lg">
            <h3 className="text-xl font-bold mb-2">📚 Online Book Store</h3>
            <p className="text-gray-400">
              Built a full-stack bookstore system using Java Servlets with authentication, book management, and SQL database integration.
            </p>
            <p className="text-sm text-indigo-300 mt-2">
              Java • Servlets • MySQL • HTML • CSS
            </p>
          </div>

          {/* ML */}
          <div className="bg-gray-800 p-5 rounded-2xl shadow-lg">
            <h3 className="text-xl font-bold mb-2">🌡️ Temperature Prediction Model</h3>
            <p className="text-gray-400">
              Created a machine learning model to predict minimum temperature using historical weather data and regression techniques.
            </p>
            <p className="text-sm text-indigo-300 mt-2">
              Python • Scikit-learn • Pandas
            </p>
          </div>

        </div>
      </section>

      {/* CONTACT */}
      <section className="py-12 px-6 bg-gray-800 text-center">
        <h2 className="text-2xl font-semibold text-indigo-400 mb-4">
          📬 Contact Me
        </h2>

        <div className="flex justify-center gap-4 flex-wrap">
          <a href="#" className="bg-indigo-500 px-4 py-2 rounded-lg">LinkedIn</a>
          <a href="#" className="bg-gray-700 px-4 py-2 rounded-lg">GitHub</a>
          <a href="#" className="bg-red-500 px-4 py-2 rounded-lg">Email</a>
        </div>
      </section>

      {/* FOOTER */}
      <footer className="text-center py-6 text-gray-500">
        © 2026 Theekshana Vidushan — Built with React 🚀
      </footer>

    </div>
  );
}
