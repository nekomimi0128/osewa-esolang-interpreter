# 「お世話」言語 インタプリタ (オフライン版) 🍵
## はじめに
このプロジェクトは、ユニークな日本語構文を持つ難解プログラミング言語（Esoteric Programming Language、通称esolang）である「お世話」言語のインタプリタです。Webブラウザ上で動作するオフライン版として提供されており、特別な設定なしに手軽に「お世話」言語のコードを実行し、その挙動を確認することができます。

「お世話」言語は、日常生活で使われる丁寧な日本語表現をプログラミングの命令に落とし込むことで、通常のプログラミング言語とは一線を画す体験を提供します。

## 機能
現在の「お世話」言語インタプリタは、以下の機能をサポートしています。

## 1. 変数と値の管理
変数の宣言と値の代入: 数値を格納するための変数を宣言し、値を代入します。

構文例:

お名前は「[変数名]さん」でお願いします。
「[変数名]さん」に [数値] をお渡しします。

## 2. 数値の計算
以下の算術演算が可能です。

掛け算: 変数の値を指定された数値の倍にします。

構文例: 「[変数名]さん」を [数値] 倍にしていただけますでしょうか。

足し算: 変数の値に指定された数値を足し合わせます。

構文例: 「[変数名]さん」に [数値] を足していただけますでしょうか。

引き算: 変数の値から指定された数値を引きます。

構文例: 「[変数名]さん」から [数値] を引いていただけますでしょうか。

割り算: 変数の値を指定された数値で割ります。

構文例: 「[変数名]さん」を [数値] で割っていただけますでしょうか。

剰余 (NEW): 変数の値を指定された数値で割り、そのあまりを元の変数に格納します。

構文例: 「[変数名]さん」を [数値] で割ったあまりを教えていただけますでしょうか。

## 3. 結果の報告（出力）
変数の値の出力: 変数の現在の値を出力します。

構文例: 「[変数名]さん」の値をお聞かせください。

メッセージの出力: 指定されたメッセージをそのまま出力します。

構文例: 「[メッセージ]」とご報告ください。

## 4. 条件による処理の切り替え
特定の条件に応じて処理を分岐させることができます。多層（ネスト）にすることも可能です。

より大きい場合: 指定された変数の値が、ある数値よりも大きい場合に処理を実行します。

構文例: 「[変数名]さん」が [比較数値] よりも大きいかどうか、お教えいただけますでしょうか。

等しい場合 (NEW): 指定された変数の値が、ある数値と等しいかどうかで処理を分岐します。

構文例: 「[変数名]さん」が [比較数値] と同じかどうか、お教えいただけますでしょうか。

条件ブロックの構造:

もし「はい」でございましたら
    ... (条件が真の場合の処理) ...
そうでなければ
    ... (条件が偽の場合の処理) ...
お話は以上でございます。

## 5. 繰り返し処理
指定された回数だけ、同じ処理を繰り返すことができます。

構文例:

[数値] 回繰り返してください。
    ... (繰り返す処理) ...
繰り返しは以上でございます。

## 6. ポインタとメモリ操作 (チューリング完全性)
この言語は、Brainfuckのような低レベルなメモリ操作を模倣したコマンドセットにより、理論上あらゆる計算が可能なチューリング完全性を備えています。

ポインタの移動:

右へ: ポインタを右にずらしていただけますでしょうか。

左へ: ポインタを左にずらしていただけますでしょうか。

ポインタの指すセルの値操作:

値の増加: ポインタの値を増やしていただけますでしょうか。

値の減少: ポインタの値を減らしていただけますでしょうか。

入出力:

セルの値の文字出力: ポインタの値を読み上げていただけますでしょうか。 (現在のセルの値をASCII文字として出力)

文字入力と代入: 入力をお受け取りいただけますでしょうか。 (ユーザー入力の最初の文字のASCII値を現在のセルに代入)

ループ (条件付きジャンプ):

ループ開始: もしポインタの値が0なら、この先へ行っていただけますでしょうか。

