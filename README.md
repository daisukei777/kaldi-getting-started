# kaldi getting started
## Kalid Introduction

[Kaldi](https://github.com/kaldi-asr/kaldi)はC++で記述されたオープンソースの音声認識ツールキットであり、Apache License v2.0の下で自由に利用できます。Kaldiは、柔軟性と拡張性を備えたソフトウェアで音声認識のリサーチャーが使用することを目的としています。


## 環境構築 (Visual Studio Code Remote Development)
Visual Studio Code Remote Containerを使います。Kaldi開発環境をセットアップする必要もなく、VSCodeから直接Dockerコンテナ内にアクセスして開発することができます。

### 前提条件
1. Docker [[download here]](https://www.docker.com/products/docker-desktop)
2. Visual Studio Code [[download here]](https://code.visualstudio.com/)
3. Remote - Containers
[[download here]](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### 開発用コンテナの準備
[Docker Hub](https://hub.docker.com/r/kaldiasr/kaldi)にKaldiのイメージが公開されているのでそれを使います。



1. イメージをPullします。
```
docker pull kaldiasr/kaldi
```
2. CPUの場合、以下のコマンドでKaldiコンテナを起動します。
```
docker run -it kaldiasr/kaldi:latest
```
2. GPUの場合、以下のコマンドでKaldiコンテナを起動します。
```
docker run -it --runtime=nvidia kaldiasr/kaldi:gpu-latest
```

### 開発用コンテナの準備
[.devcontainer/devcontainer.json](../.devcontainer/devcontainer.json)にはVSCodeから開発コンテナーにアクセスする方法が定義されています。詳細は[こちら](https://code.visualstudio.com/docs/remote/devcontainerjson-reference)を参考にしてください。

ここではVS Codeを起動し、コマンドパレット（F1）またはクイックアクションステータスバー項目から[Remote-Containers: Open Folder in Container]コマンドを実行し、コンテナーをセットアップするプロジェクトフォルダーを選択します。もしくはクイックアクションステータスバー項目をクリックし、コンテナを設定するプロジェクトフォルダを選択します。


 ![dev](./images/remote-dev-status-bar.png "dev")


## References
### Official site
- [Kaldi](http://kaldi-asr.org/)
- [Kaldi for Dummies tutorial](http://kaldi-asr.org/doc/kaldi_for_dummies.html)

### English content
- [kaldi-yesno-tutorial](https://github.com/keighrim/kaldi-yesno-tutorial)
- [Kaldi Tutorial](https://eleanorchodroff.com/tutorial/kaldi/index.html)

### Japanese content
- [ここ10年の音声認識のアーキテクチャの変化を雑に整理する（前編）](https://qiita.com/corocn/items/81c255e5f742f767144f)
- [音声認識について噛み砕いてみた](https://qiita.com/dcm_katou/items/9ec80f7c714631f568bb)
- [Kaldiツールキットを用いた音声認識システムの構築](http://www.ts.ip.titech.ac.jp/demos/csjkaldisp2016oct.pdf)
- [CSJ用Kaldiレシピチュートリアル](http://www.ts.ip.titech.ac.jp/demos/csjkaldi/index.html) / [Kaldiツールキットを用いた 音声認識システムの構築](http://www.ts.ip.titech.ac.jp/demos/csjkaldisp2016oct.pdf)
