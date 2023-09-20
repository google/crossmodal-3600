Automatic translations of CC3M and COCO into the following 34 Languages: Arabic
(ar), Bengali (bn), Chinese-Simplified (zh), Croatian (hr), Czech (cs), Danish
(da), Dutch (nl), Filipino (fil), Finnish (fi), French (fr), German (de), Greek
(el), Hebrew (he), Hindi (hi), Hungarian (hu), Indonesian (id), Italian (it),
Japanese (ja), Korean (ko), Maori (mi), Norwegian (no), Persian (fa), Polish
(pl), Portuguese (pt), Romanian (ro), Russian (ru), Spanish (es), Swahili (sw),
Swedish (sv), Telugu (te), Thai (th), Turkish (tr), Ukrainian (uk), Vietnamese
(vi).

LICENSE CC-BY-4.0: See https://creativecommons.org/licenses/by/4.0/

## Attribution

```
@inproceedings{ThapliyalCrossmodal2022,
  author = {Ashish Thapliyal and Jordi Pont-Tuset and Xi Chen and Radu Soricut},
  title = {{Crossmodal-3600: A Massively Multilingual Multimodal Evaluation Dataset}},
  booktitle = {EMNLP},
  year = {2022}
}
```

The original captions are from:
[Conceptual Captions (CC3M)](https://ai.google.com/research/ConceptualCaptions/download)
and
[COCO Captions](http://images.cocodataset.org/annotations/annotations_trainval2014.zip).

## Format

The translations are in JSONL format, where each line of the file is a
JSON-encoded object with:

-   `image_id`: Unique identifier of each image
-   `src_lang`: Source language
-   `trg_lang`: Target language
-   `caption_tokenized`: Original caption, tokenized
-   `translation_tokenized`: Translated caption, tokenized
-   `backtranslation_tokenized`: Back-translated caption, tokenized. These are
    provided to allow for a rough estimation of the translation quality.

## Statistics

Dataset    | Size
---------- | -----------
coco-dev   | 850,000
coco-train | 19,258,790
cc3m-dev   | 538,560
cc3m-train | 112,824,580

BLEU-4 scores calculated using sacre-bleu with `reference=caption_tokenized`,
`hypothesis=backtranslation_tokenized`, and `tokenization=none`.

LangId        | ar    | bn    | cs    | da    | de    | el    | es    | fa    | fi    | fil   | fr    | he    | hi    | hr    | hu    | id    | it    | ja    | ko    | mi    | nl    | no    | pl    | pt    | ro    | ru    | sv    | sw    | te    | th    | tr    | uk    | vi    | zh
------------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ---
BLEU coco-dev | 47.12 | 51.20 | 56.40 | 70.51 | 59.02 | 66.73 | 68.04 | 47.54 | 50.24 | 65.72 | 67.01 | 51.71 | 53.59 | 56.56 | 54.02 | 49.96 | 68.18 | 44.08 | 43.76 | 45.63 | 67.31 | 70.82 | 52.35 | 68.59 | 66.02 | 45.93 | 72.20 | 49.18 | 48.79 | 29.88 | 52.46 | 49.62 | 50.07 | 35.67
BLEU cc3m-dev | 44.62 | 45.24 | 54.40 | 68.45 | 54.13 | 61.42 | 61.87 | 42.19 | 50.19 | 60.58 | 61.05 | 49.63 | 47.76 | 54.03 | 51.11 | 46.25 | 61.38 | 37.67 | 35.51 | 38.47 | 67.25 | 67.99 | 50.59 | 62.16 | 61.52 | 45.97 | 68.20 | 46.50 | 44.84 | 30.53 | 49.86 | 48.83 | 44.76 | 30.57
