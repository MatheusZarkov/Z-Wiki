---
{"dg-publish":true,"permalink":"/03-ai/stable-diffusion/como-atualizar-a1111/","noteIcon":""}
---

Easy auto updates! In your folder right click on "webui-user.bat" And click edit. (I use notepad) Add git pull between the last to lines "Set" and "Call". Like bellow!

(--medvram --autolaunch) optional.  
Make bigger images with --medvram  
Auto lunch Web up with --autolaunch

```shell
set COMMANDLINE_ARGS= --medvram --autolaunch
git pull
call webui.bat
```

Depois retorna para 

```shell
@echo off

set PYTHON=
set GIT=
set VENV_DIR=
set COMMANDLINE_ARGS= --xformers --medvram

call webui.bat

```