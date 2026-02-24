# Komezusenge Bolice

**Full-Stack Developer · Penetration Tester · AI Enthusiast**

---

## About

Python developer and cybersecurity professional focused on building robust backend systems and securing them. I enjoy the intersection of development and security — writing the code, then stress-testing it to make it bulletproof.

- Building **REST APIs** with Django and FastAPI
- Performing **web, mobile & API penetration testing**
- Competing in **CTF challenges** on PicoCTF and TryHackMe
- Integrating **AI/ML** into real-world applications

---

## Tech Stack

**Languages** — Python, JavaScript, TypeScript, Bash

**Frontend** — React, TypeScript

**Backend** — Django, FastAPI, Node.js, Express.js

**Security** — Burp Suite, OWASP ZAP, Nmap, Metasploit, Wireshark, SQLMap, Hydra

---

## Security Focus

| Area | Details |
|---|---|
| **Web & API Pentesting** | OWASP Top 10 — SQLi, XSS, IDOR, Broken Auth, CSRF |
| **Mobile Security** | Insecure storage, API exposure, certificate pinning bypass |
| **Network Analysis** | Port scanning, traffic analysis, MITM |
| **CTF Competitions** | Web exploitation, cryptography, forensics, reverse engineering |

---

## Platforms

[![TryHackMe](https://img.shields.io/badge/TryHackMe-212C42?style=for-the-badge&logo=tryhackme&logoColor=white)](https://tryhackme.com/p/bolice)
[![PicoCTF](https://img.shields.io/badge/PicoCTF-05A6F0?style=for-the-badge&logoColor=white)](https://play.picoctf.org/users/bolice)

> **Want your live TryHackMe rank card here?** See the [setup guide](#tryhackme-live-rank-card) at the bottom.

---

## GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Bolice1&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&rank_icon=github" alt="GitHub Stats" />

<br/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Bolice1&layout=compact&theme=tokyonight&hide_border=true&count_private=true" alt="Top Languages" />

<br/>

<img src="https://github-readme-streak-stats-eight.vercel.app?user=Bolice1&theme=tokyonight&hide_border=true" alt="GitHub Streak" />

</div>

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/komezusenge-bolice-0b8280380/)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-212C42?style=flat-square&logo=tryhackme&logoColor=white)](https://tryhackme.com/p/bolice)
[![PicoCTF](https://img.shields.io/badge/PicoCTF-05A6F0?style=flat-square&logoColor=white)](https://play.picoctf.org/users/bolice)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/voidghost46/)

---

*"Code it. Break it. Secure it."*

---

## TryHackMe Live Rank Card

The TryHackMe S3 badge URL (`tryhackme-badges.s3.amazonaws.com`) is unreliable and often fails to render on GitHub. The fix is a GitHub Action that downloads the image into your repo daily and references it locally.

**Step 1 — Create `.github/workflows/update-thm-badge.yml`:**

```yaml
name: Update TryHackMe Badge
permissions:
  contents: write
on:
  schedule:
    - cron: '0 0 * * *'
  workflow_dispatch:

jobs:
  update-badge:
    runs-on: ubuntu-22.04
    steps:
      - uses: actions/checkout@v3
        with:
          persist-credentials: true
          fetch-depth: 0
      - name: Configure Git
        run: |
          git config --global user.name "GitHub Actions Bot"
          git config --global user.email "actions@github.com"
      - name: Fetch TryHackMe Badge
        uses: DhanushNehru/tryhackme-badge-action-workflow@v1.0
        continue-on-error: true
        with:
          image_path: './assets/tryhackme-badge.png'
          username: 'bolice'
          user_id: 'YOUR_THM_USER_ID'
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
      - name: Commit and push badge
        run: |
          git add ./assets/tryhackme-badge.png || true
          if git diff --cached --quiet; then echo "No changes"; exit 0; fi
          git commit -m "Updated THM badge"
          git push origin "HEAD:${{ github.ref_name }}"
```

**Step 2 — Find your TryHackMe user ID:** Go to your profile settings on TryHackMe — the numeric user ID is shown in your profile URL or account page.

**Step 3 — Replace the TryHackMe badge in the Platforms section above with:**

```markdown
[![TryHackMe](./assets/tryhackme-badge.png)](https://tryhackme.com/p/bolice)
```
