# design-brief

> Claude Code skill — Visual design direction for Remotion presentations

Remotion プレゼンテーションのビジュアルデザイン方向性を決めるスキル。コンテンツのアウトラインを読み、感情の流れとビジュアルメタファーを分析して 2〜3 案のデザイン方向性（配色・書体・アニメーション言語・ムード）を提示する。

## What it does

1. コンテンツアウトラインを読んでテーマと感情の流れを把握
2. 2〜3 案のデザイン方向性を提案（配色・書体・アニメーション言語・ムード）
3. 選ばれた案をもとに `tech/remotion/src/themes/<name>.ts` を生成

## Installation

```
/plugin install design-brief@eruto-skills
```

## Usage

```
/design-brief [content-outline file path, or presentation description]
```

## License

MIT
