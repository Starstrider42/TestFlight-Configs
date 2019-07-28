Starstrider42's TestFlight Configs
============

These are alternative configs created for [TestFlight 1.8](https://github.com/KSP-RO/TestFlight). Currently, only engines and heat shields are supported; I will be adding configs for other stock parts and mods I play with as time permits.

The configs are inspired by the ones that ship with Realism Overhaul, but are designed to be a bit more forgiving at the expense of realism. General principles I followed when writing the stock configs:
* Most liquid-fueled engines have rated burn times of 2-5 minutes, depending on whether they're intended for launch or orbital maneuvers. (5 minute burns may be needed by low-TWR interplanetary spacecraft.) Solid-fueled engines have rated burn times corresponding to 50-60% thrust for similar reasons. Jet engines have much longer rated burn times to allow long flights.
* Reusable engines will "forget" previous burns when idling for long enough. In addition to allowing multiple burns with no penalty for cumulative burn time, this rule ensures that engines will be more likely to fail after each ignition, not just the first one.
* Generally, solid-fueled engines are more reliable than liquid-fueled engines, but when they do fail, the results are more spectacular. Monopropellant, nuclear, and ion engines are immune to certain failure modes.
* I've tried to follow hints from the part descriptions. In particular, the RT-series boosters and the 3.75 m Kerbodyne engines are a bit prone to exploding, and the Kerbodyne engines start out very unreliable.
* Parts can inherit engineering experience from other parts, but only from the same manufacturer. The amount of data transferred is normally 50% for parts in the same series, but can vary from 75% (nearly identical components) to 25% (not really related, but the company must have learned general principles from the previous model).

License
------------
These configs are released under the MIT License. A copy of the license can be found in the file `LICENSE` in the mod directory, or online at http://opensource.org/licenses/MIT.
