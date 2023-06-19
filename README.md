# installing-texlive-windows-mac-ubuntu

---

# TEX Live

# Mac

## Homebrewを利用したインストール

```zsh
brew install --cask mactex
sudo tlmgr update --self --all
sudo tlmgr paper a4
```

## インストール済みパッケージの更新

```zsh
sudo tlmgr update --self --all
```

# Ubuntu

```bash
sudo apt install texlive-full
```

# Windows

```powershell
choco install texli
```

---

# 参考文献

- [TeX Users Group](https://www.tug.org/texlive/doc/texlive-ja/texlive-ja.pdf)
  - [TeX Live](https://www.tug.org/texlive/doc/texlive-ja/texlive-ja.pdf)
    - [Installing TeX Live over the Internet](https://www.tug.org/texlive/acquire-netinstall.html)
      - [install-tl-windows.exe](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe)
    - [TeX Live ガイド](https://www.tug.org/texlive/doc/texlive-ja/texlive-ja.pdf)

- [TeX Wiki](https://texwiki.texjp.org/)

---

Copyright (c) 2023 YA-androidapp(https://github.com/YA-androidapp) All rights reserved.
