McuComm
=======
　PWM方式のサーボモータを制御するためのコンポーネントです。

コンポーネントの仕様
--------------------
　このコンポーネントはInPortをMotionLoader、ヒューマンインターフェイス、またはそれに準ずるコンポーネントからコマンドを受け取ります。  
　そのコマンドをPWM方式のサーボモータに沿ったをものに変換をし、シリアルポートから出力。  
　マイコンで読み取り、PWMに変換することでサーボモータを制御します。  

[![画像1][image1]](https://github.com/downloads/s-ryuki/Pictures/McuComm_Comm.png)
[image1]:https://github.com/downloads/s-ryuki/Pictures/McuComm_Comm.png

　sensorからはマイコンに接続されているセンサの値が出力されます。  
　提供するプログラムはmbed NXP LPC1768ですが、McuCommの通信プロトコルに沿ってPWMを出力できればどのようなマイコンでも使用可能です。  
　McuCommのShell上には送信したID、TergetPosition、Timeが表示されます。
