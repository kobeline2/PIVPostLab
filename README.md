# PIVPostLab

PIVPostLab は MATLAB 用の PIV 後処理アプリです. PIV ソフトウェアが出力する X,Y,U,V,精度指標 を読み込み, 渦度,レイノルズ応力,速度ベクトル可視化 などの解析をワンクリックで実行します.

## 特長

* GUI で簡単操作.
* 渦度,レイノルズ応力,乱流強度 など基本統計量を自動計算.
* ベクトル場のカラーオーバーレイやストリームライン描画.
* バッチ処理で大量ファイルを一括解析.
* 解析結果を PNG,TIFF,Mat-file でエクスポート.

## 動作環境

* MATLAB R2021b 以降.
* Signal Processing Toolbox (レイノルズ応力計算に使用).
* Image Processing Toolbox (可視化に使用).

## インストール

1. 本リポジトリをクローンまたは ZIP ダウンロードして展開.
2. MATLAB で `addpath(genpath('PIVPostLab'))` を実行.
3. `pivpostlab` をコマンドウインドウで起動.

## 使い方

```matlab
% 例: ファイル読み込みと解析
app = pivpostlab;
app.loadData('piv_output.csv'); % X,Y,U,V,cc
app.computeVorticity;
app.computeReynoldsStress;
app.showVectorOverlay;
```

## フォルダ構成

```
PIVPostLab/
 ├─ src/            % コアクラスと関数
 ├─ ui/             % App Designer ファイル
 ├─ examples/       % サンプルデータ
 └─ docs/           % ドキュメント
```

## ライセンス

MIT License.

## 引用

研究成果を公表する際は, 以下を引用してください.

```
Koshiba T., PIVPostLab: MATLAB PIV Post‑Processing App, 2025, GitHub repository.
```
