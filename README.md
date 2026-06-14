# newProject
Ceylon Tourism website
[ceylon_tourism.html](https://github.com/user-attachments/files/28927293/ceylon_tourism.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Ceylon Tourism</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"/>
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{
  --gold:#C9A84C;
  --gold-light:#E8C96D;
  --dark:#0D1B2A;
  --dark2:#1A2E45;
  --text:#2D3748;
  --muted:#718096;
  --light:#F7F8FC;
  --white:#FFFFFF;
  --green:#1A6B44;
  --radius:12px;
}
html{scroll-behavior:smooth}
body{font-family:'Inter',sans-serif;color:var(--text);background:var(--white);overflow-x:hidden}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:999;padding:0 5%;display:flex;align-items:center;justify-content:space-between;height:70px;background:rgba(13,27,42,0.95);backdrop-filter:blur(10px);border-bottom:1px solid rgba(201,168,76,0.2)}
.logo{font-family:'Playfair Display',serif;font-size:1.6rem;font-weight:700;color:var(--white);letter-spacing:1px}
.logo span{color:var(--gold)}
.nav-links{display:flex;gap:2rem;list-style:none}
.nav-links a{color:rgba(255,255,255,0.85);text-decoration:none;font-size:0.88rem;font-weight:500;letter-spacing:0.5px;transition:color 0.3s}
.nav-links a:hover{color:var(--gold)}
.nav-cta{background:var(--gold);color:var(--dark);padding:0.5rem 1.3rem;border-radius:6px;font-weight:600;font-size:0.85rem;text-decoration:none;transition:background 0.3s}
.nav-cta:hover{background:var(--gold-light)}

/* HERO */
.hero{height:100vh;position:relative;display:flex;align-items:center;justify-content:center;text-align:center;overflow:hidden}
.hero-bg{position:absolute;inset:0;background:url('https://images.unsplash.com/photo-1588598198321-9735fd3dc5d5?w=1600&q=80') center/cover;filter:brightness(0.45)}
.hero-overlay{position:absolute;inset:0;background:linear-gradient(180deg,rgba(13,27,42,0.3) 0%,rgba(13,27,42,0.7) 100%)}
.hero-content{position:relative;z-index:1;max-width:780px;padding:0 1.5rem}
.hero-badge{display:inline-block;border:1px solid var(--gold);color:var(--gold);font-size:0.75rem;letter-spacing:2px;padding:0.35rem 1rem;border-radius:20px;margin-bottom:1.5rem;text-transform:uppercase}
.hero h1{font-family:'Playfair Display',serif;font-size:clamp(2.8rem,6vw,5rem);font-weight:700;color:var(--white);line-height:1.15;margin-bottom:1.2rem}
.hero h1 em{color:var(--gold);font-style:normal}
.hero p{color:rgba(255,255,255,0.8);font-size:1.1rem;line-height:1.7;margin-bottom:2.5rem;max-width:560px;margin-left:auto;margin-right:auto}
.hero-btns{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap}
.btn-primary{background:var(--gold);color:var(--dark);padding:0.9rem 2rem;border-radius:8px;font-weight:600;text-decoration:none;font-size:0.95rem;transition:all 0.3s}
.btn-primary:hover{background:var(--gold-light);transform:translateY(-2px)}
.btn-outline{border:2px solid rgba(255,255,255,0.6);color:var(--white);padding:0.9rem 2rem;border-radius:8px;font-weight:500;text-decoration:none;font-size:0.95rem;transition:all 0.3s}
.btn-outline:hover{border-color:var(--gold);color:var(--gold)}
.hero-stats{position:absolute;bottom:2.5rem;left:0;right:0;z-index:1;display:flex;justify-content:center;gap:3rem}
.stat{text-align:center}
.stat-num{font-family:'Playfair Display',serif;font-size:1.8rem;font-weight:700;color:var(--gold)}
.stat-label{font-size:0.75rem;color:rgba(255,255,255,0.7);letter-spacing:1px;text-transform:uppercase;margin-top:2px}

