# LR2021 radio firmware

What the LR2021 radio boards fetch for themselves over WiFi.  Public so a board
can read it with no credential.  `firmware.txt` is the index; its header documents it.

A board OFFERS a newer build on its screen and installs only when somebody
presses UPDATE; the new image boots on trial and rolls back by itself unless
it hears the other board or reaches this server within three minutes.

| version | built | label | size | file | notes |
| --- | --- | --- | ---: | --- | --- |
| **v0.1.23** | 2026-09-18 21:25 | `0.1.23+7b8327b` | 6.20 MB | `lr2021-ws43/app-0.1.23+7b8327b-f23b22ad.bin` | Update-Pfad: ein abgebrochenes Funk-Update blockiert den Slot nicht mehr; ein fehlgeschlagener Download wird nicht sofort endlos wiederholt |
| **v0.1.22** | 2026-09-18 17:38 | `0.1.22+deaed6e` | 6.20 MB | `lr2021-ws43/app-0.1.22+deaed6e-1b2b4310.bin` | WLAN-Update repariert: der Download wartete auf sein eigenes Ende (blieb bei 0 kB stehen) |
| **v0.1.21** | 2026-09-18 16:11 | `0.1.21+664caad` | 6.20 MB | `lr2021-ws43/app-0.1.21+664caad-219ca35e.bin` | Headset-Mikrofon: der Pegelregler dreht in den Sprechpausen nicht mehr auf (erstes Wort nach... |
| **v0.1.20** | 2026-09-18 14:26 | `0.1.20+81bb4ab` | 6.20 MB | `lr2021-ws43/app-0.1.20+81bb4ab-85967781.bin` | Auto zu Auto: S2 wird nicht mehr nach einer einzelnen schwachen Messung verlassen (3 Bericht... |
| **v0.1.19** | 2026-09-17 10:14 | `0.1.19+565d371-dirty` | 6.15 MB | `lr2021-ws43/app-0.1.19+565d371-dirty-a551967d.bin` | Margin RSSI>floor+20, fair probe loss, OTA policy, SD re-open+CRC, BT bonds, VR card, log tools |

The 5 newest are listed and offered, and they are all this repository holds: every publish
replaces its git history with a single commit.
Each board keeps every image it has run on its own card.
