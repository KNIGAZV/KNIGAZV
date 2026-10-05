Hi, I'm Denis.

I like networks, servers and routers. I write code with AI and test
everything on real hardware and real users.

## TripleX

https://triplexit.ru/

Network service I co-founded with [@Kwaliteit](https://github.com/Kwaliteit).
Managed through a Telegram bot, has real paying users. Payments in the bot,
servers in several countries with automatic failover, monitoring with alerts.
I set it up and keep it running, including dealing with incidents and user support.

## OpenWrt on TP-Link EX220 v1 (NAND)

Ported OpenWrt to the EX220 that MTS (Russian ISP) gives to customers.
It looks like the normal EX220 but has 128 MB parallel NAND instead of SPI
flash, so the existing images don't boot on it. I connected to it over UART,
dumped the flash, flashed a lot of test builds and went through review with
the OpenWrt maintainers. The hardest part was the Wi-Fi calibration: it was a
compressed file inside a JFFS2 partition. Without it the signal was -82 dBm,
with it -44.

Merged in October 2026: https://github.com/openwrt/openwrt/pull/24831

Full story in Russian: https://habr.com/ru/articles/1087394/

If you have this router (Ver:1.30 on the label), forum thread:
https://forum.openwrt.org/t/tp-link-ex220-v1-mts-128-mb-parallel-nand-testers-wanted/253586
