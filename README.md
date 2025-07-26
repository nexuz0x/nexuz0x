<h1 align="center">Hi 👋, I'm Nexuz</h1>
<h3 align="center">Offensive Security Enthusiast & Cybersecurity Learner</h3>

- 🌱 I’m currently learning **Ethical hacking and offensive security concepts**
- 📫 Reach me at: **nexuz0x@proton.me**

<h3 align="center">Connect with me:</h3>
<p align="center">
  <!-- You can add social icons here (e.g., GitHub, LinkedIn) -->
</p>

<h3 align="center">Languages and Tools:</h3>
<p align="center">
  <a href="https://www.java.com" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg"
         alt="Java" width="30" height="30" style="margin: 0 8px;" />
  </a>
  <a href="https://www.linux.org/" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg"
         alt="Linux" width="30" height="30" style="margin: 0 8px;" />
  </a>
  <a href="https://www.php.net" target="_blank" rel="noreferrer">
    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg"
         alt="PHP" width="30" height="30" style="margin: 0 8px;" />
  </a>
  <a href="https://www.wireshark.org/" target="_blank" rel="noreferrer">
    <img src="https://upload.wikimedia.org/wikipedia/commons/c/c6/Wireshark_icon_new.png"
         alt="Wireshark" width="30" height="30" style="margin: 0 8px;" />
  </a>
  <a href="https://www.metasploit.com/" target="_blank" rel="noreferrer">
    <img src="https://gdm-catalog-fmapi-prod.imgix.net/ProductLogo/17df60fe-5944-44ad-b73a-531294eea4a0.png?auto=format%2Ccompress&fit=max&w=256&q=75&ch=Width%2CDPR"
         alt="Metasploit" width="30" height="30" style="margin: 0 8px;" />
  </a>
</p>




name: Generate pacman animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate pacman-contribution-graph.svg
        uses: abozanona/pacman-contribution-graph@main
        with:
          github_user_name: ${{ github.repository_owner }}


      - name: push pacman-contribution-graph.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

          
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/nexuz0x/nexuz0x/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/nexuz0x/nexuz0x/output/pacman-contribution-graph.svg">
  <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/nexuz0x/nexuz0x/output/pacman-contribution-graph.svg">
</picture>

###

<img src="https://raw.githubusercontent.com/nexuz0x/nexuz0x/output/snake.svg" alt="Snake animation" />

###
