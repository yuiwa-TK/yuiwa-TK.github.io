---
title: "Log Create Mypage"
date: 2023-04-05T23:41:19+09:00
draft: false
---

## From downloading Hugo to deploying to github pages.
1. Install hugo with brew.
    ```bash
    brew install hugo
    ```
2. Select and download the hugo theme PaperMod.
    ```bash
    hugo new site (myreponame).github.io
    cd (myreponame).github.io
    git init. # init git repo.
    ```
3. create config.yml
    - PaperMod recommends using yml rather than toml.
    - Add this line to config.yml
    ```yml
    theme: "PaperMod"
    ```
