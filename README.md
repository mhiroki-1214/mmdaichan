<!-- Markdown: Open Preview to the side -->
# MMDアイちゃんの説明 #
## ファイルの中身確認 ##
中に入ってる物は以下の通りです。
```
haihu
  ┗ musubiai2.0
       ┗ PmxView
            ┗ aichan.x (小道具類のファイル)
       ┗ tex (テクスチャファイル)
       ┗ aichan.pmx (ボーンを少しいじった)
       ┗ musubiai.fx (エフェクトとか。)
       ┗ musubiai2.0.pmx (変換してそのまんま)
  ┗ aichan_motion
         ┗ tewohuruyatu.vmd (もーしょん)
  ┗ gazou (説明用画像)
```
***
## ファイルの詳細とかいろいろ ##

たぶん見たことないファイル形式があるので一応説明を


### aichan.x の xファイル ... アクセサリファイル   ###
初音ミクとかでいうところのネギであったり、   
ステージ上の細かな小道具などを使用するため。   

### texの中身 ... アイちゃんの外見を作る肌みたいなもん   ###
基本は**いじらない**こと。   
万が一消しちゃったらやべえアイちゃんが出ます。  　

### musubiai.fx の fxファイル ... エフェクト   ###
服の模様とか、キラキラした何かを付け加えるとか。   
ぶっちゃけ無くても出来上がりますが、あったほうが綺麗です。

### tewohuruyatu.vmd の vmdファイル ... motion ###
読み込んだモデルに動きを付けます。   
MMDアイちゃんは大体のモーションに対応できます。   
ただし、人外(クリーチャーとか怪獣とか)モーションはムリでーす。

### aichan.pmxとmusubiai2.0.pmx の pmxファイル　... 骨組み   ###
骨格だと思ってください。   
これがないと上記のものが意味ないファイルです。   
消しちゃったら迷うことなく全部削除してzipを再解凍しちゃってください。   
    
