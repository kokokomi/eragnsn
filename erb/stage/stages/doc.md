# stages
各ステージの定義を置く場所です  

## ファイル名
stage_{stageId}.erbの形式でファイルを作る  
stageIdは1以上 MAX_STAGE_ID(global.erhに定義)未満  

## 実装が必要な関数
|関数名|引数|戻り値|実装する内容|
|---|---|---|:---|
|stage_initialize_{stageId}|-|-|攻略開始時に呼び出される。初期化が不要であれば空でよい|
|stage_{stageId}_stage_name|-|選択肢などに表示されるステージ名|ステージ名を入れる。 **FUNCTIONSでRETURNSするだけでなくRESULTSにステージ名を入れる必要がある** |
|stage_{stageId}_can_challenge|-|攻略可否のtrue/false|ステージに入れる場合はtrueを返す。攻略に条件が必要な場合はここで条件を書く|
|stage_get_max_floor_{stageId}|-|最大階層|ステージの最大階層を返す|
|stage_explore_{stageId}|-|イベントを発生させた場合はtrue|「周辺を探索」を選んだときに呼び出される。ここでランダムイベントを起こす|
|stage_foward_{stageId}|-|-|「先へ進む」を選んだときに呼び出される。戦闘を発生させたりイベントを起こす|
