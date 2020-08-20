# VSCode で Java プロジェクトを使えるようにする  
ここでの説明は、以下の OS 環境を想定する。
- Windows 10  

VSCode で Java 環境を整える前に、以下の事前準備だけは済ませておく。:hamster:
https://www.webfx.com/tools/emoji-cheat-sheet/

## 事前準備
- VSCode ポータブルのインストール（配置）
- Java（OpenJDK 11）のインストール

準備ができていない場合は、以下のページを参照する。

VSCode ポータブル版のインストール方法:  
[https://github.com/fs5013-furi-sutao/explain.how_to_install_vscode.portable](https://github.com/fs5013-furi-sutao/explain.how_to_install_vscode.portable)

Java をインストールする（Scoop を使って）:  
[https://github.com/fs5013-furi-sutao/explain.how_to_install_java.with_scoop](https://github.com/fs5013-furi-sutao/explain.how_to_install_java.with_scoop)

## 拡張機能 Java Extension Pack のインストール  
拡張機能ペインを開く。拡張機能ペイン（EXTENSIONS）を開くには、`Ctr + Shift + X'` を押下する。

ペインが開いたら、検索窓に「java」と入力する。

インストール候補に `Java Extension Pack` が表示されたら、`install` ボタンを押す。

インストールが完了したら、必要なものがきちんとインストールされているか、念のため確認をしておく。

拡張機能ペインの検索窓に「@installed」と入力する。

Java Extension Pack をインストールすることで、以下の 6 つの拡張機能がひと通りインストールされるはずである。

- Language Support for Java(TM) by Red Hat
- Debugger for Java
- Java Test Runner
- Maven for Java
- Project Manager for Java
- Visual Studio IntelliCode

## 最初の Java プロジェクト
もっとも簡単な Java プロジェクトを作って動かしてみる。

まず、サイドバーを `Ctr + B` で閉じる。

### 1. コマンドパレットを開く
`Ctr + Shift + P` でコマンドパレットを開く。

### 2. Java プロジェクト作成コマンドの実行
コマンドパレットに「create java」と入力する。コマンドの候補に `Java: Create Java Project...` と表示されるので、このコマンドを Enter で選択する。

### 3. プロジェクトの種類を決定 
「Select the project type」とプロジェクトの種類を求められるので、「No build tools」を選択する。

### 4. フォルダの選択
フォルダ選択ダイアログが開いて、プロジェクトを作成する場所を求められるので、フォルダを選択して「Select the project location」ボタンを押して決定する。

例えば、デスクトップにプロジェクトを作成したい場合は、デスクトップを選択する。

### 5. プロジェクト名の入力
「Input a Java project name」とプロジェクト名の入力を求められるので、好きなプロジェクト名を入力する。

今回は「first.java.project」と入力して、Enter キーを押す。

やっぱ、やめる・・・という場合は、ここで `Esc` キーを押せば、プロジェクトの作成をキャンセルできる。

### 6. ちょっぴり待つ
これだけやれば、あとは Project Manager がプロジェクトを作成し、Language Support for Java が Java Language Server を起動してくれる。

## エクスプローラを見る
プロジェクトが出来上がると、サイドバーが開く。フォルダ階層が表示され、以下のような構成になっているはず。

```
first.java.project
├─ lib
└─ src
     App.java
  README.md
```

## ファイルを開く
この中から `App.java` を開く。

ファイルには既に以下のコードが生成されている。拡張機能が効いていると、`main` メソッドの上に「`Run` | `Debug`」というリンクが表示されているのが分かる。

```java
public class App {
    Run | Debug
    public static void main(String[] args) throws Exception {
        System.out.println("Hello, World!");
    }
}
```

## プログラムを動かす
では、表示されている `Run` リンクを押してみる。プログラムが実行されたのが分かる。

![Java プログラムの実行](./run_java_on_vscoe.gif?raw=true)

プログラムはショートカット、`F5` でも実行を開始できる。

***
以上。




