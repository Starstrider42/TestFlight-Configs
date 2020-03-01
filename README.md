Starstrider42's TestFlight Configs
============

These are alternative configs created for [TestFlight 1.8](https://github.com/KSP-RO/TestFlight). Currently, only engines and heat shields are supported; I will be adding configs for other stock parts and mods I play with as time permits.

The configs are inspired by the ones that ship with Realism Overhaul, but are designed to be a bit more forgiving at the expense of realism. I've tried to follow hints from the part descriptions. For example, the RT-series boosters and the 3.75 m Kerbodyne engines are a bit prone to exploding, and the Kerbodyne engines start out very unreliable.

Parts can inherit engineering experience from other parts, but only from the same manufacturer. The amount of data transferred is normally 50% for parts in the same series, but can vary from 75% (nearly identical components) to 25% (not really related, but the company must have learned general principles from the previous model).

Engines
-------

* All engines follow the Realism Overhaul failure curve: they are up to ten times more likely to fail in the first five seconds after ignition, have their nominal failure rate up until their rated burn time, then grow much more likely to fail after that. Burn time is tracked in a way that does not reset if you shut down and quickly restart an engine.
* Reusable engines will "forget" previous burns when shut down for long enough. This allows multiple burns with no penalty for cumulative burn time, while ensuring a failure spike at the start of each burn.
* Engines that have ignition failures are less likely to ignite above a dynamic pressure of 5 kPa (90 m/s at Kerbin sea level), with the ignition chance falling to half its normal value at 27 kPa (210 m/s at sea level). Engines designed for air starts, like the Launch Escape System, have higher pressure thresholds.
* All gimbaled engines have a common set of gimbal failures: gimbal lock (57%), gimbal speed loss (29%), and a permanent gimbal offset (14%).
* Bipropellant rockets have rated burn times of 2-5 minutes, depending on whether they're intended for launch or deep-space maneuvers. They typically have 45-99% reliability (chance of *not* failing in one RBT), and may suffer a wide range of failures (see table below). They also have a chance of failure every time they are ignited. For launch engines this is typically 0.5-25%; for deep-space engines, it's 0.1-15%.
* Monopropellant rockets have 50-99.8% reliability, and are immune to ignition failures. Otherwise, they behave like bipropellant rockets.
* Solid-fuel rockets have rated burn times corresponding to 50-60% thrust. They have 60-99.5% reliability and are immune to most failure modes, but have a higher chance of exploding when they do fail. They rarely suffer ignition failures (0.05-10% of the time).
* Jet engines have rated burn times of hours to allow for extended flights. They are initially only 20% reliable (i.e., even a short flight can see a failure), but become 99.9% reliable when fully developed. Jet engines have similar failure modes to liquid-fueled rockets, but always ignite and are less likely to overheat.
* The J-404 and RAPIER currently do not have TestFlight support, because TestFlight does not support stock multi-mode engines.
* Nuclear engines and other thermal rockets have rated burn times of 10-15 minutes to allow low-thrust interplanetary burns. Like jet engines, they have low initial reliability (30%) to compensate for their long burn time. They have similar failure modes to monopropellant rockets, but are even more reliable when mature (99.9%).
* Ion thrusters typically have rated burn times of 20-30 minutes and reliabilities of 35-99.5%. They cannot explode or overheat, but are more likely than other kinds of thrusters to lose specific impulse.
* Electromagnetic thrusters typically have rated burn times of 10-20 minutes and reliabilities of 40-99.8%. They have a variety of failure modes, but will never explode.

| Engine type     | Shutdown | Low I<sub>sp</sub> | Low Thrust | Overheat | Explode |
| --------------- | -------- | ------------------ | ---------- | -------- | ------- |
| Liquid-Fuel     | 52%      | 26%                | 13%        | 6%       | 3%      |
| Solid-Fuel      |          | 89%                |            |          | 11%     |
| Jet Turbine     | 53%      | 27%                | 13%        | 3%       | 3%      |
| Ramjet          | 57%      | 28%                | 14%        |          |         |
| Turboramjet     | 55%      | 28%                | 14%        |          | 3%      |
| Thermal Rocket  | 52%      | 26%                | 13%        | 6%       | 3%      |
| Electrostatic   | 29%      | 57%                | 14%        |          |         |
| Electromagnetic | 36%      | 36%                | 18%        | 9%       |         |

Heat Shields
------------

* Ablative heat shields have a constant failure rate while the shield is ablating. The rate does not depend on how long the shield has been hot or on the ablation rate.
* Heat shields are typically 45-99.5% reliable over a 6-minute re-entry.
* Inflatable heat shields like the stock 10-meter do not currently have any failure modes.

License
------------
These configs are released under the MIT License. A copy of the license can be found in the file `LICENSE` in the mod directory, or online at http://opensource.org/licenses/MIT.
