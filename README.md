# ⚾ Backyard Baseball — Dogers vs Yeeters

A cartoon, Backyard-Baseball-style game that plays by the real rules of baseball.
It's a single self-contained HTML file — **no build, no dependencies**.

## ▶️ How to play

Just open `index.html` in any modern browser (double-click it, or
`File → Open`). That's it.

1. Click **▶ Play Ball!** to start.
2. When **your** team (the 🔵 Dogers) is batting, click **🎯 Pitch** to send
   the pitch in.
3. Hit **SPACE** (or tap/click the field) to **SWING**.
4. **Timing is everything** — connect right as the ball crosses the plate:
   - 🎯 **Perfect** → 💥 home run
   - 🟢 **Good** → single / double / triple
   - 😬 **Slightly off** → weak grounder, fly out, or foul
   - 💨 **Way off / chasing junk** → whiff
5. The 🟠 **Yeeters** bat automatically (CPU) when they're up.

A little white marker sweeps the **swing meter** at the bottom of the field —
swing when it's in the gold "PERFECT" zone.

## 🧢 The full roster on the field

Every defensive position is drawn on the diamond, just like real baseball:

- **Pitcher** (with wind-up + follow-through animation)
- **Catcher** crouched behind the plate with a mitt
- **Umpire** standing behind the catcher (mask + chest protector)
- **1B, 2B, 3B, Shortstop**, and **Left / Center / Right** fielders
- The **batter** at the plate with a full swing animation
- Base **runners** that round the bags when you get a hit

## 🧤 Live fielding (it plays itself out)

Once the ball is struck, nothing is pre-decided — the play is **simulated**:

- The nearest fielder **runs** toward the ball (you'll see them sprint across
  the grass).
- Fly balls, line drives and pop-ups can be **caught in the air** for a
  **flyout / lineout / popout** — if a fielder gets there in time.
- Grounders are **fielded** and **thrown to first base**; whether you're out or
  safe comes from a real timing race: fielder distance + throw time vs. how fast
  the runner legs it out.
- Balls into the gaps drop for **singles, doubles, and triples** depending on
  how deep they land and how long the throw back takes.
- The ball is drawn with a **shadow + height arc**, so you can read fly balls
  vs. grounders.

### Double plays, assists & tag outs

- **Double plays** — a grounder with a runner on first and fewer than two outs
  can be turned 6-4-3 style: force at second, relay to first.
- **Force outs** — the lead forced runner (or the batter at first) is retired
  when the throw beats them to the bag.
- **Outfield assists / tag outs** — get greedy on the bases and an outfielder
  will gun you down: runners are thrown out trying to take an extra base, and
  batters are nailed trying to **stretch** a single into a double.
- Runners hold up on catchable fly balls; runs don't count when the third out
  is a force out — just like the real rules.

## 📋 Baseball rules implemented

- Balls & strikes count (4 balls = walk, 3 strikes = strikeout)
- Fouls count as strikes (but never the third strike)
- 3 outs end a half-inning, teams switch
- Forced runner advancement on walks (incl. bases-loaded RBI walk)
- Runners advance by the number of bases on a hit; runs score from 3rd/home
- **3 innings** (top = Yeeters, bottom = Dogers), then the game is called

## 🪵 DIY scoreboard

A hand-made plywood-and-nails box score under the field tracks runs by inning
plus the total for each team, with glowing light-bulb **B / S / O** count
indicators — built in pure HTML/CSS to look like something nailed together in
the backyard.

## 🎨 Tech

Plain HTML5 `<canvas>` + vanilla JavaScript + CSS. No frameworks, no assets to
download — everything (players, field, scoreboard) is drawn in code.
