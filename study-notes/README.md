# Blender Study Notes<a id="TOP"></a>

### <b>index</b>

[QuestでVR再生](#220601) | [階層構造の設定](#220602)
***


<a name="220601"></a>
# <b>QuestでVR再生</b>

1. [Oculus Link](https://github.com/mubirou/Unity3D/tree/master/study-notes#oculus-link%E3%81%AE%E6%BA%96%E5%82%99) の準備をする
1. [モデリング](https://github.com/mubirou/Blender/tree/master/introduction#014-%E3%83%86%E3%82%AF%E3%83%8B%E3%83%83%E3%82%AF%E3%83%92%E3%83%B3%E3%83%881)を行う
1. [Blender]-[オブジェクトモード]-[追加]-[**カメラ**]（位置＝VR視点を調整）
1. [Blender]-[編集]-[プレファレンス]-[アドオン]-[🔎"VR"]-[**✓ 3D View: VR Scene Inspection**] を選択
1. [VR]-[ビューポートフィードバック]-[**VRコントローラーを表示**] を **✓**
1. [VR]-[VRセッション]-[**▶ Start VR Session**]

* コントローラの操作方法
    * 右ジョイスティック：回転･垂直
    * 左ジョイスティック：水平･前後
    * A or X：高さを初期値に戻す
    * 左右の中指トリガー：拡大縮小
    * レイキャスト選択：ジャンプ

参考：[ITA3channel](https://www.youtube.com/watch?v=V6twUh5qMr8)  
参考：[S.Fuka(S.Haruya)](https://zenn.dev/sfuka/scraps/af95feae08b3ec)  
実行環境：Blender 3.2.0、Windows 10、Meta Quest 40.0、Oculusアプリ  
作成者：夢寐郎  
作成日：2022年06月19日  


<a id="220602"></a>
# <b>階層構造の設定</b>

1. オブジェクトを複数作成
1. [オブジェクトモード] にする
1. [Shift] キーを押しながら階層構造をつくりたいオブジェクトを選択
1. **最後に"親"にしたいオブジェクトを [Ctrl] キーを押しながら選択**
1. [**オブジェクト**]-[**ペアレント**]-[**オブジェクト**] を選択

（階層例）  
　  ├ 立方体  
　  │   └ 立方体.001  
　  │      └ 立方体.002  

実行環境：Blender 3.2.0、Windows 10  
作成者：夢寐郎  
作成日：2022年06月21日  
[[TOP]](#TOP)


<a id="XXX"></a>
# <b>XXXXX</b>

1. XXX
    ```c#
    XXXX
    ```
    * XXX
    * XXXX

実行環境：Blender 3.2.0、Windows 10  
作成者：夢寐郎  
作成日：202X年XX月XX日  
更新日：202X年XX月XX日  
[[TOP]](#TOP)


© 2022 夢寐郎