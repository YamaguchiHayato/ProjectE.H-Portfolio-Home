<link rel="stylesheet" href="style.css">

# ELEMENTAL HUNTERS  
## 最大4人で遊べる2D視点アクションゲーム

<a href="Image/title.png" target="_blank">
<img src="Image/title.png" width="100%">
</a>

## Image 01: タイトル画面

<br>

## 目次  
- ## 0. [README](#0-readme)
  ## &emsp; 0-1.[PV](#part0-1)
  ## &emsp; 0-2.[ゲーム紹介スライド](#part0-2)
  ## &emsp; 0-3.[技術紹介スライド](#part0-3)

- ## 1. [プロフィール](#1プロフィール)
- ## 2. [作品概要](#2作品概要)
- ## 3. [チーム構成と担当箇所](#3チーム構成と担当箇所)
  ## &emsp; 3-0.[開発チーム構成](#part3-0)
  ## &emsp; 3-1.[担当箇所](#part3-1)

- ## 4. [ゲームの特徴](#4-ゲームの特徴)
  ## &emsp; 4-1[ゲームの特徴](#part4-1)

- ## 5. [操作方法](#5-操作方法)
  ## &emsp; 5-1.[基本操作](#part5-1)
  ## &emsp; 5-2.[攻撃方法](#part5-2)
  ## &emsp; 5-3.[復活システム](#part5-3)
  ## &emsp; 5-4.[攻撃アクション集](#part5-4)

- ## 6.[キャラクター紹介](#6-キャラクター紹介)
  ## &emsp; 6-1.[PV](#part6-1)
  ## &emsp; 6-2.[SwordCharacter](#part6-2) 
  ## &emsp; 6-3.[HammerCharacter](#part6-3)
  ## &emsp; 6-4.[WandCharacter](#part6-4)
  ## &emsp; 6-5.[TwinGunCharacter](#part6-5)

- ## 7.[技術的工夫点](#7技術的工夫点)
  ## &emsp; 7-0.[こだわった箇所](#part7-0)
  ## &emsp; 7-1.[キャラクター共通基盤の設計](#part7-1)
  ## &emsp; 7-2.[階層型ステートパターンの導入によるアクション管理](#part7-2)
  ## &emsp; 7-3.[テーブルによるコンボ/攻撃ステータス管理](#part7-3)
  ## &emsp; 7-4.[旧式入力システムと新式入力システム](#part7-4)
  ## &emsp; 7-5.[発射リクエスト/Factoryによる生成ステムの構築](#part7-5)
  ## &emsp; 7-6.[データ駆動によるステージの読み込みシステムの構築](#part7-6)

- ## 8. [今後の展望](#8今後の展望)
- ## 9. [リンク集](#9-リンク集) 
****

## 0.README
- ## <a id = "part0-1"></a>0-1.PV
  <a href = "Image/PV.mp4" target = "100%">
  <video src="./Video/ToCutForward.mp4" controls width="100%"></video>
  </a>

  ## ゲームの流れ、プレイアブルキャラの紹介、ボス戦、戦闘の流れを短時間で確認できる紹介動画です。
****

- ## <a id = "part0-2"></a>0-2.ゲーム説明スライド
  <a href="Image/ゲーム説明スライド_サムネ.png" target="_blank">
  <img src="Image/ゲーム説明スライド_サムネ.png" width="100%">
  </a>
<br>
  <a href="Slide/ゲーム概要スライド.pptx" target="_blank">PowerPoint版はこちら</a>

  <a href="PDF/ゲーム概要スライド.pdf" target= "_blank">PDF版はこちら</a>
</p>

## ゲームの流れをまとめたスライドです。
---

- ## <a id = "part0-3">

## 技術紹介スライド
   <a href="Slide/技術紹介スライド.png" target="_blank">
   <img src="Image/技術紹介スライド_サムネ.png" width="100%">
   </a>
  <a href="Slide/技術紹介スライド.pptx" target="_blank">PowerPoint版はこちら</a>
  
  <a href="PDF/技術紹介スライド.pdf" target= "_blank"> PDF版はこちら</a>
  
  ## 実装技術を簡易的に説明したスライドです。
****




## 1.プロフィール

- ## 氏名: 山口 隼(ヤマグチ ハヤト)
  
- ## 所属: 河原電子ビジネス専門学校 ゲームクリエイター科 27卒
  
- ## 希望職種: プログラマ
  
- ##  強み: ゲームにおける操作感やギミックの仕組みを分析し、C++で設計・実装することを強みとしています。本ポートフォリオでは、チーム制作で担当した「プレイヤーアクション・NPC制御・攻撃処理・ステージ進行管理」の設計に加え、課題に対して「どうクラスを分ければ保守性が上がるか」「どうデータを分離すれば調整しやすくなるか」を常に考えながらコーディングを行っています。

