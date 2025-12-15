# ISI Storm Chasers

A collection of mods to make storms fun. Storms should not be timeouts.

## Smoothie Durations

Extends the duration of smoothies to 10 minutes (up from 5) so you can pretend there's enough time to knock out a quest.

## Smoothie Immunity

Consuming a smoothie will negate storm damage (but not the other effects)

## Smoothie Spawns

Drinking a smoothie now summons a small swarm of the zombies for that biome. The zombies are not immediately aggressive, so you might be able to sneak away.

This also makes it easier to find the zombies needed for the biome challenges.

## Storm Adjustments

- Reduces storm warning period to 30 seconds.
- Reduces storm duration to 3 minutes.
- Provides ability to adjust storm damage and frequency. Left at default of 2 damage every 1 second.
- Provides an option to adjust grace period (non-damaging stage of storms). Left at default of 30 seconds.

## Testing

### General Testing Notes

Storms do not spawn on day 1, so you'll need to advance the time to day 2 or later.

| Console Command | Duration | Biome | Description |
|---------------|----------|-------|-------------|
| `weather storm` | 1 hour | All biomes | Triggers storm in all biomes |
| `weather storm 2` | 2 hours | All biomes | Triggers 2-hour storm in all biomes |
| `weather storm 2 burnt_forest` | 2 hours | Burnt Forest only | Triggers 2-hour storm in specific biome |

*biome names: `pine_forest`, `burnt_forest`, `desert`, `snow`, `wasteland`*

### Smoothie Durations Testing

__Test Steps:__

1. Consume the smoothie for the current biome (Black Lung Serum, Sunstroke Tonic, Scorcher Stew, Fallout Flush)
2. __Expected Result:__ Both hazard protection and speed boost should last 10 minutes (600 seconds) instead of 5 minutes

### Smoothie Immunity Testing

__Test Steps:__

1. During a storm, consume the corresponding biome smoothie
2. Stand in the storm without shelter
3. __Expected Result:__ No storm damage taken while smoothie is active

### Smoothie Spawns Testing

__Test Steps:__

1. Consume the corresponding smoothie for the current biome
2. __Expected Result:__ 5 biome-specific zombies spawn nearby

### Storm Adjustments Testing

__Test Steps:__

1. Trigger a storm in any biome: `weather storm 1 [biome_name]`
2. __Expected Results:__
   - Storm lasts 3 minutes (on 60-minute days)
   - Stage 1 - Grace period lasts 30 seconds
   - Stage 2 - Storm deals 4 damage every 2 seconds
