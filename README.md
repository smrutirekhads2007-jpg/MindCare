index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>MindCare – Your Mental Health Companion</title>
  <link rel="stylesheet" href="style.css" />
  <script src="script.js" defer></script>
</head>
<body>
  <div id="loadingOverlay" class="loading-overlay">
    <div class="spinner"></div>
    <div class="loading-msg">Preparing your experience…<br>Take a deep breath 🌱</div>
  </div>
  <nav>
    <a href="index.html" class="navtab">Home</a>
    <a href="test.html" class="navtab">Test</a>
    <a href="psychiatrist.html" class="navtab">Psychiatrist</a>
    <a href="dashboard.html" class="navtab">Dashboard</a>
    <a href="login.html" class="navtab">Login</a>
    <a href="signup.html" class="navtab">Signup</a>
  </nav>
  <section class="hero">
  <div class="hero-logo">MindCare</div>
  <div class="hero-tagline">Mental Health Support, Inspiration, and Growth</div>
  <div class="motivation-rotator" id="motivationRotator"></div>
  <a href="test.html"><button class="hero-btn">Take Self-Assessment</button></a>
</section>
  <div class="mission-section">
    <b>Our Mission:</b> To empower you to understand, support, and heal your mind. MindCare is your companion for self-reflection, growth, and community—wherever you are on your journey.
  </div>
  <div class="features-row">
    <a href="test.html" class="feature-card" style="text-decoration:none;">
      <div class="icon">🧠</div>
      <h3>Science-Based Test</h3>
      <p>Take an easy, research-backed quiz to check for signs of depression or anxiety. Get instant, actionable feedback.</p>
    </a>
    <a href="dashboard.html" class="feature-card" style="text-decoration:none;">
      <div class="icon">🔥</div>
      <h3>Motivational Quotes</h3>
      <p>Read powerful, soul-stirring quotes to help you rise above tough moments and ignite hope within.</p>
    </a>
    <a href="psychiatrist.html" class="feature-card" style="text-decoration:none;">
      <div class="icon">🩺</div>
      <h3>Professional Guidance</h3>
      <p>Find the best psychiatrists worldwide and request appointments directly from the app.</p>
    </a>
   
  </div>
  <footer>
    &copy; 2025 MindCare. Your journey matters.
  </footer>
  <script>
     function showLoadingOverlay() {
    setTimeout(() => {
      document.getElementById("loadingOverlay").classList.add("hidden");
    }, 2000);
  }
  document.addEventListener("DOMContentLoaded", function() {
    showLoadingOverlay();
  });
  </script>
  <script>
document.addEventListener("DOMContentLoaded", function () {
  const lastVisit = localStorage.getItem("lastVisit");
  const today = new Date().toDateString();

  if (lastVisit !== today) {
    alert("🌞 Your new session is ready with a fresh quote and video full of positive vibes!");
    localStorage.setItem("lastVisit", today);
  }
});
</script>
<!-- Chatbot button and window -->
<button id="chatbot-button">💬</button>
<div id="chatbot-window">
    <div id="chat-messages"></div>
    <div id="chat-input">
        <input type="text" id="user-input" placeholder="Type your message...">
        <button id="send-button">Send</button>
    </div>
</div>
<script src="chatbot.js"></script>


</body>
</html>
