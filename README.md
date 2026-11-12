# base-unit-trait-covert

The `Covert` unit trait: a unit type with it is a covert agent.

A unit type with this trait has the missions that only a covert agent has, on top of `DiplomaticMissions`, and may survive them. Which missions those are, and the odds, are the game's rules.

For example: Civ2: Spy.

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(Covert)`:

```ts
import Covert from '@civ-clone/base-unit-trait-covert/Covert';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, Covert));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
