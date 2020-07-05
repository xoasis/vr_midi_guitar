# vr_midi_guitar
VR Midi Guitar Project

MidiギターをVRで実現しようというプロジェクトです。

◇　開発パート

1. Valve Index Controller Input/Code Mapping
2. Code to Avator Index Guitar Animation
3. Stroke collision sound play

◇　概要

1. Valve Index Controller Input/Code Mapping

Valve Index ControllerからのSkelton入力の指の形を決めて、それに対しての再生するコード(C/C7/Cm等)を決定するユーザーインターフェースの部分です。
ここで決定したコードを2.と3.に渡します。

2. Code to Avator Index Guitar Animation

1.から渡されたコードに応じて、持っている楽器のコードをアバターにギター演奏させる部分です。
当プログラムを使用している際、アバターの上半身(どこまで制御を受けるべきかは恐らく楽器によって異なる)
はコントローラの位置などを無視して、このアニメーションに従います。

ギター以外の楽器も弾けるように出来たらいいと思いますが、当プロジェクトのスコープではギターとします。

3. Stroke collision sound play

1.で設定されたコードに対して、6本の弦にコリジョンとなる「ピック」が当たった際に、音を発生させる仕組みを実装します。
ピックが衝突した時の強さ（速さ）に応じて、音量を変えるのが要件になります

◇　未定の部分

再生する音をどうするかは未定です。
動的に音を生成するライブラリをサポートする形が良いと思いますが、評価が必要です。
専門家の助言をお待ちしております。
