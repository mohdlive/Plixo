# Think Like an Ethical Hacker — Workshop Demos

Security‑awareness demos for the **“Think Like an Ethical Hacker” (فكّر كهاكر أخلاقي)** workshop —
GDG on Campus · King Faisal University. Presented by **م. محمد الهاشم**.

> هذه المواد تعليمية للتوعية الأمنية فقط: اسم تطبيق وهمي (Plixo)، وبيانات وهميّة فقط.

---

> ⚠️ **Educational use only.** These pages exist to teach people how phishing and weak
> passwords work so they can protect themselves. The login page is a **fictitious brand
> (“Plixo”)** and is meant to be used with **dummy data only**. Do **not** use it to imitate a
> real company, deceive anyone, or collect real credentials. Nothing here transmits or stores
> real personal data.

## What's inside

| File | What it is |
| --- | --- |
| `index.html` | **Plixo** — a realistic-but-fake social login page. A phishing-awareness demo: whatever you type is shown straight back to you on the same screen to prove how easily a fake page captures input. |
| `GoodPassChecker.html` | **كم تصمد كلمة مرورك؟** — an interactive password-strength visualizer that estimates how long a password would take to crack, from *instant* to *centuries*. |
| `deck.pdf` | The full workshop presentation (Arabic), downloadable for attendees. |
| `فكّر كهاكر أخلاقي.jpeg` | The workshop poster. |

## The demos

### 1. Phishing login demo — `index.html`
Looks like a normal social app sign-in. When a visitor submits (with **dummy** credentials), the
page flips to a clear explanation: *this was a fake page; a real attacker would now have your
login.* It then shows the tell-tale signs of phishing and how to stay safe. The capture is purely
client-side — the typed values are displayed locally and are **never sent to any server**.

> If you deploy the **live-feed variant** of the page, opening it with `#wall` (e.g.
> `index.html#wall`) shows a presenter dashboard where attendees' dummy entries appear in real
> time. That variant uses Firebase — paste your own `firebaseConfig` into the page, start the
> Realtime Database in **test mode** for the event, and **lock the rules down afterward**
> (`{"rules": {".read": false, ".write": false}}`). Dummy data only.

### 2. Password strength — `GoodPassChecker.html`
Type a password (or try the sample chips) and watch the estimated crack time, strength tier, and
character stats update live. The point: **length beats complexity**, and reused or common
passwords fall instantly. Nothing is stored or sent.

## Running / hosting

Both demos are self-contained static HTML — no build step, no backend (except the optional
Firebase live feed above).

- **Locally:** open the `.html` file in any modern browser. *(Tip: the Firebase live-feed variant
  needs to be served over `http(s)`, not opened as a `file://`.)*
- **GitHub Pages (this repo):** Settings → Pages → Deploy from branch → `main` / root. Pages then
  serves:
  - `https://mohdlive.github.io/Plixo/` → the phishing demo
  - `https://mohdlive.github.io/Plixo/GoodPassChecker.html` → the password tool
  - `https://mohdlive.github.io/Plixo/deck.pdf` → the presentation

Attendees can scan a QR code to each URL to open the demos on their own phones.

## About the workshop

A 3-hour, hands-on session for a non-technical audience. The idea: **you can't defend against a
trick you don't understand**, so we look at things through an attacker's eyes — to spot deception
and protect our own accounts, never to cause harm. It covers the hacker mindset, spotting phishing
and fake links, and a practical “digital shield” of protection steps.

## Author

**م. محمد الهاشم — Mohammed Najeeb Al-Hashem**
Interested in cybersecurity · Data Analytics & BI specialist and trainer.

- LinkedIn: https://www.linkedin.com/in/mohammed-najeeb-al-hashem/
- X: https://x.com/MN_Alhashem
- Telegram: https://t.me/profesorclub

## License & disclaimer

Shared for education and awareness. Use responsibly and only on systems you own or have explicit
permission to test. Provided “as is,” without warranty of any kind.
