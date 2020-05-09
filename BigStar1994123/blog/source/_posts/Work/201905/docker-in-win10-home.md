---
title: docker-in-win10-home
tags:
  - 工作
  - docker
category:
  - 工作日誌
date: 2019-03-08 16:45:42
---
# 應用 Docker 在 Win10 Home 版 #

Win10 Home 版因為沒有支援 Hyper-V  
所以 **Docker Desktop for Windows** 無法安裝  
[Docker Desktop for Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows)  
只有 Windows 10 Professinal or Enterprise 64-bit 才可以  

Home版只能安裝 Docker Toolbox 去模擬 Linux 環境跑 Docker  
安裝完畢後跑跑看新手教學  
[MsDoc: Use Docker](https://docs.microsoft.com/zh-tw/dotnet/core/docker/building-net-docker-images)  
最後執行 Localhost:5000 跑不起來  

最後找到解法  
必須先在模擬環境內下 `docker-machine ip` 取得IP位置  
先能正確的 Run 起來  
[StackOverflow: This site can't be reached](https://stackoverflow.com/a/44116869/5760789)