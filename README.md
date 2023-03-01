# 👋 Hello! Welcome to my Github profile.
## My name is rauny and my nickname is "raunykkj"!

<div>
<a href="https://instagram.com/rauny_kkj" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
<a href="https://www.twitch.tv/rauny_kkj" target="_blank"><img src="https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white" target="_blank"></a>
<a href = "mailto:lordgoku1238@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
</div>

<div>
<a href="https://github.com/raunykkj">
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=raunykkj&layout=compact&langs_count=7&theme=dracula"/>
<img height="180em" src="https://github-readme-stats.vercel.app/api?username=raunykkj&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
</div>



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
          github_user_name: raunykkj
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
