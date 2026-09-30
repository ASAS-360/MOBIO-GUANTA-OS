# VYRSIA — Unreal Engine Master Build Specification

## Product direction
VYRSIA is a realistic, non-combat, open-world civilian experience set in Baghdad. The browser HTML build is retained only as a prototype reference; the production target is Unreal Engine 5.x.

Core pillars:
- Realistic Baghdad with no sci-fi layer.
- Third-person open-world exploration.
- Civilian gameplay: jobs, shopping, transport, property, tourism, hotels, restaurants, social life, events and business.
- MOBIO / GUANTA as the in-world phone.
- BATTUTA as the navigation system.
- VSN / VYRSYON as the in-world currency.
- Commercial advertising integrated into the city world, not intrusive pop-ups.

## Platform strategy
Primary: Windows PC for the full-quality build.
Secondary: iOS / Android using scalable visual profiles.

Mobile must use reduced crowd density, traffic density, shadow distance, reflections, texture resolution, foliage and post-processing to preserve frame pacing.

## Engine architecture
Recommended Unreal systems:
- World Partition for Baghdad streaming.
- Data Layers for districts, interiors, traffic and mission states.
- Level Instances for reusable shops, homes, hotels and city blocks.
- HLOD for city performance.
- Enhanced Input for touch, gamepad and keyboard/mouse.
- Chaos Vehicles for drivable civilian cars.
- NavMesh + Mass AI / lightweight AI for crowds and traffic.
- StateTree / Behavior Trees for civilian NPC logic.
- Gameplay Tags for districts, services, jobs and quests.
- SaveGame for persistent progress.
- UMG / Common UI for HUD and menus.

## Baghdad world scale
Rule: 1 Unreal Unit = 1 cm. The world must feel geographically large enough that the player cannot cross a district in seconds.

Priority districts:
- Tahrir / Saadoun / Firdos / Abu Nuwas.
- Mutanabbi / Rashid / Qushla / Mustansiriya.
- Karrada.
- Jadriya.
- Mansour.
- Kadhimiya.
- Adhamiya.
- Allawi.

The Tigris is a major physical world feature with real shoreline boundaries, embankments, boats, bridge crossings and night reflections. No walking on water.

## Landmark package
High-priority landmarks:
- Baghdad Tower.
- Central Bank of Iraq new building.
- Unknown Soldier Monument.
- Al-Shaheed Monument.
- Freedom Monument / Tahrir Square.
- Al-Kadhimiya Shrine.
- Abu Hanifa Mosque.
- Al-Qadiriyya complex.
- Our Lady of Salvation Church.
- Major historic Baghdad churches.
- Mandaean Manda.
- Historic Jewish heritage / synagogue location in old Baghdad, represented respectfully.
- Baghdad Mall and hotel.
- Zawraa Park and amusement city.
- Dijlah Village.
- Palestine Hotel.
- Ishtar Hotel.
- Mansour Hotel.
- Al-Rasheed Hotel.
- Mövenpick Baghdad where applicable.
- Bloom / relevant modern hospitality landmark.
- Heart of the World hotel / complex if confirmed by reference material.
- Baghdad Central Station.
- Iraqi Museum.
- Qushla Clock Tower.
- Al-Mustansiriya.
- Kahramana Monument.
- University of Baghdad / Jadriya campus identity.

Priority bridges:
- Jumhuriya Bridge.
- Shuhada Bridge.
- Sarafiya Bridge.
- 14 July suspension bridge.
- Double-deck bridge.

Every landmark must be built from reference photography, correct proportions, facade logic, surrounding roads and night lighting. Placeholder blocks are not acceptable in the final build.

## Human character standard
The player must be a real human character, never a robot, capsule or procedural primitive.

Required pipeline:
- High-quality realistic human base.
- Full skeleton / rig.
- Facial rig.
- Civilian clothing.
- Realistic hands, feet and skin materials.
- LODs for performance.

Animation set:
- Idle variations.
- Walk / fast walk / jog / sprint.
- Start / stop.
- 90° / 180° turns.
- Pivot.
- Stairs and curb stepping.
- Sit / stand.
- Phone use.
- Talk / shop.
- Enter / exit vehicle.
- Drive / passenger.
- Contextual interactions.

Movement quality:
- Acceleration / deceleration.
- Motion Matching or equivalent responsive locomotion.
- Foot IK and Full Body IK.
- Ground alignment and slope correction.
- No foot sliding.
- No clipping into roads or walls.

## Third-person camera
- Smooth spring-arm follow.
- Camera collision against walls and objects.
- Minimum distance so the camera never cuts through the character.
- Manual orbit.
- Auto-recenter option.
- Adjustable sensitivity.
- Adjustable FOV on supported platforms.
- Separate walk and vehicle camera profiles.
- Interior camera rules.
- Vehicle chase camera.

## Physics and collision
Non-negotiable:
- No walking through walls.
- No sinking into roads.
- No floating.
- No walking through vehicles.
- No driving through buildings.
- No crossing the Tigris except via intended bridges / boats.
- Correct stairs, curbs and doors.
- Character capsule matched to the human mesh.

## Baghdad night lighting
Baghdad must remain visually alive and readable at night:
- Warm street lights.
- Hotel facade lighting.
- Bridge lighting.
- Shrine / mosque / church architectural lighting.
- Mall signs.
- Shopfronts.
- Traffic lights.
- Headlights / taillights.
- DOOH screens.
- Residential window variation.
- Tigris reflections.

