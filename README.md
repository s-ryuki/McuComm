McuComm
=======
　PWM方式のサーボモータを制御するためのコンポーネントです。  
InPortをMotionLoaderとつなぐことによって、HumanInterface、またはそれに準ずるコンポーネントからの  
コマンド通りにサーボモータを制御することが可能です。
　私たちの実験ではMcuCommから出力されるコマンドをmbed NXP LPC1768で読み取り、  
PWMに変換して使用しました。McuCommのOutPortからTimedLongSeq型で出力されるコマンドを読み取ることができれば、  
他のマイコンでも使用することが可能です。
　McuCommのShell上にはID、TergetPosition、Timeが表示されます。
