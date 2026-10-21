# Field Ops — Construction Works

A separate browser-based 3D construction simulator. This project is informed by the expanded Field Ops 3D game in `xz64uj777/Chatdemo`, but does not replace or overwrite it.

## Foundation branch

- 3D construction site, marked work zone, camera follow, and touch-screen layout.
- Starter excavator, wheel loader, and dump truck.
- Four starter contract stages: foundation excavation, spoil hauling, gravel spreading, and concrete placement.
- Cash, rank, rewards, contract progress, and visible site changes.
- Three.js 0.160.0; browser ES module, no build step required.

## Controls — minimal-controls branch

The experimental `minimal-controls` branch replaces the direction pad and extra tool buttons with dual touch joysticks:

- **Left joystick:** drive and steer.
- **Right joystick:** operate the boom/stick/bucket where the selected machine supports them.
- **Machine:** cycle machines.
- **Action:** perform the current contract action when in the right location with the required machine.
- **Menu:** open contracts/pause.

Only the essential action controls remain visible; detailed menus are opened when needed.

## Important gameplay status

This is still an early foundation, not yet feature-equivalent to the older Field Ops 3D game. In particular, true terrain deformation, persistent material quantities, truck loading/hauling physics, machine-specific hydraulic physics, save persistence, audio, and multi-site progression still need implementation and testing. Some starter tasks currently use simplified visual progress rather than full physical simulation.

The old game already contains six machine types, six contract/job stages, a two-joystick layout, persistent local progress, material transfer and delivery, continuous grading, asphalt paving, excavation, demolition, crane girder placement, fuel/wear, audio and effects, a minimap, and multiple distinct work zones. New-work development should build on these lessons rather than regress to a button-heavy or repetitive task loop.

## Run it

Serve `index.html` from a web server or GitHub Pages. It imports Three.js 0.160.0 from jsDelivr, so an internet connection is required.

## Deployment

The repository has a GitHub Actions Pages workflow. A live URL is not claimed until a deployment has been confirmed successfully.

## Development direction: connected depot-to-site career

The next playable milestone is a small connected world, not a menu of disconnected jobs.

### Build order
1. **Depot and local roads:** establish the player's home yard, equipment parking, loading area, and drivable road connection to a first construction site.
2. **Optional lowboy transport loop:** a road tractor (semi-truck) and detachable lowboy trailer become a usable transport rig. Load an owned machine using suitable ramps and trailer clearance, secure it, transport it to the site, unload it, and return to the yard. Oversize loads may need a heavier tractor/trailer combination. Include a clear skip/delivery option so transport never becomes mandatory busywork.
3. **One complete residential build:** demolition/clearing, excavation, spoil removal, sub-base, forms/rebar, concrete delivery and placement, framing lifts, roofing/exterior, driveway and landscaping. Each stage visibly changes the same property.
4. **Project replay and practice:** resume saved career progress, replay unlocked stages without career rewards, reset a vehicle to its start point, and use a free-practice mode.
5. **Expand the world and fleet:** quarry and suppliers, varied landscapes, then additional building types and machines such as concrete mixer trucks, articulated-boom concrete pumps, telehandlers, cranes, rollers, pavers, and utility equipment.

### Design rules
- Keep the normal HUD to two joysticks and only essential actions; put transport choices, stage selection, and settings in the site-office menu.
- Owned equipment should live at the depot and be transported or delivered to a job, not simply appear beside the player.
- Offer three choices where appropriate: drive/operate the whole process, pay for delivery/skip routine steps, or practice without career pressure.
- The world and construction site should visibly retain completed work; material should have a source, destination, and purpose.
- Make the first end-to-end residential project fun and reliable before adding a large fleet or a huge map.

This is the intended roadmap, not a claim that all these systems are already implemented. The current branch remains an early prototype; its starter tasks still use simplified visual progress and need browser/mobile testing.

### Equipment accuracy and visual target

Use the correct machine for each construction task, with recognizable proportions and working parts rather than a pile of generic yellow vehicles. The first transport vehicle is a **road tractor / semi-truck pulling a detachable lowboy trailer**—not an agricultural tractor. Match equipment to the job: excavator for digging, dozer for pushing/rough grading, loader for loading and spreading, dump truck for hauling, compactor/roller for compacting, mixer truck and concrete pump truck for concrete placement, telehandler or crane for lifting framing, and paver/roller for asphalt. Introduce only the equipment needed for the current project, then expand the fleet.

Aim for believable, attractive game-ready 3D models and readable motion: articulated excavator boom and bucket, loader arms and bucket, truck/trailer connection, rotating wheels, crane boom/hook, concrete pump's articulated boom, and visible construction stages. Prioritize correct silhouettes, scale, pivots, contact with the ground, and satisfying material/site changes before chasing photorealism. Keep performance suitable for mobile browsers. This is a practical quality target, not a promise of photorealistic graphics.
