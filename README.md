## ALPHINDIC 👋
Node.js 18+
npm 9+
React 18
Vite 5
@vitejs/plugin-react 4
name: Build ALPHINDIC

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: npm
      - run: npm install
      - run: npm run build
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap');

:root {
  --navy: #092f50;
  --blue: #0b5fa5;
  --red: #c93535;
  --ink: #102a3b;
  --muted: #607383;
  --paper: #f6f8fa;
  --line: #dbe4ea;
  --white: #fff;
  --shadow: 0 18px 50px rgba(8, 47, 80, .10);
}
* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { margin: 0; font-family: "DM Sans", sans-serif; color: var(--ink); background: var(--paper); }
a { color: inherit; text-decoration: none; }
button, input { font: inherit; }
button { cursor: pointer; }
.container { width: min(1120px, calc(100% - 40px)); margin: auto; }
.header { background: rgba(255,255,255,.96); border-bottom: 1px solid var(--line); position: sticky; top: 0; z-index: 20; backdrop-filter: blur(12px); }
.nav { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
.brand { display: flex; align-items: center; gap: 10px; }
.brandMark { width: 42px; height: 42px; display: grid; place-items: center; border-radius: 12px; background: var(--navy); color: #fff; font-weight: 700; font-size: 22px; }
.brand strong { display: block; letter-spacing: 2px; }
.brand small { color: var(--red); font-size: 9px; letter-spacing: 1.3px; font-weight: 700; }
nav { display: flex; gap: 25px; color: var(--muted); font-size: 14px; }
nav a:hover { color: var(--blue); }
.cartButton, .secondary { border: 1px solid var(--line); background: white; padding: 11px 16px; border-radius: 10px; font-weight: 600; }
.cartButton span { background: var(--red); color: white; border-radius: 50px; padding: 2px 7px; margin-left: 5px; font-size: 12px; }
.hero { background: linear-gradient(135deg, #edf5fb 0%, #fff 58%, #f9eeee 100%); padding: 80px 0 72px; border-bottom: 1px solid var(--line); }
.heroGrid { display: grid; grid-template-columns: 1.25fr .75fr; align-items: center; gap: 70px; }
.pill, .eyebrow { font-size: 11px; letter-spacing: 1.8px; font-weight: 700; color: var(--red); }
.hero h1 { font-size: clamp(44px, 6vw, 76px); line-height: .98; letter-spacing: -3px; margin: 18px 0; }
.hero h1 em { font-family: "Playfair Display", serif; font-weight: 600; color: var(--blue); letter-spacing: -2px; }
.heroText { color: var(--muted); max-width: 600px; font-size: 17px; line-height: 1.7; }
.heroActions { display: flex; gap: 12px; margin: 28px 0; }
.primary { border: 0; background: var(--navy); color: #fff; padding: 13px 19px; border-radius: 10px; font-weight: 700; display: inline-block; }
.primary:hover { background: var(--blue); }
.trustRow { display: flex; gap: 20px; flex-wrap: wrap; font-size: 12px; color: var(--muted); }
.heroCard { background: var(--navy); color: white; min-height: 370px; border-radius: 26px; padding: 45px; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; box-shadow: var(--shadow); position: relative; overflow: hidden; }
.heroCard:after { content: ""; position: absolute; width: 280px; height: 280px; border: 1px solid rgba(255,255,255,.14); border-radius: 50%; }
.orb { width: 150px; height: 150px; border: 1px solid rgba(255,255,255,.35); border-radius: 50%; display: grid; place-items: center; font-size: 60px; font-weight: 700; position: relative; z-index: 1; }
.heroCard h2 { margin: 18px 0 3px; letter-spacing: 5px; position: relative; z-index: 1; }
.heroCard p, .heroCard small { color: #bcd0de; position: relative; z-index: 1; }
.heroCardLine { width: 45px; height: 2px; background: var(--red); margin: 18px; position: relative; z-index: 1; }
.quickOrder { padding: 80px 0; }
.sectionHeading { display: flex; justify-content: space-between; align-items: end; gap: 20px; margin-bottom: 30px; }
.sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 38px; margin: 8px 0 0; letter-spacing: -1.5px; }
.number { color: var(--muted); font-size: 13px; }
.searchRow { display: flex; gap: 10px; margin-bottom: 25px; }
.searchRow input { flex: 1; border: 1px solid var(--line); padding: 15px 17px; border-radius: 11px; background: white; outline: none; }
.searchRow input:focus { border-color: var(--blue); }
.searchRow button { border: 0; border-radius: 11px; background: var(--red); color: white; padding: 0 20px; font-weight: 700; }
.categories { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 10px; }
.category { white-space: nowrap; background: white; border: 1px solid var(--line); padding: 12px 16px; border-radius: 50px; color: var(--muted); }
.category span { margin-right: 7px; color: var(--blue); }
.category.active { background: var(--navy); color: white; border-color: var(--navy); }
.productGrid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 25px; }
.productCard { background: white; border: 1px solid var(--line); border-radius: 16px; padding: 20px; min-height: 250px; display: flex; flex-direction: column; }
.productIcon { width: 46px; height: 46px; border-radius: 13px; background: #eaf4fb; color: var(--blue); display: grid; place-items: center; font-weight: 800; }
.tag { font-size: 10px; color: var(--red); text-transform: uppercase; letter-spacing: 1px; font-weight: 700; margin-top: 18px; }
.productCard h3 { margin: 8px 0; font-size: 18px; }
.productCard p { color: var(--muted); font-size: 13px; line-height: 1.5; margin: 0 0 18px; }
.productCard button { margin-top: auto; border: 1px solid var(--navy); background: white; color: var(--navy); padding: 10px; border-radius: 9px; font-weight: 700; }
.productCard button:hover { background: var(--navy); color: white; }
.empty { text-align: center; padding: 40px; color: var(--muted); }
.services { background: var(--navy); color: white; padding: 75px 0; }
.light .eyebrow { color: #e98a8a; }
.light h2 { color: white; }
.serviceGrid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: rgba(255,255,255,.16); }
.serviceGrid > div { padding: 30px; background: var(--navy); }
.serviceGrid b { color: #e98a8a; font-size: 12px; }
.serviceGrid h3 { font-size: 23px; margin-bottom: 8px; }
.serviceGrid p { color: #bcd0de; line-height: 1.6; font-size: 14px; }
.how { padding: 80px 0; }
.steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; margin-top: 35px; }
.steps div { border-top: 2px solid var(--navy); padding-top: 20px; }
.steps span { color: var(--red); font-weight: 800; }
.steps h3 { margin-bottom: 5px; }
.steps p { color: var(--muted); line-height: 1.6; font-size: 14px; }
.prescriptionBox { margin-bottom: 80px; background: white; border: 1px solid var(--line); border-radius: 20px; padding: 35px; display: grid; grid-template-columns: 1fr auto; gap: 20px; align-items: center; }
.prescriptionBox p { color: var(--muted); max-width: 650px; line-height: 1.6; }
.check { display: flex; gap: 8px; align-items: center; color: var(--muted); font-size: 13px; }
.check input { accent-color: var(--blue); }
footer { background: #071f34; color: white; padding: 50px 0; }
.footerGrid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 40px; }
.footerBrand { font-size: 22px; letter-spacing: 3px; font-weight: 700; }
footer p, footer a { color: #9fb4c4; font-size: 13px; line-height: 1.7; display: block; }
footer b { font-size: 11px; letter-spacing: 1.5px; }
.overlay { position: fixed; inset: 0; background: rgba(0,0,0,.4); z-index: 50; display: flex; justify-content: flex-end; }
.drawer { background: white; width: min(440px, 100%); height: 100%; padding: 28px; box-shadow: -10px 0 30px rgba(0,0,0,.15); overflow: auto; }
.drawerHead { display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid var(--line); padding-bottom: 18px; }
.drawerHead h2 { margin: 0; }
.drawerHead button { border: 0; background: transparent; font-size: 30px; }
.cartItems { margin: 20px 0; }
.cartItem { display: flex; justify-content: space-between; gap: 15px; padding: 16px 0; border-bottom: 1px solid var(--line); }
.cartItem b { display: block; font-size: 14px; }
.cartItem small { color: var(--muted); display: block; margin-top: 5px; }
.qty { display: flex; align-items: center; gap: 8px; }
.qty button { border: 1px solid var(--line); background: white; width: 28px; height: 28px; border-radius: 7px; }
.emptyCart { text-align: center; margin-top: 100px; color: var(--muted); }
.bigPlus { margin: auto; width: 70px; height: 70px; display: grid; place-items: center; border-radius: 50%; background: #edf5fb; color: var(--blue); font-size: 40px; }
.full { width: 100%; margin-top: 20px; text-align: center; }
.drawerCheck { margin-top: 20px; }

@media (max-width: 850px) {
  nav { display: none; }
  .heroGrid { grid-template-columns: 1fr; gap: 40px; }
  .heroCard { min-height: 300px; }
  .productGrid { grid-template-columns: repeat(2, 1fr); }
  .serviceGrid, .steps { grid-template-columns: 1fr; }
  .prescriptionBox, .footerGrid { grid-template-columns: 1fr; }
}
@media (max-width: 560px) {
  .container { width: min(100% - 24px, 1120px); }
  .nav { min-height: 66px; }
  .brand small { display: none; }
  .cartButton { padding: 9px 11px; font-size: 12px; }
  .hero { padding: 55px 0; }
  .hero h1 { font-size: 48px; }
  .heroActions, .searchRow { flex-direction: column; }
  .heroActions > *, .searchRow > * { width: 100%; text-align: center; padding: 13px; }
  .productGrid { grid-template-columns: 1fr; }
  .sectionHeading { align-items: flex-start; flex-direction: column; }
  .sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 30px; }
}@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap');

:root {
  --navy: #092f50;
  --blue: #0b5fa5;
  --red: #c93535;
  --ink: #102a3b;
  --muted: #607383;
  --paper: #f6f8fa;
  --line: #dbe4ea;
  --white: #fff;
  --shadow: 0 18px 50px rgba(8, 47, 80, .10);
}
* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { margin: 0; font-family: "DM Sans", sans-serif; color: var(--ink); background: var(--paper); }
a { color: inherit; text-decoration: none; }
button, input { font: inherit; }
button { cursor: pointer; }
.container { width: min(1120px, calc(100% - 40px)); margin: auto; }
.header { background: rgba(255,255,255,.96); border-bottom: 1px solid var(--line); position: sticky; top: 0; z-index: 20; backdrop-filter: blur(12px); }
.nav { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
.brand { display: flex; align-items: center; gap: 10px; }
.brandMark { width: 42px; height: 42px; display: grid; place-items: center; border-radius: 12px; background: var(--navy); color: #fff; font-weight: 700; font-size: 22px; }
.brand strong { display: block; letter-spacing: 2px; }
.brand small { color: var(--red); font-size: 9px; letter-spacing: 1.3px; font-weight: 700; }
nav { display: flex; gap: 25px; color: var(--muted); font-size: 14px; }
nav a:hover { color: var(--blue); }
.cartButton, .secondary { border: 1px solid var(--line); background: white; padding: 11px 16px; border-radius: 10px; font-weight: 600; }
.cartButton span { background: var(--red); color: white; border-radius: 50px; padding: 2px 7px; margin-left: 5px; font-size: 12px; }
.hero { background: linear-gradient(135deg, #edf5fb 0%, #fff 58%, #f9eeee 100%); padding: 80px 0 72px; border-bottom: 1px solid var(--line); }
.heroGrid { display: grid; grid-template-columns: 1.25fr .75fr; align-items: center; gap: 70px; }
.pill, .eyebrow { font-size: 11px; letter-spacing: 1.8px; font-weight: 700; color: var(--red); }
.hero h1 { font-size: clamp(44px, 6vw, 76px); line-height: .98; letter-spacing: -3px; margin: 18px 0; }
.hero h1 em { font-family: "Playfair Display", serif; font-weight: 600; color: var(--blue); letter-spacing: -2px; }
.heroText { color: var(--muted); max-width: 600px; font-size: 17px; line-height: 1.7; }
.heroActions { display: flex; gap: 12px; margin: 28px 0; }
.primary { border: 0; background: var(--navy); color: #fff; padding: 13px 19px; border-radius: 10px; font-weight: 700; display: inline-block; }
.primary:hover { background: var(--blue); }
.trustRow { display: flex; gap: 20px; flex-wrap: wrap; font-size: 12px; color: var(--muted); }
.heroCard { background: var(--navy); color: white; min-height: 370px; border-radius: 26px; padding: 45px; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; box-shadow: var(--shadow); position: relative; overflow: hidden; }
.heroCard:after { content: ""; position: absolute; width: 280px; height: 280px; border: 1px solid rgba(255,255,255,.14); border-radius: 50%; }
.orb { width: 150px; height: 150px; border: 1px solid rgba(255,255,255,.35); border-radius: 50%; display: grid; place-items: center; font-size: 60px; font-weight: 700; position: relative; z-index: 1; }
.heroCard h2 { margin: 18px 0 3px; letter-spacing: 5px; position: relative; z-index: 1; }
.heroCard p, .heroCard small { color: #bcd0de; position: relative; z-index: 1; }
.heroCardLine { width: 45px; height: 2px; background: var(--red); margin: 18px; position: relative; z-index: 1; }
.quickOrder { padding: 80px 0; }
.sectionHeading { display: flex; justify-content: space-between; align-items: end; gap: 20px; margin-bottom: 30px; }
.sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 38px; margin: 8px 0 0; letter-spacing: -1.5px; }
.number { color: var(--muted); font-size: 13px; }
.searchRow { display: flex; gap: 10px; margin-bottom: 25px; }
.searchRow input { flex: 1; border: 1px solid var(--line); padding: 15px 17px; border-radius: 11px; background: white; outline: none; }
.searchRow input:focus { border-color: var(--blue); }
.searchRow button { border: 0; border-radius: 11px; background: var(--red); color: white; padding: 0 20px; font-weight: 700; }
.categories { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 10px; }
.category { white-space: nowrap; background: white; border: 1px solid var(--line); padding: 12px 16px; border-radius: 50px; color: var(--muted); }
.category span { margin-right: 7px; color: var(--blue); }
.category.active { background: var(--navy); color: white; border-color: var(--navy); }
.productGrid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 25px; }
.productCard { background: white; border: 1px solid var(--line); border-radius: 16px; padding: 20px; min-height: 250px; display: flex; flex-direction: column; }
.productIcon { width: 46px; height: 46px; border-radius: 13px; background: #eaf4fb; color: var(--blue); display: grid; place-items: center; font-weight: 800; }
.tag { font-size: 10px; color: var(--red); text-transform: uppercase; letter-spacing: 1px; font-weight: 700; margin-top: 18px; }
.productCard h3 { margin: 8px 0; font-size: 18px; }
.productCard p { color: var(--muted); font-size: 13px; line-height: 1.5; margin: 0 0 18px; }
.productCard button { margin-top: auto; border: 1px solid var(--navy); background: white; color: var(--navy); padding: 10px; border-radius: 9px; font-weight: 700; }
.productCard button:hover { background: var(--navy); color: white; }
.empty { text-align: center; padding: 40px; color: var(--muted); }
.services { background: var(--navy); color: white; padding: 75px 0; }
.light .eyebrow { color: #e98a8a; }
.light h2 { color: white; }
.serviceGrid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: rgba(255,255,255,.16); }
.serviceGrid > div { padding: 30px; background: var(--navy); }
.serviceGrid b { color: #e98a8a; font-size: 12px; }
.serviceGrid h3 { font-size: 23px; margin-bottom: 8px; }
.serviceGrid p { color: #bcd0de; line-height: 1.6; font-size: 14px; }
.how { padding: 80px 0; }
.steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; margin-top: 35px; }
.steps div { border-top: 2px solid var(--navy); padding-top: 20px; }
.steps span { color: var(--red); font-weight: 800; }
.steps h3 { margin-bottom: 5px; }
.steps p { color: var(--muted); line-height: 1.6; font-size: 14px; }
.prescriptionBox { margin-bottom: 80px; background: white; border: 1px solid var(--line); border-radius: 20px; padding: 35px; display: grid; grid-template-columns: 1fr auto; gap: 20px; align-items: center; }
.prescriptionBox p { color: var(--muted); max-width: 650px; line-height: 1.6; }
.check { display: flex; gap: 8px; align-items: center; color: var(--muted); font-size: 13px; }
.check input { accent-color: var(--blue); }
footer { background: #071f34; color: white; padding: 50px 0; }
.footerGrid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 40px; }
.footerBrand { font-size: 22px; letter-spacing: 3px; font-weight: 700; }
footer p, footer a { color: #9fb4c4; font-size: 13px; line-height: 1.7; display: block; }
footer b { font-size: 11px; letter-spacing: 1.5px; }
.overlay { position: fixed; inset: 0; background: rgba(0,0,0,.4); z-index: 50; display: flex; justify-content: flex-end; }
.drawer { background: white; width: min(440px, 100%); height: 100%; padding: 28px; box-shadow: -10px 0 30px rgba(0,0,0,.15); overflow: auto; }
.drawerHead { display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid var(--line); padding-bottom: 18px; }
.drawerHead h2 { margin: 0; }
.drawerHead button { border: 0; background: transparent; font-size: 30px; }
.cartItems { margin: 20px 0; }
.cartItem { display: flex; justify-content: space-between; gap: 15px; padding: 16px 0; border-bottom: 1px solid var(--line); }
.cartItem b { display: block; font-size: 14px; }
.cartItem small { color: var(--muted); display: block; margin-top: 5px; }
.qty { display: flex; align-items: center; gap: 8px; }
.qty button { border: 1px solid var(--line); background: white; width: 28px; height: 28px; border-radius: 7px; }
.emptyCart { text-align: center; margin-top: 100px; color: var(--muted); }
.bigPlus { margin: auto; width: 70px; height: 70px; display: grid; place-items: center; border-radius: 50%; background: #edf5fb; color: var(--blue); font-size: 40px; }
.full { width: 100%; margin-top: 20px; text-align: center; }
.drawerCheck { margin-top: 20px; }

@media (max-width: 850px) {
  nav { display: none; }
  .heroGrid { grid-template-columns: 1fr; gap: 40px; }
  .heroCard { min-height: 300px; }
  .productGrid { grid-template-columns: repeat(2, 1fr); }
  .serviceGrid, .steps { grid-template-columns: 1fr; }
  .prescriptionBox, .footerGrid { grid-template-columns: 1fr; }
}
@media (max-width: 560px) {
  .container { width: min(100% - 24px, 1120px); }
  .nav { min-height: 66px; }
  .brand small { display: none; }
  .cartButton { padding: 9px 11px; font-size: 12px; }
  .hero { padding: 55px 0; }
  .hero h1 { font-size: 48px; }
  .heroActions, .searchRow { flex-direction: column; }
  .heroActions > *, .searchRow > * { width: 100%; text-align: center; padding: 13px; }
  .productGrid { grid-template-columns: 1fr; }
  .sectionHeading { align-items: flex-start; flex-direction: column; }
  .sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 30px; }
}
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap');

:root {
  --navy: #092f50;
  --blue: #0b5fa5;
  --red: #c93535;
  --ink: #102a3b;
  --muted: #607383;
  --paper: #f6f8fa;
  --line: #dbe4ea;
  --white: #fff;
  --shadow: 0 18px 50px rgba(8, 47, 80, .10);
}
* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { margin: 0; font-family: "DM Sans", sans-serif; color: var(--ink); background: var(--paper); }
a { color: inherit; text-decoration: none; }
button, input { font: inherit; }
button { cursor: pointer; }
.container { width: min(1120px, calc(100% - 40px)); margin: auto; }
.header { background: rgba(255,255,255,.96); border-bottom: 1px solid var(--line); position: sticky; top: 0; z-index: 20; backdrop-filter: blur(12px); }
.nav { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
.brand { display: flex; align-items: center; gap: 10px; }
.brandMark { width: 42px; height: 42px; display: grid; place-items: center; border-radius: 12px; background: var(--navy); color: #fff; font-weight: 700; font-size: 22px; }
.brand strong { display: block; letter-spacing: 2px; }
.brand small { color: var(--red); font-size: 9px; letter-spacing: 1.3px; font-weight: 700; }
nav { display: flex; gap: 25px; color: var(--muted); font-size: 14px; }
nav a:hover { color: var(--blue); }
.cartButton, .secondary { border: 1px solid var(--line); background: white; padding: 11px 16px; border-radius: 10px; font-weight: 600; }
.cartButton span { background: var(--red); color: white; border-radius: 50px; padding: 2px 7px; margin-left: 5px; font-size: 12px; }
.hero { background: linear-gradient(135deg, #edf5fb 0%, #fff 58%, #f9eeee 100%); padding: 80px 0 72px; border-bottom: 1px solid var(--line); }
.heroGrid { display: grid; grid-template-columns: 1.25fr .75fr; align-items: center; gap: 70px; }
.pill, .eyebrow { font-size: 11px; letter-spacing: 1.8px; font-weight: 700; color: var(--red); }
.hero h1 { font-size: clamp(44px, 6vw, 76px); line-height: .98; letter-spacing: -3px; margin: 18px 0; }
.hero h1 em { font-family: "Playfair Display", serif; font-weight: 600; color: var(--blue); letter-spacing: -2px; }
.heroText { color: var(--muted); max-width: 600px; font-size: 17px; line-height: 1.7; }
.heroActions { display: flex; gap: 12px; margin: 28px 0; }
.primary { border: 0; background: var(--navy); color: #fff; padding: 13px 19px; border-radius: 10px; font-weight: 700; display: inline-block; }
.primary:hover { background: var(--blue); }
.trustRow { display: flex; gap: 20px; flex-wrap: wrap; font-size: 12px; color: var(--muted); }
.heroCard { background: var(--navy); color: white; min-height: 370px; border-radius: 26px; padding: 45px; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; box-shadow: var(--shadow); position: relative; overflow: hidden; }
.heroCard:after { content: ""; position: absolute; width: 280px; height: 280px; border: 1px solid rgba(255,255,255,.14); border-radius: 50%; }
.orb { width: 150px; height: 150px; border: 1px solid rgba(255,255,255,.35); border-radius: 50%; display: grid; place-items: center; font-size: 60px; font-weight: 700; position: relative; z-index: 1; }
.heroCard h2 { margin: 18px 0 3px; letter-spacing: 5px; position: relative; z-index: 1; }
.heroCard p, .heroCard small { color: #bcd0de; position: relative; z-index: 1; }
.heroCardLine { width: 45px; height: 2px; background: var(--red); margin: 18px; position: relative; z-index: 1; }
.quickOrder { padding: 80px 0; }
.sectionHeading { display: flex; justify-content: space-between; align-items: end; gap: 20px; margin-bottom: 30px; }
.sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 38px; margin: 8px 0 0; letter-spacing: -1.5px; }
.number { color: var(--muted); font-size: 13px; }
.searchRow { display: flex; gap: 10px; margin-bottom: 25px; }
.searchRow input { flex: 1; border: 1px solid var(--line); padding: 15px 17px; border-radius: 11px; background: white; outline: none; }
.searchRow input:focus { border-color: var(--blue); }
.searchRow button { border: 0; border-radius: 11px; background: var(--red); color: white; padding: 0 20px; font-weight: 700; }
.categories { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 10px; }
.category { white-space: nowrap; background: white; border: 1px solid var(--line); padding: 12px 16px; border-radius: 50px; color: var(--muted); }
.category span { margin-right: 7px; color: var(--blue); }
.category.active { background: var(--navy); color: white; border-color: var(--navy); }
.productGrid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 25px; }
.productCard { background: white; border: 1px solid var(--line); border-radius: 16px; padding: 20px; min-height: 250px; display: flex; flex-direction: column; }
.productIcon { width: 46px; height: 46px; border-radius: 13px; background: #eaf4fb; color: var(--blue); display: grid; place-items: center; font-weight: 800; }
.tag { font-size: 10px; color: var(--red); text-transform: uppercase; letter-spacing: 1px; font-weight: 700; margin-top: 18px; }
.productCard h3 { margin: 8px 0; font-size: 18px; }
.productCard p { color: var(--muted); font-size: 13px; line-height: 1.5; margin: 0 0 18px; }
.productCard button { margin-top: auto; border: 1px solid var(--navy); background: white; color: var(--navy); padding: 10px; border-radius: 9px; font-weight: 700; }
.productCard button:hover { background: var(--navy); color: white; }
.empty { text-align: center; padding: 40px; color: var(--muted); }
.services { background: var(--navy); color: white; padding: 75px 0; }
.light .eyebrow { color: #e98a8a; }
.light h2 { color: white; }
.serviceGrid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: rgba(255,255,255,.16); }
.serviceGrid > div { padding: 30px; background: var(--navy); }
.serviceGrid b { color: #e98a8a; font-size: 12px; }
.serviceGrid h3 { font-size: 23px; margin-bottom: 8px; }
.serviceGrid p { color: #bcd0de; line-height: 1.6; font-size: 14px; }
.how { padding: 80px 0; }
.steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; margin-top: 35px; }
.steps div { border-top: 2px solid var(--navy); padding-top: 20px; }
.steps span { color: var(--red); font-weight: 800; }
.steps h3 { margin-bottom: 5px; }
.steps p { color: var(--muted); line-height: 1.6; font-size: 14px; }
.prescriptionBox { margin-bottom: 80px; background: white; border: 1px solid var(--line); border-radius: 20px; padding: 35px; display: grid; grid-template-columns: 1fr auto; gap: 20px; align-items: center; }
.prescriptionBox p { color: var(--muted); max-width: 650px; line-height: 1.6; }
.check { display: flex; gap: 8px; align-items: center; color: var(--muted); font-size: 13px; }
.check input { accent-color: var(--blue); }
footer { background: #071f34; color: white; padding: 50px 0; }
.footerGrid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 40px; }
.footerBrand { font-size: 22px; letter-spacing: 3px; font-weight: 700; }
footer p, footer a { color: #9fb4c4; font-size: 13px; line-height: 1.7; display: block; }
footer b { font-size: 11px; letter-spacing: 1.5px; }
.overlay { position: fixed; inset: 0; background: rgba(0,0,0,.4); z-index: 50; display: flex; justify-content: flex-end; }
.drawer { background: white; width: min(440px, 100%); height: 100%; padding: 28px; box-shadow: -10px 0 30px rgba(0,0,0,.15); overflow: auto; }
.drawerHead { display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid var(--line); padding-bottom: 18px; }
.drawerHead h2 { margin: 0; }
.drawerHead button { border: 0; background: transparent; font-size: 30px; }
.cartItems { margin: 20px 0; }
.cartItem { display: flex; justify-content: space-between; gap: 15px; padding: 16px 0; border-bottom: 1px solid var(--line); }
.cartItem b { display: block; font-size: 14px; }
.cartItem small { color: var(--muted); display: block; margin-top: 5px; }
.qty { display: flex; align-items: center; gap: 8px; }
.qty button { border: 1px solid var(--line); background: white; width: 28px; height: 28px; border-radius: 7px; }
.emptyCart { text-align: center; margin-top: 100px; color: var(--muted); }
.bigPlus { margin: auto; width: 70px; height: 70px; display: grid; place-items: center; border-radius: 50%; background: #edf5fb; color: var(--blue); font-size: 40px; }
.full { width: 100%; margin-top: 20px; text-align: center; }
.drawerCheck { margin-top: 20px; }

@media (max-width: 850px) {
  nav { display: none; }
  .heroGrid { grid-template-columns: 1fr; gap: 40px; }
  .heroCard { min-height: 300px; }
  .productGrid { grid-template-columns: repeat(2, 1fr); }
  .serviceGrid, .steps { grid-template-columns: 1fr; }
  .prescriptionBox, .footerGrid { grid-template-columns: 1fr; }
}
@media (max-width: 560px) {
  .container { width: min(100% - 24px, 1120px); }
  .nav { min-height: 66px; }
  .brand small { display: none; }
  .cartButton { padding: 9px 11px; font-size: 12px; }
  .hero { padding: 55px 0; }
  .hero h1 { font-size: 48px; }
  .heroActions, .searchRow { flex-direction: column; }
  .heroActions > *, .searchRow > * { width: 100%; text-align: center; padding: 13px; }
  .productGrid { grid-template-columns: 1fr; }
  .sectionHeading { align-items: flex-start; flex-direction: column; }
  .sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 30px; }
}
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap');

:root {
  --navy: #092f50;
  --blue: #0b5fa5;
  --red: #c93535;
  --ink: #102a3b;
  --muted: #607383;
  --paper: #f6f8fa;
  --line: #dbe4ea;
  --white: #fff;
  --shadow: 0 18px 50px rgba(8, 47, 80, .10);
}
* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { margin: 0; font-family: "DM Sans", sans-serif; color: var(--ink); background: var(--paper); }
a { color: inherit; text-decoration: none; }
button, input { font: inherit; }
button { cursor: pointer; }
.container { width: min(1120px, calc(100% - 40px)); margin: auto; }
.header { background: rgba(255,255,255,.96); border-bottom: 1px solid var(--line); position: sticky; top: 0; z-index: 20; backdrop-filter: blur(12px); }
.nav { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
.brand { display: flex; align-items: center; gap: 10px; }
.brandMark { width: 42px; height: 42px; display: grid; place-items: center; border-radius: 12px; background: var(--navy); color: #fff; font-weight: 700; font-size: 22px; }
.brand strong { display: block; letter-spacing: 2px; }
.brand small { color: var(--red); font-size: 9px; letter-spacing: 1.3px; font-weight: 700; }
nav { display: flex; gap: 25px; color: var(--muted); font-size: 14px; }
nav a:hover { color: var(--blue); }
.cartButton, .secondary { border: 1px solid var(--line); background: white; padding: 11px 16px; border-radius: 10px; font-weight: 600; }
.cartButton span { background: var(--red); color: white; border-radius: 50px; padding: 2px 7px; margin-left: 5px; font-size: 12px; }
.hero { background: linear-gradient(135deg, #edf5fb 0%, #fff 58%, #f9eeee 100%); padding: 80px 0 72px; border-bottom: 1px solid var(--line); }
.heroGrid { display: grid; grid-template-columns: 1.25fr .75fr; align-items: center; gap: 70px; }
.pill, .eyebrow { font-size: 11px; letter-spacing: 1.8px; font-weight: 700; color: var(--red); }
.hero h1 { font-size: clamp(44px, 6vw, 76px); line-height: .98; letter-spacing: -3px; margin: 18px 0; }
.hero h1 em { font-family: "Playfair Display", serif; font-weight: 600; color: var(--blue); letter-spacing: -2px; }
.heroText { color: var(--muted); max-width: 600px; font-size: 17px; line-height: 1.7; }
.heroActions { display: flex; gap: 12px; margin: 28px 0; }
.primary { border: 0; background: var(--navy); color: #fff; padding: 13px 19px; border-radius: 10px; font-weight: 700; display: inline-block; }
.primary:hover { background: var(--blue); }
.trustRow { display: flex; gap: 20px; flex-wrap: wrap; font-size: 12px; color: var(--muted); }
.heroCard { background: var(--navy); color: white; min-height: 370px; border-radius: 26px; padding: 45px; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; box-shadow: var(--shadow); position: relative; overflow: hidden; }
.heroCard:after { content: ""; position: absolute; width: 280px; height: 280px; border: 1px solid rgba(255,255,255,.14); border-radius: 50%; }
.orb { width: 150px; height: 150px; border: 1px solid rgba(255,255,255,.35); border-radius: 50%; display: grid; place-items: center; font-size: 60px; font-weight: 700; position: relative; z-index: 1; }
.heroCard h2 { margin: 18px 0 3px; letter-spacing: 5px; position: relative; z-index: 1; }
.heroCard p, .heroCard small { color: #bcd0de; position: relative; z-index: 1; }
.heroCardLine { width: 45px; height: 2px; background: var(--red); margin: 18px; position: relative; z-index: 1; }
.quickOrder { padding: 80px 0; }
.sectionHeading { display: flex; justify-content: space-between; align-items: end; gap: 20px; margin-bottom: 30px; }
.sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 38px; margin: 8px 0 0; letter-spacing: -1.5px; }
.number { color: var(--muted); font-size: 13px; }
.searchRow { display: flex; gap: 10px; margin-bottom: 25px; }
.searchRow input { flex: 1; border: 1px solid var(--line); padding: 15px 17px; border-radius: 11px; background: white; outline: none; }
.searchRow input:focus { border-color: var(--blue); }
.searchRow button { border: 0; border-radius: 11px; background: var(--red); color: white; padding: 0 20px; font-weight: 700; }
.categories { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 10px; }
.category { white-space: nowrap; background: white; border: 1px solid var(--line); padding: 12px 16px; border-radius: 50px; color: var(--muted); }
.category span { margin-right: 7px; color: var(--blue); }
.category.active { background: var(--navy); color: white; border-color: var(--navy); }
.productGrid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 25px; }
.productCard { background: white; border: 1px solid var(--line); border-radius: 16px; padding: 20px; min-height: 250px; display: flex; flex-direction: column; }
.productIcon { width: 46px; height: 46px; border-radius: 13px; background: #eaf4fb; color: var(--blue); display: grid; place-items: center; font-weight: 800; }
.tag { font-size: 10px; color: var(--red); text-transform: uppercase; letter-spacing: 1px; font-weight: 700; margin-top: 18px; }
.productCard h3 { margin: 8px 0; font-size: 18px; }
.productCard p { color: var(--muted); font-size: 13px; line-height: 1.5; margin: 0 0 18px; }
.productCard button { margin-top: auto; border: 1px solid var(--navy); background: white; color: var(--navy); padding: 10px; border-radius: 9px; font-weight: 700; }
.productCard button:hover { background: var(--navy); color: white; }
.empty { text-align: center; padding: 40px; color: var(--muted); }
.services { background: var(--navy); color: white; padding: 75px 0; }
.light .eyebrow { color: #e98a8a; }
.light h2 { color: white; }
.serviceGrid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: rgba(255,255,255,.16); }
.serviceGrid > div { padding: 30px; background: var(--navy); }
.serviceGrid b { color: #e98a8a; font-size: 12px; }
.serviceGrid h3 { font-size: 23px; margin-bottom: 8px; }
.serviceGrid p { color: #bcd0de; line-height: 1.6; font-size: 14px; }
.how { padding: 80px 0; }
.steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; margin-top: 35px; }
.steps div { border-top: 2px solid var(--navy); padding-top: 20px; }
.steps span { color: var(--red); font-weight: 800; }
.steps h3 { margin-bottom: 5px; }
.steps p { color: var(--muted); line-height: 1.6; font-size: 14px; }
.prescriptionBox { margin-bottom: 80px; background: white; border: 1px solid var(--line); border-radius: 20px; padding: 35px; display: grid; grid-template-columns: 1fr auto; gap: 20px; align-items: center; }
.prescriptionBox p { color: var(--muted); max-width: 650px; line-height: 1.6; }
.check { display: flex; gap: 8px; align-items: center; color: var(--muted); font-size: 13px; }
.check input { accent-color: var(--blue); }
footer { background: #071f34; color: white; padding: 50px 0; }
.footerGrid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 40px; }
.footerBrand { font-size: 22px; letter-spacing: 3px; font-weight: 700; }
footer p, footer a { color: #9fb4c4; font-size: 13px; line-height: 1.7; display: block; }
footer b { font-size: 11px; letter-spacing: 1.5px; }
.overlay { position: fixed; inset: 0; background: rgba(0,0,0,.4); z-index: 50; display: flex; justify-content: flex-end; }
.drawer { background: white; width: min(440px, 100%); height: 100%; padding: 28px; box-shadow: -10px 0 30px rgba(0,0,0,.15); overflow: auto; }
.drawerHead { display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid var(--line); padding-bottom: 18px; }
.drawerHead h2 { margin: 0; }
.drawerHead button { border: 0; background: transparent; font-size: 30px; }
.cartItems { margin: 20px 0; }
.cartItem { display: flex; justify-content: space-between; gap: 15px; padding: 16px 0; border-bottom: 1px solid var(--line); }
.cartItem b { display: block; font-size: 14px; }
.cartItem small { color: var(--muted); display: block; margin-top: 5px; }
.qty { display: flex; align-items: center; gap: 8px; }
.qty button { border: 1px solid var(--line); background: white; width: 28px; height: 28px; border-radius: 7px; }
.emptyCart { text-align: center; margin-top: 100px; color: var(--muted); }
.bigPlus { margin: auto; width: 70px; height: 70px; display: grid; place-items: center; border-radius: 50%; background: #edf5fb; color: var(--blue); font-size: 40px; }
.full { width: 100%; margin-top: 20px; text-align: center; }
.drawerCheck { margin-top: 20px; }

@media (max-width: 850px) {
  nav { display: none; }
  .heroGrid { grid-template-columns: 1fr; gap: 40px; }
  .heroCard { min-height: 300px; }
  .productGrid { grid-template-columns: repeat(2, 1fr); }
  .serviceGrid, .steps { grid-template-columns: 1fr; }
  .prescriptionBox, .footerGrid { grid-template-columns: 1fr; }
}
@media (max-width: 560px) {
  .container { width: min(100% - 24px, 1120px); }
  .nav { min-height: 66px; }
  .brand small { display: none; }
  .cartButton { padding: 9px 11px; font-size: 12px; }
  .hero { padding: 55px 0; }
  .hero h1 { font-size: 48px; }
  .heroActions, .searchRow { flex-direction: column; }
  .heroActions > *, .searchRow > * { width: 100%; text-align: center; padding: 13px; }
  .productGrid { grid-template-columns: 1fr; }
  .sectionHeading { align-items: flex-start; flex-direction: column; }
  .sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 30px; }
}
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap');

:root {
  --navy: #092f50;
  --blue: #0b5fa5;
  --red: #c93535;
  --ink: #102a3b;
  --muted: #607383;
  --paper: #f6f8fa;
  --line: #dbe4ea;
  --white: #fff;
  --shadow: 0 18px 50px rgba(8, 47, 80, .10);
}
* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { margin: 0; font-family: "DM Sans", sans-serif; color: var(--ink); background: var(--paper); }
a { color: inherit; text-decoration: none; }
button, input { font: inherit; }
button { cursor: pointer; }
.container { width: min(1120px, calc(100% - 40px)); margin: auto; }
.header { background: rgba(255,255,255,.96); border-bottom: 1px solid var(--line); position: sticky; top: 0; z-index: 20; backdrop-filter: blur(12px); }
.nav { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
.brand { display: flex; align-items: center; gap: 10px; }
.brandMark { width: 42px; height: 42px; display: grid; place-items: center; border-radius: 12px; background: var(--navy); color: #fff; font-weight: 700; font-size: 22px; }
.brand strong { display: block; letter-spacing: 2px; }
.brand small { color: var(--red); font-size: 9px; letter-spacing: 1.3px; font-weight: 700; }
nav { display: flex; gap: 25px; color: var(--muted); font-size: 14px; }
nav a:hover { color: var(--blue); }
.cartButton, .secondary { border: 1px solid var(--line); background: white; padding: 11px 16px; border-radius: 10px; font-weight: 600; }
.cartButton span { background: var(--red); color: white; border-radius: 50px; padding: 2px 7px; margin-left: 5px; font-size: 12px; }
.hero { background: linear-gradient(135deg, #edf5fb 0%, #fff 58%, #f9eeee 100%); padding: 80px 0 72px; border-bottom: 1px solid var(--line); }
.heroGrid { display: grid; grid-template-columns: 1.25fr .75fr; align-items: center; gap: 70px; }
.pill, .eyebrow { font-size: 11px; letter-spacing: 1.8px; font-weight: 700; color: var(--red); }
.hero h1 { font-size: clamp(44px, 6vw, 76px); line-height: .98; letter-spacing: -3px; margin: 18px 0; }
.hero h1 em { font-family: "Playfair Display", serif; font-weight: 600; color: var(--blue); letter-spacing: -2px; }
.heroText { color: var(--muted); max-width: 600px; font-size: 17px; line-height: 1.7; }
.heroActions { display: flex; gap: 12px; margin: 28px 0; }
.primary { border: 0; background: var(--navy); color: #fff; padding: 13px 19px; border-radius: 10px; font-weight: 700; display: inline-block; }
.primary:hover { background: var(--blue); }
.trustRow { display: flex; gap: 20px; flex-wrap: wrap; font-size: 12px; color: var(--muted); }
.heroCard { background: var(--navy); color: white; min-height: 370px; border-radius: 26px; padding: 45px; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; box-shadow: var(--shadow); position: relative; overflow: hidden; }
.heroCard:after { content: ""; position: absolute; width: 280px; height: 280px; border: 1px solid rgba(255,255,255,.14); border-radius: 50%; }
.orb { width: 150px; height: 150px; border: 1px solid rgba(255,255,255,.35); border-radius: 50%; display: grid; place-items: center; font-size: 60px; font-weight: 700; position: relative; z-index: 1; }
.heroCard h2 { margin: 18px 0 3px; letter-spacing: 5px; position: relative; z-index: 1; }
.heroCard p, .heroCard small { color: #bcd0de; position: relative; z-index: 1; }
.heroCardLine { width: 45px; height: 2px; background: var(--red); margin: 18px; position: relative; z-index: 1; }
.quickOrder { padding: 80px 0; }
.sectionHeading { display: flex; justify-content: space-between; align-items: end; gap: 20px; margin-bottom: 30px; }
.sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 38px; margin: 8px 0 0; letter-spacing: -1.5px; }
.number { color: var(--muted); font-size: 13px; }
.searchRow { display: flex; gap: 10px; margin-bottom: 25px; }
.searchRow input { flex: 1; border: 1px solid var(--line); padding: 15px 17px; border-radius: 11px; background: white; outline: none; }
.searchRow input:focus { border-color: var(--blue); }
.searchRow button { border: 0; border-radius: 11px; background: var(--red); color: white; padding: 0 20px; font-weight: 700; }
.categories { display: flex; gap: 10px; overflow-x: auto; padding-bottom: 10px; }
.category { white-space: nowrap; background: white; border: 1px solid var(--line); padding: 12px 16px; border-radius: 50px; color: var(--muted); }
.category span { margin-right: 7px; color: var(--blue); }
.category.active { background: var(--navy); color: white; border-color: var(--navy); }
.productGrid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-top: 25px; }
.productCard { background: white; border: 1px solid var(--line); border-radius: 16px; padding: 20px; min-height: 250px; display: flex; flex-direction: column; }
.productIcon { width: 46px; height: 46px; border-radius: 13px; background: #eaf4fb; color: var(--blue); display: grid; place-items: center; font-weight: 800; }
.tag { font-size: 10px; color: var(--red); text-transform: uppercase; letter-spacing: 1px; font-weight: 700; margin-top: 18px; }
.productCard h3 { margin: 8px 0; font-size: 18px; }
.productCard p { color: var(--muted); font-size: 13px; line-height: 1.5; margin: 0 0 18px; }
.productCard button { margin-top: auto; border: 1px solid var(--navy); background: white; color: var(--navy); padding: 10px; border-radius: 9px; font-weight: 700; }
.productCard button:hover { background: var(--navy); color: white; }
.empty { text-align: center; padding: 40px; color: var(--muted); }
.services { background: var(--navy); color: white; padding: 75px 0; }
.light .eyebrow { color: #e98a8a; }
.light h2 { color: white; }
.serviceGrid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: rgba(255,255,255,.16); }
.serviceGrid > div { padding: 30px; background: var(--navy); }
.serviceGrid b { color: #e98a8a; font-size: 12px; }
.serviceGrid h3 { font-size: 23px; margin-bottom: 8px; }
.serviceGrid p { color: #bcd0de; line-height: 1.6; font-size: 14px; }
.how { padding: 80px 0; }
.steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 30px; margin-top: 35px; }
.steps div { border-top: 2px solid var(--navy); padding-top: 20px; }
.steps span { color: var(--red); font-weight: 800; }
.steps h3 { margin-bottom: 5px; }
.steps p { color: var(--muted); line-height: 1.6; font-size: 14px; }
.prescriptionBox { margin-bottom: 80px; background: white; border: 1px solid var(--line); border-radius: 20px; padding: 35px; display: grid; grid-template-columns: 1fr auto; gap: 20px; align-items: center; }
.prescriptionBox p { color: var(--muted); max-width: 650px; line-height: 1.6; }
.check { display: flex; gap: 8px; align-items: center; color: var(--muted); font-size: 13px; }
.check input { accent-color: var(--blue); }
footer { background: #071f34; color: white; padding: 50px 0; }
.footerGrid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 40px; }
.footerBrand { font-size: 22px; letter-spacing: 3px; font-weight: 700; }
footer p, footer a { color: #9fb4c4; font-size: 13px; line-height: 1.7; display: block; }
footer b { font-size: 11px; letter-spacing: 1.5px; }
.overlay { position: fixed; inset: 0; background: rgba(0,0,0,.4); z-index: 50; display: flex; justify-content: flex-end; }
.drawer { background: white; width: min(440px, 100%); height: 100%; padding: 28px; box-shadow: -10px 0 30px rgba(0,0,0,.15); overflow: auto; }
.drawerHead { display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid var(--line); padding-bottom: 18px; }
.drawerHead h2 { margin: 0; }
.drawerHead button { border: 0; background: transparent; font-size: 30px; }
.cartItems { margin: 20px 0; }
.cartItem { display: flex; justify-content: space-between; gap: 15px; padding: 16px 0; border-bottom: 1px solid var(--line); }
.cartItem b { display: block; font-size: 14px; }
.cartItem small { color: var(--muted); display: block; margin-top: 5px; }
.qty { display: flex; align-items: center; gap: 8px; }
.qty button { border: 1px solid var(--line); background: white; width: 28px; height: 28px; border-radius: 7px; }
.emptyCart { text-align: center; margin-top: 100px; color: var(--muted); }
.bigPlus { margin: auto; width: 70px; height: 70px; display: grid; place-items: center; border-radius: 50%; background: #edf5fb; color: var(--blue); font-size: 40px; }
.full { width: 100%; margin-top: 20px; text-align: center; }
.drawerCheck { margin-top: 20px; }

@media (max-width: 850px) {
  nav { display: none; }
  .heroGrid { grid-template-columns: 1fr; gap: 40px; }
  .heroCard { min-height: 300px; }
  .productGrid { grid-template-columns: repeat(2, 1fr); }
  .serviceGrid, .steps { grid-template-columns: 1fr; }
  .prescriptionBox, .footerGrid { grid-template-columns: 1fr; }
}
@media (max-width: 560px) {
  .container { width: min(100% - 24px, 1120px); }
  .nav { min-height: 66px; }
  .brand small { display: none; }
  .cartButton { padding: 9px 11px; font-size: 12px; }
  .hero { padding: 55px 0; }
  .hero h1 { font-size: 48px; }
  .heroActions, .searchRow { flex-direction: column; }
  .heroActions > *, .searchRow > * { width: 100%; text-align: center; padding: 13px; }
  .productGrid { grid-template-columns: 1fr; }
  .sectionHeading { align-items: flex-start; flex-direction: column; }
  .sectionHeading h2, .how h2, .prescriptionBox h2 { font-size: 30px; }
}





<!--
**alphindic/ALPHINDIC** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
