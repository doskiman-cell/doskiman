<!--
Doskiman Music - Single-file homepage

INSTRUCTIONS:
1) Save this file as `index.html` and upload to the root of your website (public_html or similar).
2) Create a subfolder called `assets` and upload your images and audio there with these filenames:
   - assets/studio-hero.jpg    (hero / mic photo)
   - assets/studio1.jpg        (team / control room photo)
   - assets/studio2.jpg        (mixer close-up photo)
   - assets/sacred-river.mp3   (featured track Sacred River) [optional]
   - assets/roots-and-wings.mp3 (featured track Roots and Wings) [optional]
3) Replace or add streaming links where noted.
4) To set up email (bookings@doskiman.com) create the mailbox with your host or use Google Workspace / Zoho Mail.

This file is intentionally self-contained (no build tools required).
-->

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Doskiman Music — Soulful music. Inspired by soulful people.</title>
  <meta name="description" content="Doskiman Music — soulful gospel & neo-soul. Featured: Sacred River, Roots and Wings.">

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#2f1f14; /* deep brown */
      --accent:#b77a3a; /* warm gold */
      --muted:#8b6a53;
      --cream:#f5efe9;
      --max-width:1100px;
    }
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,"Helvetica Neue",Arial; color:var(--cream);background:var(--bg)}

    a{color:var(--accent);text-decoration:none}

    header{position:relative}
    .hero{
      min-height:72vh;display:flex;align-items:center;justify-content:center;text-align:center;position:relative;overflow:hidden;
      background:#000 center/cover no-repeat;
    }
    .hero::after{
      content:"";position:absolute;inset:0;background:linear-gradient(180deg,rgba(15,10,8,0.55) 10%, rgba(15,10,8,0.85) 70%);
    }
    .hero .container{position:relative;z-index:2;max-width:var(--max-width);padding:48px 20px}

    .brand{font-family:'Playfair Display',serif;font-size:48px;letter-spacing:-1px;margin:0}
    .tag{margin-top:12px;color:var(--muted);font-size:18px}

    .cta-row{margin-top:28px;display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
    .btn{background:rgba(0,0,0,0.45);border:1px solid rgba(255,255,255,0.05);padding:12px 22px;border-radius:8px;font-weight:600;cursor:pointer}
    .btn.primary{background:var(--accent);color:var(--bg)}

    nav{position:absolute;top:18px;left:0;right:0;z-index:5;padding:0 24px;display:flex;justify-content:space-between;align-items:center}
    .nav-left{display:flex;gap:14px;align-items:center}
    .logo{font-family:'Playfair Display',serif;font-weight:700;color:var(--cream)}
    .nav-right{display:flex;gap:12px;align-items:center}
    .nav-link{color:rgba(255,255,255,0.9);font-size:15px}

    main{max-width:var(--max-width);margin:0 auto;padding:60px 20px 120px}

    .featured-heading{font-family:'Playfair Display',serif;font-size:40px;color:var(--cream);text-align:center;margin-bottom:28px}

    .grid{display:grid;grid-template-columns:repeat(2,1fr);gap:20px}
    .card{background:#2a1a12;padding:14px;border-radius:10px}
    .card img{width:100%;height:300px;object-fit:cover;border-radius:8px}
    .card h4{margin:12px 0 6px;font-family:'Playfair Display',serif}
    .card p{margin:0;color:var(--muted);font-size:14px}

    .music-row{display:flex;flex-direction:column;gap:12px;margin-top:20px}
    .track{display:flex;align-items:center;gap:14px;padding:12px;background:linear-gradient(0deg, rgba(255,255,255,0.01), rgba(255,255,255,0.01));border-radius:8px}
    .track .meta{flex:1}
    .track .meta h5{margin:0;font-family:'Playfair Display',serif}
    .track audio{width:160px}

    footer{padding:34px 20px;background:#1f1410;color:var(--muted);margin-top:80px}
    .footer-inner{max-width:var(--max-width);margin:0 auto;display:flex;justify-content:space-between;gap:20px;align-items:center}
    .socials a{margin-left:10px}

    /* responsive */
    @media(max-width:800px){
      .brand{font-size:36px}
      .grid{grid-template-columns:1fr}
      .hero{min-height:62vh}
    }

    /* small helper */
    .sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0,0,0,0);white-space:nowrap;border:0}
  </style>
</head>
<body>

<header>
  <nav>
    <div class="nav-left">
      <div class="logo">Doskiman Music</div>
    </div>
    <div class="nav-right">
      <a class="nav-link" href="#music">Music</a>
      <a class="nav-link" href="#about">About</a>
      <a class="nav-link" href="#contact">Contact</a>
    </div>
  </nav>

  <section class="hero" id="top" style="background-image:url('assets/studio-hero.jpg')">
    <div class="container">
      <h1 class="brand">Doskiman Music</h1>
      <div class="tag">Soulful music. Inspired by soulful people.</div>

      <div class="cta-row">
        <a class="btn primary" href="#sacred">Sacred River</a>
        <a class="btn" href="#roots">Roots and Wings</a>
        <a class="btn" href="https://youtube.com/@motlalepulamoloi659?si=iYBsG-4pxX9tHUfW" target="_blank">Watch on YouTube</a>
      </div>
    </div>
  </section>
</header>

<main>
  <section id="music">
    <h2 class="featured-heading">Featured</h2>

    <div class="grid">
      <div class="card">
        <img src="assets/studio1.jpg" alt="Doskiman and crew in the studio">
        <h4>Sacred River</h4>
        <p>Featured single — a reflective gospel piece that flows like a river.</p>

        <div class="music-row" id="sacred">
          <div class="track">
            <div class="meta">
              <h5>Sacred River</h5>
              <p class="sr-only">Audio controls for Sacred River</p>
            </div>
            <audio controls preload="none">
              <source src="assets/sacred-river.mp3" type="audio/mpeg">
              Your browser does not support the audio element.
            </audio>
          </div>
        </div>
      </div>

      <div class="card">
        <img src="assets/studio2.jpg" alt="Studio mixer close-up">
        <h4>Roots and Wings</h4>
        <p>Rooted in tradition, lifted by hope — a song about faith and freedom.</p>

        <div class="music-row" id="roots">
          <div class="track">
            <div class="meta">
              <h5>Roots and Wings</h5>
            </div>
            <audio controls preload="none">
              <source src="assets/roots-and-wings.mp3" type="audio/mpeg">
              Your browser does not support the audio element.
            </audio>
          </div>
        </div>
      </div>
    </div>

  </section>

  <section id="about" style="margin-top:48px">
    <h2 class="featured-heading">About Doskiman Music</h2>
    <div style="max-width:900px;margin:0 auto;text-align:center;color:var(--muted);font-size:16px">
      Doskiman Music creates warm, soulful gospel and neo-soul music rooted in personal story and community. Songs like <em>Sacred River</em> and <em>Roots and Wings</em> blend heartfelt lyrics with organic instrumentation — a sound for quiet reflection and joyful praise.
    </div>
  </section>

  <section id="contact" style="margin-top:48px">
    <h2 class="featured-heading">Contact / Booking</h2>
    <div style="max-width:700px;margin:0 auto;display:flex;gap:20px;flex-direction:column;align-items:center">
      <p style="color:var(--muted);text-align:center">For bookings, collaborations or press, email <a href="mailto:bookings@doskiman.com">bookings@doskiman.com</a> or use the contact form below.</p>

      <form id="contactForm" style="width:100%;background:#231614;padding:18px;border-radius:8px">
        <label class="sr-only" for="name">Name</label>
        <input id="name" name="name" placeholder="Your name" required style="width:100%;padding:10px;border-radius:6px;border:1px solid rgba(255,255,255,0.04);background:#20130f;color:var(--cream);margin-bottom:10px">

        <label class="sr-only" for="email">Email</label>
        <input id="email" name="email" type="email" placeholder="Your email" required style="width:100%;padding:10px;border-radius:6px;border:1px solid rgba(255,255,255,0.04);background:#20130f;color:var(--cream);margin-bottom:10px">

        <label class="sr-only" for="message">Message</label>
        <textarea id="message" name="message" placeholder="Message" rows="4" style="width:100%;padding:10px;border-radius:6px;border:1px solid rgba(255,255,255,0.04);background:#20130f;color:var(--cream);margin-bottom:10px"></textarea>

        <button type="submit" class="btn primary" style="width:100%">Send Message</button>
      </form>

      <small style="color:var(--muted);margin-top:8px">Or follow on <a href="https://youtube.com/@motlalepulamoloi659?si=iYBsG-4pxX9tHUfW" target="_blank">YouTube</a> • <a href="https://tiktok.com/@doskim4n" target="_blank">TikTok</a></small>
    </div>
  </section>

</main>

<footer>
  <div class="footer-inner">
    <div>
      <div style="font-family:'Playfair Display',serif;font-size:18px;color:var(--cream)">Doskiman Music</div>
      <div style="font-size:13px;color:var(--muted)">Soulful music. Inspired by soulful people.</div>
    </div>

    <div style="text-align:right">
      <div style="font-size:13px;color:var(--muted)">Follow</div>
      <div class="socials">
        <a href="https://youtube.com/@motlalepulamoloi659?si=iYBsG-4pxX9tHUfW" target="_blank">YouTube</a>
        <a href="https://tiktok.com/@doskim4n" target="_blank">TikTok</a>
      </div>
    </div>
  </div>
</footer>

<script>
  // Simple contact form handler (no backend). This will open user's email client as a fallback.
  document.getElementById('contactForm').addEventListener('submit', function(e){
    e.preventDefault();
    var name = document.getElementById('name').value.trim();
    var email = document.getElementById('email').value.trim();
    var message = document.getElementById('message').value.trim();
    if(!name || !email || !message){
      alert('Please complete all fields.');
      return;
    }
    var subject = encodeURIComponent('Booking request from ' + name);
    var body = encodeURIComponent('Name: ' + name + '\nEmail: ' + email + '\n\n' + message);
    window.location.href = 'mailto:bookings@doskiman.com?subject=' + subject + '&body=' + body;
  });

  // Smooth scroll for anchor buttons
  document.querySelectorAll('a[href^="#"]').forEach(function(anchor){
    anchor.addEventListener('click', function(e){
      var target = document.querySelector(this.getAttribute('href'));
      if(target){
        e.preventDefault();
        target.scrollIntoView({behavior:'smooth',block:'start'});
      }
    });
  });
</script>

</body>
</html>
# doskiman
