```
@startuml
opt アカウント

opt アカウントの情報を変更するとき

ユーザー -> Webサーバー : 編集したアカウント情報送信
Webサーバー-> DBサーバー : アカウント情報を送信
DBサーバー --> DBサーバー : アカウント情報を保存
DBサーバー --> Webサーバー : 保存したアカウント情報送信
Webサーバー -> ユーザー : アカウント情報表示

end

end

opt 投稿記事(コメント)の表示

ユーザー -> Webサーバー : 投稿記事(コメント)選択
Webサーバー-> DBサーバー : 選択された投稿記事(コメント)を送信
DBサーバー -> Webサーバー : 選択された投稿記事(コメント)を送信
Webサーバー -> ユーザー : 投稿記事(コメント)の表示

opt 記事(コメント)変更するとき

ユーザー -> Webサーバー : 編集した記事(コメント)を送信
Webサーバー-> DBサーバー : 変更した記事(コメント)を送信
DBサーバー --> DBサーバー : 変更した記事(コメント)を保存
DBサーバー --> Webサーバー : 保存した記事(コメント)を送信
Webサーバー -> ユーザー : 変更した記事(コメント)表示

end

opt 記事(コメント)を削除するとき

ユーザー -> Webサーバー : 選択した記事(コメント)を送信
Webサーバー-> DBサーバー : 選択した記事(コメント)を送信
DBサーバー --> DBサーバー : 選択した記事(コメント)を削除
DBサーバー --> Webサーバー : 記事(コメント)を送信
Webサーバー -> ユーザー : 記事(コメント)を表示

end

end

opt 履歴の表示
ユーザー -> Webサーバー : 履歴一覧の選択
Webサーバー -> DBサーバー : 履歴一覧の要求
DBサーバー --> Webサーバー : 履歴一覧の送信
Webサーバー --> ユーザー : 履歴一覧の表示

end

opt お気に入りのアカウント(記事)を表示するとき

ユーザー -> Webサーバー : お気に入りのアカウント(記事)表示
Webサーバー-> DBサーバー : お気に入りのアカウント(記事)情報の要求
DBサーバー --> Webサーバー : お気に入りのアカウント(記事)情報を送信
Webサーバー -> ユーザー : お気に入りのアカウント(記事)の表示

end

@enduml
```
