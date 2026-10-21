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
