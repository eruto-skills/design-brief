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

## Codex / Claude Code installation

This package supports both Codex and Claude Code. The plugin entry point is
`skills/design-brief/SKILL.md`; the root `SKILL.md` remains the standalone source.

For Codex, add the public `eruto-skills` marketplace in the plugin UI using
`https://github.com/eruto-skills/marketplace`, then install `design-brief`.
To install as a standalone user skill instead:

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/eruto-skills/design-brief.git ~/.agents/skills/design-brief
```

On Windows PowerShell:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE/.agents/skills" | Out-Null
git clone https://github.com/eruto-skills/design-brief.git "$env:USERPROFILE/.agents/skills/design-brief"
```

In Codex, select the installed skill by name or invoke `$design-brief` with a task.
In Claude Code:

```text
/plugin marketplace add eruto-skills/marketplace
/plugin install design-brief@eruto-skills
```

The instructions use the tools available in the current host. Scripts are resolved
from the actual skill directory, rather than a fixed author path. Additional browser,
Python, or format-specific dependencies are described in `SKILL.md` and the references;
installing the plugin alone does not install those external programs.

## Maintaining the plugin package

Edit the root `SKILL.md` and its supporting resources, then run:

```bash
node scripts/package-plugin.mjs
node scripts/package-plugin.mjs --check
```

Commit the generated `skills/` files with the source changes. CI checks that both
layouts match, including the Claude manifest. Do not edit generated files directly.
