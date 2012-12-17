McuComm
=======
　PWM方式のサーボモータを制御するためのコンポーネントです。  
　PWM方式のサーボモータをコマンド式サーボモータと同じように扱うことができます。  
　マイコンを中継する必要があります。  

コンポーネントの仕様
--------------------
　このコンポーネントはInPortをMotionLoader、MotionEditorまたはそれに準ずるコンポーネントからコマンドを受け取ります。  
　そのコマンドをPirkus社製のコマンド式サーボモータに沿ったをものに変換をし、シリアルポートから出力。  
　マイコンでコマンドを読み取り、PWMに変換することでサーボモータを制御します。  

　　　[![画像1][image1]](https://github.com/downloads/s-ryuki/Pictures/McuComm_Comm.png)
[image1]:https://github.com/downloads/s-ryuki/Pictures/McuComm_Comm.png

　sensor(OutPort)からはマイコンに接続されているセンサの値が出力されます。  
　提供するプログラムはmbed NXP LPC1768ですが、McuCommの通信プロトコルに沿ってPWMを  
　出力できればどのようなマイコンでも使用可能です。  
　McuCommのShell上には送信したID、TergetPosition、Timeが表示されます。  
　提供したマイコンプログラムは[こちら](http://mbed.org/users/matsu/code/mbed-for-McuComm/)です
　  
使用方法
--------
　　　(1)使用するPCとロボットを接続します。  
　　　(2)COM番号を確認し、mcu.iniの「port」を編集します。  
　　　(3)mcu.iniのその他の情報を編集し、保存します。  
　　　(4)Mcu_Comm.pyを起動します。  
　　　(5)「モーション編集モード」で使用する場合はInPortをMotionEditorに、  
　　　　　「モーション再生モード」で使用する場合はInPortをMotionLoaderに繋ぎます。
　  
　使用するサーボモータの個数やサーボモータの可動域情報は、iniフォルダ内のmcu.iniで変更します。  

　　　　[![画像2][image2]](https://github.com/downloads/s-ryuki/Pictures/McuComm_ini.png)
[image2]:https://github.com/downloads/s-ryuki/Pictures/McuComm_ini.png
####　　　画面説明####
　　　　　　①使用するCOMポート  
　　　　　　②通信ボーレート    
　　　　　　③タイムアウト  
　　　　　　④センサ値の個数  
　　　　　　⑤サーボモータの個数  
　　　　　　⑥サーボIDに対応する番号  
　　　　　　⑦Shellにセンサ値を表示する/しない  
　　　　　　⑧サーボモータの可動域および角度数値のオフセット[/0.1deg]
