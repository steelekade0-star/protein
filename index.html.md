# Protein website   
  
<!doctype html>  
<html lang="en">  
<head>  
  <meta charset="utf-8" />  
  <meta name="viewport" content="width=device-width,initial-scale=1" />  
  <title>$PROTEIN</title>  
  <meta name="description" content="$PROTEIN — Eat. Lift. Hold. Repeat." />  
  <style>  
    :root{  
      --bg:#070A10;  
      --card: rgba(255,255,255,.06);  
      --line: rgba(255,255,255,.10);  
      --text:#EEF2FF;  
      --muted: rgba(238,242,255,.72);  
      --accent:#38ff8b;  
      --accent2:#ffb020;  
      --radius:18px;  
      --shadow: 0 18px 60px rgba(0,0,0,.45);  
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;  
      --sans: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial;  
    }  
    *{box-sizing:border-box}  
    body{  
      margin:0;  
      font-family: var(--sans);  
      color:var(--text);  
      background:  
        radial-gradient(900px 600px at 20% 0%, rgba(56,255,139,.12), transparent 60%),  
        radial-gradient(900px 600px at 90% 10%, rgba(255,176,32,.10), transparent 55%),  
        var(--bg);  
    }  
    .wrap{max-width:980px;margin:0 auto;padding:22px}  
    .card{  
      border:1px solid var(--line);  
      background: var(--card);  
      border-radius: var(--radius);  
      box-shadow: var(--shadow);  
      overflow:hidden;  
    }  
    .pad{padding:18px}  
    .top{  
      display:flex;align-items:center;justify-content:space-between;gap:14px;  
      padding:14px 18px;  
      position:sticky;top:0;z-index:10;  
      background: rgba(7,10,16,.72);  
      backdrop-filter: blur(12px);  
      border-bottom:1px solid var(--line);  
    }  
    .brand{display:flex;align-items:center;gap:12px}  
    .mark{  
      width:42px;height:42px;border-radius:14px;  
      border:1px solid var(--line);  
      background: linear-gradient(135deg, rgba(56,255,139,.22), rgba(255,176,32,.18));  
      display:grid;place-items:center;  
    }  
    .brand b{display:block;font-weight:900;letter-spacing:.4px}  
    .brand span{display:block;font-size:12px;color:var(--muted);margin-top:2px}  
    .actions{display:flex;gap:10px;flex-wrap:wrap;justify-content:flex-end}  
    .btn{  
      border:1px solid var(--line);  
      background: rgba(255,255,255,.06);  
      color:var(--text);  
      padding:10px 12px;border-radius:14px;  
      font-weight:800;font-size:13px;  
      cursor:pointer;  
      transition:.2s transform,.2s background;  
      text-decoration:none;  
      user-select:none;  
    }  
    .btn:hover{transform: translateY(-1px); background: rgba(255,255,255,.10)}  
    .btn.primary{border-color: rgba(56,255,139,.35)}  
    .btn.accent{border-color: rgba(255,176,32,.35)}  
    .hero{  
      margin-top:18px;  
      display:grid;gap:18px;  
    }  
    h1{  
      margin:0;  
      font-size:46px;  
      letter-spacing:-1px;  
      line-height:1.05;  
    }  
    p{margin:12px 0 0 0;color:var(--muted);line-height:1.6}  
    .row{display:flex;gap:10px;flex-wrap:wrap;margin-top:16px}  
    .pill{  
      border:1px solid var(--line);  
      background: rgba(0,0,0,.18);  
      padding:8px 10px;border-radius:999px;  
      font-size:12px;  
      color:rgba(238,242,255,.86);  
      font-family:var(--mono);  
    }  
    .sectionTitle{margin:0 0 8px 0;font-weight:900;font-size:16px}  
    .grid{  
      display:grid;grid-template-columns:1fr 1fr;gap:18px;margin-top:18px;  
    }  
    @media (max-width: 860px){ .grid{grid-template-columns:1fr} h1{font-size:40px;} }  
    .mono{font-family:var(--mono)}  
    .divider{height:1px;background:var(--line);margin:14px 0}  
    .list{margin:0;padding-left:18px;color:var(--muted);line-height:1.7}  
    .toast{  
      position:fixed;left:50%;bottom:18px;transform:translateX(-50%);  
      padding:12px 14px;border-radius:14px;  
      background: rgba(7,10,16,.82);  
      border:1px solid rgba(255,255,255,.14);  
      backdrop-filter: blur(10px);  
      box-shadow: 0 18px 60px rgba(0,0,0,.5);  
      color: rgba(238,242,255,.95);  
      font-size:13px;  
      opacity:0; pointer-events:none;  
      transition: opacity .25s ease;  
      max-width:92vw;  
      z-index:9999;  
    }  
    .toast.show{opacity:1}  
  </style>  
