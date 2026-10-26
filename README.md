<!DOCTYPE html>
<html lang="hi">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Janova Jobs | Career Portal</title>
  <style>
    :root {
      --bg: #050d1b;
      --panel: #0b1930;
      --panel2: #102341;
      --line: #1c3658;
      --text: #edf5ff;
      --muted: #a0b4d0;
      --blue: #277bff;
      --purple: #873cff;
      --red: #ed3558;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0
    }

    html {
      scroll-behavior: smooth
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: Inter, Segoe UI, Arial, sans-serif;
      line-height: 1.5
    }

    a {
      text-decoration: none;
      color: inherit
    }

    button,
    input {
      font: inherit
    }

    button {
      cursor: pointer
    }

    .wrap {
      width: min(1440px, 94%);
      margin: auto
    }

    nav {
      position: sticky;
      top: 0;
      z-index: 20;
      background: #061126ed;
      backdrop-filter: blur(18px);
      border-bottom: 1px solid var(--line)
    }

    .nav {
      height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px
    }

    .brand {
      font-size: 25px;
      font-weight: 900;
      letter-spacing: -1px
    }

    .brand span {
      color: #628cff
    }

    .brand small {
      display: block;
      font-size: 10px;
      letter-spacing: 2px;
      color: var(--muted)
    }

    .links {
      display: flex;
      gap: 24px;
      align-items: center;
      font-size: 13px;
      color: #d4e1f5
    }

    .links a:hover {
      color: #8aa9ff
    }

    .btn {
      border: 0;
      border-radius: 9px;
      padding: 12px 18px;
      color: white;
      background: linear-gradient(110deg, var(--blue), var(--purple));
      font-weight: 750;
      transition: .2s
    }

    .btn:hover {
      transform: translateY(-2px);
      filter: brightness(1.15)
    }

    .menu {
      display: none;
      background: none;
      color: white;
      border: 1px solid var(--line);
      padding: 9px 12px;
      border-radius: 8px
    }

    .hero {
      position: relative;
      overflow: hidden;
      background: radial-gradient(ellipse at 75% 40%, #243d83 0, transparent 35%),
        linear-gradient(120deg, #091a38, #071126 65%, #16113d);
      border-bottom: 1px solid var(--line)
    }

    .hero-inner {
      padding: 78px 0 62px;
      max-width: 780px
    }

    .pill {
      display: inline-flex;
      gap: 8px;
      align-items: center;
      border: 1px solid #3567ad;
      border-radius: 50px;
      padding: 7px 13px;
      color: #a9c9ff;
      font-size: 12px;
      background: #12264a;
      margin-bottom: 20px
    }

    h1 {
      font-size: clamp(38px, 5vw, 66px);
      line-height: 1.08;
      letter-spacing: -2px
    }

    .grad {
      background: linear-gradient(90deg, #6ba6ff, #bb76ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent
    }

    .hero p {
      color: #b6c9e4;
      margin: 20px 0 25px;
      max-width: 570px
    }

    .search {
      display: flex;
      gap: 8px;
      padding: 7px;
      background: white;
      border-radius: 12px;
      max-width: 690px;
      box-shadow: 0 15px 55px #0005
    }

    .search input {
      flex: 1;
      min-width: 0;
      border: 0;
      outline: 0;
      padding: 12px;
      color: #102341
    }

    .trending {
      margin-top: 19px;
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      align-items: center;
      font-size: 12px;
      color: var(--muted)
    }

    .trending button {
      background: #132746;
      border: 1px solid #264568;
      color: #dce9ff;
      border-radius: 20px;
      padding: 6px 12px
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 14px;
      margin: 25px auto
    }

    .stat {
      padding: 22px 16px;
      border: 1px solid var(--line);
      border-radius: 13px;
      background: linear-gradient(145deg, #112746, #0a162a);
      transition: .2s
    }

    .stat:hover {
      transform: translateY(-4px);
      border-color: #477de1
    }

    .stat .ico {
      font-size: 24px
    }

    .stat h3 {
      font-size: 17px;
      margin: 8px 0 3px
    }

    .stat p {
      font-size: 12px;
      color: var(--muted)
    }

    .content {
      display: grid;
      grid-template-columns: 235px minmax(0, 1fr) 260px;
      gap: 18px
    }

    .panel {
      border: 1px solid var(--line);
      border-radius: 13px;
      background: linear-gradient(145deg, #0c1c34, #081529);
      overflow: hidden;
      margin-bottom: 18px
    }

    .ph {
      padding: 16px 17px;
      border-bottom: 1px solid var(--line);
      font-weight: 800;
      display: flex;
      justify-content: space-between;
      gap: 10px
    }

    .pb {
      padding: 15px
    }

    .quick a {
      display: block;
      padding: 12px 2px;
      border-bottom: 1px solid #1a304b;
      font-size: 13px;
      color: #cfdef2
    }

    .quick a:last-child {
      border-bottom: 0
    }

    .quick a:hover {
      color: #8baaff
    }

    .tabs {
      display: flex;
      overflow: auto;
      border-bottom: 1px solid var(--line)
    }

    .tab {
      white-space: nowrap;
      background: none;
      border: 0;
      border-bottom: 2px solid transparent;
      padding: 16px 15px;
      color: var(--muted);
      font-size: 12px;
      font-weight: 750
    }

    .tab.active {
      color: #91b5ff;
      border-color: #6489ff
    }

    .job {
      display: grid;
      grid-template-columns: 92px minmax(0, 1fr) auto;
      align-items: center;
      gap: 13px;
      padding: 17px;
      border-bottom: 1px solid #182e49
    }

    .job:last-child {
      border-bottom: 0
    }

    .job:hover {
      background: #10213a
    }

    .badge {
      font-size: 10px;
      font-weight: 800;
      text-align: center;
      padding: 7px 5px;
      border-radius: 6px;
      background: #15345c;
      color: #8dbbff
    }

    .badge.red {
      background: #45182c;
      color: #ff9bb1
    }

    .badge.green {
      background: #103b34;
      color: #74e5c3
    }

    .badge.gold {
      background: #443016;
      color: #ffce77
    }

    .job h3 {
      font-size: 13px;
      margin-bottom: 5px
    }

    .job p {
      font-size: 11px;
      color: var(--muted)
    }

    .job .btn {
      font-size: 11px;
      padding: 9px 11px
    }

    .tag {
      font-size: 9px;
      background: #163a2e;
      color: #80e7b7;
      padding: 3px 6px;
      border-radius: 4px;
      margin-left: 5px
    }

    .updates {
      list-style: none
    }

    .updates li {
      padding: 12px 0;
      border-bottom: 1px solid #1a304b;
      font-size: 12px
    }

    .updates li:last-child {
      border: 0
    }

    .updates small {
      display: block;
      color: var(--muted);
      margin-top: 4px
    }

    .dot {
      display: inline-block;
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: #49d6a0;
      margin-right: 8px
    }

    .exam-grid {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 12px
    }

    .exam {
      border: 1px solid var(--line);
      background: var(--panel);
      padding: 16px 10px;
      border-radius: 10px;
      text-align: center
    }

    .exam strong {
      display: block;
      font-size: 13px
    }

    .exam span {
      font-size: 11px;
      color: var(--muted)
    }

    .exam:hover {
      border-color: #647fff
    }

    .section-title {
      font-size: 22px;
      margin: 35px 0 17px
    }

    footer {
      margin-top: 42px;
      padding: 30px 0;
      border-top: 1px solid var(--line);
      color: var(--muted);
      font-size: 12px
    }

    .foot {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap
    }

    .foot a {
      margin-right: 15px;
      color: #d5e2fa
    }

    .disclaimer {
      margin-top: 18px;
      color: #8fa5c1;
      font-size: 11px
    }

    .empty {
      padding: 30px;
      text-align: center;
      color: var(--muted);
      display: none
    }

    @media(max-width:1050px) {
      .content {
        grid-template-columns: 220px minmax(0, 1fr)
      }

      .right {
        grid-column: 1/-1;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 15px
      }

      .exam-grid {
        grid-template-columns: repeat(3, 1fr)
      }

      .stats {
        grid-template-columns: repeat(3, 1fr)
      }

      .links {
        gap: 13px
      }
    }

    @media(max-width:720px) {
      .nav {
        height: 65px
      }

      .menu {
        display: block
      }

      .links {
        display: none;
        position: absolute;
        top: 65px;
        left: 0;
        right: 0;
        background: #08162b;
        padding: 20px;
        flex-direction: column;
        align-items: stretch;
        border-bottom: 1px solid var(--line)
      }

      .links.open {
        display: flex
      }

      .hero-inner {
        padding: 55px 0 40px
      }

      h1 {
        letter-spacing: -1px
      }

      .stats {
        grid-template-columns: repeat(2, 1fr);
        gap: 10px
      }

      .content {
        grid-template-columns: 1fr
      }

      .left,
      .right {
        display: block;
        grid-column: auto
      }

      .job {
        grid-template-columns: 74px minmax(0, 1fr);
        gap: 10px;
        padding: 14px 10px
      }

      .job .btn {
        grid-column: 2;
        justify-self: start
      }

      .exam-grid {
        grid-template-columns: repeat(2, 1fr)
      }

      .search .btn {
        padding: 10px
      }

      .stat {
        padding: 15px 12px
      }
    }
  </style>
</head>

<body>
  <nav>
    <div class="wrap nav">
      <a class="brand" href="#home"><span>Janova</span> Jobs
        <small>YOUR DREAM · OUR MISSION</small></a>
      <div class="links" id="navlinks">
        <a href="#home">Home</a><a href="#jobs">Latest Jobs</a>
        <a href="#jobs">Admit Card</a><a href="#jobs">Results</a>
        <a href="#exams">Popular Exams</a>
      </div>
      <button class="menu" id="menu">☰ Menu</button>
    </div>
  </nav>

  <section class="hero" id="home">
    <div class="wrap">
      <div class="hero-inner">
        <div class="pill">✦ GOVERNMENT JOBS & EXAM UPDATES</div>
        <h1>Find Your Dream Job<br>With <span class="grad">Janova Jobs.</span></h1>
        <p>Latest government vacancies, exam results, admit cards and admission updates — sab ek jagah, ek modern
          platform par.</p>
        <div class="search">
          <input id="search" placeholder="Search job, exam ya department..." aria-label="Search updates">
          <button class="btn" id="searchBtn">⌕ Search</button>
        </div>
        <div class="trending">Trending:
          <button data-term="SSC">SSC</button><button data-term="Railway">Railway</button>
          <button data-term="UPSC">UPSC</button><button data-term="Bihar">Bihar</button>
          <button data-term="Bank">Banking</button><button data-term="JEE">JEE</button>
        </div>
      </div>
    </div>
  </section>

  <main class="wrap">
    <section class="stats">
      <a class="stat" href="#jobs" data-category="Jobs">
        <div class="ico">💼</div>
        <h3>Latest Jobs</h3>
        <p>Vacancy notifications</p>
      </a>
      <a class="stat" href="#jobs" data-category="Admit Card">
        <div class="ico">🎫</div>
        <h3>Admit Cards</h3>
        <p>Hall ticket updates</p>
      </a>
      <a class="stat" href="#jobs" data-category="Results">
        <div class="ico">📊</div>
        <h3>Results</h3>
        <p>Exam result notices</p>
      </a>
      <a class="stat" href="#jobs" data-category="Answer Key">
        <div class="ico">📝</div>
        <h3>Answer Keys</h3>
        <p>Answer key notices</p>
      </a>
      <a class="stat" href="#jobs" data-category="Admissions">
        <div class="ico">🎓</div>
        <h3>Admissions</h3>
        <p>Application forms</p>
      </a>
    </section>

    <section class="content" id="jobs">
      <aside class="left">
        <div class="panel">
          <div class="ph">⚡ Quick Links</div>
          <div class="pb quick">
            <a href="https://upsc.gov.in/" target="_blank" rel="noopener">↗ UPSC Official Website</a>
            <a href="https://ssc.gov.in/" target="_blank" rel="noopener">↗ SSC Official Website</a>
            <a href="https://www.rrbcdg.gov.in/" target="_blank" rel="noopener">↗ Railway Recruitment</a>
            <a href="https://bpsc.bihar.gov.in/" target="_blank" rel="noopener">↗ BPSC Bihar</a>
            <a href="https://www.ibps.in/" target="_blank" rel="noopener">↗ IBPS Banking</a>
          </div>
        </div>
        <div class="panel">
          <div class="ph">🔔 Stay Updated</div>
          <div class="pb">
            <p style="font-size:13px;color:var(--muted);margin-bottom:12px">Latest updates dekhne ke liye regular visit
              karein.</p>
            <button class="btn" style="width:100%" id="notify">Enable Alerts</button>
          </div>
        </div>
      </aside>

      <section class="panel">
        <div class="tabs" id="tabs">
          <button class="tab active" data-category="All">All Updates</button>
          <button class="tab" data-category="Jobs">Latest Jobs</button>
          <button class="tab" data-category="Admit Card">Admit Card</button>
          <button class="tab" data-category="Results">Results</button>
          <button class="tab" data-category="Answer Key">Answer Key</button>
          <button class="tab" data-category="Admissions">Admissions</button>
        </div>
        <div id="listing">
          <article class="job" data-category="Jobs">
            <div class="badge green">LATEST JOB</div>
            <div>
              <h3>SSC Recruitment <span class="tag">DEMO</span></h3>
              <p>Staff Selection Commission · Sample listing</p>
            </div>
            <a class="btn official" href="https://ssc.gov.in/" target="_blank" rel="noopener">Official Site ↗</a>
          </article>
          <article class="job" data-category="Jobs">
            <div class="badge">RAILWAY</div>
            <div>
              <h3>Railway Recruitment <span class="tag">DEMO</span></h3>
              <p>Railway Recruitment Boards · Sample listing</p>
            </div>
            <a class="btn official" href="https://www.rrbcdg.gov.in/" target="_blank" rel="noopener">Official Site ↗</a>
          </article>
          <article class="job" data-category="Admit Card">
            <div class="badge red">ADMIT CARD</div>
            <div>
              <h3>SSC Exam Admit Card <span class="tag">DEMO</span></h3>
              <p>Hall ticket information · Verify official notice</p>
            </div>
            <a class="btn official" href="https://ssc.gov.in/" target="_blank" rel="noopener">Check ↗</a>
          </article>
          <article class="job" data-category="Results">
            <div class="badge">RESULT</div>
            <div>
              <h3>Competitive Exam Results <span class="tag">DEMO</span></h3>
              <p>Result announcements · Sample listing</p>
            </div>
            <a class="btn official" href="https://upsc.gov.in/" target="_blank" rel="noopener">Check ↗</a>
          </article>
          <article class="job" data-category="Answer Key">
            <div class="badge" style="background:#34205e;color:#d2b8ff">ANSWER KEY</div>
            <div>
              <h3>Exam Answer Key <span class="tag">DEMO</span></h3>
              <p>Provisional answer key · Sample listing</p>
            </div>
            <a class="btn official" href="https://ssc.gov.in/" target="_blank" rel="noopener">Check ↗</a>
          </article>
          <article class="job" data-category="Admissions">
            <div class="badge gold">ADMISSION</div>
            <div>
              <h3>College Admission Updates <span class="tag">DEMO</span></h3>
              <p>Application information · Sample listing</p>
            </div>
            <a class="btn official" href="https://www.nTA.ac.in/" target="_blank" rel="noopener">Check ↗</a>
          </article>
        </div>
        <div class="empty" id="empty">Koi update nahi mila. Dusra keyword try karein.</div>
        <div style="padding:14px 17px;color:var(--muted);font-size:11px">
          Demo content only. Actual vacancy, eligibility aur dates verify karein.
        </div>
      </section>

      <aside class="right">
        <div class="panel">
          <div class="ph">⚡ Latest Updates</div>
          <div class="pb">
            <ul class="updates">
              <li><span class="dot"></span>SSC recruitment information<small>Demo update · Official notice check
                  karein</small></li>
              <li><span class="dot" style="background:#ff5a78"></span>Railway recruitment information<small>Demo update
                  · Official notice check karein</small></li>
              <li><span class="dot" style="background:#6b9cff"></span>Bihar examination information<small>Demo update ·
                  Official notice check karein</small></li>
              <li><span class="dot" style="background:#b58aff"></span>Admission notifications<small>Demo update ·
                  Official notice check karein</small></li>
            </ul>
          </div>
        </div>
        <div class="panel">
          <div class="ph">💡 Career Tip</div>
          <div class="pb">
            <h3 style="font-size:16px">Prepare Smartly</h3>
            <p style="font-size:12px;color:var(--muted);margin:9px 0 14px">Official syllabus dekhein, previous papers
              solve karein aur deadlines note karein.</p>
            <a href="#exams" class="btn" style="display:inline-block">Explore Exams →</a>
          </div>
        </div>
      </aside>
    </section>

    <h2 class="section-title" id="exams">✦ Popular Exam Categories</h2>
    <section class="exam-grid">
      <a class="exam" href="https://upsc.gov.in/" target="_blank" rel="noopener"><strong>🏛 UPSC</strong><span>Civil
          Services</span></a>
      <a class="exam" href="https://ssc.gov.in/" target="_blank" rel="noopener"><strong>🎯 SSC</strong><span>CGL / CHSL
          / MTS</span></a>
      <a class="exam" href="https://www.rrbcdg.gov.in/" target="_blank" rel="noopener"><strong>🚆
          Railway</strong><span>RRB Exams</span></a>
      <a class="exam" href="https://www.ibps.in/" target="_blank" rel="noopener"><strong>🏦 Banking</strong><span>IBPS
          Exams</span></a>
      <a class="exam" href="https://bpsc.bihar.gov.in/" target="_blank" rel="noopener"><strong>📚
          Bihar</strong><span>State Exams</span></a>
      <a class="exam" href="https://www.nta.ac.in/" target="_blank" rel="noopener"><strong>🎓 NTA</strong><span>Entrance
          Exams</span></a>
    </section>
  </main>

  <footer>
    <div class="wrap foot">
      <a class="brand" href="#home"><span>Janova</span> Jobs<small>YOUR DREAM · OUR MISSION</small></a>
      <div><a href="#home">Home</a><a href="#jobs">Updates</a><a href="#exams">Exams</a></div>
    </div>
    <div class="wrap disclaimer">
      Disclaimer: Janova Jobs is an independent information portal and is not affiliated with any government department.
      Sample listings are not actual vacancy announcements. Always verify details on the relevant official website.
      <p style="margin-top:12px">© <span id="year"></span> Janova Jobs. All rights reserved.</p>
    </div>
  </footer>

  <script>
    const search = document.getElementById("search");
    const listing = document.getElementById("listing");
    const items = [...listing.querySelectorAll(".job")];
    const empty = document.getElementById("empty");
    const tabs = [...document.querySelectorAll(".tab")];
    let category = "All";

    function render() {
      let shown = 0;
      const q = search.value.trim().toLowerCase();
      items.forEach(item => {
        const matchCategory = category === "All" || item.dataset.category === category;
        const matchText = item.textContent.toLowerCase().includes(q);
        item.style.display = matchCategory && matchText ? "grid" : "none";
        if (matchCategory && matchText) shown++;
      });
      empty.style.display = shown ? "none" : "block";
    }

    function setCategory(value) {
      category = value;
      tabs.forEach(t => t.classList.toggle("active", t.dataset.category === value));
      render();
      document.getElementById("jobs").scrollIntoView({ behavior: "smooth", block: "start" });
    }

    tabs.forEach(t => t.addEventListener("click", () => setCategory(t.dataset.category)));
    document.querySelectorAll("[data-category].stat").forEach(card => {
      card.addEventListener("click", () => setCategory(card.dataset.category));
    });
    document.querySelectorAll("[data-term]").forEach(button => {
      button.addEventListener("click", () => {
        search.value = button.dataset.term;
        category = "All";
        tabs.forEach(t => t.classList.toggle("active", t.dataset.category === "All"));
        render();
        document.getElementById("jobs").scrollIntoView({ behavior: "smooth" });
      });
    });
    document.getElementById("searchBtn").addEventListener("click", render);
    search.addEventListener("input", render);
    document.getElementById("menu").addEventListener("click", () => {
      document.getElementById("navlinks").classList.toggle("open");
    });
    document.querySelectorAll("#navlinks a").forEach(a => {
      a.addEventListener("click", () => document.getElementById("navlinks").classList.remove("open"));
    });
    document.getElementById("year").textContent = new Date().getFullYear();
    document.getElementById("notify").addEventListener("click", () => {
      alert("Notification feature abhi demo hai. Real job alerts ke liye backend aur notification service integrate karni hogi.");
    });
    render();
  </script>
</body>

</html>
