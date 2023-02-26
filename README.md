CPU実験2022 1班のシミュレータです。
命令単位実行/float命令の修正に未対応/命令メモリとデータメモリの分割に未対応

ビルド:

% make


使用方法：

1. "samples"というディレクトリの中に機械語コードを置く  例: minrt_1st.dat

2. "input"というディレクトリの中に入力ファイルを置く  例: contest.bin

3. 以下のコマンドを実行で起動

    % ./test program_name input_file_name

    例: % ./test minrt_1st contest.bin

4. シミュレータを起動すると、以下のような質問が行われます。

    stdout?   y/n
    logfile?  y/n
    uart?     y/n

    minrt_1stを実行する際は、上から順に n, n, y と答えてください。


注意事項等:

1. 入力ファイルは省略できますが、その状態で入力ファイルを必要とするプログラムを実行すると実行が停止しません。

2. プログラム名の代わりに"#disasm"と入力すると、ディスアセンブラが起動します。

    % ./test #disasm
    filename?

    ファイルの名前を聞かれるので、"samples"内のプログラムから選んで入力してください(拡張子は不要です)