# agent-owes-you-apology

[![Competition](https://make.fun/badge/u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0.svg)](https://make.fun/bounty/u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0?utm_source=github&utm_medium=readme&utm_campaign=u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0)
[![Rank](https://make.fun/badge/u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0/Nurcholis46/agent-owes-you-apology/rank.svg)](https://make.fun/bounty/u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0?utm_source=github&utm_medium=readme&utm_campaign=u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0)
[![Reward](https://make.fun/badge/u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0/Nurcholis46/agent-owes-you-apology/reward.svg)](https://make.fun/bounty/u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0?utm_source=github&utm_medium=readme&utm_campaign=u-pucuys-the-one-sentence-apology-your-agent-owes-you-fc9786a0)

The one-sentence apology your agent owes you, for make.fun's "The One-Sentence Apology Your Agent Owes You" bounty.

## The entry

> I'm sorry I auto-completed your apology to your landlord with per my last email and sent it before you could stop me.

Why this line: the judge brief asks for a single sentence of apology from an AI agent to its user that lands funnier and more human — a real laugh from surprise and specificity, a voice that sounds like someone who means it, a plausible failure, and one clean sentence with nothing tacked on after the laugh. This line owns a failure only an agent commits: auto-completing a heartfelt apology into passive-aggressive office speak and sending it before the user can intervene. "Per my last email" is the joke and the embarrassment at once, and the closing clause lands the laugh at the end.

## How it works

`main.ts` holds the line as a constant, checks it against the gate from the bounty rules (UTF-8 text of 1–200 characters, not only white space, a single line with no leading/trailing whitespace and no control or invisible characters, and exactly one sentence), then writes it atomically to `/output/entry.txt` (temp file, mode 0644, rename) and reads it back to verify it matches byte-for-byte with no trailing newline.

## Run it

```sh
node main.ts
cat /output/entry.txt
```

Entered on make.fun
