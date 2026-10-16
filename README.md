# Hayate — LLM で変換する Mac の日本語入力

Hayate（ハヤテ）は、Mac 用の日本語入力（IME）です。かな漢字変換の候補は、アプリに同梱した自前の言語モデル（ローカル LLM）が、前の文といま打っている文を読んで選びます。モデルは Mac の中で動くので、変換のために打った文を外へ送りません。

- サイト: https://hayate.im/
- 概要: https://hayate.im/about/
- 動作環境: macOS 15 以降・Apple Silicon 搭載の Mac
- 料金: 無料版あり（いまはベータ版）

## 入れ方

```sh
brew install --cask hayate-ime/hayate/hayate
```

または https://hayate.im/docs/install/ から .pkg をダウンロードしてください。

## できること

- **変換キーを押さない** — 打った端から漢字になり、手を止めるとその一瞬で文全体が見直されます。Space で変換する打ち方にも切り替えられます
- **同音語の使い分け** — 清算と精算のように迷う字は、候補の下に使い分けが 1 行出ます
- **校正** — ら抜き・重ね言葉・慣用句の誤りを、打ったその場で指摘します
- **書き直し・返事の提案** — ⌃⇧R で直前の 1 文を仕事の文面に直し、空の入力欄では返事の案を並べます
- **音声入力** — ⌥⇧V で話した言葉が文になります。認識は Mac の中で行います
- **業界の言葉・組織の辞書** — 医療などの専門の語、社内の共有用語辞書と表記ルール（有料プラン）

## LLM で変換するしくみ

辞書が読みから候補を出し、ChatGPT などの LLM と同じ種類の、文の続きを予測する言語モデルが、文として自然なものを選びます。モデルはかな漢字変換のために自前で学習し、Mac の中で速く動く大きさにしてアプリに入れています。ネットワークが無くても変換できます。

データの行き先と保存するものは https://hayate.im/security/ にまとめています。

## 不具合・要望

[Issues](https://github.com/hayate-ime/hayate-mac/issues) か、https://hayate.im/contact/ へお寄せください。

このリポジトリは窓口で、Hayate のソースコードは置いていません。

---

**English:** Hayate is a Japanese input method (IME) for macOS that uses an on-device language model (local LLM) to pick kana–kanji conversion candidates from the surrounding text. Conversion runs entirely on your Mac. Requires macOS 15+ on Apple Silicon. Install with `brew install --cask hayate-ime/hayate/hayate` or from https://hayate.im/.
