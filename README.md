### Olá! 👋 Eu sou o Diego. Estou fazendo uma transição de carreira e entrando nesse mundo maravilhoso que é a programação.

- 📚 Atualmente estudando TypeScript, C# e MySql.
- 👨‍🎓 Recém-formado em Análise e Desenvolvimento de Sistemas.


![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=arghyll&show_icons=true&theme=merko&count_private=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=arghyll&layout=compact&theme=merko)

<div style="display: inline_block"><br>
  <img align="center" alt="Diego-Js" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-plain.svg">
  <img align="center" alt="Diego-Ts" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg">
  <img align="center" alt="Diego-HTML" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Diego-CSS" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Diego-Csharp" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/csharp/csharp-original.svg">
  <img align="center" alt="Diego-MySql" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg">
</div>

##

<div>
  <a href="https://instagram.com/arghyll" target="_blank"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href="https://facebook.com/arghyll" target="_blank"><img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/diego-alvarez-9a2a091b4/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
  <a href = "mailto:carvalho.84@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
</div>

![Snake animation](https://github.com/Arghyll/Arghyll/blob/output/github-contribution-grid-snake.svg)
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
