# honey world format 🐝🍯

The honey world format is a new Minecraft world storage format heavily inspired by the [Slime world format created by Hypixel](https://hypixel.net/threads/dev-blog-5-storing-your-skyblock-island.2190753/).
It aims at simplicity (meaning not storing anything unimportant) but also completeness (meaning including everything important like entities).
This results in a much more compact file size comparing to the legacy Anvil world format, especially because more modern technology is used (we use zstd while Anvil uses zlib which is much less performant).

**Latest version:** [`0x0001`](./versions/0x0001.md)