ループ終了: ポインタの値が0でなければ、ここへ戻っていただけますでしょうか。

例（「ABC」の出力）:

ポインタの値を増やしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタを右にずらしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタを右にずらしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を読み上げていただけますでしょうか。
ポインタを右にずらしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を読み上げていただけますでしょうか。
ポインタを右にずらしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を読み上げていただけますでしょうか。

## 実行方法
このプロジェクトは単一のHTMLファイルとして提供されています。

このHTMLファイルをWebブラウザで開きます。

表示されたテキストエリアに「お世話」言語のコードを入力します。

「実行していただきます 🚀」ボタンをクリックすると、コードが実行され、結果が下部の「ご報告 (出力結果):」エリアに表示されます。

もしコードの書き方が分からなくなった場合は、テキストエリアにたすけてくださいと入力して実行すると、詳細なヘルプテキストが表示されます。

## 開発環境
フロントエンド: React (CDN経由)

スタイリング: Tailwind CSS (CDN経由)

JSX変換: Babel Standalone (CDN経由)

## 貢献
「お世話」言語の改善や機能追加にご興味がありましたら、ぜひ貢献を検討してください。Lexer、Parser、Evaluatorの各モジュールが独立しているため、新しい命令の追加や既存機能の改善が比較的容易です。

難解プログラミング言語 (Esoteric Programming Language) として
「お世話」言語は、その極めて特徴的な日本語構文と、非効率的でありながらも低レベルなメモリ操作（Brainfuckライクな機能）を組み合わせることで、実用性よりも言語としての概念的な探求や遊び心を重視した、難解プログラミング言語に分類されます。これは、プログラミング言語の多様性と表現の可能性を示す試みです。

# "Osewa" Language Interpreter (Offline Version) 🍵
## Introduction
This project is an interpreter for "Osewa" (meaning "care" or "service" in Japanese) Language, an Esoteric Programming Language (esolang) with a unique Japanese syntax. It's provided as an offline version that runs in a web browser, allowing you to easily execute "Osewa" Language code and observe its behavior without special setup.

"Osewa" Language offers a distinctive programming experience by translating polite Japanese expressions used in daily life into programming commands, setting it apart from conventional programming languages.

## Features
The current "Osewa" Language interpreter supports the following features:

## 1. Variable and Value Management
Variable Declaration and Value Assignment: Declare variables to store numerical values and assign values to them.

Syntax Example:

お名前は「[variable name]さん」でお願いします。 (Please make the name "[variable name]-san".)
「[variable name]さん」に [number] をお渡しします。 (I will hand over [number] to "[variable name]-san".)

## 2. Numerical Calculations
The following arithmetic operations are available:

Multiplication: Multiplies the value of a variable by a specified number.

Syntax Example: 「[variable name]さん」を [number] 倍にしていただけますでしょうか。 (Would you please multiply "[variable name]-san" by [number]?)

Addition: Adds a specified number to the value of a variable.

Syntax Example: 「[variable name]さん」に [number] を足していただけますでしょうか。 (Would you please add [number] to "[variable name]-san"?)

Subtraction: Subtracts a specified number from the value of a variable.

Syntax Example: 「[variable name]さん」から [number] を引いていただけますでしょうか。 (Would you please subtract [number] from "[variable name]-san"?)

Division: Divides the value of a variable by a specified number.

Syntax Example: 「[variable name]さん」を [number] で割っていただけますでしょうか。 (Would you please divide "[variable name]-san" by [number]?)

Modulo (NEW): Stores the remainder of dividing the variable's value by a specified number into the original variable.

Syntax Example: 「[variable name]さん」を [number] で割ったあまりを教えていただけますでしょうか。 (Would you please tell me the remainder when "[variable name]-san" is divided by [number]?)

## 3. Reporting Results (Output)
Output Variable Value: Outputs the current value of a variable.

Syntax Example: 「[variable name]さん」の値をお聞かせください。 (Please tell me the value of "[variable name]-san".)

Output Message: Outputs the specified message as is.

Syntax Example: 「[message]」とご報告ください。 (Please report "[message]".)

