# Points or Cash

A one-page calculator that tells you whether to book a hotel room with points or pay cash.

## How it works

1. Pick a program: Hyatt, IHG, Bonvoy or Hilton.
2. Enter the room's cash price (all-in, with taxes and fees) and the points needed for the same stay.
3. The page works out the value you'd get per point:

   `cents per point = cash price × 100 ÷ points`

   and compares it with your own value for that program.

| Verdict | Colour | When |
|---|---|---|
| Book on points | Green | Redemption is 10% or more above your value |
| Close call | Orange | Within 10% of your value, either way |
| Pay cash | Red | Redemption is 10% or more below your value |

## Point values

The values live in the `REGISTER` list near the top of the script in `index.html`:

| Program | Value per point |
|---|---|
| Hyatt | 1.65¢ |
| Bonvoy | 0.8¢ |
| IHG | 0.6¢ |
| Hilton | 0.4¢ |

To change one, edit its `centsPerPoint`. To add a program, add a line to the list. The close-call band is `CLOSE_CALL_PCT` (10 by default).

## Running it

It's a single HTML file with no build step. Open `index.html` in a browser, or turn on GitHub Pages for this repo (Settings → Pages → Deploy from branch `main`, folder `/`).
