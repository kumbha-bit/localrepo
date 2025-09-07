<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sactech Control System</title>
  <style>
    * { margin:0; padding:0; box-sizing:border-box; }
    body { font-family: Arial, sans-serif; }

    nav {
      background-color: #1f2937;
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 30px;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .logo {
      font-size: 24px;
      font-weight: bold;
      color: #4f46e5;
      cursor: pointer;
    }

    ul {
      list-style: none;
      display: flex;
      gap: 25px;
      align-items: center;
    }

    li { position: relative; }

    a {
      color: white;
      text-decoration: none;
      padding: 8px 12px;
      display: block;
      transition: 0.3s;
    }

    a:hover { background-color: #4f46e5; border-radius: 5px; }

    .dropdown-content {
      display: none;
      position: absolute;
      top: 38px;
      left: 0;
      background-color: #374151;
      min-width: 220px;
      border-radius: 5px;
      overflow: hidden;
    }

    .dropdown-content a { padding: 10px 15px; }

    .dropdown:hover .dropdown-content { display: block; }

    /* Mobile */
    .menu-toggle {
      display: none;
      flex-direction: column;
      cursor: pointer;
      gap: 5px;
    }

    .menu-toggle div {
      width: 25px;
      height: 3px;
      background-color: white;
    }

    @media (max-width: 768px) {
      ul {
        display: none;
        flex-direction: column;
        position: absolute;
        top: 65px;
        left: 0;
        width: 100%;
        background-color: #1f2937;
        padding: 15px 0;
      }

      ul.show { display: flex; }

      .dropdown-content {
        position: static;
      }

      .menu-toggle { display: flex; }
    }

    section { height: 600px; padding: 50px; }
  </style>
</head>
<body>

<nav>
  <div class="logo" onclick="window.location.href='#home'">Sactech</div>
  <div class="menu-toggle" onclick="toggleMenu()">
    <div></div><div></div><div></div>
  </div>
  <ul id="navbar">
    <li><a href="#home">Home</a></li>
    <li><a href="#about">About Us</a></li>
    <li class="dropdown">
      <a href="javascript:void(0)">Services ▼</a>
      <div class="dropdown-content">
        <a href="#plc">PLC Assembling & Wiring</a>
        <a href="#panel">Control Panel Manufacturing</a>
        <a href="#turnkey">Turnkey Project Installation</a>
        <a href="#automation">Industrial Automation Solutions</a>
      </div>
    </li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#contact">Contact Us</a></li>
  </ul>
</nav>

<section id="home" style="background:#e5e7eb;">Home Section</section>
<section id="about" style="background:#d1d5db;">About Us Section</section>
<section id="plc" style="background:#cbd5e1;">PLC Section</section>
<section id="panel" style="background:#a1a1aa;">Control Panel Section</section>
<section id="turnkey" style="background:#9ca3af;">Turnkey Project Section</section>
<section id="automation" style="background:#6b7280;">Industrial Automation Section</section>
<section id="projects" style="background:#4b5563;">Projects Section</section>
<section id="contact" style="background:#1f2937;">Contact Section</section>

<script>
  function toggleMenu() {
    const nav = document.getElementById('navbar');
    nav.classList.toggle('show');
  }
</script>

</body>
</html>

