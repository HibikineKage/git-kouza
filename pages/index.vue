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
    slide
      p 使用可能なメールアドレスを入力
      p メールアドレスは大学のものを推奨します
      p 少なくともPCからアクセスできるメールアドレスを使ってください
      p 覚えてタイプ可能なパスワードを入力(後で使います)
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
        li git-testを開く(エクスプローラーはまだ閉じないでね)
        li sample.txt(名前は何でも)を作成
        li sample.txtをテキストエディタで開く(VSCode使ってみてもいいよ)
        

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
