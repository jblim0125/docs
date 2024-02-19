---
layout: post
title: VIM with python3 on Mac
author: jblim0125
date: 2024-02-16
category: 2024
---

# Mac Manually install VIM with supporting Python3

## 1. python3 alias 설정 
사용하고 있는 쉘에 다음을 설정 `.zsh` or `.bash_profile`
```shell
alias python="python3"
```
## 2. homebrew 을 이용해 vim 설치  
```shell
$ brew install vim
```
## 3. vim alias 설정  
Mac 기본 `VIM` 위치 `/usr/bin/vim`  
homebrew 이용해 설치한 `VIM` 위치 `/usr/local/bin/vim`  
```shell
alias vim=/usr/local/bin/vim
```
Please restart Your Mac, restart Your Terminal and reenter your terminal!!!

then, we need to checkout whether that Homebrew`VIM` supports `Python3` or Not:
```shell
$ vim --version | grep python
output:
    +conceal           +linebreak         +python3           +visual
```