<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Shop</title>
<style>
:root{
  --navy:#131921; --navy2:#232F3E; --navy3:#37475A;
  --orange:#FF9900; --search:#FEBD69; --yellow:#FFD814; --yellow-h:#F7CA00; --buy:#FFA41C; --buy-h:#FA8900;
  --link:#007185; --link-h:#C7511F; --price:#B12704; --star:#FFA41C; --green:#007600;
  --bg:#EAEDED; --card:#fff; --line:#DDD; --text:#0F1111; --muted:#565959;
  --font:"Amazon Ember",Arial,"Helvetica Neue",sans-serif;
}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--text);font:14px/1.4 var(--font)}
a{color:var(--link);text-decoration:none} a:hover{color:var(--link-h);text-decoration:underline}
button,input,select{font:inherit}
button{cursor:pointer}
:focus-visible{outline:2px solid var(--orange);outline-offset:1px}

/* ---------- top header ---------- */
.top{background:var(--navy);color:#fff;display:flex;align-items:center;gap:14px;padding:8px 14px;position:sticky;top:0;z-index:30}
.logo{color:#fff;font:700 24px var(--font);letter-spacing:-.5px;padding:4px 8px;border:1px solid transparent;border-radius:2px;white-space:nowrap}
.logo:hover{border-color:#fff;text-decoration:none;color:#fff}
.logo::after{content:"";display:block;height:3px;border-radius:0 0 40px 40px;background:var(--orange);margin-top:-2px}
.search{flex:1;display:flex;height:40px;border-radius:4px;overflow:hidden;min-width:0}
.search:focus-within{box-shadow:0 0 0 3px var(--orange)}
.search select{background:#E6E6E6;border:0;border-right:1px solid #CDCDCD;padding:0 8px;color:#555;max-width:130px;border-radius:4px 0 0 4px}
.search input{flex:1;border:0;padding:0 12px;min-width:0;outline:0}
.search button{width:46px;border:0;background:var(--search);color:var(--navy);font-size:18px}
.search button:hover{background:var(--orange)}
.hd-link{color:#fff;padding:6px 8px;border:1px solid transparent;border-radius:2px;line-height:1.2;white-space:nowrap;background:none}
.hd-link:hover{border-color:#fff;text-decoration:none;color:#fff}
.hd-link small{display:block;font-size:12px;color:#ccc}
.hd-link b{font-size:14px}
.cartlink{display:flex;align-items:flex-end;gap:2px;font-weight:700}
.cartlink .n{color:var(--orange);font-size:16px;font-weight:700;min-width:18px;text-align:center}
.cartlink svg{width:34px;height:30px}

.sub{background:var(--navy2);color:#fff;display:flex;gap:4px;padding:0 14px;overflow-x:auto;white-space:nowrap}
.sub button{background:none;border:1px solid transparent;color:#fff;padding:8px 10px;border-radius:2px}
.sub button:hover,.sub button[aria-current="true"]{border-color:#fff}

/* ---------- hero + category cards ---------- */
.hero{height:260px;background:linear-gradient(180deg,#6b8bab 0%,#a8bdd1 55%,var(--bg) 100%);display:flex;align-items:center;justify-content:center;text-align:center;color:#fff}
.hero h1{font:700 40px/1.1 var(--font);margin:0 0 8px;text-shadow:0 1px 3px rgba(0,0,0,.35)}
.hero p{margin:0;font-size:18px;text-shadow:0 1px 3px rgba(0,0,0,.35)}
.page{max-width:1500px;margin:0 auto;padding:0 14px 30px}
.tiles{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:18px;margin-top:-150px;position:relative}
.tile{background:var(--card);padding:18px;display:flex;flex-direction:column}
.tile h2{font:700 21px/1.25 var(--font);margin:0 0 12px}
.tile .mini{display:grid;grid-template-columns:1fr 1fr;gap:12px;flex:1}
.tile .mini button{background:none;border:0;padding:0;text-align:left;color:var(--text)}
.tile .mini .ph{aspect-ratio:1/1;font-size:30px}
.tile .mini span{font-size:12px;display:block;margin-top:2px}
.tile .more{margin-top:14px;background:none;border:0;padding:0;color:var(--link);text-align:left}
.tile .more:hover{color:var(--link-h);text-decoration:underline}

/* placeholder image */
.ph{background:#E3E6E6;color:#8a9494;display:grid;place-items:center;font:700 56px var(--font);width:100%;overflow:hidden}
.ph img{width:100%;height:100%;object-fit:cover}

/* ---------- results ---------- */
.results{display:grid;grid-template-columns:230px 1fr;gap:20px;margin-top:20px}
.side{background:var(--card);padding:14px 16px;align-self:start}
.side h3{font:700 14px var(--font);margin:14px 0 6px} .side h3:first-child{margin-top:0}
.side label{display:block;padding:2px 0;cursor:pointer}
.side button.lnk{background:none;border:0;padding:2px 0;color:var(--text);display:block;text-align:left}
.side button.lnk[aria-current="true"]{font-weight:700}
.side button.lnk:hover{color:var(--link-h)}
.bar{display:flex;justify-content:space-between;align-items:center;background:var(--card);padding:10px 14px;margin-bottom:14px;gap:10px;flex-wrap:wrap}
.bar h2{font:700 18px var(--font);margin:0}
.bar select{padding:5px 8px;background:#F0F2F2;border:1px solid #D5D9D9;border-radius:8px}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:14px}
.card{background:var(--card);padding:14px;display:flex;flex-direction:column;position:relative}
.card .imgbtn{background:none;border:0;padding:0;display:block;width:100%}
.card .ph{aspect-ratio:1/1;margin-bottom:10px}
.card h3{font:400 15px/1.3 var(--font);margin:0 0 4px}
.card h3 button{background:none;border:0;padding:0;text-align:left;color:var(--text);cursor:pointer}
.card h3 button:hover{color:var(--link-h);text-decoration:underline}
.badge{position:absolute;top:10px;left:10px;background:#CC0C39;color:#fff;font-size:12px;font-weight:700;padding:3px 7px;border-radius:2px;z-index:1}
.rate{display:flex;align-items:center;gap:6px;font-size:13px;color:var(--link)}
.stars{position:relative;display:inline-block;color:#ccc;letter-spacing:1px;font-size:16px;line-height:1}
.stars i{position:absolute;inset:0;overflow:hidden;color:var(--star);white-space:nowrap;font-style:normal}
.price{display:flex;align-items:flex-start;margin:6px 0 2px;color:var(--text)}
.price .cur{font-size:13px;margin-top:3px}
.price .int{font-size:26px;line-height:1;font-weight:400}
.price .frac{font-size:13px;margin-top:3px}
.was{color:var(--muted);font-size:12px}
.was s{margin-left:2px}
.deliv{font-size:13px;color:var(--text);margin:2px 0 10px;flex:1}
.deliv b{font-weight:700}
.free{color:var(--green)}
.btn{display:block;width:100%;border:0;border-radius:20px;padding:8px 12px;margin-top:6px;background:var(--yellow);color:var(--text);text-align:center}
.btn:hover{background:var(--yellow-h)}
.btn.buy{background:var(--buy)} .btn.buy:hover{background:var(--buy-h)}
.btn[disabled]{background:#E7E9E9;color:#888;cursor:not-allowed}
.stock-out{color:var(--price);font-size:15px}
.none{background:var(--card);padding:30px}

/* ---------- product modal ---------- */
.modal{position:fixed;inset:0;background:rgba(15,17,17,.6);display:none;align-items:flex-start;justify-content:center;overflow:auto;z-index:50;padding:40px 14px}
.modal.open{display:flex}
.sheet{background:#fff;max-width:900px;width:100%;display:grid;grid-template-columns:1fr 1fr;gap:26px;padding:24px;position:relative;border-radius:8px}
.sheet .ph{aspect-ratio:1/1}
.sheet h2{font:400 24px/1.25 var(--font);margin:0 0 6px}
.sheet .x{position:absolute;top:8px;right:12px;background:none;border:0;font-size:28px;line-height:1}
.sheet .box{border:1px solid #D5D9D9;border-radius:8px;padding:14px;margin-top:14px}
hr{border:0;border-top:1px solid var(--line);margin:10px 0}

/* ---------- cart view ---------- */
.cartpage{display:none;grid-template-columns:1fr 300px;gap:18px;margin-top:20px;align-items:start}
.cartbox{background:var(--card);padding:20px}
.cartbox h1{font:400 28px var(--font);margin:0 0 6px}
.crow{display:grid;grid-template-columns:140px 1fr auto;gap:16px;padding:16px 0;border-top:1px solid var(--line)}
.crow .ph{aspect-ratio:1/1;font-size:36px}
.crow h3{font:700 17px var(--font);margin:0 0 4px}
.cact{display:flex;gap:10px;align-items:center;margin-top:8px;font-size:13px;flex-wrap:wrap}
.cact select{padding:3px 6px;background:#F0F2F2;border:1px solid #D5D9D9;border-radius:8px}
.cact button.lnk{background:none;border:0;padding:0;color:var(--link)}
.cact button.lnk:hover{color:var(--link-h);text-decoration:underline}
.cact .sep{width:1px;height:14px;background:var(--line)}
.crow .p{font-weight:700;font-size:18px}
.subtotal{text-align:right;font-size:18px;padding-top:10px;border-top:1px solid var(--line)}
.checkout{background:var(--card);padding:18px}
.checkout p{margin:0 0 10px}
.checkout .big{font-size:18px}

footer .back{display:block;width:100%;background:var(--navy3);color:#fff;border:0;padding:14px;text-align:center}
footer .back:hover{background:#485769}
footer .legal{background:var(--navy);color:#ddd;text-align:center;padding:26px 14px;font-size:12px}

@media (max-width:860px){
  .results,.cartpage{grid-template-columns:1fr}
  .side{display:none}
  .sheet{grid-template-columns:1fr}
  .hd-link.acc{display:none}
  .top{flex-wrap:wrap}.search{order:5;flex-basis:100%}
  .hero{height:200px}.hero h1{font-size:28px}
  .tiles{margin-top:-90px}
  .crow{grid-template-columns:90px 1fr}.crow .p{grid-column:2}
}
</style>
</head>
<body>

<header>
  <div class="top">
    <a class="logo" href="#" id="logo">yourshop</a>
    <form class="search" id="searchForm" role="search">
      <select id="searchCat" aria-label="Search category"><option value="All">All</option></select>
      <input id="q" type="search" placeholder="Search products" aria-label="Search products">
      <button type="submit" aria-label="Search">&#128269;</button>
    </form>
    <a class="hd-link acc" href="#"><small>Hello, guest</small><b>Account</b></a>
    <a class="hd-link cartlink" href="#cart" aria-label="Cart">
      <svg viewBox="0 0 34 30" fill="none" stroke="#fff" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M2 3h5l3 15h16l3-11H8"/><circle cx="13" cy="25" r="2"/><circle cx="24" cy="25" r="2"/></svg>
      <span class="n" id="count">0</span><span>Cart</span>
    </a>
  </div>
  <nav class="sub" id="subnav" aria-label="Categories"></nav>
</header>

<main>
  <div id="home">
    <section class="hero"><div><h1>Great deals, every day</h1><p>Browse the shop and save</p></div></section>
  </div>
  <div class="page">
    <div class="tiles" id="tiles"></div>

    <section class="results" id="results">
      <aside class="side" id="side"></aside>
      <div>
        <div class="bar"><h2 id="resTitle"></h2>
          <label>Sort by <select id="sort">
            <option value="featured">Featured</option>
            <option value="low">Price: Low to High</option>
            <option value="high">Price: High to Low</option>
            <option value="rating">Avg. Customer Review</option>
          </select></label>
        </div>
        <div class="grid" id="grid"></div>
      </div>
    </section>

    <section class="cartpage" id="cartpage">
      <div class="cartbox" id="cartbox"></div>
      <aside class="checkout" id="checkout"></aside>
    </section>
  </div>
</main>

<footer>
  <button class="back" id="top">Back to top</button>
  <div class="legal" id="legal"></div>
</footer>

<div class="modal" id="modal" role="dialog" aria-modal="true" aria-label="Product details"><div class="sheet" id="sheet"></div></div>

<script src="products.js"></script>
<script>
(function(){
  const $ = id => document.getElementById(id);
  const el = (tag, cls, text) => { const e=document.createElement(tag); if(cls) e.className=cls; if(text!=null) e.textContent=text; return e; };
  const fmt = new Intl.NumberFormat(SHOP.locale,{style:"currency",currency:SHOP.currency});
  const money = n => fmt.format(n);
  const byId = Object.fromEntries(PRODUCTS.map(p => [p.id,p]));

  /* ---------- state ---------- */
  let cart = {};
  try { cart = JSON.parse(localStorage.getItem("cart")||"{}"); } catch(e){}
  for (const id in cart) if (!byId[id] || byId[id].soldOut) delete cart[id];
  const state = { cat:"All", q:"", sort:"featured", minRating:0, maxPrice:Infinity };
  const save = () => { try { localStorage.setItem("cart",JSON.stringify(cart)); } catch(e){} };
  const cats = [...new Set(PRODUCTS.map(p=>p.category))];

  /* ---------- small builders ---------- */
  function image(p, cls){
    const d = el("div","ph " + (cls||""));
    if (p.image){
      const i = document.createElement("img"); i.alt = p.name; i.loading="lazy"; i.src = p.image;
      i.onerror = () => { d.textContent = p.id; };
      d.appendChild(i);
    } else d.textContent = p.id;
    return d;
  }
  function stars(r){
    const s = el("span","stars","★★★★★"); s.setAttribute("role","img"); s.setAttribute("aria-label", r+" out of 5 stars");
    const i = el("i",null,"★★★★★"); i.style.width = (r/5*100)+"%"; s.appendChild(i); return s;
  }
  function rating(p){
    const r = el("div","rate"); r.appendChild(stars(p.rating)); r.appendChild(el("span",null,p.reviews.toLocaleString(SHOP.locale))); return r;
  }
  function price(v){
    const parts = fmt.formatToParts(v); const w = el("div","price");
    let cur="", int="", frac="", dec=false;
    parts.forEach(x => { if(x.type==="currency") cur+=x.value; else if(x.type==="integer"||x.type==="group") int+=x.value; else if(x.type==="fraction") frac=x.value; });
    w.append(el("span","cur",cur), el("span","int",int));
    if (frac) w.appendChild(el("span","frac",frac));
    return w;
  }
  function was(p){
    if (!p.oldPrice || p.oldPrice<=p.price) return null;
    const d = el("div","was","List: "); d.appendChild(el("s",null,money(p.oldPrice)));
    d.append(" (" + Math.round((1-p.price/p.oldPrice)*100) + "% off)"); return d;
  }
  function delivery(p){
    const d = el("div","deliv");
    if (p.soldOut){ d.appendChild(el("span","stock-out","Currently unavailable.")); return d; }
    const free = p.price>=50;
    if (free){ d.appendChild(el("b","free","FREE delivery")); } else d.appendChild(el("span",null,"Delivery calculated at checkout"));
    return d;
  }
  function addToCart(id, n){ cart[id]=(cart[id]||0)+(n||1); save(); renderCount(); }

  /* ---------- header, nav, footer ---------- */
  document.title = SHOP.name;
  $("logo").textContent = SHOP.name;
  $("legal").textContent = "© " + new Date().getFullYear() + " " + SHOP.name + " · " + SHOP.email;
  cats.forEach(c => $("searchCat").appendChild(Object.assign(document.createElement("option"),{value:c,textContent:c})));
  function renderNav(){
    const n = $("subnav"); n.textContent="";
    ["All",...cats].forEach(c => {
      const b = el("button",null,c); b.setAttribute("aria-current", String(state.cat===c && !isCart()));
      b.onclick = () => { state.cat=c; state.q=""; $("q").value=""; $("searchCat").value=c; go(""); update(); };
      n.appendChild(b);
    });
    const d = el("button",null,"Today's Deals"); d.onclick=()=>{ state.cat="Deals"; go(""); update(); }; d.setAttribute("aria-current", String(state.cat==="Deals"&&!isCart())); n.appendChild(d);
  }

  /* ---------- home tiles (category cards with 4 products) ---------- */
  function renderTiles(){
    const t = $("tiles"); t.textContent="";
    cats.forEach(c => {
      const card = el("div","tile"); card.appendChild(el("h2",null,"Shop " + c));
      const mini = el("div","mini");
      PRODUCTS.filter(p=>p.category===c).slice(0,4).forEach(p => {
        const b = el("button"); b.appendChild(image(p)); b.appendChild(el("span",null,p.name));
        b.onclick = () => openModal(p.id); mini.appendChild(b);
      });
      const more = el("button","more","See more");
      more.onclick = () => { state.cat=c; update(); $("results").scrollIntoView({behavior:"smooth"}); };
      card.append(mini,more); t.appendChild(card);
    });
  }

  /* ---------- filters sidebar ---------- */
  function renderSide(){
    const s = $("side"); s.textContent="";
    s.appendChild(el("h3",null,"Category"));
    ["All",...cats].forEach(c => { const b=el("button","lnk",c); b.setAttribute("aria-current",String(state.cat===c)); b.onclick=()=>{state.cat=c;update();}; s.appendChild(b); });
    s.appendChild(el("h3",null,"Customer Reviews"));
    [4,3,2,1].forEach(r => {
      const b = el("button","lnk"); b.setAttribute("aria-current",String(state.minRating===r));
      b.append(stars(r), " & Up"); b.onclick=()=>{ state.minRating = state.minRating===r?0:r; update(); }; s.appendChild(b);
    });
    s.appendChild(el("h3",null,"Price"));
    [["Any price",Infinity],["Under 25",25],["Under 50",50],["Under 100",100]].forEach(([l,v]) => {
      const b = el("button","lnk",v===Infinity?l:l.replace("Under ","Under "+fmt.format(0).replace(/[\d.,\s]/g,"")));
      b.setAttribute("aria-current",String(state.maxPrice===v)); b.onclick=()=>{state.maxPrice=v;update();}; s.appendChild(b);
    });
  }

  /* ---------- results grid ---------- */
  function list(){
    let l = PRODUCTS.filter(p =>
      (state.cat==="All" || (state.cat==="Deals" ? p.oldPrice>p.price : p.category===state.cat)) &&
      p.rating>=state.minRating && p.price<=state.maxPrice &&
      (!state.q || (p.name+" "+p.description+" "+p.category).toLowerCase().includes(state.q.toLowerCase())));
    if (state.sort==="low") l.sort((a,b)=>a.price-b.price);
    if (state.sort==="high") l.sort((a,b)=>b.price-a.price);
    if (state.sort==="rating") l.sort((a,b)=>b.rating-a.rating);
    return l;
  }
  function renderGrid(){
    const l = list(), g = $("grid"); g.textContent="";
    $("resTitle").textContent = l.length + " result" + (l.length===1?"":"s") + (state.q?' for "'+state.q+'"':"") + (state.cat!=="All"?" in "+(state.cat==="Deals"?"Today's Deals":state.cat):"");
    if (!l.length){ g.appendChild(el("div","none","No results. Try a different search or clear a filter.")); return; }
    l.forEach(p => {
      const c = el("article","card");
      if (was(p) && !p.soldOut) c.appendChild(el("span","badge",Math.round((1-p.price/p.oldPrice)*100)+"% off"));
      const ib = el("button","imgbtn"); ib.setAttribute("aria-label","View "+p.name); ib.appendChild(image(p)); ib.onclick=()=>openModal(p.id);
      const h = el("h3"); const hb = el("button",null,p.name); hb.onclick=()=>openModal(p.id); h.appendChild(hb);
      c.append(ib,h,rating(p),price(p.price));
      const w = was(p); if (w) c.appendChild(w);
      c.appendChild(delivery(p));
      const add = el("button","btn",p.soldOut?"Unavailable":"Add to Cart"); add.disabled=p.soldOut;
      add.onclick = () => { addToCart(p.id); add.textContent="Added ✓"; setTimeout(()=>add.textContent="Add to Cart",1200); };
      c.appendChild(add);
      g.appendChild(c);
    });
  }

  /* ---------- product modal ---------- */
  function openModal(id){
    const p = byId[id], s = $("sheet"); s.textContent="";
    const x = el("button","x","×"); x.setAttribute("aria-label","Close"); x.onclick=closeModal;
    const right = el("div"); right.appendChild(el("h2",null,p.name)); right.appendChild(rating(p)); right.appendChild(el("hr"));
    right.appendChild(price(p.price)); const w=was(p); if(w) right.appendChild(w);
    right.appendChild(el("p",null,p.description)); right.appendChild(el("p",null,"Category: "+p.category));
    const box = el("div","box"); box.appendChild(delivery(p));
    if (!p.soldOut){
      if (!p.buyLink) {} 
      const add = el("button","btn","Add to Cart"); add.onclick=()=>{ addToCart(id); closeModal(); };
      box.appendChild(add);
      if (p.buyLink){ const a = el("a","btn buy","Buy Now"); a.href=p.buyLink; a.target="_blank"; a.rel="noopener"; box.appendChild(a); }
      else { const b = el("button","btn buy","Buy Now"); b.onclick=()=>{ addToCart(id); closeModal(); go("cart"); }; box.appendChild(b); }
    }
    right.appendChild(box);
    s.append(x, image(p), right);
    $("modal").classList.add("open"); x.focus();
  }
  function closeModal(){ $("modal").classList.remove("open"); }
  $("modal").onclick = e => { if (e.target===$("modal")) closeModal(); };
  document.addEventListener("keydown", e => { if(e.key==="Escape") closeModal(); });

  /* ---------- cart ---------- */
  function renderCount(){ $("count").textContent = Object.values(cart).reduce((a,b)=>a+b,0); }
  function renderCart(){
    const box = $("cartbox"), co = $("checkout"); box.textContent=""; co.textContent="";
    const ids = Object.keys(cart);
    box.appendChild(el("h1",null, ids.length ? "Shopping Cart" : "Your cart is empty"));
    let n=0, total=0;
    if (!ids.length){ const a=el("a",null,"Continue shopping"); a.href="#"; box.appendChild(a); }
    ids.forEach(id => {
      const p=byId[id], q=cart[id]; n+=q; total+=p.price*q;
      const r = el("div","crow"); r.appendChild(image(p));
      const mid = el("div"); mid.appendChild(el("h3",null,p.name));
      const stock = el("div","free","In stock"); mid.appendChild(stock);
      const act = el("div","cact");
      const sel = el("select"); sel.setAttribute("aria-label","Quantity");
      for (let i=1;i<=Math.max(10,q);i++){ const o=el("option",null,"Qty: "+i); o.value=i; if(i===q) o.selected=true; sel.appendChild(o); }
      sel.onchange = () => { cart[id]=+sel.value; save(); renderCount(); renderCart(); };
      const del = el("button","lnk","Delete"); del.onclick=()=>{ delete cart[id]; save(); renderCount(); renderCart(); };
      act.append(sel, el("span","sep"), del); mid.appendChild(act);
      r.append(mid, el("div","p",money(p.price*q))); box.appendChild(r);
    });
    if (ids.length){
      const sub = el("div","subtotal"); sub.append("Subtotal ("+n+" item"+(n===1?"":"s")+"): ", el("b",null,money(total))); box.appendChild(sub);
      const p1 = el("p","big"); p1.append("Subtotal ("+n+" item"+(n===1?"":"s")+"): ", el("b",null,money(total))); co.appendChild(p1);
      co.appendChild(el("p","was",SHOP.shipping));
      const go1 = el("button","btn","Proceed to checkout");
      go1.onclick = () => {
        const lines = ids.map(id=>cart[id]+" x "+byId[id].name+" ("+money(byId[id].price*cart[id])+")");
        const body = "Hi, I'd like to order:\n\n"+lines.join("\n")+"\n\nTotal: "+money(total)+"\n\nMy name:\nMy delivery address:\n";
        location.href = "mailto:"+SHOP.email+"?subject="+encodeURIComponent("Order from "+SHOP.name)+"&body="+encodeURIComponent(body);
      };
      co.appendChild(go1);
    } else co.style.display="none";
    if (ids.length) co.style.display="";
  }

  /* ---------- routing: "" = shop, "#cart" = cart ---------- */
  const isCart = () => location.hash==="#cart";
  function go(h){ if (h) location.hash=h; else if (location.hash) history.pushState("",document.title,location.pathname+location.search); show(); }
  function show(){
    const c = isCart();
    $("home").style.display = $("tiles").style.display = (c || state.cat!=="All" || state.q) ? "none" : "";
    $("results").style.display = c ? "none" : "";
    $("cartpage").style.display = c ? "grid" : "none";
    if (c) renderCart();
    renderNav(); window.scrollTo(0,0);
  }
  function update(){ show(); renderSide(); renderGrid(); }
  window.addEventListener("hashchange", update);

  /* ---------- wiring ---------- */
  $("searchForm").onsubmit = e => { e.preventDefault(); state.q=$("q").value.trim(); state.cat=$("searchCat").value; go(""); update(); };
  $("sort").onchange = e => { state.sort=e.target.value; renderGrid(); };
  $("top").onclick = () => window.scrollTo({top:0,behavior:"smooth"});
  $("logo").onclick = e => { e.preventDefault(); Object.assign(state,{cat:"All",q:"",minRating:0,maxPrice:Infinity}); $("q").value=""; $("searchCat").value="All"; go(""); update(); };

  renderTiles(); renderCount(); update();
})();
</script>
</body>
</html>