### Q : そもそもどれがメインなの ###
A : pmxファイルです。   
MMD等でモデル読み込みをする際には**pmx**を読み込んでください。
### Q : texファイルの中身をpmxと同じ階層に置きたいんやけど ###
A : やったことないのでわかりません。試してください。   
vmdの制作でテクスチャファイルをどこの階層に置くかは作り方次第です。   
自分はごちゃごちゃしてだるいなと思ってテクスチャファイルをまとめちゃってます。   
### Q : aichan.pmx と musibiai2.0.pmxの違いは何？ ###
A : _end3 と書いてあるボーンがあるかないかです。   
今回、VRoidからMMDに変換しており、その際に出てる_end3というボーンは邪魔でしかないです。   
というか、vmdで使用することがまずないので消してます。
***
## MMDのダウンロード ##
まずはMikuMikuDanceをダウンロードするところからです。   
[こちら](https://drive.google.com/uc?id=1XurGlDnQy-EfpO13JcqCocQhjuHtXx6P&export=download)からダウンロードしてください。   
ダウンロードしたファイルの中身は以下のようになってると思います
```
MikuMikuDance_v○○○
     ┗ Data (ミクのトーンとか)
     ┗ UserFile (サンプルとかいろいろ)
     ┗ MikuMikuDance.exe (実行ファイル)
     ┗ readme.txt 
```
まずはMikuMi.exeを実行してみてください。   
こんな感じの画面が出ると思います。   
![none](gazou/mmd_nanimonaiyo.png)    
ひとまずこの画面が開けれたらokです。   
仮にエラーが出て開けないんやけどとかは   
***サイドバイサイド構成エラー***の可能性大なのでそこをクリアしてください。   

エラーが出なかった、クリアしたら次にモデルのアイちゃんをここに登場させてみましょう。
## アイちゃん召喚　(pmx読み込み)
下のなんかカラフルに並んでる意味不明な奴らの   
赤い枠のモデル操作の中に読み込みというのがあるので、   
そこにaichan.pmxかmusubiai2.0.pmxを開きましょう。   
読み込む際に作成者のポップが出ると思いますがokでいいです。
![none](gazou/mmd_model1.png)
　　　　　　　　　　　　　↓
![none](gazou/mmd_model2.png)
上のようにアイちゃんが手を横に伸ばしてる感じで読まれてたらokです。  
もし、足元が変やでとかあれば別のpmxを読み込んでそっちもおかしいんやけどとかであればメールを送ってください。直します。   

ひとまず召喚ができました。   
がこれでは変な骨組みが見えてるアイちゃんを眺めるだけになるので   
次は動かしてみましょう。

## アイ、動きます。　(vmd読み込み)
まずは左上のファイルのタブを開いてみましょう。   
そしたらこんな感じのやつが出るので赤い枠のをクリック
![none](gazou/mmd_motion.png)
ついででポーズデータってなんや？とかモーションデータ保存ってなんや？という疑問を解消しときます。   
ポーズデータは握り方とか手をピース✌にしたりとか細かな部分のデータです。基本的にモーションを組み合わせて使います。単体で使うとしたら何かポーズをさせて撮影する程度。   

モーションデータ保存はポーズデータやら連続して別の動きをしたりとか、表情操作とかを別のモデルでもしたいよ！ていう時に使う。


では、vmd読み込みに戻ります。   
読み込みを押したらファイル選択画面が出ると思うので   
tewohuruyatu.vmdを試しに開いてみてください。   
なんとかハサン専用やで！と言われますが、無問題なのでそのままokを押してください。
![none](gazou/mmd_motion2.png)
変化したと思います。   
左側のフレーム操作枠を見てもらえたら赤い粒粒が出てるのがわかります。   
その粒粒を通過するたびにボーン操作が行われて動きがついてる感じ。
あとは再生です。   
下のカラフルな枠達の右下、少し黒っぽい枠です
![none](gazou/mmd_motion3.png)
赤い枠で囲っているところの再生を押したら動き出します。   
このモーションはちょっと長めですけどうまーいこと動いてるので　　　ボーンの枠とかも見てください。


以上 MMDの基本的な操作でした。
***


## 取り扱いについて。公開範囲とかいろいろ ##
MMDなんで初音ミクと共演させれるとかできます。  
また使用ルールも載せておきます
<dl>
  <dt>動画使用する場合はURLを載せること</dt>
  <dd>作ってもないのに作りました！とかいう不思議な記憶を持つ人が沸くので</dd>
  <dt>卑猥なコンテンツはNG</dt>
  <dd>いわゆるR-18MMDですよね。いじれば簡単なんでしょうけど不愉快なのでやめてください。</dd>
  <dt>過度な改造は禁止</dt>
  <dd>これをベースに別キャラなどもダメです。アクセサリーで・・・とかは大丈夫です。</dd>
  <dt>おバカ全開の寒い動画はNG</dt>
  <dd>呆れを通り越して可哀そうで泣けてくるからです。</dd>
</dl>
これくらいです。あとは節度を守ってください。   


## その他、Q&Aとか ##   
身内の小さなコミュニティですが、すでにURLをのっけて公開はしてます。  
そこで得た質問等をここで消化しておきます。
<dl>
  <dt>VRChatで使いたい</dt>
  <dd>構いません。が、自作等の俺が作ったんやで！という記憶変換、R-18に発展している発展場に近づくなどをしないでくださいね。</dd>
  <dt>カスタムスキンとして別ゲーで使いたい</dt>
  <dd>個人で楽しむ程度であれば。公開はしないでください。主に中国人とかが食いついてだるいことになるので</dd>
  <dt>Live2Dで使いたい</dt>
  <dd>何に使うのかわかりませんが、個人で楽しむ程度で。公開は無し。</dd>
  <dt>Unityで使いたい</dt>
  <dd>これに関しては上の使用ルールを守ってもらえればいいです。</dd>
</dl>
これくらいです。また、随時更新します。   
