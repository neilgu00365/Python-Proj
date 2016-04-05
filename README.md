  
##pythonをインストール  
###1.pythonをインストールする    
公式からダウンロードをしインストール、依存ライブラリなどをその都度導入するのは非常に大変なのであらかじめパッケージされたものを使う。  
今回はubuntu、windowsともに[Anaconda](https://www.continuum.io/downloads)というディストリビューションを使う。  
DOWNLOAD FOR FREE のところに行き、対応するOSの使いたいpythonのバージョンを選ぶ。(今回ではpython3を使うことが目的なので、3.Xの方を選ぶ。)  
ダウンロードが済んだら、インストールをする。  
windowsはインストーラ形式なので実行し、すべてに対し肯定の選択肢を取るとインストールが終わる。
ubuntuは端末から  
$bash Anaconda3-2.4.1-Linux-x86_64.sh  
みたいに打ち込み、肯定のの選択肢を取り続けるとインストールが終わる。  
これが終わると取りあえずpythonが使えるようになる。  

###2.OpenCV3.0をインストールする  
windowsの場合  
ここに行き、自分のバージョンにあったOpenCVのwhlファイルを探しダウンロードする。  
コマンドプロンプトを開き、  
pip install ダウンロードしたファイルと打ち込む。  

ubuntuの場合ターミナルを開き、次を打ち込む。  
condaをパスに追加する：　　
PATH=$PATH:$HOME/anaconda/bin  
再起動させずに即時反映させるには、下記のコマンドを実行する。  
$source ~/.profile  
$conda install --channel https://conda.anaconda.org/menpo opencv3  

$conda create -n opencv numpy scipy scikit-learn matplotlib python=3  
$source activate opencv  
$conda install -c https://conda.binstar.org/menpo opencv3  
$python3
>>>import cv2   
>>>print(cv2.__version__)  
>>>exit()  

おしまい  
