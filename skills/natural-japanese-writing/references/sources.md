# 設計根拠と参考資料

最終確認日: 2026-10-01

このSkillは、日本語の自然さを固定的な禁止語や文長規則へ還元せず、意味保持、意味関係の復元可能性、文脈適合、書き手の声の保持を分けて扱う。

## 多言語LLMと翻訳調

### Guo et al. (2024), “Do Large Language Models Have an English ‘Accent’?”

https://arxiv.org/abs/2410.15956

英語中心の多言語LLMが、非英語出力で英語的な語彙・構文傾向を示す問題を扱う。主な対象言語は日本語ではないため、日本語への直接的な実証とはみなさない。

本Skillでは、「文法的に成立すること」と「その媒体や分野の日本語として自然に読めること」を分ける根拠として参照する。

### Gao and Das (2024), “Customizing Language Model Responses with Contrastive In-Context Learning”

https://arxiv.org/abs/2401.17390

好ましい例と避けたい例の対照から、説明しにくい文体上の差を伝える方法を扱う。

## 日本語の表記と翻訳品質

### 日本翻訳連盟, 「JTF日本語標準スタイルガイド（翻訳用）」

https://www.jtf.jp/tips/styleguide

和訳時の表記統一に使える外部基準。表記統一自体を本Skillの標準動作にはせず、ユーザーや文書が明示的に特定の表記規則を求める場合に使う。

### 日本翻訳連盟, 「JTF翻訳品質評価ガイドライン」

https://www.jtf.jp/tips/translation_quality_guidelines

翻訳品質を単一の「自然さ」だけで評価せず、正確さ、用語、用途への適合などを分けて扱う考え方の参考にした。

## 意味構造とAI生成文の編集に関する比較資料

### nanaism/yomiyasu

https://github.com/nanaism/yomiyasu

AI生成日本語について、主述関係、非生物主語、抽象的な動詞、名詞化、指示語、装飾などを具体的に診断するSkill。問題を表層語の置換だけでなく文の構造として扱う点を比較対象にした。

### Zenn, 「AIが生成する『不自然な日本語』をどう直すか」に関する解説

https://zenn.dev/algoartis/articles/0b1c731881b25c

単語レベルの置換だけでは、不自然な抽象表現を別の抽象表現へ移すだけになるという問題意識を参考にした。

本Skillではこの着想を一般化し、述語が表す動作・状態・失敗モード、照応、因果、限定を読み手が復元できるかを確認する。
