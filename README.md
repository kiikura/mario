# mario

Cheat Sheet

## Custom Elements

```
document.re
```

```

```
# JS基礎

## DOM操作
- 要素にHTML要素を追加する: node.innerHTML = "<img src='xxx.png'>";
- 要素をJSで作って追加する: node.appendChild(document.createElement("<img>"));
- 要素の属性を取得する:  node.getAttribute("src");
- 要素の属性を設定する:  node.setAttribute("src","xxx.png");
- 要素の属性を削除する:  node.removeAttribute("src");
- タグ名で要素を検索する: document.querySelector("img"); //最初に見つかったimgタグを返す。



# リソース

## 画像
- mario-standing.png: マリオの立ち画像
- mario-jumping.png: マリオのジャンプ画像

## サウンド（おまけ）
`SMB.audio.play("サウンド名")`で音が鳴る
- powerup: パワーアップ
- powerdown: パワーダウン
- jump: ジャンプ

## CSS
マリオタグを作るにあたって事前にスタイルは定義済みです
- class属性にjumpingをつける -> ジャンプアニメーションを開始する
- super-mario属性が存在する -> imgを1.4倍する
※ keyframeやtransitionの指定はアニメーション用です  
※ マリオタグにはShadow DOMをつかう場合はそのままではダメです

## イベント
### smb-controllerのイベント
- up: 十字キーの上を押した
- down: 十字キーの下を押した
- left: 十字キーの左を押した
- right: 十字キーの右を押した
- a: Aボタンを押した
- b: Bボタンを押した


```
//イベント割り付け例
document.querySelector("smb-controller").addEventListener("up", function(evt){
    alert("上がおされました")
});
```

### アニメーションの終了

- `webkitAnimationEnd`: CSSアニメーションが完了すると発行するイベント。

```
document.querySelector("smb-mario").addEventListener("webkitAnimationEnd", function(){
    alert("animation owari");
]);
```

# チャレンジ
- コントローラを置いてみる(<smb-controller>)
- 2ndコントローラを置いてみる


