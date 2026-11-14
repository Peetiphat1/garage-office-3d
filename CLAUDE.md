# Garage Office 3D

Single-file interactive 3D model (`index.html`, Three.js r128 from jsDelivr) of the user's garage/workshop. Open `index.html` in a browser; no build step.

## The space (metres)
- Interior 9.2 m wide (X) × 13.8 m deep (Z). Back wall at z = -6.9, entrance (garage door) at z = +6.9. The hand sketch labelled 13.8 across and 9.2 deep, but the user said these are swapped, so the model uses 9.2 wide, 13.8 deep.
- Arched corrugated steel roof (peak about 7 m), polished concrete floor.
- Styled after the user's photo of the real "Zero Garage": glass office on the ground, open deck above.
- Ground: glass office, 4.6 × 4 m (x -2.3..2.3, z -6.9..-2.9), centered against the back wall, black steel frame. Front door at the right of the front glass (x 0.55..1.45), hinged at x 0.55 and opening outward.
- WC on the left of the office, store on the right (dark partitions, louvered doors), both about 2.3 m wide and 1.7 m deep. Pantry from the sketch was dropped for space.
- Upper deck at +2.8 m over WC, office and store (x -4.6..4.6, z -6.9..-2.8), 150 mm concrete-look slab, steel edge beam, black posts, glass guard (0.95 m) along the front and round the stairwell. Left: enclosed glass meeting room x -3.25..0.65 (its left edge is where the arched roof still clears 5.6 m), door on its right glass folded back against it. Right: open terrace with a canvas-drawn "ZERO GARAGE" graffiti sign on the back wall, string lights on a steel frame (5.3 m), sofa with pink neon strip, coffee table, two bistro sets, plants.
- L-shaped black steel stair with open treads, 8 + 8 risers: flight 1 starts about 1 m in front of the office glass (first riser x 1.483, z -1.85..-0.85) and climbs +x to a 1.0 m square mid-landing at +1.4 m (x 3.45..4.45, z -1.85..-0.85); it then turns left and flight 2 climbs -z (x 3.45..4.45) through a stairwell in the deck to the top riser at z -3.817. Glass guards on both sides of both flights and on the landing. The 1 m corridor between the office glass and flight 1 leads to the store door.
- Headroom: the arched roof is only 3.4 m at the side walls, so the deck near the walls is low; walk mode keeps the upper walker at x <= 4.2.
- Front: 3 parking bays. Middle: a work bay (car sideways), machines on the right, workbench on the left wall.

## Features
- Realistic render: sRGB + ACES tone mapping, soft shadows from one sun, a few point lights at the tube fixtures, a procedural reflection environment (PMREM). All textures (polished concrete with saw-cut joints, corrugated steel, wood, louvers, wheel rims, screens) are drawn on canvas, so no image files.
- Orbit camera with Corner / Entrance / Inside / Top presets.
- Toggles: walls and roof, meeting room (hides the glass room only; the deck and terrace stay), cars, labels, people / scale (1.75 m figure), dimensions (width, depth, peak, office 4.6 x 4.0, mid-landing, upper floor and ceiling heights, plus a 1 m floor grid).
- Walk mode (first person): WASD or arrows, Shift to run, drag to look, on-screen pad for touch. Simple rectangle collision, stairs, upper level. Collision rectangles live in `solids` (ground), `carRects`, `upperOK` (walkable upper areas) and `upperSolids` (upper furniture) in the script; anything you add that people cannot walk through needs a rectangle there. `stairRects` is the walkable stair zone; `stairY` ramps flight 1 along x, keeps the landing level and ramps flight 2 along z. You get on or off the stair only at its two ends.
- Real-world sizes: doors 0.9 x 2.1 m, desks 0.74 m, seats 0.45 m, bench 0.9 m, bays 3.0 x 4.9 m, floor to floor 2.8 m, stairs 16 risers of 175 mm (8 + mid-landing at 1.4 m + 8) with 281 mm going, 1.0 m wide, 0.95 m rail (walk-mode ramp uses the same run and rise).
- Roller garage door shown rolled up; two-post car lift in the work bay (red car raised on it); kitchenette in the office back-left corner.

## Notes
- Cars are generic sedan models (about 4.55 x 1.82 x 1.45 m), furniture and machines are generic shapes at real size. Confirm against the real site.
- Door positions, the stair run and the WC / store layout are estimates from the sketch and a photo. The store is now enterable (0.9 m door); the WC and store doors are drawn open.
- The tool chest moved to the left wall because it blocked the office door. The drill press moved to x 4.0, z 0.5 (in front of the mid-landing) to clear flight 1.
- Not modelled from the photo: the blue car poster, dark lower wall panels on the side walls (they would hide the inside from the Corner view).
- Ideas not done yet: second work bay, textures from the photo, exporting to glTF, instancing repeated parts.
