# user-skills

Reusable Codex skills maintained by Ligo.

## Available skills

| Skill | Description |
| --- | --- |
| [`zsh-config-summary`](zsh-config-summary/) | Portable Zsh configuration summary for Linux and macOS using Oh My Zsh and Oh My Posh. |

## Install

Clone the repository and copy the skill into the Codex skills directory:

```sh
git clone --depth 1 https://github.com/Ligo04/user-skills.git
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R user-skills/zsh-config-summary "${CODEX_HOME:-$HOME/.codex}/skills/"
```

## Use

Invoke the skill as `$zsh-config-summary`, or ask Codex for a portable Zsh configuration summary.

The skill describes Zsh startup files, the selected Oh My Zsh plugins, and the bundled Oh My Posh prompt. It does not install dependencies or modify shell configuration automatically.

## Skill contents

```text
zsh-config-summary/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── amro.omp.json
```

The bundled prompt uses icon glyphs; a Nerd Font is recommended when applying it to a terminal.
