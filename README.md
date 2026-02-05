<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>PrimeCover Insurance</title>
  <meta name="description" content="PrimeCover Insurance — Affordable, reliable health and life insurance plans with easy claims and 24/7 support.">
  <style>
    :root{--accent:#0b7b6b;--accent-2:#0f9f85;--muted:#6b7280;--bg:#f7faf9}
    *{box-sizing:border-box}
    body{font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,'Helvetica Neue',Arial;line-height:1.5;margin:0;color:#0f172a;background:var(--bg)}
    header{background:#fff;border-bottom:1px solid #e6edf0}
    .container{max-width:1100px;margin:0 auto;padding:24px}
    .nav{display:flex;align-items:center;justify-content:space-between;gap:16px}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:48px;height:48px;border-radius:8px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;color:#fff;font-weight:700}
    nav a{margin-left:12px;text-decoration:none;color:#0f172a;font-weight:600}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr;gap:20px;align-items:center;padding:48px 0}
    .hero-grid{display:flex;flex-direction:column;gap:18px}
    .kicker{display:inline-block;background:rgba(11,123,107,0.12);color:var(--accent);padding:6px 10px;border-radius:999px;font-weight:600;font-size:13px}
    h1{font-size:2rem;margin:0;color:#062b26}
    p.lead{color:var(--muted);margin:0;max-width:640px}
    .cta-group{display:flex;gap:12px}
    .btn{padding:12px 18px;border-radius:10px;border:0;cursor:pointer;font-weight:700}
    .btn-primary{background:var(--accent);color:#fff}
    .btn-ghost{background:transparent;border:2px solid #e6eef0;color:var(--accent)}

    /* Cards */
    .features{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px;margin-top:24px}
    .card{background:#fff;padding:18px;border-radius:12px;box-shadow:0 6px 18px rgba(15,23,42,0.06)}
    .card h3{margin:0 0 6px 0}
    .muted{color:var(--muted);font-size:14px}

    /* Plans */
    .plans{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px;margin:28px 0}
    .plan{background:#fff;padding:18px;border-radius:12px;border:1px solid #e6eef0}
    .plan .price{font-size:22px;font-weight:800;color:var(--accent)}

    /* Contact */
    .contact{display:grid;grid-template-columns:1fr;gap:18px;background:#fff;padding:20px;border-radius:12px}
    label{display:block;font-weight:700;margin-bottom:6px}
    input,textarea,select{width:100%;padding:10px;border-radius:8px;border:1px solid #e6eef0;font-size:15px}
    textarea{min-height:120px}

    /* FAQ */
    .faq{margin:18px 0}
    .faq-item{background:#fff;padding:12px;border-radius:10px;margin-bottom:8px}
    .faq-item summary{font-weight:700;cursor:pointer}

    footer{padding:24px 0;color:var(--muted);font-size:14px}

    /* Responsive */
    @media(min-width:800px){
      .hero{grid-template-columns:1fr 420px}
      h1{font-size:2.4rem}
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="logo">CN</div>
        <div>
          <div style="font-weight:800">Care Nest</div>
          <div style="font-size:12px;color:var(--muted)">Insurance & Care</div>
        </div>
      </div>
      <nav aria-label="Main Navigation">
        <a href="#services">Services</a>
        <a href="#plans">Plans</a>
        <a href="#claims">Claims</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero" aria-labelledby="hero-heading">
      <div class="hero-grid">
        <span class="kicker">Trusted · Affordable · Fast Claims</span>
        <h1 id="hero-heading">Care Nest — Insurance that looks after your family</h1>
        <p class="lead">Simple health and life insurance plans designed for families and individuals. Easy online purchase, transparent pricing, and a 24/7 claims support team ready to help.</p>

        <div class="cta-group">
          <button class="btn btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Get a Quote</button>
          <a class="btn btn-ghost" href="#plans">View Plans</a>
        </div>

        <div class="features" aria-hidden="false">
          <div class="card">
            <h3>Cashless Hospitals</h3>
            <p class="muted">Large network of empaneled hospitals for cashless treatment.</p>
          </div>
          <div class="card">
            <h3>Family Floater Options</h3>
            <p class="muted">Cover your spouse and children in one cost-effective policy.</p>
          </div>
          <div class="card">
            <h3>Simple Claims</h3>
            <p class="muted">Fast claim settlement with 24/7 assistance and minimal paperwork.</p>
          </div>
        </div>

      </div>

      <aside class="card" aria-labelledby="quote-title">
        <h2 id="quote-title">Quick quote</h2>
        <p class="muted">Choose a plan and get an instant estimate.</p>
        <form id="quick-quote" onsubmit="event.preventDefault(); getQuote();">
          <label for="type">Plan type</label>
          <select id="type" required>
            <option value="individual">Individual</option>
            <option value="family">Family Floater</option>
            <option value="senior">Senior Citizen</option>
          </select>

          <label for="age">Age</label>
          <input id="age" type="number" min="0" max="120" value="30" required>

          <label for="sum">Sum insured</label>
          <select id="sum" required>
            <option value="300000">₹3,00,000</option>
            <option value="500000">₹5,00,000</option>
            <option value="1000000">₹10,00,000</option>
          </select>

          <div style="margin-top:12px;display:flex;gap:8px">
            <button class="btn btn-primary" type="submit">Estimate Premium</button>
            <button class="btn" type="button" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Contact Advisor</button>
          </div>

          <p id="estimate" style="margin-top:10px;color:var(--muted)"></p>
        </form>
      </aside>
    </section>

    <section id="services">
      <h2>What we offer</h2>
      <div class="features" style="margin-top:12px">
        <div class="card"><h3>Health Insurance</h3><p class="muted">Hospitalisation cover, daycare procedures, and maternity add-ons.</p></div>
        <div class="card"><h3>Life Insurance</h3><p class="muted">Term plans and return-of-premium options for financial security.</p></div>
        <div class="card"><h3>Senior Care</h3><p class="muted">Plans tailored for senior citizens with simplified medical checks.</p></div>
        <div class="card"><h3>Critical Illness</h3><p class="muted">Lump-sum payouts on diagnosis of listed critical conditions.</p></div>
      </div>
    </section>

    <section id="plans">
      <h2>Popular plans</h2>
      <div class="plans">
        <div class="plan">
          <h3>Starter Health</h3>
          <p class="muted">For individuals and young families</p>
          <p class="price">₹<span class="price">2,499</span>/yr</p>
          <ul class="muted">
            <li>₹3,00,000 sum insured</li>
            <li>Cashless hospitals</li>
            <li>Free preventive checkup</li>
          </ul>
          <button class="btn btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Buy</button>
        </div>

        <div class="plan">
          <h3>Family Care</h3>
          <p class="muted">Covers partner & children</p>
          <p class="price">₹<span class="price">5,999</span>/yr</p>
          <ul class="muted">
            <li>₹5,00,000 sum insured</li>
            <li>Maternity add-on available</li>
            <li>No-claim bonus</li>
          </ul>
          <button class="btn btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Buy</button>
        </div>

        <div class="plan">
          <h3>Senior Secure</h3>
          <p class="muted">For policyholders 60+</p>
          <p class="price">₹<span class="price">8,499</span>/yr</p>
          <ul class="muted">
            <li>₹3,00,000 sum insured</li>
            <li>Specialized geriatric cover</li>
            <li>Fast-track claim support</li>
          </ul>
          <button class="btn btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Buy</button>
        </div>
      </div>
    </section>

    <section id="claims">
      <h2>Claims & Support</h2>
      <div class="card" style="margin-top:12px">
        <h3>How to raise a claim</h3>
        <ol class="muted">
          <li>Call our 24/7 claims helpline at <strong>1800-123-CARE (2273)</strong>.</li>
          <li>Submit filled claim form & hospital bills via email or our portal.</li>
          <li>Our claims team will assist and guide you through the process until settlement.</li>
        </ol>
        <p class="muted">For cashless admissions, contact our network hospital and inform Care Nest before admission.</p>
      </div>
    </section>

    <section id="contact" style="margin-top:18px">
      <h2>Contact us</h2>
      <div class="contact" style="margin-top:12px">
        <form id="contact-form" onsubmit="event.preventDefault(); submitContact();">
          <label for="name">Full name</label>
          <input id="name" type="text" required>

          <label for="email">Email</label>
          <input id="email" type="email" required>

          <label for="phone">Phone</label>
          <input id="phone" type="tel" pattern="[0-9+\- ]{7,20}" required>

          <label for="message">Message</label>
          <textarea id="message" required placeholder="How can we help?"></textarea>

          <div style="display:flex;gap:8px;margin-top:8px">
            <button class="btn btn-primary" type="submit">Send Message</button>
            <button class="btn" type="button" onclick="resetForm()">Reset</button>
          </div>

          <p id="contact-result" class="muted" style="margin-top:8px"></p>
        </form>

        <div style="padding:12px;background:#f8faf8;border-radius:10px">
          <h4>Office</h4>
          <p class="muted">PrimeCover Insurance<br>123 Wellness Avenue<br>Bengaluru, India</p>
          <p class="muted"><strong>Phone:</strong> 1800-123-CARE (2273)<br><strong>Email:</strong> support@carenest.example</p>
        </div>
      </div>
    </section>

    <section class="faq">
      <h2>FAQ</h2>
      <div>
        <details class="faq-item">
          <summary>How long does claim settlement take?</summary>
          <p class="muted">For cashless claims, most settlements are processed within 48–72 hours after submission of documents. Reimbursement claims depend on document completeness but typically complete within 7–21 business days.</p>
        </details>

        <details class="faq-item">
          <summary>Can I add my family to an existing policy?</summary>
          <p class="muted">Yes — family floater and add-on options are available at policy renewal or during purchase for applicable plans.</p>
        </details>
      </div>
    </section>

  </main>

  <footer>
    <div class="container" style="display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap">
      <div>© <strong>PrimeCover Insurance</strong> — All rights reserved</div>
      <div style="color:var(--muted)">Designed with care · Privacy · Terms</div>
    </div>
  </footer>

  <script>
    function getQuote(){
      const age = Number(document.getElementById('age').value || 30);
      const sum = Number(document.getElementById('sum').value || 300000);
      const type = document.getElementById('type').value;

      // simple premium estimator (illustrative only)
      let baseRate = 0.006; // 0.6% of sum insured
      if(type==='family') baseRate *= 1.6;
      if(type==='senior') baseRate *= 2.8;
      // age loading
      if(age>50) baseRate *= 1.8;
      const premium = Math.round(sum * baseRate / 12); // monthly approx

      document.getElementById('estimate').textContent = 'Approx. premium: ₹' + premium + ' / month (indicative)';
    }

    function submitContact(){
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const phone = document.getElementById('phone').value.trim();
      const message = document.getElementById('message').value.trim();

      if(!name||!email||!phone||!message){
        document.getElementById('contact-result').textContent = 'Please fill all fields.';
        return;
      }

      // In a real site, you'd send this to your server via fetch/XHR.
      document.getElementById('contact-result').textContent = 'Thanks ' + name.split(' ')[0] + '! We received your message and will contact you shortly.';
      document.getElementById('contact-form').reset();
    }

    function resetForm(){
      document.getElementById('contact-form').reset();
      document.getElementById('contact-result').textContent='';
    }
  </script>
  <script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00DdL00000g8w1y',
				'CareNestWebDeployment',
				'https://orgfarm-afea3160f2-dev-ed.develop.my.site.com/ESWCareNestWebDeployment1764069847513',
				{
					scrt2URL: 'https://orgfarm-afea3160f2-dev-ed.develop.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://orgfarm-afea3160f2-dev-ed.develop.my.site.com/ESWCareNestWebDeployment1764069847513/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>

</body>
</html>
