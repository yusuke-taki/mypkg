# リポジトリの概要
<ロボットシステム学　課題２>  
第10回で作成したROSのパッケージをベースに、オリジナリティーある改造をして、GitHubに置いてください。ROSで何か（必ずしもハードウェアである必要はありません）を動かしている様子をビデオに撮影してYouTubeに公開してください。第9回の内容も考慮し、リポジトリにはライセンスや著作権の記述もしてください。ROSの設定ファイルにもライセンスを記述する箇所がありますので、ご注意ください。
_ _ _
# 実装内容
今回の課題２はROSの授業についていくので精一杯だったので、上田先生が作成したROSのパッケージを自分できちんと動かせるかを試しました。
_ _ _
# 動作環境  
・Raspberry Pi 4 Model B(8G)    
・Ubuntu 20.04.1 LTS  
・ROS Noetic
_ _ _
# インストール方法
**・ROS**    
[ros_setup_scripts_Ubuntu20.04](http://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server)をもとにROSの環境構築をします。  

**・ワークスペース**     
[ロボットシステム学第１０回](https://ryuichiueda.github.io/robosys2020/lesson10_ros.html#/)をもとにワークスペースを作成します。  

**・パッケージ**  
以下のコマンドを実行して、パッケージをクローンします。   
`$ cd ~/catkin_ws/src`  
`$ cd clone https://github.com/FujitaRyo/mypkg`  
catkin_makeを使用して、本パッケージをビルドします。  
`$ cd ~/catkin_ws`  
`$ catkin_make`  
`$ source ~/.bashrc`  
_ _ _
# 実行方法  
端末１  
`$ roscore`  

端末２   
`$ rosrun mypkg count.py` or `rosrun mypkg twice.py`  

端末３  
`$ rosnode list`と`$ rostopic list`でノードとトピックを確認します。  
`$ rostopic echo /count_up` or `$ rostopic echo /twice`でデータを取り出します。　
_ _ _
# デモ動画  
・count.py  
https://www.youtube.com/watch?v=di_exuS_x94  
・twice.py  
_ _ _
# 参考著者  
[Ryuichi Ueda](https://github.com/ryuichiueda)
_ _ _
# ライセンス
BSD 3-Clause License