## 4. Conditional Processing
Allows branching of processing based on specific conditions. Nested conditions are also possible.

Greater Than: Executes processing if the value of the specified variable is greater than a certain number.

Syntax Example: 「[variable name]さん」が [comparison number] よりも大きいかどうか、お教えいただけますでしょうか。 (Would you please inform me if "[variable name]-san" is greater than [comparison number]?)

Equals (NEW): Branches processing based on whether the value of the specified variable is equal to a certain number.

Syntax Example: 「[variable name]さん」が [comparison number] と同じかどうか、お教えいただけますでしょうか。 (Would you please inform me if "[variable name]-san" is the same as [comparison number]?)

Conditional Block Structure:

もし「はい」でございましたら (If the answer is "Yes")
    ... (Processing if the condition is true) ...
そうでなければ (Otherwise)
    ... (Processing if the condition is false) ...
お話は以上でございます。 (That is all for this conversation.)

## 5. Iterative Processing
Allows repeating the same processing a specified number of times.

Syntax Example:

[number] 回繰り返してください。 (Please repeat [number] times.)
    ... (Processing to be repeated) ...
繰り返しは以上でございます。 (The repetition is over.)

## 6. Pointer and Memory Operations (Turing Completeness)
This language achieves Turing completeness—theoretically capable of any computation—through a command set that mimics low-level memory operations similar to Brainfuck.

Pointer Movement:

Right: ポインタを右にずらしていただけますでしょうか。 (Would you please shift the pointer to the right?)

Left: ポインタを左にずらしていただけますでしょうか。 (Would you please shift the pointer to the left?)

Cell Value Manipulation:

Increment Value: ポインタの値を増やしていただけますでしょうか。 (Would you please increment the pointer's value?)

Decrement Value: ポインタの値を減らしていただけますでしょうか。 (Would you please decrement the pointer's value?)

Input/Output:

Character Output from Cell Value: ポインタの値を読み上げていただけますでしょうか。 (Would you please read aloud the pointer's value?) (Outputs the current cell's value as an ASCII character)

Character Input and Assignment: 入力をお受け取りいただけますでしょうか。 (Would you please receive input?) (Assigns the ASCII value of the first character of user input to the current cell)

Loops (Conditional Jump):

Loop Start: もしポインタの値が0なら、この先へ行っていただけますでしょうか。 (If the pointer's value is 0, would you please go to this point?)

Loop End: ポインタの値が0でなければ、ここへ戻っていただけますでしょうか。 (If the pointer's value is not 0, would you please return to this point?)

Example (Outputting "ABC"):

ポインタの値を増やしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタを右にずらしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタを右にずらしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を読み上げていただけますでしょうか。
ポインタを右にずらしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を読み上げていただけますでしょうか。
ポインタを右にずらしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を増やしていただけますでしょうか。
ポインタの値を読み上げていただけますでしょうか。

## How to Run
This project is provided as a single HTML file.

Open this HTML file in your web browser.

Enter your "Osewa" Language code into the displayed text area.

Click the "実行していただきます 🚀" (Please execute) button to run the code. The result will be displayed in the "ご報告 (出力結果):" (Report (Output Result):) area below.

If you forget how to write code, type たすけてください (Please help me) into the text area and execute it to display detailed help text.

## Development Environment
Frontend: React (via CDN)

Styling: Tailwind CSS (via CDN)

JSX Transformation: Babel Standalone (via CDN)

## Contributing
If you are interested in improving "Osewa" Language or adding new features, please consider contributing. The Lexer, Parser, and Evaluator modules are independent, making it relatively easy to add new commands or enhance existing functionalities.

## As an Esoteric Programming Language
"Osewa" Language is classified as an Esoteric Programming Language because it prioritizes conceptual exploration and playfulness over practicality, by combining its highly distinctive Japanese syntax with low-level memory operations (Brainfuck-like features) that are inefficient yet demonstrate Turing completeness. It stands as an endeavor to showcase the diversity and expressive potential of programming languages.
