# roblox EZWeatherSystem

## Inspiration:
me and bro wanted to make a mic up game but with weather lolol

## Usage:

There are 2 modules to this system: ```weatherclass.ts, weathersystem.ts```

(NOTE: These systems only operate on client)

### Create a new weather description by using the WeatherClass

```typescript
let Weather = new WeatherClass(AreaParticleEmitter : ParticleEmitter | undefined, FloorParticleEmitter : ParticleEmitter | undefined, SoundEffect : Sound | undefined, Properties : Properties);

// Properties are written like so:
// {Inst : Instance, Properties : PropertiesToChange}
// Basically it will execute a tween on Inst of properties PropertiesToChange.
```

(Note: You can create as much weather descriptions as you want)


### Create a new weather system for the client by using the WeatherSystem

```typescript
let WeatherSystem = new WeatherSystem();

//boom that's it
```

Current code:

```typescript
let Weather = new WeatherClass(AreaParticleEmitter : ParticleEmitter | undefined, FloorParticleEmitter : ParticleEmitter | undefined, SoundEffect : Sound | undefined, Properties : Properties);
let WeatherSystem = new WeatherSystem();
```

### Apply the `Weather` to the `WeatherSystem` by using the `WeatherSystem.applyWeather(Weather)` function

```typescript
let Weather = new WeatherClass(AreaParticleEmitter : ParticleEmitter | undefined, FloorParticleEmitter : ParticleEmitter | undefined, SoundEffect : Sound | undefined, Properties : Properties);
let WeatherSystem = new WeatherSystem();

WeatherSystem.applyWeather(Weather);
```
This will tween the properties to the instances specified and it will set the particle emitter around the player to be `AreaParticleEmitter` and the particle emitter under the player to be `FloorWeatherEmitter` and it will set the current playing sound to be the `SoundEffect`.

## API:

`class WeatherClass(AreaParticleEmitter : ParticleEmitter | undefined, FloorParticleEmitter : ParticleEmitter | undefined, SoundEffect : Sound | undefined, Properties : Properties)`

`public void WeatherClass.applyWeather()`

`class WeatherSystem()`

`public WeatherClass.applyWeather(Weather : Weather)`
