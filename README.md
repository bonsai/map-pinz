# map-pinz

JSON / JSONLをURLで渡すだけで、位置情報を3D Globe上のピンとして表示するGitHub Pages viewer。

## One source

`https://bonsai.github.io/map-pinz/?url=JSONL_URL`

`jsonl=` / `data=` も使用可能。

## Multiple sources

同じ `url` を複数指定すると、sourceごとに別レイヤーで表示します。

```text
https://bonsai.github.io/map-pinz/?url=https://bonsai.github.io/festivals/data/festivals.jsonl&url=https://example.com/onsen.jsonl&url=https://example.com/taki.jsonl
```

画面上でレイヤーごとの表示 / 非表示を切り替えられます。

## JSON / JSONL

1行1JSONのJSONL、またはJSON配列 / 単一JSONを読み込めます。最低限 `lat` / `lon` と `name` があれば表示。

`location.lat` / `location.lon`、latitude / longitude、lng も認識します。

## Design

- Vanilla JavaScript
- Three.js + three-globe
- Node / npm / build step 不要
- 各domain repoをcanonにする
- festivals / onsen / taki / その他のGeo dataを同じviewerで表示

## Demo layers

ダミーデータを同時表示するURL:

`https://bonsai.github.io/map-pinz/?url=https://bonsai.github.io/map-pinz/data/festival.jsonl&url=https://bonsai.github.io/map-pinz/data/onsen.jsonl&url=https://bonsai.github.io/map-pinz/data/taki.jsonl`
