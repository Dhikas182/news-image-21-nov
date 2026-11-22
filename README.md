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
- **30 more stories in two columns** — 37 verified stories in total,
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

## Program

`main.py` (Python 3.13, standard library only) draws the image from
scratch: its own 5×7 pixel font, its own PNG writer (zlib + struct),
no network, no fonts, no external files. Two runs write byte-identical
output.

```sh
MAKEFUN_OUTPUT_DIR=out python3 main.py   # writes out/entry.png
```

Output: PNG 1024×1024, 27,546 bytes, sha256
`d5616b81b2db22f138e2ff497dc4e0f5327631ff3ec7bd6a7e8f2732975f4f82`.
