# HedgeLib and Puyo Text Editor development Docker image

![github actions workflow](https://github.com/kaszarobert/hedgelib_puyotexteditor_dev/actions/workflows/docker-image.yml/badge.svg)

Note: this is for development purposes, use [https://github.com/kaszarobert/hedgelib_docker](https://github.com/kaszarobert/hedgelib_docker) instead

A simple Docker image that builds [HedgeLib](https://github.com/Radfordhound/HedgeLib) and [Puyo Text Editor](https://github.com/nickworonekin/puyo-text-editor) from source for working with Sonic game based PAC (and other) files. The docker build takes about 270-300s.

Usage example:

```
docker container run -v $(pwd):/app --user $(id -u):$(id -g) kaszarobert/hedgelib_puyotexteditor_dev HedgeArcPack /app/text/text_common_en.pac /app/text_cnvrs2/text_common_en
```

```
docker container run -v $(pwd):/app --user $(id -u):$(id -g) kaszarobert/hedgelib_puyotexteditor_dev PuyoTextEditor /app/text_cnvrs2/text_common_en/ui_Menu.cnvrs-text -o /app/text_xml/text_common_en/ui_Menu.xml
```
