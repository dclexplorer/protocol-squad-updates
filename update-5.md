# INTRODUCTION

Welcome to the fifth grant update from Decentraland Alternative Explorer project. This team has the main goal of developing an explorer version using two different technologies:
- Bevy targeting to Desktop
- Godot targeting to Mobile

As secondary objectives we have:
- Make reliable explorer-agnostic tests to ensure the well-working of new explorers
- Develop experimental builds on VR and Web using Godot

The project is progressing as planned.

# HIGHLIGHTS

### General highlights:

Last month, we focused on the application's reliability. We prepared both explorers for the testing sessions.

We published a Open Beta for Play Store for Android, and we have a closed Beta for iOS.

19 march we had the Mobile Testing Session for Android, you can see it here: https://drive.google.com/file/d/15hilUPrWumoamA8QOih7erUkTgorTJAB/view

### Detailed Godot highlights:

#### Features
- Add in world builder as custom place.
- Change custom places for the demo.

#### Fix
- Correct pointer events.
- Timestamp for pointer events.
- Loading screen logo same as menu.
- Disable UI mic when needed.
- Animation player should reset.
- Avatar loading issues.
- Correct promise base type initialization to prevent crashes.
- Comms sender blocks the JavaScript runtime.
- Promises between onStart and onUpdate aren't resolved.
- Some avatar has a bad-hiding of lower_body (and head stuffs).
- Bunch of fixes including unspecified items.

#### Refactor
- Implement sign-in with decentraland.zone/auth.


#### Documentation
- No specific documentation changes were listed in the provided commits.

#### Chore
- Add .aab artifact, change logo, and package name.
- Update android app version.
- Cancel workflows for branches.

You can track the code changed in this month here: https://github.com/decentraland/godot-explorer/compare/32dc9db093c38ae1e02be64a8cb2a4d4c72a0aad...0df27ef8de0912390593c194b7ce923db93cc01b

### Detailed Bevy highlights:

#### Features
- Migrate to bevy 0.13
- Use dcl auth server
- Add scene unload distance (separate to load distance to reduce scene thrashing)
- Add scene component count tracker
- Add ui for initial batch of settings
- - Window mode
- - Aa mode
- - Shadow mode
- - Fog mode
- - Bloom mode
- - Oob rendering
- - Scene load/unload
- - Scene thread count
- - Target frame rate

#### Performance
- Switch global allocator to mimalloc
- Throttle image and mesh gpu uploads to reduce framerate hitches
- Use patched wgpu to reduce cpu load
- Reuse a single instance of duplicate meshes from gltfs
- Reuse a single instance of duplicate materials from gltfs

#### Bugfixes:
- Stop audio streams on drop (fixes high cpu usage)
- Default skinned mesh collider bits to 0
- Stop falling animation loop
- Fix teleport location when no spawn point specified
- Normalize wearable joint weights to avoid stretching wearables
- Avoid div/0 for empty-middled 9slices
- Use shader instead of flexbox for 9slice layout to avoid seams on fractional pixels
- Don't panic on spamming profile window
- Process rpc calls before onStart
- Increase pix/m for textshape
- Fix textshape size calc for reused nodes
- Fix up gltf positions before initial render
- Fix audiosource panning div/0 when emitter == camera
- Round normals and directions for raycasts to 2^-14 so js tests axis gt/lt/eq 0 or 1 work as expected when very close to zero
- Skip colliders when the raycast begins inside the collider
- Send hover enter/leave only on change
- Audio doesn't attempt to replay if play is spammed
- Process ground-colliders in player dynamic update so player is correctly synchronized with platforms
- Use opensea v2 api
- Use blend for mtmAuto if alpha texture is specified
- Pass new details to scenes if wallet details change after spawn
- don't strip "_collider" from meshName for collider meshes
- interpret "_collider" as a collider if it occurs anywhere in the name
- Allow http for vanilla fetch
- Enable colliders for skinned meshes based on rest pose
- Set PbAvatarBase and PbEquippedData for primary user
- Update signedFetch headers to try and match foundation client
- Fix uvs and background color for UiBackground components
- Fix param parsing in js requestTeleport
- Add js setInterval
- Handle \n in textshape and uiText
- Fix attach location for entities with parents
- Handle shouldReset on animations as per foundation (it specifies if the anim should be restarted, not if the final position should reset to initial position on finish)
- Allow strings for teleport
- Fix emote and wearable urns to always take at most 6 ':'-separated parts
- Fix typo in js EnvironmentApi::getBootstrapData
- Fix crash on minimise with egui fontsize 0
- Fix gathering of "hides" for wearables
- Improve 3rd person cam position
- Fix crdt timestamp for transform updates sent to scenes
- Fix scrollarea dui component

# Blockers

No blockers in this update.

# Next Steps

As everything seems to be on track as planned, the public roadmap in https://github.com/orgs/decentraland/projects/43 contains what we're working on.

Save the date! We have planned a live test for 9 april for the Bevy explorer for Desktop (Windows/Linux/Mac) and a showcase for the VR version!

April is the last month for the proposal!

We are going to focus on the stability of the platform, improve the visuals, fix bugs, and have the experimental VR version!

# Additional notes and links

- Join us on our Discord server: https://discord.com/invite/6mGqPnjujT
- Public home page to get links: https://dclexplorer.com/
- Public roadmap: https://github.com/orgs/decentraland/projects/43
- Godot project: https://github.com/decentraland/godot-explorer/
- Bevy project: https://github.com/decentraland/bevy-explorer/
- Scene Explorer Tests: https://github.com/decentraland/scene-explorer-tests

# Reporting

category,description,token,amount,receiver,link
Team Compensation,Team Compensantion (January),DAI,12500,0x85bc980eb632434c562414791146cc86cea12c51,https://etherscan.io/tx/0xc39ec91767932a8db23105412dac5d271153cae431a58e609135dfe146710fec
Team Compensation,Team Compensantion (January),DAI,10500,0x6db12e73904eb12f9c40b7d995b2a870254b3625,https://etherscan.io/tx/0xc39ec91767932a8db23105412dac5d271153cae431a58e609135dfe146710fec
Team Compensation,Team Compensantion (January),DAI,10500,0xbcae59ff0aa916b6c38adde712c39da3eb5443c4,https://etherscan.io/tx/0xc39ec91767932a8db23105412dac5d271153cae431a58e609135dfe146710fec
Team Compensation,Team Compensantion (January),DAI,1200,0xae185e420a7b0e82963f6edb80078d0ce9d40b40,https://etherscan.io/tx/0xc39ec91767932a8db23105412dac5d271153cae431a58e609135dfe146710fec
Team Compensation,Team Savings (January),DAI,1666,0xae185e420a7b0e82963f6edb80078d0ce9d40b40,https://etherscan.io/tx/0xc39ec91767932a8db23105412dac5d271153cae431a58e609135dfe146710fec