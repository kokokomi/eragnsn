# stages
各ステージの定義を置く場所です  

## ファイル名
stage_{stageId}.erbの形式でファイルを作る  
stageIdは1以上 MAX_STAGE_ID(global.erhに定義)未満  

## 実装が必要な関数
|関数名|引数|戻り値|実装する内容|
|---|---|---|:---|
|stage_initialize_{stageId}|stageId|-|ステージの定義を設定する。ゲーム開始時に呼び出される|
|stage_{stageId}_can_challenge|-|攻略可否のtrue/false|ステージに入れる場合はtrueを返す。攻略に条件が必要な場合はここで条件を書く|
|stage_explore_{stageId}|-|イベントを発生させた場合はtrue|「周辺を探索」を選んだときに呼び出される。ここでランダムイベントを起こす|
|stage_foward_{stageId}|-|-|「先へ進む」を選んだときに呼び出される。戦闘を発生させたりイベントを起こす|
