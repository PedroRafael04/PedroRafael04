<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:060d1a,50:0d2137,100:0a1628&height=220&section=header&text=Pedro%20Rafael&fontSize=56&fontColor=4FC3F7&animation=fadeIn&fontAlignY=40&desc=Back-end%20Developer%20%7C%20Computer%20Science%20Student&descAlignY=58&descSize=17&descColor=90CAF9"/>

</div>

<br/>

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pedro-rafael-9a1a891a7/)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:pedrorafaelofficial@gmail.com)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=flat-square&logo=instagram&logoColor=white)](https://instagram.com/raffaels__)
![Location](https://img.shields.io/badge/📍_Indaial,_SC-Brazil-1565C0?style=flat-square)

</div>

---

## $ whoami

```java
public class PedroRafael {

    private final String name     = "Pedro Rafael de Souza e Silva";
    private final String role     = "Back-end Developer";
    private final String course   = "Bachelor in Computer Science";
    private final String location = "Indaial, SC — Brazil";

    private final String[] languages = { "Java", "Python" };
    private final String[] interests = { "Back-end Architecture",
                                         "Open Source", "Academic Research" };

    public String getMotivation() {
        return "No amount of money ever bought a second of time. " +
               "Value it and keep learning!";
    }
}
```

---

## 📊 Languages & Stats

<details>
<summary><b>🖥 Abrir dashboard interativo (HTML)</b></summary>

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8"/>
<title>Pedro Rafael — GitHub Dashboard</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Outfit:wght@400;600;800&display=swap');
  *, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
  :root {
    --bg:#060d1a; --surface:#0d1b2e; --border:#1a2f4a;
    --accent:#4FC3F7; --accent2:#0288D1;
    --java:#F89820; --python:#3776AB;
    --text:#cdd9e5; --muted:#607d8b;
  }
  body { background:var(--bg); font-family:'Outfit',sans-serif; color:var(--text); display:flex; justify-content:center; padding:36px 20px; }
  .dashboard { display:grid; grid-template-columns:1fr 1fr; gap:20px; max-width:880px; width:100%; }
  .card { background:var(--surface); border:1px solid var(--border); border-radius:16px; padding:28px 28px 24px; position:relative; overflow:hidden; transition:transform .25s, box-shadow .25s; }
  .card:hover { transform:translateY(-5px); box-shadow:0 16px 48px rgba(79,195,247,.10); }
  .card::after { content:''; position:absolute; top:0; left:0; right:0; height:2px; background:linear-gradient(90deg,var(--accent2),var(--accent),transparent); }
  .card-title { font-size:11px; font-weight:600; letter-spacing:2.5px; text-transform:uppercase; color:var(--accent); margin-bottom:22px; }
  .pie-wrap { display:flex; align-items:center; gap:26px; }
  .donut-container { position:relative; flex-shrink:0; }
  .donut-svg { transform:rotate(-90deg); }
  .donut-label { position:absolute; inset:0; display:flex; flex-direction:column; align-items:center; justify-content:center; font-family:'JetBrains Mono',monospace; }
  .donut-label span { font-size:11px; color:var(--muted); }
  .donut-label strong { font-size:20px; color:var(--accent); font-weight:700; }
  .legend { display:flex; flex-direction:column; gap:14px; flex:1; }
  .legend-row { display:flex; align-items:center; gap:10px; font-family:'JetBrains Mono',monospace; font-size:12px; }
  .dot { width:10px; height:10px; border-radius:50%; flex-shrink:0; }
  .bar-bg { flex:1; height:5px; background:var(--border); border-radius:4px; overflow:hidden; }
  .bar { height:100%; border-radius:4px; }
  .pct { min-width:42px; text-align:right; color:var(--text); font-weight:700; }
  .lang-name { min-width:56px; color:var(--muted); }
  .stats-list { display:flex; flex-direction:column; gap:10px; }
  .stat-row { display:flex; align-items:center; justify-content:space-between; padding:10px 14px; background:var(--bg); border:1px solid var(--border); border-radius:10px; transition:border-color .2s; }
  .stat-row:hover { border-color:var(--accent2); }
  .stat-label { display:flex; align-items:center; gap:10px; font-family:'JetBrains Mono',monospace; font-size:12px; color:var(--muted); }
  .stat-value { font-family:'JetBrains Mono',monospace; font-size:20px; font-weight:700; color:var(--text); }
  .stat-value.hi { color:var(--accent); }
  .rank-badge { position:absolute; right:24px; top:50%; transform:translateY(-50%); width:68px; height:68px; }
  .rank-badge svg { transform:rotate(-90deg); }
  .rank-letter { position:absolute; inset:0; display:flex; align-items:center; justify-content:center; font-family:'JetBrains Mono',monospace; font-size:26px; font-weight:700; color:var(--text); }
  .full { grid-column:1 / -1; }
  .pills { display:flex; justify-content:space-around; gap:12px; }
  .pill { flex:1; text-align:center; padding:18px 12px; background:var(--bg); border:1px solid var(--border); border-radius:12px; transition:border-color .2s, transform .2s; }
  .pill:hover { border-color:var(--accent2); transform:translateY(-3px); }
  .pill-label { font-size:10px; letter-spacing:2px; text-transform:uppercase; color:var(--muted); font-family:'JetBrains Mono',monospace; margin-bottom:8px; }
  .pill-value { font-size:26px; font-weight:800; font-family:'JetBrains Mono',monospace; }
  .pill-sub { font-size:11px; color:var(--border); margin-top:4px; font-family:'JetBrains Mono',monospace; }
  .bio { grid-column:1 / -1; display:flex; align-items:center; gap:20px; padding:24px; background:var(--surface); border:1px solid var(--border); border-radius:16px; }
  .avatar { width:64px; height:64px; border-radius:50%; background:linear-gradient(135deg,var(--accent2),var(--accent)); display:flex; align-items:center; justify-content:center; font-size:22px; font-weight:800; color:var(--bg); flex-shrink:0; }
  .bio-info h2 { font-size:18px; font-weight:700; color:var(--text); }
  .bio-info p  { font-size:13px; color:var(--muted); margin-top:4px; font-family:'JetBrains Mono',monospace; }
  .bio-info em { font-size:12px; color:var(--accent); font-style:normal; }
</style>
</head>
<body>
<div class="dashboard">

  <div class="bio">
    <div class="avatar">PR</div>
    <div class="bio-info">
      <h2>Pedro Rafael de Souza e Silva</h2>
      <p>Back-end Developer &nbsp;|&nbsp; BSc Computer Science &nbsp;|&nbsp; Indaial, SC — Brazil</p>
      <em>"No amount of money ever bought a second of time. Value it and keep learning!"</em>
    </div>
  </div>

  <div class="card">
    <div class="card-title">Most Used Languages</div>
    <div class="pie-wrap">
      <div class="donut-container">
        <svg class="donut-svg" width="120" height="120" viewBox="0 0 120 120">
          <circle cx="60" cy="60" r="48" fill="none" stroke="#1a2f4a" stroke-width="18"/>
          <circle cx="60" cy="60" r="48" fill="none" stroke="#F89820" stroke-width="18" stroke-dasharray="195.94 301.44" stroke-dashoffset="0"/>
          <circle cx="60" cy="60" r="48" fill="none" stroke="#3776AB" stroke-width="18" stroke-dasharray="105.50 301.44" stroke-dashoffset="-195.94"/>
        </svg>
        <div class="donut-label"><strong>2</strong><span>langs</span></div>
      </div>
      <div class="legend">
        <div class="legend-row">
          <span class="dot" style="background:#F89820"></span>
          <span class="lang-name">Java</span>
          <div class="bar-bg"><div class="bar" style="width:65%;background:#F89820"></div></div>
          <span class="pct">65%</span>
        </div>
        <div class="legend-row">
          <span class="dot" style="background:#3776AB"></span>
          <span class="lang-name">Python</span>
          <div class="bar-bg"><div class="bar" style="width:35%;background:#3776AB"></div></div>
          <span class="pct">35%</span>
        </div>
      </div>
    </div>
  </div>

  <div class="card" style="position:relative;">
    <div class="card-title">GitHub Stats — PedroRafael04</div>
    <div class="stats-list">
      <div class="stat-row"><div class="stat-label"><span>⭐</span> Stars Earned</div><span class="stat-value hi">—</span></div>
      <div class="stat-row"><div class="stat-label"><span>🕐</span> Commits (last year)</div><span class="stat-value">—</span></div>
      <div class="stat-row"><div class="stat-label"><span>🔀</span> Pull Requests</div><span class="stat-value hi">—</span></div>
      <div class="stat-row"><div class="stat-label"><span>📁</span> Repositórios</div><span class="stat-value">—</span></div>
      <div class="stat-row"><div class="stat-label"><span>🤝</span> Contribuições</div><span class="stat-value">—</span></div>
    </div>
    <div class="rank-badge">
      <svg width="68" height="68" viewBox="0 0 68 68">
        <circle cx="34" cy="34" r="28" fill="none" stroke="#1a2f4a" stroke-width="6"/>
        <circle cx="34" cy="34" r="28" fill="none" stroke="#4FC3F7" stroke-width="6" stroke-dasharray="105 176" stroke-linecap="round"/>
      </svg>
      <div class="rank-letter">A</div>
    </div>
  </div>

  <div class="card full">
    <div class="pills">
      <div class="pill"><div class="pill-label">Focus</div><div class="pill-value" style="font-size:18px;color:#4FC3F7">Back-end</div><div class="pill-sub">Development</div></div>
      <div class="pill"><div class="pill-label">Degree</div><div class="pill-value" style="font-size:18px;color:#F89820">BCC</div><div class="pill-sub">Computer Science</div></div>
      <div class="pill"><div class="pill-label">Open Source</div><div class="pill-value" style="font-size:18px;color:#3776AB">✓</div><div class="pill-sub">Contributor</div></div>
      <div class="pill"><div class="pill-label">Location</div><div class="pill-value" style="font-size:18px;color:#4FC3F7">SC</div><div class="pill-sub">Brazil</div></div>
    </div>
  </div>

</div>
</body>
</html>
```

</details>

---

<div align="center">

<img height="175" src="https://github-readme-stats.vercel.app/api?username=PedroRafael04&show_icons=true&theme=tokyonight&hide_border=true&bg_color=060d1a&title_color=4FC3F7&icon_color=4FC3F7&text_color=cdd9e5&count_private=true" alt="Pedro Rafael GitHub Stats"/>

<img height="175" src="https://github-readme-stats.vercel.app/api/top-langs/?username=PedroRafael04&layout=donut&theme=tokyonight&hide_border=true&bg_color=060d1a&title_color=4FC3F7&text_color=cdd9e5&langs_count=2" alt="Most Used Languages"/>

</div>

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com?user=PedroRafael04&theme=tokyonight-duo&hide_border=true&background=060d1a&ring=4FC3F7&fire=4FC3F7&currStreakLabel=cdd9e5" alt="GitHub Streak"/>

</div>

---

## 🛠️ Tech Stack

<div align="center">

![Java](https://img.shields.io/badge/Java-F89820?style=for-the-badge&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-0d1b2e?style=for-the-badge&logo=github&logoColor=4FC3F7)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

</div>

---

## 📬 Contact Me

<div align="center">

[![LinkedIn](https://img.shields.io/badge/Pedro%20Rafael-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pedro-rafael-9a1a891a7/)
[![Gmail](https://img.shields.io/badge/pedrorafaelofficial@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pedrorafaelofficial@gmail.com)
[![Instagram](https://img.shields.io/badge/@raffaels__-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/raffaels__)

</div>

---

<div align="center">

<sub><i>"No amount of money ever bought a second of time. Value it and keep learning!"</i></sub>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0a1628,50:0d2137,100:060d1a&height=100&section=footer"/>

</div>
