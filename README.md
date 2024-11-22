
# 概要<img src="https://github.com/Ruprous/LineUp-Images/blob/main/lineupimage.png" alt="サンプル画像" width="50">  
  
このツールは、指定したディレクトリ内の画像を横幅3000px固定で並べるアプリケーションです。画像間にマージンを設定でき、列数や画像のリサイズ方法も柔軟に指定可能です。ディレクトリの選択と保存先の指定はGUI（エクスプローラー）で行うことができ、背景色は透明または黒を選択できます。出力はPNG形式で保存されます  
<img src="https://pbs.twimg.com/media/Gc-F8KGaAAE4D2u?format=png&name=900x900" alt="サンプル画像" width="300">
<img src="https://pbs.twimg.com/media/Gc-F9osaAAQR4o5?format=jpg&name=4096x4096" alt="サンプル画像" width="300">  
これが→こう!!



---

## 必要な環境

### EXEを利用する場合
- **OS**: Windows 10 以降
- **Pythonのインストールは不要**

### Pythonスクリプトを利用する場合
- **Python 3.8以上**
- 以下のPythonライブラリが必要です:
  - `Pillow`
  - `tkinter`（Python標準ライブラリ）

ライブラリをインストールするには、以下のコマンドを使用してください:
```bash
pip install pillow
```

---

## 使い方

### **1. EXEを利用する場合**
1. **EXEファイルをダブルクリック**
   - `LineUp-Images.exe` をダブルクリックで実行。
2. **入力内容**
   実行後に以下の操作が求められます：
   - **ディレクトリ選択**: エクスプローラーが表示され、画像ファイルが格納されているフォルダを選択します。
   - **保存先とファイル名の指定**: エクスプローラーで保存先フォルダとファイル名を選択します（拡張子は`.png`）。
   - **背景の選択**: 背景を透明にするか黒にするかを選択します。
       - `yes`: 背景を透明に設定。
       - `no`: 背景を黒（`#000000`）に設定。
   - **横に並べたい画像の数（列数）**: 横に並べる画像の数を入力します。
   - **画像と画像の間のマージン（px）**: 各画像間のスペースをピクセル単位で入力します（0〜300の範囲）。

---

### **2. Pythonスクリプトを利用する場合**
1. **スクリプトを実行**
   - ターミナルまたはコマンドプロンプトで以下を実行してください:
     ```bash
     python LineUp-Images.py
     ```
   または、`run.bat` をダブルクリックして実行することも可能です。

2. **入力内容**
   - EXE版と同様に操作。

---

## 出力
- 処理が完了すると、指定した保存先に画像が保存されます。

---

## 注意点

1. **ディレクトリ内の画像形式**
   - サポートされている画像形式:
     - `.jpg`, `.jpeg`, `.png`, `.bmp`, `.gif`
   - 他の形式のファイルは無視されます。

2. **マージンの制限**
   - マージンは `0〜300px` の範囲内で指定してください。

3. **画像サイズ**
   - 各画像は指定された列数とマージンに基づいて正方形にリサイズされます。
   - 元画像のアスペクト比は維持され、不足部分には設定した背景色が追加されます。

---

## 実行例

### ディレクトリ構成
```plaintext
images/
├── image1.jpg
├── image2.png
├── image3.jpeg
└── image4.bmp
```

### EXE実行例
1. `LineUp-Images.exe` をダブルクリック。
2. エクスプローラーが表示され、`images/` ディレクトリを選択。
3. エクスプローラーが表示され、保存先フォルダとファイル名を選択（例: `result.png`）。
4. ターミナルで以下のように入力を求められます：
   ```plaintext
   背景を透明にしますか？(yes/no): yes
   横に並べたい画像の数（列数）を入力してください: 3
   画像と画像の間のマージン（px）を入力してください（0〜300の範囲）: 20
   ```

### Pythonスクリプト実行例
同様の流れで操作可能です。

---

## ファイル内容
- `LineUp-Images.exe`: EXE形式の実行ファイル
- `LineUp-Images.py`: ソースコード
- `run.bat`: Pythonスクリプトを簡単に実行するバッチファイル
- `LICENSE`: ライセンス情報
- `README.md`: このファイル
