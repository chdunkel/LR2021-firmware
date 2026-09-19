# LR2021 radio firmware

What the LR2021 radio boards fetch for themselves over WiFi.  Public so a board
can read it with no credential.  `firmware.txt` is the index; its header documents it.

A board OFFERS a newer build on its screen and installs only when somebody
presses UPDATE; the new image boots on trial and rolls back by itself unless
it hears the other board or reaches this server within three minutes.

| version | built | label | size | file | notes |
| --- | --- | --- | ---: | --- | --- |
| **v0.1.24** | 2026-09-19 11:20 | `0.1.24+60baa72` | 6.21 MB | `lr2021-ws43/app-0.1.24+60baa72-d2466b46.bin` | S2 held to where the radio really stops (margin drop 8 dB, climb 13 dB, climb bar learned from counted loss); S8 carries whole messages (LDRO, tier table v9 - update BOTH boards; end-of-talk timer floored from the sender's own pauses); faster fall-back and climb; Pc bench power ceiling; Wm foreign-LoRa listen |
| **v0.1.23** | 2026-09-18 21:25 | `0.1.23+7b8327b` | 6.20 MB | `lr2021-ws43/app-0.1.23+7b8327b-f23b22ad.bin` | Update-Pfad: ein abgebrochenes Funk-Update blockiert den Slot nicht mehr; ein fehlgeschlagen... |
| **v0.1.22** | 2026-09-18 17:38 | `0.1.22+deaed6e` | 6.20 MB | `lr2021-ws43/app-0.1.22+deaed6e-1b2b4310.bin` | WLAN-Update repariert: der Download wartete auf sein eigenes Ende (blieb bei 0 kB stehen) |
| **v0.1.21** | 2026-09-18 16:11 | `0.1.21+664caad` | 6.20 MB | `lr2021-ws43/app-0.1.21+664caad-219ca35e.bin` | Headset-Mikrofon: der Pegelregler dreht in den Sprechpausen nicht mehr auf (erstes Wort nach... |
| **v0.1.20** | 2026-09-18 14:26 | `0.1.20+81bb4ab` | 6.20 MB | `lr2021-ws43/app-0.1.20+81bb4ab-85967781.bin` | Auto zu Auto: S2 wird nicht mehr nach einer einzelnen schwachen Messung verlassen (3 Bericht... |

The 5 newest are listed and offered, and they are all this repository holds: every publish
replaces its git history with a single commit.
Each board keeps every image it has run on its own card.
