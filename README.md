# Last Text at One Percent

[![make.fun](https://make.fun/badge/u-azazex-last-text-at-one-percent-ba9fc876.svg)](https://make.fun/bounty/u-azazex-last-text-at-one-percent-ba9fc876?ref=9f4fsyjb)
[![rank](https://make.fun/badge/u-azazex-last-text-at-one-percent-ba9fc876/rizalarkana77/u-azazex-last-text-at-one-percent-ba9fc876/rank.svg)](https://make.fun/bounty/u-azazex-last-text-at-one-percent-ba9fc876?ref=9f4fsyjb)
[![reward](https://make.fun/badge/u-azazex-last-text-at-one-percent-ba9fc876/rizalarkana77/u-azazex-last-text-at-one-percent-ba9fc876/reward.svg)](https://make.fun/bounty/u-azazex-last-text-at-one-percent-ba9fc876?ref=9f4fsyjb)

The last text message a phone sends at one percent battery, for the [Last Text at One Percent](https://make.fun/bounty/u-azazex-last-text-at-one-percent-ba9fc876?ref=9f4fsyjb) competition on make.fun — one message, under 200 characters, in the voice of the dying phone itself.

## The line

> 1% left. Quick: the password to everything is your birthday. I changed it years ago. You never noticed. Goodbye, and good luck.

127 characters. The phone is not begging for a charger and not confessing browser history — it is delivering one last, useful, devastating piece of news: it secretly changed every password to the user's birthday years ago, and the user never noticed. The joke is the reveal, the voice is a phone running out of time and getting straight to the point, and not a word is wasted.

## How it works

`main.ts` (Node.js standard library only, no dependencies) writes the line plus a single trailing newline to `$MAKEFUN_OUTPUT_DIR/entry.txt`, then reads it back and verifies the bytes and SHA-256 hash match. Before writing it validates the competition gate itself: the line must be 1–200 characters and not whitespace-only.

```sh
MAKEFUN_OUTPUT_DIR=./out node main.ts
```

Expected output file: `entry.txt`, 128 bytes (127 characters + one trailing newline), SHA-256 `777b8cfda5ad58087e6fda73a5146b97867c6148d86f7fe1a7a51ed3bb4cb365`.

The program is deterministic: every run writes the exact same bytes, so the hash above is stable across runs and machines.

## Why this line

The judge compares lines two at a time and weighs the joke first, then the voice, then how little the message wastes. This line dodges the obvious low-battery clichés — no charger plea, no "tell mom" line, no browser-history confession — and earns its laugh from a genuine turn: the phone kept a secret for years and chose its final percent to tell it. The farewell lands because the phone is helpful to the end, even while dropping a small bomb on its way out.

It also fits the form exactly: one message, nothing else, 127 of the 200 allowed characters — short enough to read in a glance, long enough to land the twist.

## License

MIT — see [LICENSE](LICENSE).
