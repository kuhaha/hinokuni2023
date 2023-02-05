## テキスト解析及び機械学習による卒業研究テーマトレンドの可視化
### 1. テキスト解析（word_wakati.py）`
- `word_seq(text, parser=None)`
- `create_parser(worker='janome', parts_of_speech=['名詞'],stop_words=[])`
1. 日本語文字列textに対し形態素解析器Janome/MeCabによって形態素解析を行う
2. 指定品詞を抽出
3. 不要語、記号を削除
4. 上記で得られた単語をリストで返す

### 2. 卒業論文題目における単語出現頻度の可視化（wordcloud.ipynb）
1. 卒業論文題目一覧表(.csv)を読み込み, pandas.DataFrameに保存
2. 対象年度、対象研究室を指定
3. 不要語、品詞を指定
4. 集計対象年度範囲を指定
5. 研究室・年度範囲の題目をリストとして抽出
6. `word_seq()`を呼び出して解析し、単語リストをスペース区切りで再び文字列化
　<br>例えば "**自律走行ロボットの制御方法に関する研究**"->"**自律..走行..ロボット..制御..方法..関する..研究**"
7. nlpotで出現頻度を調査し、WordCloud、Unigram図で可視化
### 3. ThemeRiverによるテーマ変遷トレンドの可視化（themeriver.ipynb）

