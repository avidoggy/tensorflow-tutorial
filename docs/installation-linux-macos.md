# 安裝

本教學文主要著重在個人學習成長上，所以使用到的資料集也相對的不會很大，故 GPU 的部分就跳過了。

## MacOS

MacOS 只要先確認有透過 [Brew](https://brew.sh/) 或 [MacPorts](https://www.macports.org) 安裝了 [wget](https://www.gnu.org/software/wget/) 即可跟 Linux 一樣安裝！

## Linux

- 確認 Python

  ```bash
  $ python --version
  Python 2.7.10
  ```

- 安裝 Pip - [官方安裝教學](https://pip.pypa.io/en/stable/installing/)

  ```bash
  # 從 pip 官網取得安裝腳本
  $ wget https://bootstrap.pypa.io/get-pip.py

  # Install to the user site
  $ python get-pip.py --user

  # 確認 pip
  $ pip --version
  pip 9.0.1 from <Pip 安裝位置>
  ```

- 作者個人偏好保持系統乾淨，所以 [virtualenv](https://virtualenv.pypa.io/en/stable/) 就請各位自行決定是否需要安裝
  - virtualenv is a tool to create isolated Python environments.

  ```bash
  $ pip install virtualenv

  # 建立一個專屬於 TensorFlow 的虛擬環境
  $ mkdir tensorflow-virtualenv
  $ cd tensorflow-virtualenv
  $ virtualenv .virtualenv  # 名字可以自取

  # 啟動虛擬環境
  source .virtualenv/bin/activate

  # 關閉虛擬環境
  $ deactivate

  # 作者習慣偷懶，因為 .virtualenv/bin/activate 不是那麼好打
  $ ln -s .virtualenv/bin/activate activate-virtualenv
  # 所以現在我們可以直接
  source activate-virtualenv
  ```

- 安裝 TensorFlow - [官方安裝教學](https://www.tensorflow.org/install/)

  ```bash
  # Python 2.7; CPU support (no GPU support)
  $ pip install tensorflow
  ```

- 安裝 Jupyter (選配：Coding 的 IDE 看個人喜好) - [官方安裝教學](http://jupyter.org/install.html)

  ```bash
  $ pip install jupyter

  # 啟動 Jupyter
  $ jupyter notebook

  # 若要關閉 Jupyter，請直接 ctrl + x 終止他即可
  ```
