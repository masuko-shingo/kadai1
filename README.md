# kadai1
2020年ロボットシステム学課題１デバイスドライバ
# 概要

上田先生のデバイスドライバmyled10.cをベースに一部改造しました。

改造した部分は、出力を行うGPIOピンをGPIO:25からGPIO:21に変更しています。

デバイスドライバとは関係ないのですが、第七～八回授業中に行ったsushiの表示するコードなどが残っています



# 動作環境
|||
|:--:|:--:|
| Raspberry Pi | Raspberry Pi Model 3B+ |
| OS | Ubuntu20.04 |

# 実行方法
```
$ git clone https://github.com/masuko-shingo/kadai1.git     //このリポジトリをローカルにクローンする
$ cd kadai1/myled/
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
$ echo 1 > /dev/myled0      //ledの点灯
$ echo 0 > /dev/myled0      //ledの消灯
```

# 回路図
![回路図ロボシス課題１](https://user-images.githubusercontent.com/72721963/101239901-aa4b0a80-372e-11eb-9ddb-fcbab11e1ce7.png)

# 動画
https://youtu.be/TRhwyz44XkY
# Copyright
Copyright © (Free Software Foundation, Inc.) 2020  Ryuichi Ueda + Shingo Masuko. 

This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
