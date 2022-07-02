---
layout: post
categories: PC
tags:
- Linux
- Manjaro
copylight: ''
title: Manjaro と Xubuntu をデュアルブートしたら Karnel Panic になった！！！
image: "/blog/assets/images/2022/06/23/manjaro-gnome.jpg"
headAlt: Manjaroのデスクトップ画面

---
Xubuntuは起動するのにManjaroくんが起動しない…

## 現象

実は最近、ManjaroでWi-Fiにうまく接続できない状態になっていまして、問題の切り分けの一環としてXubuntuをデュアルブートしました。

その結果、Xubuntuは起動するもののManjaroがKarnel Panicとなって起動しなくなりました。

## 解決法

まず、grubメニューで「Advanced options for Manjaro」を選択します。

(スクショなくてすみません)

その後、"fallback"という文字が含まれるカーネルを選択し、Enterキーで起動します。

これで起動したら、ログインしてターミナルを開きます。

まず、`lsblk -l`コマンドを実行してディスクの状況を調べます。

    [user@mainpc ~]$ lsblk -l
    NAME      MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
    nvme0n1   259:0    0 238.5G  0 disk 
    nvme0n1p1 259:1    0   300M  0 part /boot/efi
    nvme0n1p2 259:2    0 192.5G  0 part /
    nvme0n1p3 259:3    0  45.6G  0 part