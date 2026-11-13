# Roblox Developer Toolkit

Reusable Luau modules for Roblox experiences. Includes cooldowns, combat math, table helpers, and player utilities.

## Install
Copy `src` ModuleScripts into `ReplicatedStorage/DeveloperToolkit` in Roblox Studio. Require each module where needed. CooldownManager is server-side state; do not trust client cooldown checks for security.

## Example
See `examples/Example.server.luau`. No external dependencies.

## API
- `CooldownManager.new()`; `:tryUse(key, seconds)` -> boolean, remaining seconds; `:remaining(key)`; `:clear(key)`
- `DamageCalculator.calculate(base, multiplier, armor)` -> nonnegative damage (armor is fractional reduction from 0 to 1)
- `TableUtils.shallowCopy(table)`, `TableUtils.keys(table)`
- `PlayerUtils.isValidPlayer(player)`

MIT licensed.
