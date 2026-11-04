# Modular 10" Mini Rack: Bambu Lab A1 mini edition

This is a version of the [Modular 10"/10 inch Rack](https://www.printables.com/model/1170708-modular-1010-inch-rack) by **bwees** that prints on a **Bambu Lab A1 mini** (180 × 180 × 180 mm bed). It adds:

- **Join plates.** A 1U plate that ties the left and right side frames together. A 254 mm wide panel doesn't fit the bed, so each plate is printed as two halves. The halves are bolted together in the middle with 2× M4 countersunk bolts and nuts.
- **Mac mini 2012 holder.** Two brackets that bolt to the front uprights in U2. Each has a side wall and a ledge for the Mac mini to sit on.
- **Ready-to-print plates.** Bambu Studio projects and STLs laid out for the A1 mini bed.

Finished rack: about **284 W × 208 D × 119 H mm** (3U), with 220 mm of clear width between the side frames.

## Files

```
stl/        single parts, one per file
plates/     ready-to-print A1 mini plates (several parts each)
assembly/   minirack-assembly.FCStd, the whole rack assembled in FreeCAD with a Mac mini placeholder box
```

### What to print (one rack)

| Plate | Print | What you get |
|---|---|---|
| `plates/uprights-3U-x4.stl` | 1× | 4 × 3U uprights |
| `plates/feet-x2-gussets-x4.3mf` | 1× | 2 bottom feet + 4 gussets |
| `plates/rack-join-10inch-flat-x1.stl` | **2×** (front + back) | 1 join plate (left + right half) per print |
| `plates/macmini2012-holder-plate.3mf` | 1× | left + right Mac mini bracket |

Optional, from `stl/`: Top Handle (Minimal Overhangs) and Side Support.

### Single parts (`stl/`)

| File | From |
|---|---|
| `Modular Rack 3U Upright.stl`, `Modular Rack Bottom Foot.stl`, `Modular Rack 1x3 Gusset.stl`, `Modular Rack Side Support.stl`, `Modular Rack Top Handle Minimal Overhangs.stl` | bwees' original, unmodified |
| `rack-join-10inch-left.stl`, `rack-join-10inch-right.stl` | this fork: join plate halves |
| `macmini2012-holder-left.stl`, `macmini2012-holder-right.stl` | this fork: Mac mini 2012 brackets |

### Join plate: print it flat

`rack-join-10inch-flat-x1.stl` lies on its front face. It needs **no supports** and takes about **2 h 41 min / 38 g of PETG** per join (0.20 mm Standard profile). Printed flat, the layers run along the bending load, so the part is stronger, and the front face is smooth from the build plate.

If you'd rather print all 4 halves on one plate, use `plates/rack-join-10inch-standing-x2.stl` or the `plates/rack-join-10inch-standing.3mf` project. It takes about 8 h and ends up weaker.

### Hardware

- Rack screws, as in the original: M5 through the slots, which have horizontal play for tolerance.
- Join splice: 2× M4 × 10 countersunk bolts (ISO 10642) + 2× M4 nuts per join. A 10 mm bolt ends flush with the back of the rib. The nuts drop into hex traps in the left half.

### Mounting

- **U1 (bottom):** join plate, front and back. Its lower slots bolt into the foot and its upper slots into the upright, both on the inner hole column, so it also braces the joint between the foot and the upright.
- **U2:** Mac mini holder brackets.

## Credits & license

- The original rack design is the **[Modular 10"/10 inch Rack](https://www.printables.com/model/1170708-modular-1010-inch-rack) by [bwees](https://www.printables.com/@bwees)** on Printables, licensed **CC BY-NC-SA 4.0**. bwees made the uprights, feet, gussets, side support and top handle. Thank you for a great modular system!
- The join plate, the Mac mini 2012 holder and the A1 mini plate layouts were made for this fork by [IllyaMoore](https://github.com/IllyaMoore).

This fork uses the same **[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)** license as the original (see [`LICENSE`](LICENSE)). You may share and remix it with attribution, for **non-commercial** use only, and you must release your changes under the same license.