- ## Email: CA01244029@st.kawahara.ac.jp
****

## 2.作品概要

-  ## 使用言語: 
   ## &emsp; C++14 <br>
   ## &emsp; DirectX

- ## 開発環境: 
   ## &emsp; VisualStudio 2022 <br>
   ## &emsp; 学内エンジン

- ## 開発ツール: 
  ## &emsp; バージョン管理: GitHub / Forkクライアント
  ## &emsp; 連絡手段: Teams
****

## 3.チーム構成と担当箇所

- ## <a id = "part3-0"></a>3-0.開発チーム構成:
  - ## アウトゲーム全般担当:1人
    ## &emsp; UI/演出/ゲームフロー全体の管理

  <br>

  - ## インゲーム担当2人 
    ## &emsp; Bossキャラクター/NPC担当
    ## &emsp; Playerキャラクター/ステージ制御担当

  ## 計3人構成
****

- ## <a id = "part3-1"></a>3-1.担当箇所：
  ## &emsp; ステージモデルの制作
  ## &emsp; ステージの読み込み・進行管理システムの構築
  ## &emsp; プレイヤーアクションの設計・実装（状態遷移、コンボルート等）
  ## &emsp; NPCキャラクターの実装。
  ## &emsp; 武器の当たり判定とダメージ計算の実装
  ## &emsp; ダメージポップアップの演出・UI実装
****

- ## 4.ゲームの特徴
  - ## <a id = "part4-1"></a>4-1.ゲームの特徴
    ## ■ 特徴-1 共闘ができるアクションゲーム。
    ## &emsp; ユーザーとNPCが共闘する3Dアクションゲームです。
    ## &emsp; 勿論ソロプレイも可能となっています。
  
  - ## ■ 特徴-2 ボスの討伐のために繰り広げられるスピーディーなバトル
    ## &emsp; 制限時間以内にボスの討伐を行うことがゲームクリアの目的となっています。
    ## &emsp; また、攻撃を組み合わせることでコンボを発動することも可能となっており攻撃手段の幅を増やしています。
****

## 5.操作方法
  - ## <a id = "part5-1"></a>5-1.基本操作
  <a href = "Image/操作説明.png" target = "_blank">
  <img src = "Image/操作説明.png" width = "100%">

  ## &emsp; 移動/ジャンプ/攻撃などの基本動作をまとめています。
  ## &emsp; また、攻撃は同じBアクションでも入力状態によって異なるアクションができます。
  ## &emsp; ※5-2を参照

  - ## <a id = "part5-2"></a>5-2.攻撃方法
    <a href = "Image/Action Table.png" target = "_blank">
   <img src = "Image/Action Table.png" width = "100%">

  ## &emsp; Bボタンの単発入力、連打、長押し、ジャンプ中入力、ダッシュ中入力などにより攻撃アクションが変化します。
  ## &emsp; また、Combo 1〜3は固有の技名ではなく、武器種や状態に応じて派生する共通コンボアクションとして表記しています。　　

  - ## <a id = "part5-3"></a>5-3.復活システム
    - ## 概要: 他キャラクターのHPが0になった際、近くでYボタンを押すことで数秒間かけて復活をさせることができます。
    - ## 復活中は無防備になってしまうため、タイミングが重要にもなってきます。
    <video src="./Video/ReboneSystem.mp4" controls width="100%"></video>

  - ## <a id = "part5-4"></a>5-4.攻撃方法
    - ## 種類とボタン配置(動画はソードキャラクターのものとなっています。)
      - ## 通常攻撃: Bを単発で押す。
      <video src="./Video/NormalAttack.mp4" controls width="100%"></video>
 
      - ## チャージ攻撃: Bを長押し
      <video src="./Video/ChargeAttack.mp4" controls width="100%"></video>

      - ## 連続攻撃: Bを連打
      <video src="./Video/RushAttack.mp4" controls width="100%"></video>
 
      - ## 斬り進む攻撃: ダッシュ状態でB
      <video src="./Video/ToCutForward.mp4" controls width="100%"></video>

      - ## 空中攻撃: ジャンプ状態でB
      <video src="./Video/AirAttack.mp4" controls width="100%"></video>
****

## 6.キャラクター紹介
   - ## <a id = "part6-1"></a>6-1.PV
   - ## <a id = "part6-2"></a>6-2.SwordCharacter
   - ## <a id = "part6-3"></a>6-3.Hammerharacter
   - ## <a id = "part6-4"></a>6-4.WandCharacter
   - ## <a id = "part6-5"></a>6-5.TwinGunCharacter


