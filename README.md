# ファイナンス機械学習
![表紙](https://images-na.ssl-images-amazon.com/images/I/61u3hc9ySpL._SX355_BO1,204,203,200_.jpg)
- [Amazon](https://www.amazon.co.jp/%E3%83%95%E3%82%A1%E3%82%A4%E3%83%8A%E3%83%B3%E3%82%B9%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E2%80%95%E9%87%91%E8%9E%8D%E5%B8%82%E5%A0%B4%E5%88%86%E6%9E%90%E3%82%92%E5%A4%89%E3%81%88%E3%82%8B%E6%A9%9F%E6%A2%B0%E5%AD%A6%E7%BF%92%E3%82%A2%E3%83%AB%E3%82%B4%E3%83%AA%E3%82%BA%E3%83%A0%E3%81%AE%E7%90%86%E8%AB%96%E3%81%A8%E5%AE%9F%E8%B7%B5-%E3%83%9E%E3%83%AB%E3%82%B3%E3%82%B9%E3%83%BB%E3%83%AD%E3%83%9A%E3%82%B9%E3%83%BB%E3%83%87%E3%83%BB%E3%83%97%E3%83%A9%E3%83%89/dp/4322134637)
- ノート
  - https://docs.google.com/document/d/18a4L_hgwFPBYkIX-6pwpFrO2sMYXOe5pOHtBuprdaUI/edit?usp=sharing

## github




- GitHub では既存の Repository を Template として、新しい Repository を作成することができる
  - https://dev.classmethod.jp/articles/github-template-repository/

## Python のバージョン

- Mac OS python 3.7.4 で動作確認
- pyenv により、python のバージョンを変更する
  - https://qiita.com/Kohey222/items/19eb9b3cbcec9b176625

## 仮想環境の設定

- 仮想環境名

  - env-tensorflow-project-template-TODO-change-this-name
    - setup.sh

- venv: Python 仮想環境管理
  - https://qiita.com/fiftystorm36/items/b2fd47cf32c7694adc2e

```
$ python3 -m venv [newenvname]
$ source [newenvname]/bin/activate
$ ([newenvname])\$ deactivate
```

## Jupyter の設定

- Jupyter で複数カーネルを簡単に選択するための設定

  - https://qiita.com/tomochiii/items/8b937f15c79a0c3eae0e

```
# 利用可能なカーネルの表示
$ jupyter kernelspec list

# 仮想環境をアクティベート
$ source [newenvname]/bin/activate
# カーネルを追加
$ ipython kernel install --user --name=[newenvname] --display-name=[newenvname]
```

- カーネルを削除

```
$ jupyter kernelspec uninstall [newenvname]
```

- JupyterLab のターミナルフォントを変更する

  - https://thr3a.hatenablog.com/entry/20190916/1568618516

  1. 上のメニューバーより「Setting」→「Advanced Settings Editor」をクリック
  2. 左がデフォルト設定値一覧で、右にユーザーがオーバーライドしたい設定を JSON で記述する。
  3. User Preferences に以下を追記する。

```
{
    "fontFamily": "Monaco"
}
```

## graphviz のインストール

- tf.keras.utils.plot_model(model, show_shapes=True) で必要

```
brew install graphviz
```

## dataset

- TensorFlow で使えるデータセット機能が強かった話
  - https://qiita.com/Suguru_Toyohara/items/820b0dad955ecd91c7f3
