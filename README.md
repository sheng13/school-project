![school-project：機器學習課程 notebook 索引](docs/readme-banner.svg)

# school-project

機器學習與 AI 課程練習，包含一維梯度下降、MNIST 全連接網路，以及 MNIST／CIFAR-10 卷積網路。現有內容是 Python notebook 與一份 Colab 連結清單，不是打包好的應用程式。

## 練習索引

以下依程式內容整理，而非只依檔名判斷主題。

| 練習 | 檔案 | 內容與依賴線索 |
| --- | --- | --- |
| 一維梯度下降 | [Gradient_descent.ipynb](Gradient_descent.ipynb) | 對 `y=x²` 以導數 `2x` 更新位置；使用 NumPy 與 Matplotlib 繪圖 |
| MNIST 全連接網路 | [keras_mnist.ipynb](keras_mnist.ipynb) | 載入資料、查看影像與形狀、建立 Flatten／Dense 模型並訓練評估 |
| MNIST 卷積網路 | [keras_CNN_mnist.ipynb](keras_CNN_mnist.ipynb) | Conv2D／MaxPooling2D、one-hot 標籤、訓練曲線與 Pandas 混淆表 |
| 另一份 MNIST 卷積練習 | [Gradient_descen.ipynb](Gradient_descen.ipynb) | 雖以 `Gradient_descen` 命名，程式實際也是 MNIST CNN，並非前述一維梯度下降範例 |
| CIFAR-10 卷積網路 | [keras_CNN_Cifar10.ipynb](keras_CNN_Cifar10.ipynb) | 載入彩色影像、卷積模型、類別預覽與訓練曲線 |
| 外部筆記連結 | [AI目錄之下](AI目錄之下) | 純文字檔，收錄四個 Colab Drive 網址；不是目錄，也未逐一標註主題 |

## 如何閱讀與開啟

可先看梯度下降範例，再比較 MNIST 的全連接與卷積模型，最後閱讀 CIFAR-10。GitHub 可預覽 notebook，不需先建立執行環境。

若要自行操作，可用支援 Python 3 的 Jupyter 開啟檔案，或使用各 notebook 首格原有的 Colab 連結。先閱讀程式，再由上而下執行；TensorFlow／Keras 範例會透過資料集 API 下載 MNIST 或 CIFAR-10，訓練也會使用運算資源。外部 Colab Drive 連結的存取權與可用性，仍取決於原分享設定。

## 重跑前注意

- 儲存庫沒有鎖定套件版本或提供環境清單。程式同時使用 `from tensorflow import keras` 與獨立 `keras` 匯入，重跑前需確認兩者版本相容。
- 依各檔案內容，還會用到 NumPy、Matplotlib，以及部分 MNIST 範例中的 Pandas；本頁不假定某一套現成環境可直接重現全部練習。
- MNIST CNN 模型宣告 `(28, 28, 1)` 輸入，但載入資料後沒有明確補上通道維度；應核對資料形狀與所用 Keras 版本的行為。
- MNIST CNN 繪圖函式有 `validation` 圖例，但呼叫時傳入的是同一組訓練指標，且 `fit()` 沒有設定驗證資料；不要把圖例視為獨立驗證結果。
- 梯度下降範例的輸出註解不完全對應目前參數；閱讀時以程式設定為準。notebook 內保存的輸出也不代表已在你的環境重跑成功。

## 課程資料與權利

這些檔案是課程練習，不是 TensorFlow、Keras 或 Colab 官方教材，也沒有提供官方作業解答的證明。原 notebook 的 Colab 入口與連結清單均保留不變；連結存在不代表已確認外部內容或作者身分。

儲存庫未附獨立授權檔。使用 notebook、資料集或引用外部內容前，請分別確認其來源與使用條件，並保留原有署名及聲明。