</head>  
<body>  
  <div class="top">  
    <div class="brand">  
      <div class="mark">💪</div>  
      <div>  
        <b>$PROTEIN</b>  
        <span>Eat. Lift. Hold. Repeat.</span>  
      </div>  
    </div>  
    <div class="actions">  
      <button class="btn" id="copyCA">Copy CA</button>  
      <a class="btn primary" id="pump" href="#" target="_blank" rel="noreferrer">Buy on pump.fun</a>  
      <a class="btn accent" id="dex" href="#" target="_blank" rel="noreferrer">Dexscreener</a>  
    </div>  
  </div>  
  
  <div class="wrap">  
    <section class="hero">  
      <div class="card">  
        <div class="pad">  
          <h1>BUILT FOR GAINS.</h1>  
          <p>  
            $PROTEIN is the clean gym-culture memecoin on Solana.  
            No complicated nonsense — just community, memes, and momentum.  
          </p>  
  
          <div class="row">  
            <div class="pill">Chain: Solana</div>  
            <div class="pill">Ticker: $PROTEIN</div>  
            <div class="pill">CA: <span class="mono" id="caShort"></span></div>  
          </div>  
  
          <div class="divider"></div>  
  
          <p class="mono" style="margin-top:0;word-break:break-all;">  
            <b>Contract Address (CA):</b><br/>  
            <span id="caFull"></span>  
          </p>  
        </div>  
      </div>  
  
      <div class="grid">  
        <div class="card">  
          <div class="pad">  
            <div class="sectionTitle">How to Buy</div>  
            <ol class="list">  
              <li>Tap <b>Buy on pump.fun</b>.</li>  
              <li>Connect Phantom (or your Solana wallet).</li>  
              <li>Swap SOL → <b>$PROTEIN</b>.</li>  
              <li>Always verify the <b>CA</b> matches this site.</li>  
            </ol>  
          </div>  
        </div>  
  
        <div class="card">  
          <div class="pad">  
            <div class="sectionTitle">Links</div>  
            <ul class="list">  
              <li><a id="pump2" href="#" target="_blank" rel="noreferrer">pump.fun coin page</a></li>  
              <li><a id="dex2" href="#" target="_blank" rel="noreferrer">Dexscreener chart</a></li>  
            </ul>  
            <div class="divider"></div>  
            <p style="margin-top:0;font-size:12px;">  
              Not financial advice. Memecoins are risky.  
            </p>  
          </div>  
        </div>  
      </div>  
    </section>  
  </div>  
  
  <div class="toast" id="toast"></div>  
  
  <script>  
    const CA = "5badyEX5tgwtM4n96osM4CQncQ2VGwRiykPHUTQqpump";  
    const PUMP = `https://pump.fun/coin/${CA}`;  
    const DEX  = `https://dexscreener.com/solana/${CA}`;  
  
    const $ = (s)=>document.querySelector(s);  
    const toast = (msg)=>{  
      const t=$("#toast");  
      t.textContent=msg;  
      t.classList.add("show");  
      clearTimeout(t._h);  
      t._h=setTimeout(()=>t.classList.remove("show"), 1500);  
    };  
    const short = (s)=> s.slice(0,4)+"…"+s.slice(-4);  
  
    $("#caShort").textContent = short(CA);  
    $("#caFull").textContent = CA;  
  
    $("#pump").href = PUMP;  
    $("#dex").href  = DEX;  
    $("#pump2").href = PUMP;  
    $("#dex2").href  = DEX;  
  
    $("#copyCA").addEventListener("click", async ()=>{  
      try{  
        await navigator.clipboard.writeText(CA);  
        toast("CA copied ✅");  
      }catch{  
        toast("Copy failed on iOS — long press to copy.");  
      }  
    });  
  </script>  
</body>  
</html>  
