# News Image 21 Nov 2026 — "The World Today"

[![make.fun · news-image-20261121](https://make.fun/badge/news-image-20261121.svg)](https://make.fun/bounty/news-image-20261121?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261121)
[![rank](https://make.fun/badge/news-image-20261121/Dhikas182/news-image-21-nov/rank.svg)](https://make.fun/bounty/news-image-20261121/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261121)
[![reward](https://make.fun/badge/news-image-20261121/Dhikas182/news-image-21-nov/reward.svg)](https://make.fun/bounty/news-image-20261121?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261121)

A make.fun entry for
[news-image-20261121](https://make.fun/bounty/news-image-20261121):
one 1024×1024 image summing up the world news of
**Saturday 21 November 2026**.

## Design

Winner-style layout, learned from the 17 November winner
(50 sourced stories + UTC timeline + date check):

- **Big readable banner date** — `SATURDAY 21 NOVEMBER 2026` in large
  type, legible even at 300 px across.
- **Hero story in large type** — Iran strikes US bases in Bahrain:
  the IRGC claims hits at al-Riffa and Awali; Bahrain reports an
  industrial fire, no casualties.
- **6 headline cards** — two tankers hit near the Strait of Hormuz,
  Mexico capturing FBI most-wanted cartel boss "El Chapo Isidro",
  a Russian missile hitting Kryvyi Rih (2 killed, 60 hurt), US stocks
  sliding into correction (S&P -3.7%, Nasdaq -5.28%), COP31 running
  past its deadline over fossil fuels, and the EU–Indonesia trade deal
  signed after 10 years of talks.
- **42 more stories in three columns** — 49 verified stories in total,
  across every continent and many fields.
- **UTC timeline strip** — the day's key moments from 00:09 to 21:00 UTC.

Every story was individually verified against live reporting dated
21 November 2026 (Reuters, AP, BBC, Al Jazeera, AFP, NPR, UPI, Nature,
Eos). Several items carried by 21 November briefings were checked and
dropped because they happened on earlier days: the ICJ genocide ruling
and the Shenzhen trilateral (19–20 Nov), the UK–EU deal signing
(20 Nov), the FBI database hack and the Palisades arson verdict
(20 Nov), the Riemann hypothesis claim (20 Nov), and GTA VI's first-day
sales (19–20 Nov). See `research-21-nov.md` for the full audit.

Expanded 22 Nov 2026 from 37 to 49 stories: the 19 November entry
(36 stories) missed the top 50 while winners carried 48+ stories, so
12 more verified 21 November stories were added (F1 Las Vegas
qualifying, three Premier League results, France protests and the
Nations Championship final, Bahrain's warning, the Zagreb rally,
the Depardieu/Houellebecq investigation, Estonia's drone alert,
Bournemouth's record win, Japan sidelined at the China summit) and
the brief grid went from two columns to three. Every brief line was
measured in pixels against its 305 px column budget (script-checked,
not hand-counted) after the 20 November entry lost 9 titles to
overflow. The 37-story render is kept as `reference-37.png`.

## Program

`main.py` (Python 3.13, standard library only) draws the image from
scratch: its own 5×7 pixel font, its own PNG writer (zlib + struct),
no network, no fonts, no external files. Two runs write byte-identical
output.

```sh
MAKEFUN_OUTPUT_DIR=out python3 main.py   # writes out/entry.png
```

Output: PNG 1024×1024, 26,736 bytes, sha256
`87fd164fc053e921cede35cc0cfcd10af47564b42e2a19be967eee585dc5918e`.