/* SECTIONS */
section{padding:6rem 5%}
.section-tag{font-size:0.75rem;color:var(--gold);letter-spacing:2px;text-transform:uppercase;font-weight:600;margin-bottom:0.6rem}
.section-title{font-family:'Playfair Display',serif;font-size:clamp(1.9rem,3.5vw,2.8rem);font-weight:700;color:var(--dark);line-height:1.2;margin-bottom:1rem}
.section-sub{color:var(--muted);font-size:1rem;line-height:1.7;max-width:540px}

/* EXPERIENCES */
.experiences{background:var(--light)}
.exp-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:1.5rem;margin-top:3.5rem}
.exp-card{background:var(--white);border-radius:var(--radius);overflow:hidden;transition:transform 0.3s,box-shadow 0.3s;box-shadow:0 2px 12px rgba(0,0,0,0.06);cursor:pointer}
.exp-card:hover{transform:translateY(-6px);box-shadow:0 16px 40px rgba(0,0,0,0.12)}
.exp-img{height:220px;background-size:cover;background-position:center;position:relative}
.exp-tag{position:absolute;top:1rem;left:1rem;background:var(--gold);color:var(--dark);font-size:0.7rem;font-weight:700;padding:0.3rem 0.75rem;border-radius:20px;letter-spacing:0.5px}
.exp-body{padding:1.4rem}
.exp-body h3{font-family:'Playfair Display',serif;font-size:1.2rem;font-weight:600;color:var(--dark);margin-bottom:0.5rem}
.exp-body p{color:var(--muted);font-size:0.88rem;line-height:1.65}
.exp-meta{display:flex;align-items:center;justify-content:space-between;margin-top:1rem;padding-top:1rem;border-top:1px solid #EEE}
.exp-price{font-weight:700;color:var(--gold);font-size:0.95rem}
.exp-dur{font-size:0.8rem;color:var(--muted)}<i class="fa fa-clock"></i>

/* DESTINATIONS */
.dest-header{display:flex;align-items:flex-end;justify-content:space-between;margin-bottom:3rem;flex-wrap:wrap;gap:1rem}
.dest-grid{display:grid;grid-template-columns:repeat(3,1fr);grid-template-rows:auto auto;gap:1.2rem}
.dest-card{position:relative;border-radius:var(--radius);overflow:hidden;cursor:pointer}
.dest-card:first-child{grid-column:span 2;grid-row:span 2}
.dest-card img{width:100%;height:100%;object-fit:cover;display:block;transition:transform 0.5s}
.dest-card:hover img{transform:scale(1.05)}
.dest-card:first-child img{height:460px}
.dest-card:not(:first-child) img{height:220px}
.dest-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(13,27,42,0.85) 0%,transparent 55%);display:flex;flex-direction:column;justify-content:flex-end;padding:1.4rem}
.dest-name{font-family:'Playfair Display',serif;font-size:1.3rem;font-weight:700;color:var(--white)}
.dest-card:not(:first-child) .dest-name{font-size:1rem}
.dest-info{font-size:0.78rem;color:rgba(255,255,255,0.75);margin-top:0.25rem}
.dest-btn{margin-top:0.8rem;display:inline-block;background:rgba(201,168,76,0.9);color:var(--dark);padding:0.4rem 1rem;border-radius:6px;font-size:0.78rem;font-weight:600;text-decoration:none;transition:background 0.3s}
.dest-btn:hover{background:var(--gold)}

/* WHY CEYLON */
.why{background:var(--dark);padding:6rem 5%}
.why-inner{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:center}
.why-img-wrap{position:relative}
.why-img{width:100%;height:480px;object-fit:cover;border-radius:16px}
.why-badge-img{position:absolute;bottom:-1.5rem;right:-1.5rem;width:160px;height:160px;object-fit:cover;border-radius:12px;border:4px solid var(--dark)}
.why-content .section-title{color:var(--white)}
.why-content .section-sub{color:rgba(255,255,255,0.65)}
.features{margin-top:2.5rem;display:flex;flex-direction:column;gap:1.2rem}
.feat{display:flex;gap:1rem;align-items:flex-start}
.feat-icon{width:44px;height:44px;border-radius:10px;background:rgba(201,168,76,0.15);border:1px solid rgba(201,168,76,0.3);display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:1.1rem;color:var(--gold)}
.feat-text h4{font-size:0.95rem;font-weight:600;color:var(--white);margin-bottom:0.25rem}
.feat-text p{font-size:0.84rem;color:rgba(255,255,255,0.55);line-height:1.6}

