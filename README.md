

1.Homebrewインストール

1-1.Homebrewの公式サイトへブラウザでアクセス
https://brew.sh/index_ja.html

1-2.公式サイトへ記載されているコマンドをターミナルで実行
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

2.swiftlintインストール

2-1.ターミナルで以下のコマンドを実行
brew install swiftlint

3.設定

3-1.Build Phasesを表示
3-2.+をクリックし、New Run Script Phaseをクリック
3-3.追加したRun Scriptに以下を入力

if which swiftlint >/dev/null; then
    swiftlint
else
    echo "warning: SwiftLint not installed, download from https://github.com/realm/SwiftLint"
fi