****
## 7.技術的工夫点 7-0
   - ## <a id = "part"></a>7-0.こだわった箇所
     <a href="Image/こだわった箇所.png" target="_blank">
     <img src="Image/こだわった箇所.png" width="100%">
     </a>

   - ## <a id = "part7-1"></a>7-1.クラス設計の見直し（キャラクターの共通化）
     ## ■ 課題
     ## &emsp; 当初はキャラクターごとに移動、HP管理、アニメーション、攻撃処理を個別に実装していたため、同じような処理が複数のクラスに分散し、修正箇所の視認性が悪い状態でした。

     ## ■ どう工夫したか
     ## &emsp; キャラクターの基底として「ICharacter」を用意し、HPや攻撃ステータス、モデル管理など、実体を持つキャラクターに共通する処理をまとめました。
     ## &emsp; さらに、プレイヤーとして操作可能なキャラクターは「Player」を中心にし、武器ごとの差分は「IWeaponCharacter」から派生するSwordCharacter、HammerCharacter、WandCharacter、TwinGunCharacterに分けました。

     <a href="Image/Character.png" target="_blank">
     <img src="Image/Character.png" width="100%">
     </a>

     ## ■ 結果
    ## &emsp; キャラクター本体の共通処理と、武器ごとの固有処理を分けられたため、武器追加時に既存のPlayer処理を大きく変更せずに拡張できる構成になりました。

  - ## <a id = "part7-2"></a>7-2.階層型ステートパターンの導入によるアクション管理
    ## ■ 課題
    ## &emsp; アクションを作る際、コンボの派生条件や技ごとのダメージ設定を全てコード内にif文で書くと、技が増えるたびにコードがごちゃごちゃになり、調整も困難でした。

   <a href="Image/PlayerStateStructure.png" target="_blank">
   <img src="Image/PlayerStateStructure.png" width="100%">
   </a>


    ## ■ どう工夫したか
    ## &emsp; 攻撃の土台となる「PlayerAttackBaseState」を作り、各攻撃技がそれを引き継ぐ階層型ステートの実装。
    ## &emsp; コンボルートやダメージ倍率は構造体のテーブルとして独立させ、ロジックから切り離しました。
    ## &emsp; また、テーブルの中から今の技に合うデータを探し出し適応するように実装しています。


    ## ■ 結果
    ## &emsp; コードを直接書き換えなくても、テーブルの数値をいじるだけで技の強さやコンボの繋がりを瞬時に変えられるようになり、拡張性が大きく向上しました。

  - ## <a id = "part7-3"></a>7-3.テーブルによるコンボ/攻撃ステータス管理
    ## ■ 課題
    ## &emsp; 攻撃ごとの派生条件やダメージ倍率をステートクラス内に直接書くと、技が増えるたびに条件分岐が増え、調整しづらかったりコードとしての可読性などあらゆる面で問題が発生しました。

    ## ■ どう工夫したか
    ## &emsp; コンボの派生条件は「ComboRouteTable」、攻撃ごとのダメージ倍率やクリティカル補正は 「AttackParameterTable」に分離しました。
    ## &emsp; ステート側では、現在の状態IDと入力条件をもとにテーブルを検索し、次の状態や攻撃パラメータを取得する形にしています。

    ## ■ 結果
    ## &emsp; 攻撃ステート側の処理を増やしすぎず、コンボルートやダメージ倍率の調整をテーブル側で行えるようになりました。
    ## &emsp; これにより、アクションの調整作業とロジックの実装を分離でき、保守性と調整効率を高めることができました。

  - ## <a id = "part7-4"></a>7-4. 旧入力システム VS 新入力システム
    ## Adapterパターンによる入力責務の分離

    ## ■ 課題
    ## &emsp; 旧設計では、PlayerInputクラス内で物理コントローラー入力とNPC用の仮想入力を分岐して処理していました。
    ## &emsp; そのため、PlayerInputが「入力元の判定」と「ゲームアクションへの変換」の両方を担当しており、操作キャラクター切り替えやNPC制御を拡張しづらい構造になっていました。

    <a href="Image/Old Input System VS New Input System.png" target="_blank">
    <img src="Image/Old Input System VS New Input System.png" width="100%">
    </a>

    ## ■ どう工夫したか
    ## &emsp; AdapterPatternを導入し、物理コントローラークラスと仮想コントローラークラスに分離。
    ## &emsp; PlayerInputは入力元を直接判定せず、親クラス経由で取得した入力をIsJump(ジャンプ判定)、IsAttack(攻撃判定)、IsChargeAttack(チャージ攻撃判定)などのゲームアクションへ変換する役割に限定しました。
    ## &emsp; また、PlayerControllerHubを用意し、操作中のキャラクターにはGamePadInputAdapter(物理パッド)、非操作キャラクターにはVirtualInputAdapter(仮想パッド)を割り当てることで、キャラクターを再生成せずに操作対象を切り替えられる構成にしました。

    ## ■ 結果
    ## &emsp; PlayerInputから入力元判定のif分岐を削除でき、物理入力とNPC入力を同じ経路で扱えるようになりました。
    ## &emsp; NPCはAIが仮想入力を送ることでPlayerと同じアクション処理を利用できるため、プレイヤー操作キャラクターとNPCキャラクターの挙動差を抑えられました。
    ## &emsp; また、入力デバイスの差し替えだけで操作キャラクターを変更できるため、キャラクター選択UIとの連携もしやすい構成になりました。

    <a href="Image/NPCVirtualInputStructure.png" target="_blank">
    <img src="Image/NPCVirtualInputStructure.png" width="100%">
    </a>
    
    ## ■ 結果
    ## &emsp; NPCはAIが見えないコントローラーを操作しているような形で動作するため、Player側の移動・攻撃・復活処理を活用しながらNPCを制御できました。
    ## &emsp; 共通の入力経路を使うことで、プレイヤーとNPCの挙動差を抑えつつ、AI側の判断処理を独立して調整できるようになりました。

  - ## <a id = "part7-5"></a>7-5.発射リクエスト/Factoryによる生成ステムの構築
    ## ■ 課題
    ## &emsp; 銃キャラクターの攻撃を実装する際、各攻撃Stateが弾丸の生成、モデル情報、速度、寿命、発射位置、エフェクト通知まで直接持ってしまうと、ステートクラスが肥大化してしまう問題がありましたｓｓ

    ## ■ どう工夫したか
    ## &emsp; 攻撃ステートからは「BulletFireRequest」として弾の種類・生成基準位置・発射方向だけを「GunShooter」へ渡す形にしました。
    ## &emsp; 「GunShooter」は「BulletFactory」に弾丸生成を依頼し、「BulletFactory」側で「BulletType」に応じた弾丸クラスを生成します。
    ## &emsp; また、弾丸ごとの速度、寿命、生成位置補正は「BulletParameterTable」に分離し、モデル情報は「BulletModelRegister」から取得するようにしました。
    ## &emsp; 発射時のエフェクトなどは「IBulletFireListener」へ通知することで、弾丸生成処理と演出処理を分けています。

    <a href="Image/BulletGenerationSystemStructure.png" target="_blank">
    <img src="Image/BulletGenerationSystemStructure.png" width="100%">
    </a>

    ## ■ 結果
    ## &emsp; 攻撃ステートは発射タイミング/発射する弾丸の種類のみをしるだけとなり、生成処理やパラメータ管理を別クラスに分離できました。
    ## &emsp; その結果、弾の種類追加や速度調整を行う際の修正箇所を限定しやすくなりました。

  - ## <a id = "part7-6"></a>7-6.データ駆動によるステージ読み込みシステムの構築
    ## ■ 課題
    ## &emsp; 既存の設計ではステージごとにクラスを作成しており、ステージが増えるたびに同じような処理が増え、コピーコードが量産されていました。

    ## ■ どう工夫したか
    ## &emsp; ステージの情報を描画と座標やモデルパスなどの構成データに分離しました。
    ## &emsp; ステージごとの固有データは構造体にまとめ、LoadStageDataクラスが識別子を受け取るだけで、そのステージを自動で読み込めるように設計。

    ## ■ 結果
    ## &emsp; ステージがどれだけ増えてもクラス数は増えず、ステージデータの登録のみで運用できる形になり、開発効率が向上しました。

    ## ■ 結果
    ## &emsp; AIが「見えないコントローラー」を操作している状態になり、Playerのアクション処理を一切書き換えることなく、全く同じ挙動でNPCを動かすことに成功しました（コンポーネント指向の実現）。

## &emsp;        
****

## 8.今後の展望
- ## リファクタリング
  ## &emsp; 階層がステートパターンにイテレーターパターンを導入。

- ## ステージの追加
  ## &emsp; こちらも同様に2～3種類追加予定です。

- ## Ultimate Abilityの実装
  ## &emsp; ボスのHPの減少割合に応じてコレクションアイテムを出現させ、全て集めるとボスに大ダメージを与えれるように実装予定です。

****

## 9. リンク集
- ## Youtube: [こちらからアクセスできます](https://www.youtube.com/@%E5%B1%B1%E5%8F%A3%E9%9A%BC-kawahara)
  
- ## Googleドライブ: [こちらからアクセスできます](https://drive.google.com/drive/folders/1uRL0AiCKYP2HvznbBXS_wLJY3bZnr4bU?usp=drive_link)

- ## GitHub: [こちらからアクセスできます](https://github.com/TanimotoYuuki/Project-EH)

- ## 過去作品(個人制作): [こちらからアクセスできます](https://github.com/YamaguchiHayato/Dimensional-Flip)

- ## 過去開発(チーム開発): [こちらからアクセスできます](https://github.com/TanimotoYuuki/EhimeGuri)
****