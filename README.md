# ROS(課題2）
・このパッケージは2021年度、ロボットシステム学の第10回の授業内で上田先生が作成したROSのパッケージを改良したものである。  

# 機能
・scriptsの中にあるcount.pyは値を0から1秒間に1ずつ増やしていくプログラミングです。また、twice.pyはcount.pyの値を2倍、fourtimes.pyはcount.pyの値を4倍、sixtimes.pyはcount.pyの値を6倍、eighttimes.pyはcount.pyの値を8倍、tentimes.pyはcount.pyの値を10倍としていくプログラムです。

# 動作環境  
・Raspberry pi 4 model B  
・OS: ubuntu 20.04.3 LTS  

# 必要なもの  
・Raspberry pi 4 model B  
・ubuntuを複数動作させることができる環境  

# 準備
・このプログラムを実行するにはROSのインストールとワークスペースの構築が必要です。私は上田先生のロボットシステム学の第10回の授業スライドを参考にしながら環境を構築しました。パッケージを動かすためには、上田先生のロボットシステム学の第10回の授業スライドの9ページ目までに書いてあることを実行してください。  

参考にした上田先生の第10回の授業スライド(https://ryuichiueda.github.io/robosys2020/lesson10_ros.html#/)  

# 動作方法(1)
まず、次のようなコマンドを実行し、ディレクトリを移動します。  
`$ cd ./catkin_ws/src`  

そしたら、(https://github.com/Takuya0510/mypkg) に置いてある、scriptsのファイルを./catkin_ws/srcのディレクトリの中にクローンします。   

次に、次のようなコマンドを実行します。  

`$ roscore `  
`$ chmod +x count.py`  
`$ chmod +x twice.py`  
`$ chmod +x fourtimes.py`  
`$ chmod +x sixtimws.py`  
`$ chmod +x eighttimws.py`  
`$ chmod +x tentimws.py`  

(※　ここから先は動作方法(2)でも実行できます。)  

・count.pyを実行する為に、次のコマンドを実行します。  
`$rosrun mypkg count.py`  
そしたら、値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /count_up`  

・以下のプログラムを実行するためには先にcount.pyを実行しておく必要があります。  

・twice.pyを実行する為に、次のコマンドを実行します。  
`$rosrun mypkg twice.py`　　

そしたら、値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /twice`  

・fourtimes.pyを実行する為に、次のコマンドを実行します。  
`$rosrun mypkg fourtimes.py`  
そしたら、値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /fourtimes`  

・sixtimes.pyを実行する為に、次のコマンドを実行します。  
`$rosrun mypkg sixtimes.py`  
そしたら、値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /sixtimes`  

・eighttimes.pyを実行する為に、次のコマンドを実行します。  
`$rosrun mypkg eighttimes.py`  
そしたら、値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /eighttimes`  

・tentimes.pyを実行する為に、次のコマンドを実行します。  
`$rosrun mypkg tentimes.py`  
そしたら、値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /tentimes`  

# 動作方法(2) 
動作方法(1)の(※)の部分まで実行します。  
そしたら、次のコマンドを実行します。
`$roslaunch mypkg mypkg.launch`  
このコマンドを打つことで、動作方法(1)ではそれぞれ一つずつ立ち上げていましたが、一度ですべて立ち上げ、実行することができます。  

値を確認する方法

・count.pyの値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /count_up`  

・twice.pyの値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /twice`  　

・fourtimes.pyの値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /fourtimes`  　

・sixtimes.pyの値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /sixtimes`  　

・eighttimes.pyの値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /eighttimes`  　　

・tentimes.pyの値を確認するために別の端末から、次のコマンドを実行します。  
`$ rostopic echo /tentimes`  

# ライセンス
BSD 3-Clause "New" or "Revised" License  

# 実行動画
Youtube
[ROSのパッケージ (課題2)](https://youtu.be/fiGVqHU35II)
