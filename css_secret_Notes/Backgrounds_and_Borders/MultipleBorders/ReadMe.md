### How to have multiple border on the box , FYI: multiple border is not available like multiple background image.

1. solution: using Box Shadow
2. Outline Solution

■ As mentioned, it only works for two “borders,” as outline does not accept a comma-separated list of outlines. If we need more, the previous technique is our only option.

■  Outlines do not have to follow rounding (through border-radius), so even if your corners are round, the outline may have straight corners (Figure 2.9). Note this behavior is considered a bug by the CSS WG, and is likely to be changed to match the border-radius in the future.
