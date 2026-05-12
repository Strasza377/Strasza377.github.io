# Alex Schneider Portfolio

My name is Alex and I'm a game software engineer with over 10 years of experience, primarily in the mobile space with Unity/C#. I've worked on many different aspects of game programming including gameplay, UI, tools, platform, memory management/optimization, and app life-cycle. I have experience leading small teams of ~3-5 other people to deliver fully fleshed out features in both production and live-ops environments.

I am ideally looking for a small to medium sized game team to join and contribute to. Though I am open to discussing other roles, especially those that might benefit from my C# experience that aren't in the game development space. I would also be open to any roles that involve development using the Godot game engine as this is an engine I have enjoyed using for personal projects with both their scripting language and C#.

## Professional Projects

### Mythwalker

#### Links:

<a href="https://www.youtube.com/watch?v=RDkacY7LllQ">Gameplay footage</a>

<a href="https://www.youtube.com/watch?v=IDrlckQxy0E">Launch Trailer</a>

Unfortunately this game is no longer available on the app stores as the team was laid off and the project was sunset.

#### Description and Contributions

Mythwalker was a mobile, geo-location RPG, think Pokemon GO meets a fantasy RPG. The game featured action combat, customizable characters, resource gathering minigames, and multiplayer.

One of my major focuses on this project was to manage the assets and Unity Addressables integration. I created a code service in our project to control the loading, unloading, and downloading of all assets within the project. This unified and simplified the way the project interacted with this system and allowed for more overall consistency in the project, as well as reducing the number of loading issues. 

In addition to this, I re-organized the assets in the project and setup the bundle and Addressable groups to follow this organization to allow for better groupings of assets. This helped with the memory optimization work I did later because the connections and dependencies between various assets were both better defined and easier to control, ultimately leading to multiple fixes to memory issues on lower end mobile devices.

To top it all off on the Addressables front, I worked closely with the art and design teams to create tools for them to interact with this system. The tools enabled the art and design teams to minimize the time spent on adding their new assets into the Addressable system as well as eliminated the majority of all problems the teams faced in the past.

My efforts on the Addressables system for Mythwalker ultimately led to resolving the majority of issues the project was facing with loading assets and greatly simplified the pipeline for getting new assets into the game and functioning properly.

Aside from the Addressables and assets work, I also led a team of 3 other engineers, a designer, and an artist to rebuild the game's minigame system. I came up with an updated design for the code system and coordinated with the other engineers on the implementation details. I built out the framework and general flow, while the other engineers synced up with me to hook in improvements to various gameplay elements. I would stay in sync with the designer to ensure the feature was satisfying their requirements for both gameplay feel and for the control over the rewards and difficulty they needed. Throughout the process I acted as the primary point of contact for the production team to communicate with them about progress, blockers, and anything else related to the development.


### Cookie Jam and Cookie Jam Blast

#### Links

Cookie Jam App Store links: 

<a href="https://play.google.com/store/apps/details?id=air.com.sgn.cookiejam.gp">Google Play Store</a>

<a href="https://apps.apple.com/us/app/cookie-jam-match-3-games/id727296976">Apple App Store</a>

Cookie Jam Blast App Store links: 

<a href="https://play.google.com/store/apps/details?id=air.com.sgn.cookiejamblast.gp">Google Play Store</a>

<a href="https://apps.apple.com/us/app/cookie-jam-blast-match-3-game/id1034920425">Apple App Store</a>

Video Links:

<a href="https://www.youtube.com/watch?v=SAF8OP3FIek">Cookie Jam Pets Feature</a>

<a href="https://www.youtube.com/watch?v=EHU8LUrCOnQ">Cookie Jam Blast Airship Power Demonstration</a>

#### Description and Contributions

Cookie Jam and Cookie Jam Blast are both match-3 puzzle games available on iOS and Android mobile devices, with Blast being a pseudo sequel. Both games started as Flash/ActionScript3.0 games with their own code bases, but a large portion of the work I contributed to these projects was when we were porting the games over to Unity and creating our own internal puzzle game engine for both games to share. I built a few large systems to support both games during the porting and provided live-ops support both during and after the porting effort was completed.

One of the systems I built was what we internally called a "powers" system which had the purpose of being able to define special board interactions from that could be used in both games and be fired from multiple locations. The intention was for this system to support the basic puzzle board boosters that both games use, but also the pet and airship systems seen in the videos linked above. This ultimately resulted in a system where a designer could build a new power out of a scriptable object with multiple, modular pieces that would define the various aspects of the power such as how it charges, what the cooldown is, what effect it has on the board, and the various visual aspects. These definitions were then parsed when the game starts up to build out the objects in game that would integrate into the puzzle game's list of rules and mechanics. 

This system fully supported the 3 systems already defined in the flash versions of the game, but also provided an easier way forward to modify and A/B test them, create new interactions within these defined systems, and also build whole new systems for special board interactions. It also allowed for the design team to more easily prototype and test changes without engineering interactions as the base set of scriptable objects provided to them allowed for a large variety of options.

I also led the development of an updated events system for both games to utilize. The goal here was to combine the standard game event system with the cross-promotional events systems as there was a lot of overlap in functionality and therefore duplicated code. I was able to combine the two systems to share the same underlying structure, but allow for modularity within how various aspects of the event progress are defined. For example, some events had an overall progress that was tracked and displayed as the player interacted with it, while other events would just provide tokens to interact with its mechanic. This option was able to be defined in the data and allowed the code to determine which objects to piece together at runtime when setting up the event.

This change led to a more unified and simplified codebase for our events systems, resulting in fewer bugs, faster creation of new event types, and an overall easier to understand process.


