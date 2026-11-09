# Modular 10" Mini Rack: Bambu Lab A1 mini edition

A remix of the [Modular 10"/10 inch Rack](https://www.printables.com/model/1170708-modular-1010-inch-rack) by **bwees**, split and redesigned so **every part prints on a Bambu Lab A1 mini** (180 × 180 mm bed). It is built from layers: a base frame, then one 1U layer per device. The layers are a Mac mini 2012, a 4-bay hot-swap NAS, and a Raspberry Pi control floor.

![Full rack in FreeCAD](images/assembly.png)

| Layer | What it holds |
|---|---|
| [Base](#1-base-frame) | feet, uprights, join plates, side supports, top handles |
| [U2: Mac mini](#2-mac-mini-2012-layer-u2) | Mac mini 2012 |
| [U3: NAS](#3-nas-layer-u3) | 4× 2.5" 7 mm drives, front hot-swap, SATA-USB 3.0 adapters as the backplane |
| [U4: Control](#4-control-layer-u4) | Raspberry Pi 3B+ and a powered 4-port USB hub |

**Print settings for everything:** PETG, 0.20 mm Standard (Bambu A1 mini profile), **no supports**. The print times below are from Bambu Studio.

`ReadyToPrint/` holds plates that are ready to print. `stl/` holds the single parts, sorted by section. The full model is `freecad/minirack-assembly.FCStd`.

---

## 1. Base (frame)

![Base frame](images/layer-base.png)

| File (`ReadyToPrint/`) | Print | Parts | Time / plate |
|---|---|---|---|
| `rack-uprights-3u-x4.stl` | 2× | 8 uprights: two 3U stacked per corner | 4 h 07 min |
| `rack-feet-x2-gussets-x4.3mf` | 1× | 2 feet, 4 gussets | 3 h 16 min |
| `join-plate-standing-x1.3mf` | 2× | front and back join plate (left and right halves) | 2 h 16 min |
| `side-support-m6-front-back-halves.3mf` | 6× | 1 side support per plate: one per side on every layer from U2 to U4 | 1 h 39 min |
| `rack-top-handle-x1.stl` | 2× | 1 top handle per plate, placed diagonally to fit the bed | 3 h 11 min |

**Hardware**
- **Frame, join plates and side supports to the uprights:** M6 × 12 button-head screws with M6 square nuts (the bwees standard, 6.6 mm holes).
- **Each join plate:** 2× M4 × 10 countersunk screws with 2× M4 nuts, to join the two halves.
- **Each side support:** 2× M4 × 10 countersunk screws with 2× M4 nuts, to join the front and back halves.
- **Where the stacked uprights meet (top of U2):** the U3 side supports and the NAS face plate cross the joint, so they hold the two uprights together.

## 2. Mac mini 2012 layer (U2)

![Mac mini layer](images/layer-macmini.png)

| File (`ReadyToPrint/`) | Print | Parts | Time |
|---|---|---|---|
| `macmini2012-holder-left-right.3mf` | 1× | left and right Mac mini brackets | 1 h 26 min |

**Hardware:** M6 × 12 button-head screws with M6 square nuts, to fix the brackets to the uprights.

## 3. NAS layer (U3)

![NAS layer](images/layer-nas.png)

A **modular** NAS: one base plus 4 bolt-on **sockets**, so a prototype costs one socket, not a whole floor. Each 7 mm 2.5" drive slides in on rails from the front and plugs into a SATA-USB 3.0 adapter. The adapter sits fixed in the back of the socket as a backplane.

| File (`stl/nas/`) | Print | Time |
|---|---|---|
| `nas-base-left.stl` | 1× | 1 h 57 min |
| `nas-base-right.stl` | 1× | 1 h 42 min |
| `nas-socket-left.stl` | 2× | 2 h 09 min |
| `nas-socket-right.stl` | 2× | 2 h 09 min |
| `ReadyToPrint/hdd-handle-landing-2.0mm-x4.stl` | 1× | 58 min |
| `nas-socket-fit-test.stl` *(optional: the back of one socket, to check the adapter fit first)* | 1× | 1 h 17 min |

**How it works**
- **Drive slot:** the drive runs between a bottom rail and a 45° top rail, with 0.3 mm of play above and below. There are lead-ins at the front, and the walls have teardrop holes for airflow.
- **Adapter:** head 47 × 12 mm, body 41 mm long when plugged in. It sits in a tight pocket. A low front lip stops it coming out with the drive, a back stop takes the push, and a zip tie holds it down.
  - The adapter sits 4.5 mm right of the drive's centre (seen from the front), and the drive sits 2 mm higher than the adapter.
- **Handle:** clips onto the drive's front side screw holes with two pins (no screws). Two teeth hook over the drive's top edge so the drive stays level when you carry it.
  - Three handle versions are in `stl/nas/`: `hdd-handle-landing-1.5mm` / `2.0mm` / `2.5mm`. They differ only in how far the teeth reach over the drive.

**Hardware**
- **Base to the rack:** 4× M6 × 12 button-head screws with M6 square nuts. **Between the two base halves:** 2× M4 × 10 countersunk screws with 2× M4 nuts.
- **Sockets to the base:** M3 countersunk screws from under the base, with M3 nuts in the pocket on top of each bolt column, 2 per stack.
  - One socket: **M3 × 20**. Two stacked sockets: **M3 × 35**.
- **Adapters:** zip ties ≤ 3 mm wide. A lower socket uses slot rows 1 and 3, an upper socket rows 2 and 4.

## 4. Control layer (U4)

![Control layer](images/layer-control.png)

A skeleton floor: material only where something sits. The **USB hub** (76 × 41 × 12 mm, ports facing back) sits at the front centre. The SATA-USB adapter cables (130 mm) come straight up behind it into the hub. The **Raspberry Pi 3B+** sits on the right with its USB and Ethernet ports facing the hub, so the hub cable is short.

| File (`stl/control-floor/`) | Print | Time |
|---|---|---|
| `control-floor-pi-hub-left.stl` | 1× | 2 h 23 min |
| `control-floor-pi-hub-right.stl` | 1× | 3 h 08 min |

**Hardware**
- **To the rack:** 4× M6 × 12 button-head screws with M6 square nuts. **Between the halves:** 2× M4 × 10 countersunk screws with 2× M4 nuts.
- **Pi:** 4× M2.5 screws, into the 6 mm standoffs.
- **Hub and cables:** zip ties.

**Power:** 4 drives need a **powered** hub. Use a 5 V 3–4 A supply for the hub and a 5 V 2.5 A supply for the Pi. The Pi 3B+ only has USB 2.0, so expect about 35 MB/s per drive.

---

## Credits & license

The original rack design is by **[bwees](https://www.printables.com/@bwees)**: [Modular 10"/10 inch Rack](https://www.printables.com/model/1170708-modular-1010-inch-rack) on Printables. The `bwees-*` files in `stl/rack/` are his parts. This remix is shared under the same license, **[CC BY-NC-SA 4.0](LICENSE)**.
