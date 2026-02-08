# 臺語（全羅，白話字kap臺羅）ê詞性標記家私，使用 stanford-postagger

## 需要ê家私
 - python3
 - [stanford-postagger](https://nlp.stanford.edu/software/tagger.html) - full-2020-11-17 版本

## 重要 ê檔案
 - taigi.tagger.props：tagger屬性檔
 - taigi-tagged.txt：訓練模型用
 - taigi-test.txt：測試輸出入

## Án-nuá使用

 - kā `model-taigi` 囥佇`stanford-postagger-full-2020-11-17`資料鋏á內底
 - 轉換TL/POJ成做通訓練ê格式：`preprocess.py raw-taigi-input.txt > taigi-test.txt`
 - 訓練詞性標註：
  `java -classpath stanford-postagger.jar edu.stanford.nlp.tagger.maxent.MaxentTagger -prop models/taigi.tagger.props -model models/taigi.tagger -trainFile models-taigi/taigi-tagged.txt`
 - 測試輸入結果：`./stanford-postagger.sh models/taigi.tagger models/taigi-test.txt`

## 訓練ê語料
 - 巴克禮臺語譯本：
   - 約翰福音
   - TODO
 - 教育部辭典ê語料（無一定，TODO）

## 授權

 - 暫時毋知

## 詞性標記列表（暫定）
    
- |     |     |     |
    | --- | --- | --- |
    | 名詞  | \_NN |     |
    | 專有名詞 | \_PROP |     |
    | 姓氏  | \_SU |     |
    | 動詞  | \_VB |     |
    | 數詞  | \_NU |     |
    | 形容詞 | \_JJ |     |
    | 量詞  | \_CL |     |
    | 代詞  | \_PRON |     |
    | 全變調副詞 | \_ADV1 |     |
    | 部分變調副詞 | \_ADV2 |     |
    | 介詞  | \_PREP |     |
    | 連詞  | \_CO |     |
    | 助詞  | \_PA |     |
    | ê助詞  | \_E5 |     |
    | 嘆詞  | \_IN |     |
    | 擬聲擬態詞 | \_ON |     |
    | 標點符號 | \_PU |     |
    | 指示形容詞 | \_DT |     |
