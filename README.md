# SaaS Landing Page
SaaS landing website

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Loopback – customer feedback, sorted</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@500;700;800&family=DM+Sans:wght@400;500&display=swap">
<style>
:root{--bg:#F6F8FB;--panel:#fff;--ink:#16223F;--muted:#5B6785;--line:#DDE3EF;--accent:#3D5AFE;--accent-ink:#fff;--soft:#E6EBFF;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0F1530;--panel:#182044;--ink:#EAEEFF;--muted:#A3AED0;--line:#2A3563;--accent:#7C93FF;--accent-ink:#0F1530;--soft:#232D5C}}
:root[data-theme="dark"]{--bg:#0F1530;--panel:#182044;--ink:#EAEEFF;--muted:#A3AED0;--line:#2A3563;--accent:#7C93FF;--accent-ink:#0F1530;--soft:#232D5C}
*{box-sizing:border-box}html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--ink);font:400 17px/1.6 "DM Sans",system-ui,sans-serif}
h1,h2,h3{font-family:"Bricolage Grotesque",system-ui,sans-serif;line-height:1.1;margin:0}
a{color:inherit}
.wrap{max-width:1080px;margin:0 auto;padding:0 24px}
nav{display:flex;justify-content:space-between;align-items:center;padding:20px 0}
.logo{font:800 22px "Bricolage Grotesque",sans-serif;text-decoration:none}
nav div{display:flex;gap:24px;align-items:center}
nav a{text-decoration:none;color:var(--muted)}
.btn{display:inline-block;background:var(--accent);color:var(--accent-ink);padding:12px 22px;border-radius:10px;font-weight:500;text-decoration:none}
.btn.ghost{background:transparent;color:var(--ink);border:1px solid var(--line)}
a:focus-visible,button:focus-visible{outline:3px solid var(--accent);outline-offset:3px}
.hero{display:grid;grid-template-columns:1fr 1.05fr;gap:48px;align-items:center;padding:56px 0 88px}
h1{font-size:clamp(38px,5.6vw,64px);font-weight:800;letter-spacing:-.025em}
.hero p{color:var(--muted);max-width:44ch;margin:20px 0 28px}
.hero .btn+.btn{margin-left:10px}
.inbox{background:var(--panel);border:1px solid var(--line);border-radius:14px;overflow:hidden;box-shadow:0 20px 50px -24px rgba(22,34,63,.35)}
.inbox header{display:flex;gap:8px;padding:12px 16px;border-bottom:1px solid var(--line);font-size:14px;color:var(--muted)}
.inbox header b{color:var(--ink)}
.msg{display:grid;grid-template-columns:1fr auto;gap:4px 12px;padding:14px 16px;border-bottom:1px solid var(--line);font-size:15px}
.msg:last-child{border:0}
.msg small{color:var(--muted);grid-column:1/-1}
.tag{font-size:13px;padding:2px 10px;border-radius:99px;background:var(--soft);align-self:start;white-space:nowrap}
.tag.bug{background:#FFE1DC;color:#8A2A1A}.tag.ask{background:#DDF4E4;color:#1B5E36}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]) .tag.bug{background:#4A2323;color:#FFC9C0}:root:not([data-theme="light"]) .tag.ask{background:#1F4030;color:#BFEBD0}}
.msg.new{animation:in .8s ease both}
@keyframes in{from{background:var(--soft);transform:translateY(-6px);opacity:0}}
section{padding:72px 0;border-top:1px solid var(--line)}
section h2{font-size:clamp(28px,3.6vw,40px);letter-spacing:-.02em;max-width:20ch}
.feat{display:grid;grid-template-columns:1fr 1fr;gap:56px;margin-top:40px}
.feat dt{font:700 20px "Bricolage Grotesque",sans-serif;margin-top:28px}
.feat dt:first-child{margin-top:0}
.feat dd{margin:6px 0 0;color:var(--muted);max-width:46ch}
.plans{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;margin-top:40px}
.plan{border:1px solid var(--line);border-radius:14px;padding:28px;background:var(--panel)}
.plan.pick{border:2px solid var(--accent)}
.plan h3{font-size:22px}.price{font:800 40px "Bricolage Grotesque",sans-serif;margin:12px 0}
.price span{font:400 15px "DM Sans",sans-serif;color:var(--muted)}
.plan ul{padding-left:18px;color:var(--muted);margin:0 0 24px}
.cta{text-align:center}.cta h2{margin:0 auto 24px}
footer{padding:32px 0;color:var(--muted);font-size:15px;border-top:1px solid var(--line)}
@media(max-width:820px){.hero,.feat,.plans{grid-template-columns:1fr}.hero{padding-top:24px}nav a.l{display:none}}
@media(prefers-reduced-motion:reduce){.msg.new{animation:none}}
</style>
</head>
<body>
<div class="wrap">
<nav><a class="logo" href="#">Loopback</a><div><a class="l" href="#features">Features</a><a class="l" href="#pricing">Pricing</a><a class="btn" href="#pricing">Start free</a></div></nav>

<div class="hero">
<div>
<h1>Every customer message, already sorted.</h1>
<p>Loopback collects feedback from email, chat and reviews, tags each message as a bug, request or question, and sends it to the right person on your team.</p>
<a class="btn" href="#pricing">Start free</a><a class="btn ghost" href="#features">See how it works</a>
</div>
<div class="inbox" aria-label="Example inbox">
<header><b>Inbox</b> 4 new today</header>
<div class="msg new"><span>Export to CSV fails on large files</span><span class="tag bug">Bug</span><small>Maya, via email, 2 min ago</small></div>
<div class="msg"><span>Can you add Slack notifications?</span><span class="tag">Request</span><small>Dev, via chat, 18 min ago</small></div>
<div class="msg"><span>Do you offer a yearly discount?</span><span class="tag ask">Question</span><small>Ritu, via website, 1 hr ago</small></div>
<div class="msg"><span>Dark mode would be great</span><span class="tag">Request</span><small>Arun, via review, 3 hr ago</small></div>
</div>
</div>
</div>

<section id="features"><div class="wrap">
<h2>Less sorting, more fixing</h2>
<dl class="feat">
<div><dt>One inbox for everything</dt><dd>Connect email, chat and review sites. Messages land in one place, with the customer's history next to them.</dd>
<dt>Automatic tags</dt><dd>Each message gets a type and a priority when it arrives. You can change any tag, and Loopback learns from it.</dd></div>
<div><dt>Send to the right person</dt><dd>Bugs go to engineering, questions go to support. Set the rules once and they run on every new message.</dd>
<dt>See what customers ask for most</dt><dd>A weekly summary shows the top requests and how many people asked, so you can decide what to build next.</dd></div>
</dl>
</div></section>

<section id="pricing"><div class="wrap">
<h2>Simple pricing</h2>
<div class="plans">
<div class="plan"><h3>Starter</h3><div class="price">$0 <span>/month</span></div><ul><li>1 inbox</li><li>100 messages a month</li><li>Email support</li></ul><a class="btn ghost" href="#">Start free</a></div>
<div class="plan pick"><h3>Team</h3><div class="price">$29 <span>/user/month</span></div><ul><li>Unlimited inboxes</li><li>Automatic routing</li><li>Weekly summary</li></ul><a class="btn" href="#">Try Team free for 14 days</a></div>
<div class="plan"><h3>Company</h3><div class="price">Custom</div><ul><li>Single sign-on</li><li>Audit log</li><li>Dedicated support</li></ul><a class="btn ghost" href="#">Talk to sales</a></div>
</div>
</div></section>

<section class="cta"><div class="wrap"><h2>Your next 100 messages, sorted in minutes</h2><a class="btn" href="#">Start free</a></div></section>
<footer><div class="wrap">© 2026 Loopback. All rights reserved.</div></footer>
</body>
</html>
