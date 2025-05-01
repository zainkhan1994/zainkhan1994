<a href="https://github.com/zainkhan1994">
  🚀<img align="center" src="https://github-readme-streak-stats.herokuapp.com?user=zainkhan1994&theme=dark&hide_border=true&border_radius=4&date_format=M%20j%5B%2C%20Y%5D&mode=weekly&card_width=500)](https://git.io/streak-stats" />
</a>

<a href="https://github.com/zainkhan1994">
  🚀<img align="center" src="https://github-readme-stats.vercel.app/api?username=zainkhan1994&show_icons=true&theme=material-palenight" />
</a><br>

<a href="https://github.com/zainkhan1994">
  🚀<img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=zainkhan1994&layout=compact&theme=material-palenight" />
</a><br>
name: Update README

on:
  schedule:
    - cron: '0 0 * * *' # Runs daily at midnight UTC
  workflow_dispatch: # Allows you to manually trigger the workflow

jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - name: Check out repository
        uses: actions/checkout@v3

      - name: Update README with GitHub Stats
        uses: anmol098/generate-readme@v2.0.3
        with:
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}