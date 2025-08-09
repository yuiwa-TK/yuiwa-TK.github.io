---
title: "Creating a webpage with Hugo & Publishing it with Github Pages. "
date: 2023-04-05T23:41:19+09:00
draft: false
tags: ["tech"]
cover:
  image: "post-mypage.png"
  # can also paste direct link from external site
  # ex. https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png
#   alt: "<alt text>"
#   caption: "<text>"
  relative: false # To use relative path for cover image, used in hugo Page-bundles
summary: create my page!
---

## From downloading Hugo to deploying to github pages.
1. Install hugo using homebrew.
    ```zsh
    brew install hugo
    ```
2. Download hugo theme "[PaperMod](https://github.com/adityatelange/hugo-PaperMod)".
    ```zsh
    hugo new site (myreponame).github.io
    cd (myreponame).github.io
    git init. # init git repo.
    ```
3. Create config.yml
    - PaperMod recommends using yml rather than toml.
    - Add this line to config.yml
    ```yml
    theme: "PaperMod"
    ```
4. Create workflow file .github/workflows/gh-pages.yml ([Ref](https://github.com/peaceiris/actions-gh-pages))

5. Push local repo to remote repo at github
    ```bash
    git remote add origin https://github.com/(MyGitHubAccount)/(RepoName).git
    git branch -M main
    git push -u origin main
    ```
6. The homepage will be buit & deployed with GitHub Actions. The built static webpage files will appear in gh-pages branch.
7. Click setting tab and move to Pages, then change the branch from which the github pages is built (`main` to `gh-pages`). 