# 第12回課題

### circleCI成功画面
- <img width="586" alt="image" src="https://user-images.githubusercontent.com/116282189/209152178-d8ff71eb-24f7-445a-8301-db83e976e917.png">


### 対象リポジトリの中身
- <img width="662" alt="image" src="https://user-images.githubusercontent.com/116282189/209152338-7dbdd4cd-fc00-41e7-8f34-3548637fe6be.png">


### 感想
- 上手くいかなかった原因としては、configで記述したパスの位置を間違っていたことだった。リポジトリの位置から見た、相対的なパスに、対象ファイルを置かなければならなかった。
- また、yamlの記述の仕方にも注意が必要だった。CircleCIでは、リージョンは環境変数で書かなければはじかれることが分かったので、「Sub」を用いた書き方にも慣れる。
