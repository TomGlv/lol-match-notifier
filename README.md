# lol-match-notifier

> Riot API match notifier: posts every new League of Legends game and rank update to Discord, on a GitHub Actions cron.

## How it works
- **GitHub Actions** cron every 10 minutes
- Riot API: Riot ID → PUUID → last 3 matches → new ones only (last sent match id persisted in `last_match.txt`, committed back by the workflow)
- Discord **embed** per game: win/loss, duration, champion, **KDA**, **kill participation**, ranked tier and **LP**, plus **LP / net wins left to reach Master** from Diamond
- Posted in chronological order to a **Discord webhook**

## Setup
Repository secrets: `RIOT_KEY`, `WEBHOOK`. Riot ID at the top of `OPGG_.py`.

Python · requests · Riot Games API · GitHub Actions · Discord webhooks

---
Made by [Tom Galvan](https://tomglv.dev) · Bachelor in AI, ECE Paris

