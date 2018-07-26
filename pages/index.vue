<template lang="pug">
#GitSlideshow.eg-theme-bretagne
  .eg-slideshow
    slide    
      h1 はじめてのGit & GitHub講座
      h4
        a(href='https://twitter.com/Hibikine_Kage') @Hibikine Kage
    slide(enter='bounceInRight' leave='fadeOut')
      h3 Gitとは？
      ul
        li バージョン管理ソフト
        li 世界中で使われている
        li オープンソースソフトウェアのデファクトスタンダード
    slide
      h3 今日やること
      ul
        li VSCode, Git for Windowsのインストール
        li GitHubアカウント作成
        li 簡単な個人プロジェクトの作成
      p 余裕あれば
      ul
        li GitHub Studentsの登録
        li ブランチを使った複数人開発
    slide
      h3 Gitの概要
      img(src='git-zu.png')
    slide
      h3 Gitの概要
      img(src='git-zu.png')
      p バージョン管理ソフト
    slide
      h3 Gitの概要
      img(src='git-zu.png')
      p 差分をコミット(commit)として積み上げていく
      p git commit --message "READMEに説明を追加"
    slide
      h3 Gitの概要
      img(src='git-zu.png')
      p 平行して複数人で開発するための「ブランチ(branch、枝)」
      p 初期ブランチは「master」
      p コミット木のどこかを指しているイメージ
      p ブランチを分けることを「ブランチを切る」と言ったり
      p ブランチ作成直後は作成ブランチと同じコミット
      p git branch add-message-readme
    slide
      h3 Gitの概要
      img(src='git-zu.png')
      p ブランチを切り替えることを「チェックアウト(checkout)」
      p git checkout add-message-readme
      p git checkout master
    slide
      h3 Gitの概要
      img(src='git-zu.png')
      p ブランチをまとめることを「マージ(merge)」
      p 平行して進めた作業をmasterに入れたい
      p git checkout master
      p git merge add-message-readme
      p 作業途中だけどmasterの変更を取り入れたい
      p git checkout add-message-readme
      p git merge master
    slide
      h3 Gitの概要
      img(src='git-zu.png')
      p ホスティングサーバー(GitHub, BitBucketなど)に送信することを「プッシュ(push)」
      p git push -u origin master
      p git push -u add-message-readme
      p git push (2回目以降)
    slide
      h3 Gitの概要
      img(src='git-zu.png')
      p プッシュされた他人の変更を取り込むことを「プル(pull)」
      p 差分をダウンロードしてからmergeが行われるイメージ
      p git pull origin master
    slide
      h3 インストール方法
      p.
        USBで配布した中身をコピーしてください
      p.red.
        まだインストールを始めないでください!!
      p.
        VSCodeSetup-x64-1.25.1.exe
        Git-2.18.0-64-bit.exe
    slide
      h3 インストール順序
      ul
        li VSCodeのインストール
        li Git for Windowsのインストール
    slide
      h3 VSCodeとは
      p Microsoft製テキストエディタ
      p Gitで使います
    slide
      h3 VSCodeのインストール
      p VSCodeSetup-x64-1.25.1.exeを起動
      p 利用規約を承認後Next連打しインストール
    slide
      h3 Git for Windowsのインストール
      p Git-2.18.0-64-bit.exe を起動
    slide
      img(src='2018-07-20-17-51-05.png')
      p Next
    slide
      img(src='2018-07-20-17-53-16.png')
      p Next
    slide
      img(src='2018-07-20-17-56-37.png')
      p Use Visual Studio Code as Git's default editor
      p この項目がなければ一旦Windowsを再起動してください
      p Next
    slide
      img(src='2018-07-20-17-57-38.png')
      p Next
    slide
      img(src='2018-07-20-17-58-09.png')
      p Next
    slide
      img(src='2018-07-23-16-17-54.png')
      p Next
    slide
      img(src='2018-07-23-16-18-41.png')
      p Next
    slide
      img(src='2018-07-23-16-19-13.png')
      p Install
    slide
      h3 GitHubアカウントの作成
      div
        a(href='https://github.com') https://github.com
        p にアクセス
        img(src='2018-07-24-14-40-40.png')
    slide
      h3 GitHubアカウントの作成
      p 使用可能なメールアドレスを入力
      p メールアドレスは大学のものを推奨します
      p 少なくともPCからアクセスできるメールアドレスを使ってください
      p 覚えてタイプ可能なパスワードを入力(後で使います)
      p メールが届くので承認してね
    slide
      h3 プロクシ対策
      p エクスプローラを開き、適当な場所で右クリックしてGit Bashを起動
      p git config --global http-proxy http://ccproxyc.kanagawa-it.ac.jp:10080
      p git config --global https-proxy http://ccproxyc.kanagawa-it.ac.jp:10080
    slide
      h3 プロキシ解除方法
      p git config --global --unset http-proxy
      p git config --global --unset https-proxy
    slide
      h3 Gitリポジトリの作成
      h4 Processing持ってる人
      ul
        li 新規プロジェクトを作成、保存(エディタは開いたままで)
        li 保存先のフォルダーをエクスプローラーで開く
      h4 Processingない人
      ul
        li エクスプローラーで新規フォルダを作成
        li フォルダ名をgit-testにする(名前は何でもいいよ🐇)
        li git-testを開く
        li sample.txt(名前は何でも)を作成
        li sample.txtをテキストエディタで開く(VSCode使ってみてもいいよ)
    slide
      h3 .gitignoreの作成
      p 右クリックしてテキストを作成
      p.red .gitignore. (先頭と末尾にピリオド)というファイルを作成
      p .gitignoreをテキストエディタで開く
      p .gitignoreの中にファイル名を書き込むと、そのファイルはGitから無視されます
      img(src='2018-07-24-14-48-06.png')
    slide
      h3 テキストを書き込んで保存
      p size(500, 500);
      p background(255);
      p fill(255, 0, 0);
      p noStroke();
      p rect(100, 100, 200, 200);
      h4 Processingない人は
      p おはようございます
      p とでも書き込んでください
    slide
      h3 Git Bashを開く
      p git_testのディレクトリ内で右クリック、Open Git Bashを選択
      img(src='2018-07-24-15-05-06.png')
    slide
      h3 Git Bashの簡単な使い方
      h2 覚えるコマンドは cd と ls と git の3つだけです
    slide
      h3 ls
      p ディレクトリの中身が出るよ
      p 迷ったら使おう
      img(src='2018-07-24-15-07-55.png')
    slide
      h3 cd
      p ディレクトリ(場所、フォルダ)を移動するよ
      p cd .. で上のディレクトリに移動できるよ(やってみてね)
      p ディレクトリ名は途中まで打ってからTabキーを押すと補完できるよ
      img(src='2018-07-24-15-35-25.png')
    slide
     h3 gitで困ったら
     h2.red git status
     p 今の状態を教えてくれるよ
     p ここはGitが初期化されてないよっていわれた
     img(src='2018-07-24-15-45-31.png')
    slide
      h3 リポジトリを初期化しよう
      p git_testのディレクトリの中で git init
      img(src='2018-07-24-15-42-34.png')
    slide
      h3 状態を見てみる
      p git status
      p master ブランチにいるよ
      p まだコミットしてないよ
      p 追跡してない(gitに登録してない)ファイルがあるよ(git addで登録できるよ)
      img(src='2018-07-24-15-49-10.png')
    slide
      h3 ファイルの変更を登録リストに入れる
      p git add git_test.pde
      p git add --all で全部まとめて登録リストに入れられる
      img(src='2018-07-24-15-52-59.png')
    slide
      h3 ファイルの登録を解除する
      p git statusしたときに出てたけど
      p git rm --cached git_test.pde
      img(src='2018-07-24-15-57-15.png')
    slide
      h3 リストに入ったファイルをコミットにする
      p git add --all
      p git commit -m "git_testを追加"
      img(src='2018-07-24-16-01-21.png')
    slide
      h3 コミットログを見てみる
      p git log
      img(src='2018-07-24-16-03-47.png')
    slide
      h3 個人的に好きなやつ
      p git log --oneline --graph --decorate=full
      p ブランチたくさん生えてるプロジェクトでもきれい
      p ログが多いときはj, kで移動、qで抜けます(覚えておくと便利)
      img(src='2018-07-24-16-07-20.png')
    slide
      h3 さらに変更を追加
      p ellipse(400, 400, 50, 50); を最後に足す
      h4 Processingない人
      p こんにちは！ とかを追加してみてください
      p git add --all
      p git commit -m "ellipse追加"
      img(src='2018-07-24-16-22-26.png')
    slide
      h3 コミットを消す
      p git reset --hard 'HEAD^'
      p ^の数だけ戻る
      img(src='2018-07-24-16-23-17.png')
    slide
      h3 コマンド一覧
      table
        tbody
          tr
            td ls
            td ファイル一覧を表示
          tr 
            td cd
            td ディレクトリを移動
          tr
            td git init
            td Gitリポジトリを初期化
          tr
            td git status
            td gitの現在の状態を表示
          tr
            td git add --all
            td 変更をすべてステージング(リストに追加)
          tr
            td git commit -m "メッセージ"
            td コミットを行う
          tr
            td git log
            td コミットの履歴を見る(j, kでスクロール、qで抜ける)
    slide
      h3 黒い画面で困ったら
      p 変な画面に移動したらESCを連打して:q!をタイプ
      p コマンドがフリーズしたらCtrl+Cで強制終了
    slide
      h3 GitHubにアップロードする
      p GitHubを開き、右上のプラスからNew Repositoryを選択
      p git-testという名前で作成
</template>
<script>
import eagle from 'eagle.js';
import 'animate.css'
import 'eagle.js/dist/eagle.css';

export default {
  mixins: [ eagle.slideshow ],
  infos: {
    title: 'Git講座',
    description: '世界中で広く使われているバージョン管理ソフトGitとホスティングサービスGitHubのインストール方法と初心者が使い始める方法を紹介します.',
  }
};
</script>
<style lang='scss'>
//b2ccba
//ea4d5b
#GitSlideshow {
  .eg-slideshow {
    font-family: 'Rounded Mplus 1c', sans-serif;
    background-color: #3a3d3b;
    color: #f7f0dc;
    .red {
      color: #ea4d5b;
    }
    & a:link,
    & a:hover,
    & a:visited,
    & a:focus {
      color: #23acb4;
    }
    .eg-slide {
      .eg-slide-content {
        width: 25em;
        max-width: 80%;
        margin: 0 auto;
        height: 100%;
      }
    }
  }
  .eg-slide-content {
    width: 25em;
    max-width: 80%;
    margin: 0 auto;
    height: 100%;
  }
}
</style>
