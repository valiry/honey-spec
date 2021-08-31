# honey world format 🐝🍯

The honey world format is a new Minecraft world storage format heavily inspired by the [Slime world format created by Hypixel](https://hypixel.net/threads/dev-blog-5-storing-your-skyblock-island.2190753/).
It aims at simplicity (meaning not storing anything unimportant) but also completeness (meaning including everything important like entities).
This results in a much more compact file size comparing to the legacy Anvil world format, especially because more modern technology is used (we use zstd while Anvil uses zlib which is much less performant).

**Latest version:** [`0x0002`](./versions/0x0002.md)

## Note for Minecraft 1.18+

Since Minecraft 1.18 the height of a chunk grew from **256 to 384** which conflicts with honeys current implementation of chunks (to be more specific: honey only supports **16 sections, each with a height of 16 blocks**, resulting in a maximum storable chunk height of **16\*16 = 256** blocks).
This is due to the **2 byte** big bitmask (= 16 bits) representing whether or not specific sections are populated.
Thus, **Minecraft 1.18 worlds are currently NOT supported**!
If the need arises we will fix this by officially increasing the size of this bitmask to **3 instead of 2 bytes**.