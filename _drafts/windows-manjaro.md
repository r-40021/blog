---
layout: post
categories: PC
tags:
- Linux
- Manjaro
- Windows
title: Windows ユーザーが Manjaro に乗り換えて感じたメリット・デメリット
image: "/blog/assets/images/2022/06/23/manjaro-gnome.jpg"
headAlt: Manjaro のデスクトップ
copylight: ''

---
先日、メインPCのOSを、WindowsからManjaroに変えました。2週間ほど使ってみて感じたメリットとデメリットを紹介します。

## Manjaroとは？

ここでは説明を割愛しますが、今人気のLinuxディストリビューションです。

導入のハードルが富士山よりも高い(個人の感想です)Arch Linuxを簡単に扱えるようにしたのが特徴です。

## PCスペック

Core i5 1135G7

8GB RAM

256GB PCIe SSD

良くも悪くもない、普通のスペックです。

Windows 11も余裕で動くのですが、開発でDockerを使うとメモリが枯渇する問題があったため、「じゃあメモリを食わないLinuxに移行しよう！」となりました。

## メリット5つ

### メモリ使用量が少ない

「重い」と言われるGNOMEを使用していますが、Firefoxでこのブログ原稿を書いている最中でもメモリは2.5GBしか消費していません。

起動直後では1.5GBを切ることもあります。

Windowsはメモリに余裕がある場合には予め多めにメモリを確保しておく性質があるため単純な比較はできませんが、同じような状況だとWindows 11では5GBは消費します。

また、開発で仮想環境を立ち上げても、Windowsの場合はWSLを経由する必要があるのであっという間にスワップしますが、ManjaroではホストOS自体がLinuxであるため、全体で5GBほどしか消費しません。

### 軽い

そもそもPCのスペックがそれなりにあるのでWindowsとの差はあまり感じませんが、確かに動作のカクつきがほとんどないように感じます。

Windowsではスタートメニューを開く際に若干カクつくことがありました。(特に起動直後)

それがManjaroではほとんどありません。

また、ブラウザの性能を測れるSpeedometer 2.0を実行したところ、あのFirefoxですら