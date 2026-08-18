# Hide Gameview Settings

CSS Loader theme to hide the per-game
**Manage / Settings gear** on a game's Gameview page.

You can still access the per-game settings from the main home screen.

## Install

1. Switch your Steam Deck to Desktop Mode.
2. Extract the `Hide Gameview Settings` folder into:

   `/home/deck/homebrew/themes/`

3. Return to Gaming Mode.
4. Open Quick Access (`...`) -> Decky -> CSS Loader.
5. Refresh/reload themes if needed.
6. Enable **Hide Gameview Settings**.

## Notes

- The theme injects only into Steam's main Big Picture (`SP`) window.
- It scopes the rule to the game-details play section.
- Manifest v9's `REQUIRE_NAV_PATCH` is enabled so a hidden focusable
  control should also be skipped by controller navigation.
- The primary selector uses Steam's mapped CSS class for the Gameview play
  section plus semantic labels (`Manage`, `Manage Game`, `Settings`).

## If your Steam language is not English

Steam may localize the button's accessibility label. If the gear does not
disappear, use Decky's Remote CEF Debugging to inspect the gear and replace
or add its `aria-label`, `title`, or `data-tooltip-text` value in `shared.css`.
