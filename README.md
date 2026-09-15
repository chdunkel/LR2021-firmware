# LR2021 radio firmware

What the LR2021 radio boards fetch for themselves over WiFi.  Public so a board
can read it with no credential.  `firmware.txt` is the index; its header documents it.

A board OFFERS a newer build on its screen and installs only when somebody
presses UPDATE; the new image boots on trial and rolls back by itself unless
it hears the other board or reaches this server within three minutes.

| version | built | label | size | file | notes |
| --- | --- | --- | ---: | --- | --- |
| **v0.1.16** | 2026-09-15 05:23 | `0.1.16+565d371-dirty` | 6.01 MB | `lr2021-ws43/app-0.1.16+565d371-dirty-b977667a.bin` | Board kept checking for updates after a radio file pull, pull abort fixed, pulls stay on S2, baby safety |
| **v0.1.15** | 2026-09-15 03:30 | `0.1.15+565d371-dirty` | 5.99 MB | `lr2021-ws43/app-0.1.15+565d371-dirty-458bf12d.bin` | Crash fix (clock read under a spinlock, hit v0.1.14), call delay -80 ms, SD card retry and g... |
| **v0.1.14** | 2026-09-14 22:01 | `0.1.14+565d371-dirty` | 5.76 MB | `lr2021-ws43/app-0.1.14+565d371-dirty-77f311ba.bin` | Faster startup: radio up at 1.4 s, linked on S2 at 1.9 s; no split on a far restart |
| **v0.1.13** | 2026-09-14 21:13 | `0.1.13+565d371-dirty` | 5.76 MB | `lr2021-ws43/app-0.1.13+565d371-dirty-dfc6e3ea.bin` | Two talkers handled cleanly, no S8 detour after reboot, call buffer, mic race fix, 8 MB build |
| **v0.1.12** | 2026-09-14 20:21 | `0.1.12+565d371-dirty` | 5.76 MB | `lr2021-ws43/app-0.1.12+565d371-dirty-a9332822.bin` | Faster S2 after reboot, bench remote control, 8 MB slot move, rotate crash & TALK rows fixed |

The 5 newest are listed and offered, and they are all this repository holds: every publish
replaces its git history with a single commit.
Each board keeps every image it has run on its own card.
