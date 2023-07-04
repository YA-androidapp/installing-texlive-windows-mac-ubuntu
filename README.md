# installing-texlive-windows-mac-ubuntu

---

# TEX Live

## Mac

### Homebrewを利用したインストール

```zsh
brew install --cask mactex
exec $SHELL -l

sudo tlmgr update --self --all
sudo tlmgr paper a4

# CUI
brew install --cask mactex-no-gui
exec $SHELL -l

sudo tlmgr update --self --all
sudo tlmgr paper a4

# TeX Liveをフルインストールしない
brew install --cask basictex
exec $SHELL -l

sudo tlmgr update --self --all
sudo tlmgr install collection-langjapanese latexindent latexmk utf8add
sudo tlmgr paper a4
```

### インストール済みパッケージの更新

```zsh
sudo tlmgr update --self --all
```

## Ubuntu

```bash
sudo apt install texlive-full
```

## Windows

```powershell
# 管理者権限で実行
choco install texlive

tlmgr --repository http://www.texlive.info/tlgpg/ install tlgpg

tlmgr install cite collection-langjapanese latexindent latexmk url utf8add
tlmgr paper a4
```

## Docker

```bash
# pull
# Docker Hub
docker pull paperist/texlive-ja:latest

# GitHub Container Registry
docker pull ghcr.io/paperist/texlive-ja:latest
docker image tag ghcr.io/paperist/texlive-ja:latest paperist/texlive-ja:latest


# run
docker run --rm -it -v $PWD:/workdir paperist/texlive-ja:latest sh -c 'latexmk -C main.tex && latexmk main.tex && latexmk -c main.tex'
```

## 動作確認

```bash
lualatex test.tex
```

```bash
tlmgr install booktabs caption comment dotseqn filehook float framed geometry here lastpage lipsum mathrsfs multirow newtx ntheorem realscripts setspace siunitx subfigure textpos times titlesec txfonts type1cm xstring

tlmgr info mathrsfs
# Packages containing files matching `mathrsfs':
# jknapltx:
#         texmf-dist/doc/latex/jknapltx/mathrsfs.rme
#         texmf-dist/tex/latex/jknapltx/mathrsfs.sty
tlmgr install jknapltx rsfs



cd Templates/meltingrabbit.com/201708020
lualatex source.tex

cd Templates/meltingrabbit.com/2018022501
lualatex source.tex

cd Templates/rkmathi
lualatex jornal.tex
lualatex report.tex

cd Templates/t_kemmochi
lualatex jsiam.tex
lualatex mathsoc.tex

cd Templates/ipsj_v4/UTF
# ptex2pdf -l jsample
platex jsample
dvipdfmx jsample

cd Templates/latex-template-ja
lualatex thesis.tex
lualatex wordstyle.tex
```

---

# 参考文献

## TeX

- [TeX Users Group](https://www.tug.org/texlive/doc/texlive-ja/texlive-ja.pdf)
  - [TeX Live](https://www.tug.org/texlive/doc/texlive-ja/texlive-ja.pdf)
    - [Installing TeX Live over the Internet](https://www.tug.org/texlive/acquire-netinstall.html)
      - [install-tl-windows.exe](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe)
    - [TeX Live ガイド](https://www.tug.org/texlive/doc/texlive-ja/texlive-ja.pdf)

- [TeX Wiki](https://texwiki.texjp.org/)

## テンプレート

- [LaTeXスタイルファイル、MS-Wordテンプレートファイル](https://www.ipsj.or.jp/journal/submit/style.html)

- [(lt)jsarticleによる, 日本数学会・日本応用数理学会の学会アブストラクト](https://qiita.com/t_kemmochi/items/cad392a0a3e7bcf3018d)
- [Melting Rabbit's Blog ](https://meltingrabbit.com/)
- [rkmathi/jornal.tex](https://gist.github.com/rkmathi/6941a5180b7554ab915d)
- [sKujirai/latex-template-ja](https://github.com/sKujirai/latex-template-ja)

## フォント

- [yhchen/ttc2ttf](https://github.com/yhchen/ttc2ttf)

---

Copyright (c) 2023 YA-androidapp(https://github.com/yzkn) All rights reserved.
