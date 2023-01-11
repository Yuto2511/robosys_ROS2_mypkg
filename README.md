# robosys_ROS2_mypkg

![test](https://github.com/Yuto2511/robosys_ROS2_mypkg/actions/workflows/test.yml/badge.svg)

千葉工業大学　未来ロボティクス学科 2022年度 ロボットシステム学の講義で作成したROS2のパッケージ

## 動作確認済み環境

- Ubuntu22.04
- ROS2 Humble

## インストール

- このリポジトリをクローンしてビルドする.  

  ```shell
  cd ros2_ws/src
  git clone https://github.com/Yuto2511/robosys_ROS2_mypkg.git
  cd ~/ros2_ws
  colcon build
  source ~/ros2_ws/install/setup.bash
  source ~/ros2_ws/install/local_setup.bash
  
  ```

## 使い方


```shell
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/yuto/.ros/log/2023-01-11-14-04-14-821744-TABLET-OP0EEJ3K-991
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [992]
[INFO] [listener-2]: process started with pid [994]
[listener-2] [INFO] [1673413455.829577712] [listener]: Listen: 0
[listener-2] [INFO] [1673413456.306811148] [listener]: Listen: 1
[listener-2] [INFO] [1673413456.806858932] [listener]: Listen: 2
[listener-2] [INFO] [1673413457.306885299] [listener]: Listen: 3
[listener-2] [INFO] [1673413457.806686048] [listener]: Listen: 4
[listener-2] [INFO] [1673413458.306852696] [listener]: Listen: 5
[listener-2] [INFO] [1673413458.806966797] [listener]: Listen: 6

```

## 説明

![rqt graph](img/rqt_graph.png)

- /talker  
  - Int16型で0.5秒おきに、+1カウントアップしその値を、/countupへ送信するノード.
- /listener  
  - /countupに来たメッセージをコンソールに表示するノード.


## ライセンス

- このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
- © 2022 Yamaguchi Yuto