## Traffic
Civilian traffic types:
- Sedans, SUVs, taxis, Kia/minibuses, buses, delivery vehicles, motorcycles where appropriate.

Behavior:
- Lane following.
- Traffic lights.
- Junctions.
- Parking.
- Day/night density.
- Rush-hour density.
- Pedestrian crossings.
- Avoidance.

Player vehicles:
- Enter / exit.
- Drive / reverse.
- Headlights.
- Indicators.
- Horn.
- Parking.

## Civilian NPC life
NPC examples:
- Students, office workers, families, shopkeepers, tourists, taxi drivers, cafe staff, hotel staff, delivery workers, technicians, street vendors, booksellers and restaurant staff.

NPC behaviors:
- Walk routes.
- Sit / talk / shop / eat.
- Use phones.
- Wait for taxis.
- Enter shops.
- Work shifts.
- Visit religious sites respectfully.
- React to traffic, time and weather.

## Spiritual / heritage system
Respectful non-combat areas include:
- Al-Kadhimiya Shrine.
- Abu Hanifa Mosque.
- Al-Qadiriyya complex.
- Our Lady of Salvation Church.
- Other Baghdad churches.
- Mandaean Manda.
- Jewish heritage / synagogue site.

Gameplay purpose:
- Visit, learn, observe architecture, cultural history and optional quiet reflection.
- Optional Serenity / Sakeena character state.
- No religion ranking.
- No combat or disruptive advertising inside sacred spaces.

## BATTUTA navigation
BATTUTA must be a real navigation map, not dots only:
- Roads.
- Tigris.
- Bridges.
- District boundaries.
- Landmarks.
- Shops / hotels / restaurants / jobs / events.
- Player position.
- Walk / drive route planning.
- Distance and ETA.

## MOBIO / GUANTA integration
Core apps:
- Calls, Messages, Contacts, BATTUTA, MOONDO, SENDIE, ALBUM, WEATHER, CAMERA, SETTINGS.

Game integration:
- Job messages.
- NPC messages.
- Navigation.
- Calendar / events.
- Payments.
- VSN wallet.
- Hotel bookings.
- Restaurant reservations.
- Property viewing.
- Vehicle services.

## Commercial advertising model
Advertising belongs inside the city economy:
- DOOH billboards.
- Roadside digital screens.
- Mall media.
- Hotel lobby screens.
- Event sponsorship.
- Branded activations.
- Sponsored map POIs.
- Sponsored concerts / sports / cultural events.
- Product placement where legally permitted.

Metrics:
- Impression opportunity.
- View duration.
- District.
- Time slot.
- Screen.
- Campaign.
- Event.
- Footfall / vehicle traffic proxy.

No full-screen forced ads during normal gameplay.

## Core gameplay loops
Exploration:
- Walk Baghdad, discover landmarks, visit cultural sites, use BATTUTA.

Work:
- Courier, cafe, retail, hotel, technician, advertising, event support, tourism guide, transport.

Lifestyle:
- Food, coffee, shopping, clothing, cars, property, hotels, social relationships and events.

Economy:
- Earn VSN, spend VSN, save, buy transport, rent / buy property and pay for services.

## Options
Graphics:
- Low / Medium / High / Ultra where supported.

Settings:
- Resolution scale, FPS cap, shadows, reflections, crowd density, traffic density, draw distance, motion blur, depth of field, camera sensitivity, FOV, audio levels, subtitles, Arabic/English, HUD scale, minimap size, controls and accessibility.

Touch controls:
- Left movement stick.
- Right camera area.
- Context interaction.
- Sprint.
- Enter / exit vehicle.
- MOBIO.

## Performance targets
PC: target 60 FPS on a reasonable modern GPU at the appropriate quality tier.
Mobile: stable 30 FPS is more important than fake maximum detail.

Mobile optimization:
- Adaptive resolution.
- Reduced dynamic lights.
- Reduced crowd and traffic.
- Reduced shadow distance.
- Lower foliage density.
- Aggressive LOD / HLOD.
- Texture streaming.

## Production milestones
Milestone 1 — Vertical Slice:
- One polished Baghdad district.
- Real human player.
- Modern camera.
- Real collision.
- One drivable car.
- Traffic.
- 15–30 civilians.
- Day/night.
- Tigris section.
- One bridge.
- One hotel.
- One shop.
- One cafe.
- One major landmark.
- BATTUTA.
- MOBIO basic integration.
- One job.
- One advertising screen.

Milestone 2 — Central Baghdad:
- Tahrir, Saadoun, Firdos, Abu Nuwas, Mutanabbi, Rashid, Qushla, Tigris bridges, hotels and central landmarks.

Milestone 3 — District expansion:
- Karrada, Jadriya, Mansour, Kadhimiya, Adhamiya, Allawi.

Milestone 4 — Economy and commercial platform:
- Jobs, property, cars, shops, events, ad inventory, sponsor system and campaign analytics.

## Final quality gate
A build is never called final unless:
- Player locomotion is visibly human.
- Camera never clips through the character.
- No missing body parts.
- No wall penetration.
- No road sinking.
- No water walking.
- Map is readable.
- Baghdad districts feel geographically meaningful.
- Night lighting is readable and attractive.
- Core UI is understandable.
- Stable frame pacing is verified.
- Save/load works.
- No placeholder sci-fi remains.
- No military character assets remain.
- No major runtime errors remain.

VYRSIA must feel like a civilian Baghdad open-world game, not a browser technology demo.
