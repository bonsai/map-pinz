# map-pinz

JSONLをURLで渡すだけで、位置情報を3D Globe上のピンとして表示するGitHub Pages viewer。

## Usage

https://bonsai.github.io/map-pinz/?jsonl=JSONL_URL

`data=` も使用可能。

## JSONL

1行1JSON。最低限 `lat` / `lon` と `name` があれば表示。

`location.lat` / `location.lon`、latitude / longitude、lng も認識する。

## Design

- Vanilla JavaScript
- Three.js + three-globe
- Node / npm / build step 不要
- 各domain repoをcanonにする
- festivals / onsen / taki / その他のGeoJSONLを同じviewerで表示