/* TOURS */
.tours{background:var(--light)}
.tours-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:1.5rem;margin-top:3.5rem}
.tour-card{background:var(--white);border-radius:var(--radius);overflow:hidden;box-shadow:0 2px 12px rgba(0,0,0,0.06);transition:transform 0.3s,box-shadow 0.3s}
.tour-card:hover{transform:translateY(-5px);box-shadow:0 20px 50px rgba(0,0,0,0.1)}
.tour-img{height:200px;background-size:cover;background-position:center;position:relative}
.tour-badge{position:absolute;top:1rem;right:1rem;background:var(--green);color:#fff;font-size:0.7rem;font-weight:700;padding:0.3rem 0.75rem;border-radius:20px}
.tour-body{padding:1.4rem}
.stars{color:var(--gold);font-size:0.85rem;margin-bottom:0.5rem}
.tour-body h3{font-family:'Playfair Display',serif;font-size:1.1rem;font-weight:600;color:var(--dark);margin-bottom:0.5rem}
.tour-body p{color:var(--muted);font-size:0.84rem;line-height:1.6}
.tour-footer{display:flex;align-items:center;justify-content:space-between;margin-top:1.2rem}
.price{font-size:1.1rem;font-weight:700;color:var(--dark)}.price span{font-size:0.8rem;font-weight:400;color:var(--muted)}
.book-btn{background:var(--dark);color:#fff;border:none;padding:0.5rem 1.1rem;border-radius:6px;font-size:0.82rem;font-weight:600;cursor:pointer;text-decoration:none;transition:background 0.3s}
.book-btn:hover{background:var(--gold);color:var(--dark)}

/* GALLERY */
.gallery-grid{display:grid;grid-template-columns:repeat(4,1fr);grid-template-rows:200px 200px;gap:1rem;margin-top:3.5rem}
.gal-item{border-radius:10px;overflow:hidden;position:relative;cursor:pointer}
.gal-item:first-child{grid-column:span 2;grid-row:span 2}
.gal-item img{width:100%;height:100%;object-fit:cover;transition:transform 0.5s}
.gal-item:hover img{transform:scale(1.08)}

/* TESTIMONIALS */
.testimonials{background:var(--dark)}
.test-header{text-align:center;margin-bottom:3.5rem}
.test-header .section-title{color:var(--white)}
.test-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:1.5rem}
.test-card{background:rgba(255,255,255,0.05);border:1px solid rgba(255,255,255,0.08);border-radius:var(--radius);padding:1.8rem;transition:border-color 0.3s}
.test-card:hover{border-color:rgba(201,168,76,0.4)}
.quote{font-size:2rem;color:var(--gold);line-height:1;margin-bottom:1rem}
.test-text{color:rgba(255,255,255,0.75);font-size:0.9rem;line-height:1.75;margin-bottom:1.5rem;font-style:italic}
.test-author{display:flex;align-items:center;gap:0.8rem}
.avatar{width:44px;height:44px;border-radius:50%;object-fit:cover}
.auth-name{font-weight:600;color:var(--white);font-size:0.9rem}
.auth-loc{font-size:0.78rem;color:var(--muted)}

/* PLAN / CTA */
.plan{text-align:center;background:url('https://images.unsplash.com/photo-1599930113854-d6d7fd521f10?w=1600&q=80') center/cover;position:relative;padding:7rem 5%}
.plan::before{content:'';position:absolute;inset:0;background:rgba(13,27,42,0.82)}
.plan-content{position:relative;z-index:1;max-width:650px;margin:0 auto}
.plan-content .section-title{color:var(--white)}
.plan-content p{color:rgba(255,255,255,0.75);margin:1rem 0 2.5rem;font-size:1rem;line-height:1.7}
.plan-form{display:flex;gap:0.75rem;flex-wrap:wrap;justify-content:center}
.plan-form input{flex:1;min-width:200px;padding:0.85rem 1.2rem;border-radius:8px;border:none;font-size:0.9rem;outline:none;font-family:'Inter',sans-serif}
.plan-form button{background:var(--gold);color:var(--dark);border:none;padding:0.85rem 1.8rem;border-radius:8px;font-weight:700;font-size:0.9rem;cursor:pointer;transition:background 0.3s;font-family:'Inter',sans-serif}
.plan-form button:hover{background:var(--gold-light)}

/* FOOTER */
footer{background:#080F17;padding:4rem 5% 2rem}
.footer-grid{display:grid;grid-template-columns:2fr 1fr 1fr 1.5fr;gap:3rem;margin-bottom:3rem}
.footer-brand .logo{font-size:1.4rem;display:block;margin-bottom:0.8rem}
.footer-brand p{color:rgba(255,255,255,0.5);font-size:0.84rem;line-height:1.7}
.footer-socials{display:flex;gap:0.75rem;margin-top:1.3rem}
.social-btn{width:36px;height:36px;border-radius:8px;background:rgba(255,255,255,0.07);display:flex;align-items:center;justify-content:center;color:rgba(255,255,255,0.6);font-size:0.85rem;text-decoration:none;transition:all 0.3s}
.social-btn:hover{background:var(--gold);color:var(--dark)}
.footer-col h4{color:var(--white);font-size:0.88rem;font-weight:600;margin-bottom:1.2rem;letter-spacing:0.5px}
.footer-col ul{list-style:none;display:flex;flex-direction:column;gap:0.6rem}
.footer-col ul a{color:rgba(255,255,255,0.5);text-decoration:none;font-size:0.84rem;transition:color 0.3s}
.footer-col ul a:hover{color:var(--gold)}
.footer-contact li{display:flex;gap:0.75rem;align-items:flex-start;color:rgba(255,255,255,0.5);font-size:0.82rem;margin-bottom:0.8rem}
.footer-contact i{color:var(--gold);margin-top:2px;width:14px}
.footer-bottom{border-top:1px solid rgba(255,255,255,0.06);padding-top:2rem;display:flex;justify-content:space-between;align-items:center;flex-wrap:gap}
.footer-bottom p{color:rgba(255,255,255,0.3);font-size:0.8rem}
.footer-bottom a{color:rgba(255,255,255,0.3);text-decoration:none;font-size:0.8rem;transition:color 0.3s}
.footer-bottom a:hover{color:var(--gold)}

/* SCROLL REVEAL */
.reveal{opacity:0;transform:translateY(30px);transition:opacity 0.7s ease,transform 0.7s ease}
.reveal.visible{opacity:1;transform:translateY(0)}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <span class="logo">Ceylon<span>.</span></span>
  <ul class="nav-links">
    <li><a href="#experiences">Experiences</a></li>
    <li><a href="#destinations">Destinations</a></li>
    <li><a href="#tours">Tours</a></li>
    <li><a href="#gallery">Gallery</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="#plan" class="nav-cta">Plan My Trip</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <div class="hero-badge">✦ Welcome to Sri Lanka</div>
    <h1>Discover the <em>Pearl</em> of the Indian Ocean</h1>
    <p>From misty highlands to pristine beaches, ancient temples to wild safaris — Ceylon is a world of wonders waiting to be explored.</p>
    <div class="hero-btns">
      <a href="#destinations" class="btn-primary">Explore Destinations</a>
      <a href="#tours" class="btn-outline">View Tour Packages</a>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat"><div class="stat-num">8</div><div class="stat-label">UNESCO Sites</div></div>
    <div class="stat"><div class="stat-num">40+</div><div class="stat-label">National Parks</div></div>
    <div class="stat"><div class="stat-num">1,340</div><div class="stat-label">km Coastline</div></div>
    <div class="stat"><div class="stat-num">2,500+</div><div class="stat-label">Years of History</div></div>
  </div>
</section>

<!-- EXPERIENCES -->
<section class="experiences" id="experiences">
  <div class="reveal">
    <div class="section-tag">What We Offer</div>
    <div style="display:flex;justify-content:space-between;align-items:flex-end;flex-wrap:wrap;gap:1rem">
      <h2 class="section-title">Unforgettable<br>Experiences</h2>
      <p class="section-sub">Curated experiences designed to immerse you in the authentic soul of Sri Lanka.</p>
    </div>
  </div>
  <div class="exp-grid">
    <div class="exp-card reveal">
      <div class="exp-img" style="background-image:url('https://images.unsplash.com/photo-1541512416146-3cf58d6b27cc?w=600&q=80')">
        <span class="exp-tag">Wildlife</span>
      </div>
      <div class="exp-body">
        <h3>Yala Safari Adventure</h3>
        <p>Encounter leopards, elephants and exotic birds in Sri Lanka's most celebrated national park.</p>
        <div class="exp-meta">
          <span class="exp-price">From $89 / person</span>
          <span class="exp-dur"><i class="fa fa-clock"></i> Full Day</span>
        </div>
      </div>
    </div>
    <div class="exp-card reveal">
      <div class="exp-img" style="background-image:url('https://images.unsplash.com/photo-1573408301185-9519f94816b5?w=600&q=80')">
        <span class="exp-tag">Culture</span>
      </div>
      <div class="exp-body">
        <h3>Ancient Temple Trail</h3>
        <p>Walk through millennia of history visiting the sacred sites of Anuradhapura and Polonnaruwa.</p>
        <div class="exp-meta">
          <span class="exp-price">From $65 / person</span>
          <span class="exp-dur"><i class="fa fa-clock"></i> 2 Days</span>
        </div>
      </div>
    </div>
    <div class="exp-card reveal">
      <div class="exp-img" style="background-image:url('https://images.unsplash.com/photo-1586190848861-99aa4a171e90?w=600&q=80')">
        <span class="exp-tag">Adventure</span>
      </div>
      <div class="exp-body">
        <h3>Tea Highlands Trek</h3>
        <p>Hike through emerald tea estates in Nuwara Eliya and ride the iconic scenic railway.</p>
        <div class="exp-meta">
          <span class="exp-price">From $55 / person</span>
          <span class="exp-dur"><i class="fa fa-clock"></i> 3 Days</span>
        </div>
      </div>
    </div>
    <div class="exp-card reveal">
      <div class="exp-img" style="background-image:url('https://images.unsplash.com/photo-1559128010-7c1ad6e1b6a5?w=600&q=80')">
        <span class="exp-tag">Beach</span>
      </div>
      <div class="exp-body">
        <h3>South Coast Beach Escape</h3>
        <p>Relax on the golden shores of Mirissa, Unawatuna and Galle — snorkel, surf or simply unwind.</p>
        <div class="exp-meta">
          <span class="exp-price">From $45 / person</span>
          <span class="exp-dur"><i class="fa fa-clock"></i> Flexible</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- DESTINATIONS -->
<section id="destinations" style="padding:6rem 5%;background:#fff">
  <div class="dest-header reveal">
    <div>
      <div class="section-tag">Top Picks</div>
      <h2 class="section-title">Must-Visit Destinations</h2>
    </div>
    <a href="#tours" style="color:var(--gold);font-size:0.9rem;font-weight:600;text-decoration:none">View all destinations →</a>
  </div>
  <div class="dest-grid reveal">
    <div class="dest-card">
      <img src="https://images.unsplash.com/photo-1625736300986-e4f2a84e3d5d?w=900&q=80" alt="Sigiriya Rock"/>
      <div class="dest-overlay">
        <div class="dest-name">Sigiriya Rock Fortress</div>
        <div class="dest-info">Cultural Triangle • UNESCO Heritage</div>
        <a href="#tours" class="dest-btn">Explore →</a>
      </div>
    </div>
    <div class="dest-card">
      <img src="https://images.unsplash.com/photo-1571991891529-3674f27d5b45?w=600&q=80" alt="Galle Fort"/>
      <div class="dest-overlay">
        <div class="dest-name">Galle Fort</div>
        <div class="dest-info">Southern Province • Colonial Heritage</div>
      </div>
    </div>
    <div class="dest-card">
      <img src="https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=600&q=80" alt="Ella"/>
      <div class="dest-overlay">
        <div class="dest-name">Ella Highlands</div>
        <div class="dest-info">Hill Country • Nine Arch Bridge</div>
      </div>
    </div>
    <div class="dest-card">
      <img src="https://images.unsplash.com/photo-1544551763-46a013bb70d5?w=600&q=80" alt="Mirissa"/>
      <div class="dest-overlay">
        <div class="dest-name">Mirissa Beach</div>
        <div class="dest-info">Southern Coast • Whale Watching</div>
      </div>
    </div>
    <div class="dest-card">
      <img src="https://images.unsplash.com/photo-1516026672322-bc52d61a55d5?w=600&q=80" alt="Kandy"/>
      <div class="dest-overlay">
        <div class="dest-name">Kandy</div>
        <div class="dest-info">Central Province • Temple of Tooth</div>
      </div>
    </div>
  </div>
</section>

<!-- WHY CEYLON -->
<section class="why">
  <div class="why-inner">
    <div class="why-img-wrap reveal">
      <img class="why-img" src="https://images.unsplash.com/photo-1600618528240-fb9fc964b853?w=800&q=80" alt="Ceylon"/>
      <img class="why-badge-img" src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400&q=80" alt="Tea Ceylon"/>
    </div>
    <div class="why-content reveal">
      <div class="section-tag">Why Ceylon</div>
      <h2 class="section-title">A Journey Unlike Any Other</h2>
      <p class="section-sub">Sri Lanka packs an astonishing diversity of landscapes, cultures and wildlife into a single teardrop-shaped island.</p>
      <div class="features">
        <div class="feat">
          <div class="feat-icon"><i class="fa fa-leaf"></i></div>
          <div class="feat-text">
            <h4>Biodiversity Hotspot</h4>
            <p>Home to over 3,000 plant species and 400+ bird species, many found nowhere else on Earth.</p>
          </div>
        </div>
        <div class="feat">
          <div class="feat-icon"><i class="fa fa-utensils"></i></div>
          <div class="feat-text">
            <h4>World-Class Cuisine</h4>
            <p>Spice-rich curries, hoppers, kottu and fresh seafood — a culinary adventure on every plate.</p>
          </div>
        </div>
        <div class="feat">
          <div class="feat-icon"><i class="fa fa-shield-halved"></i></div>
          <div class="feat-text">
            <h4>Safe & Welcoming</h4>
            <p>Consistently ranked among Asia's most hospitable destinations with warm, friendly locals.</p>
          </div>
        </div>
        <div class="feat">
          <div class="feat-icon"><i class="fa fa-sun"></i></div>
          <div class="feat-text">
            <h4>Year-Round Sunshine</h4>
            <p>With two monsoon seasons across different coasts, there's always a perfect beach to visit.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TOURS -->
<section class="tours" id="tours">
  <div class="reveal" style="text-align:center">
    <div class="section-tag">Tour Packages</div>
    <h2 class="section-title">Handpicked Tour Packages</h2>
    <p class="section-sub" style="margin:0 auto">All-inclusive packages crafted by local experts for every type of traveller.</p>
  </div>
  <div class="tours-grid">
    <div class="tour-card reveal">
      <div class="tour-img" style="background-image:url('https://images.unsplash.com/photo-1565967511849-76a60a516170?w=600&q=80')">
        <span class="tour-badge">Bestseller</span>
      </div>
      <div class="tour-body">
        <div class="stars">★★★★★</div>
        <h3>Classic Ceylon — 10 Days</h3>
        <p>Colombo · Sigiriya · Kandy · Ella · Yala · Galle — the perfect introduction to the island.</p>
        <div class="tour-footer">
          <div class="price">$1,199 <span>/ person</span></div>
          <a href="#plan" class="book-btn">Book Now</a>
        </div>
      </div>
    </div>
    <div class="tour-card reveal">
      <div class="tour-img" style="background-image:url('https://images.unsplash.com/photo-1520637836993-5665e6e51986?w=600&q=80')">
        <span class="tour-badge">Family</span>
      </div>
      <div class="tour-body">
        <div class="stars">★★★★★</div>
        <h3>Wildlife & Beaches — 7 Days</h3>
        <p>Yala Safari · Mirissa Whale Watching · Unawatuna — perfect for families seeking adventure.</p>
        <div class="tour-footer">
          <div class="price">$849 <span>/ person</span></div>
          <a href="#plan" class="book-btn">Book Now</a>
        </div>
      </div>
    </div>
    <div class="tour-card reveal">
      <div class="tour-img" style="background-image:url('https://images.unsplash.com/photo-1504214208698-ea1916a2195a?w=600&q=80')">
        <span class="tour-badge">Luxury</span>
      </div>
      <div class="tour-body">
        <div class="stars">★★★★★</div>
        <h3>Luxury Heritage — 14 Days</h3>
        <p>5-star resorts, private guides, hot air balloon over Sigiriya and a private yacht around the south coast.</p>
        <div class="tour-footer">
          <div class="price">$3,499 <span>/ person</span></div>
          <a href="#plan" class="book-btn">Book Now</a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- GALLERY -->
<section id="gallery" style="padding:6rem 5%;background:#fff">
  <div class="reveal" style="text-align:center;margin-bottom:0">
    <div class="section-tag">Gallery</div>
    <h2 class="section-title">Ceylon Through the Lens</h2>
  </div>
  <div class="gallery-grid reveal">
    <div class="gal-item"><img src="https://images.unsplash.com/photo-1625736300986-e4f2a84e3d5d?w=800&q=80" alt="Sigiriya"/></div>
    <div class="gal-item"><img src="https://images.unsplash.com/photo-1559128010-7c1ad6e1b6a5?w=400&q=80" alt="Beach"/></div>
    <div class="gal-item"><img src="https://images.unsplash.com/photo-1573408301185-9519f94816b5?w=400&q=80" alt="Temple"/></div>
    <div class="gal-item"><img src="https://images.unsplash.com/photo-1541512416146-3cf58d6b27cc?w=400&q=80" alt="Elephant"/></div>
    <div class="gal-item"><img src="https://images.unsplash.com/photo-1586190848861-99aa4a171e90?w=400&q=80" alt="Tea"/></div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section class="testimonials" id="testimonials">
  <div class="test-header reveal">
    <div class="section-tag" style="color:var(--gold)">Testimonials</div>
    <h2 class="section-title">What Our Travellers Say</h2>
  </div>
  <div class="test-grid">
    <div class="test-card reveal">
      <div class="quote">"</div>
      <p class="test-text">Ceylon Tourism arranged everything flawlessly. The safari at Yala was breathtaking — we spotted three leopards! Truly a once-in-a-lifetime experience.</p>
      <div class="test-author">
        <img class="avatar" src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sarah"/>
        <div><div class="auth-name">Sarah Mitchell</div><div class="auth-loc">London, UK</div></div>
      </div>
    </div>
    <div class="test-card reveal">
      <div class="quote">"</div>
      <p class="test-text">The 10-day Classic Ceylon package was absolutely perfect. From the ancient ruins to the tea estates and beaches — every day was a highlight.</p>
      <div class="test-author">
        <img class="avatar" src="https://randomuser.me/api/portraits/men/32.jpg" alt="Lucas"/>
        <div><div class="auth-name">Lucas Dubois</div><div class="auth-loc">Paris, France</div></div>
      </div>
    </div>
    <div class="test-card reveal">
      <div class="quote">"</div>
      <p class="test-text">We came as strangers to Sri Lanka and left with a piece of our heart left behind. The hospitality, the food, the scenery — nothing compares.</p>
      <div class="test-author">
        <img class="avatar" src="https://randomuser.me/api/portraits/women/68.jpg" alt="Priya"/>
        <div><div class="auth-name">Priya Ramanathan</div><div class="auth-loc">Singapore</div></div>
      </div>
    </div>
  </div>
</section>

<!-- PLAN / CTA -->
<section class="plan" id="plan">
  <div class="plan-content reveal">
    <div class="section-tag" style="color:var(--gold)">Plan Your Journey</div>
    <h2 class="section-title">Ready to Explore Ceylon?</h2>
    <p>Drop us your email and our travel experts will craft a personalised itinerary just for you — completely free.</p>
    <div class="plan-form">
      <input type="text" placeholder="Your name"/>
      <input type="email" placeholder="Your email address"/>
      <button type="button">Get Free Itinerary →</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer id="contact">
  <div class="footer-grid">
    <div class="footer-brand">
      <span class="logo">Ceylon<span style="color:var(--gold)">.</span></span>
      <p>Your trusted partner for discovering the timeless beauty, culture and adventure of Sri Lanka.</p>
      <div class="footer-socials">
        <a href="https://facebook.com" class="social-btn" target="_blank"><i class="fa-brands fa-facebook-f"></i></a>
        <a href="https://instagram.com" class="social-btn" target="_blank"><i class="fa-brands fa-instagram"></i></a>
        <a href="https://twitter.com" class="social-btn" target="_blank"><i class="fa-brands fa-x-twitter"></i></a>
        <a href="https://youtube.com" class="social-btn" target="_blank"><i class="fa-brands fa-youtube"></i></a>
        <a href="https://tripadvisor.com" class="social-btn" target="_blank"><i class="fa-brands fa-tripadvisor"></i></a>
      </div>
    </div>
    <div class="footer-col">
      <h4>Destinations</h4>
      <ul>
        <li><a href="#destinations">Sigiriya</a></li>
        <li><a href="#destinations">Kandy</a></li>
        <li><a href="#destinations">Galle Fort</a></li>
        <li><a href="#destinations">Ella</a></li>
        <li><a href="#destinations">Mirissa</a></li>
        <li><a href="#destinations">Yala</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Tours</h4>
      <ul>
        <li><a href="#tours">Classic Ceylon</a></li>
        <li><a href="#tours">Wildlife & Beaches</a></li>
        <li><a href="#tours">Luxury Heritage</a></li>
        <li><a href="#experiences">Cultural Trails</a></li>
        <li><a href="#experiences">Highland Treks</a></li>
        <li><a href="#plan">Custom Tours</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Get in Touch</h4>
      <ul class="footer-contact">
        <li><i class="fa fa-location-dot"></i> 45 Galle Road, Colombo 3, Sri Lanka</li>
        <li><i class="fa fa-phone"></i> +94 11 234 5678</li>
        <li><i class="fa fa-envelope"></i> hello@ceylontourism.lk</li>
        <li><i class="fa fa-clock"></i> Mon–Sat: 8:00 AM – 6:00 PM</li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2024 Ceylon Tourism. All rights reserved.</p>
    <div style="display:flex;gap:1.5rem">
      <a href="#">Privacy Policy</a>
      <a href="#">Terms of Service</a>
      <a href="#">Cookie Policy</a>
    </div>
  </div>
</footer>

<script>
const revealEls = document.querySelectorAll('.reveal');
const obs = new IntersectionObserver((entries) => {
  entries.forEach((e, i) => {
    if (e.isIntersecting) {
      setTimeout(() => e.target.classList.add('visible'), i * 80);
      obs.unobserve(e.target);
    }
  });
}, { threshold: 0.1 });
revealEls.forEach(el => obs.observe(el));
</script>
</body>
</html>
