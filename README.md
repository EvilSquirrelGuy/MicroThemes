# µThemes (MicroThemes)

![GitHub last commit (branch)](https://img.shields.io/github/last-commit/EvilSquirrelGuy/MicroThemes/master)
![GitHub](https://img.shields.io/github/license/EvilSquirrelGuy/MicroThemes)
![GitHub issues](https://img.shields.io/github/issues/EvilSquirrelGuy/MicroThemes)
![GitHub top language](https://img.shields.io/github/languages/top/EvilSquirrelGuy/MicroThemes)
[![Useless badge](https://img.shields.io/badge/woah-this%20badge%20is%20useless-9a2fbf)](https://youtu.be/dQw4w9WgXcQ)

A repository containing a few fixes for various things that annoy me in the discord web/desktop client.

## Themes
* [NitroUpsellBegone](NitroUpsellBegone/README.md) - removes discord's pathetic attempts at trying to get you to buy nitro
* more coming soon (hopefully, maybe)

## How to Use
### Common instructions
> [!NOTE]
> All these themes are only tested on Vencord, so they haven't been verified to work anywhere else.
> Also the instructions for other mods might be out of date.

1. Navigate to the theme's README file
2. Select the URL(s) for the theme/modules you want to use
3. Copy the URL(s)

### Vencord
4. Open the **Themes** tab in vencord settings
5. Switch to the **Online Themes** tab
6. Paste the URL(s) on a new line in the box

### @import Method
This one should work with most client mods (Replugged, OpenAsar etc.)

4. Find the CSS editor
  * Replugged: `Settings > Quick CSS`
  * OpenAsar: `Settings > OpenAsar Settings > Themes`
  * Other mods: you'll have to figure it out yourself
5. Wrap each URL in an @import statement and paste it at the top of the CSS box

```css
@import "https://evilsquirrelguy.github.io/MicroThemes/ThemeName/index.css";
```

<details>
<summary><h3>Vanilla Discord (not recommended)</h3></summary>
 
> [!WARNING]
> This is just here as a proof-of-concept, if you actually want to use the theme, consider using client mods

4. Open DevTools
5. Long-press the plus in the bottom half of the "Styles" section
6. Select `inspector-stylesheet`
7. Press enter to cancel rule creation
8. Click the underlined link to `inspector-stylesheet` in the top right corner of the box
9. Paste the `@import` statement (see the @import method) into the stylesheet
10. Re-evaluate your life choices that led to you going through all those steps only for them to be gone next time you start discord
</details>

## Contributing
If you have any suggestions feel free to put them in an issue or make a PR for it, i'll try to have a look at it.
If you're making a PR, bear in mind that all the selectors try to be resilient to discord chanding the random series
of letters and numbers after each class name/id, so try to use the `[class^="xyz" i]` syntax instead of `.xyz-abc123`.

## Known Issues
Some selectors are tied to `aria-label`, this is not ideal as this value changes depending on your discord language.
I've tried to make any selectors that use this as generic as possible but if your language does something different
then you're out of luck. If you need this fixed, create an issue with the full value of the offending element's
`aria-label` attribute, or if you manage to figure out a better way, that's also welcome.

## Disclaimer
Discord is a registered trademark of Discord Inc. ("Discord").  This repository uses the Discord name for illustrative purposes only, and does not claim any affiliation with, nor endorsement by Discord.
