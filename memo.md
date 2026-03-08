# memo

## directory structure
``` bash
  projectDir/
   ├─ Assets/                     
   │   ├─ SourceFiles/
   │   │    ├─ Scripts/
   │   │    │    ├─ ThirdPersonController.cs
   │   │    │    ├─
   │   │    │    ├─
   │   │    ├─ StarterAssets/
                 └─ ThirdPersonController/
                      └─ Character
                           ├─ Animations #アニメーション用のデータ群。 JumpやStand などの*.fbx(バイナリファイル)が入っている
                           └─ Models                
   │   ├─ Prefabs # ゲーム内オブジェクトの設定ファイルを入れておくフォルダ
   │   │    ├─ PlayerRobot.prefab                
   ├─ Packages/
   │   ├─       
   │   ├─ 
   │   └─   
   ├─ ProjectSettings/
   │   ├─ 
   │   ├─ 
   │   ├─ 
   │   ├─ 
   │   └─
   │                       # 上3つが必須の要素。これらがあれば build と run ができる
   ├─
   └─
```

## ロジック

+ Main()メソッド(エントリポイント)は、Unityエンジン内に記述されているのでUserが明示的に記述することはない。
  Unityはイベント駆動型であり以下のループを回す
  ``` bash
  while (ゲーム実行中)
  {
    入力処理
    物理計算
    スクリプト更新
    描画
  }
  ```


## Editor
+ Projectウィンドウで「Assets」→「Scenes」→「<Scenename>」でSceneウィンドウに編集中のSceneが表示される
+ 「Assets」→「Prefabs」→「PlayerRobot」をクリックした後に「Hierarchy」ウィンドウで PlayerRobot を構成するパーツ(ArmとかEyeとかLegとか)がネストで表示される
+  同じく, ネスト中の「Robot」を選択すると、InspectorにPlayerRobotオブジェクトにアタッチされているスクリプトが一覧表示される

## tips
+ `*.fbx` は3Dアニメーションファイル。キャラクターのモーションデータ。Autodesk FBX (Filmbox)の略。BlenderやMaya, Mixamoなどの3Dツールで作ったアニメーションをFBXで読み込む。
+ `.*fbx`アニメーションファイルは事前に外部の3Dツールを用いて作成したものをUnityにImportしたもの。
 
## Deploy
