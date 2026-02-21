# cat-narrative-presence-rank

Ranks cat photographs by **narrative presence** — the degree to which each image implies a story unfolding across time rather than presenting a flat, resolved, static fact.

## What It Does

Given a collection of cat photographs, `cat-narrative-presence-rank` produces a score vector that ranks every image from strongest to weakest narrative presence. Images that make the viewer feel they have walked into the middle of a scene — where something has just happened, is actively happening, or is about to happen — rank highest. Images that feel complete and resolved, where the viewer looks, confirms a cat exists, and moves on, rank lowest.

## Input

An array of **2 or more cat photographs** (images). Any ordinary photographs of cats in any setting, taken by anyone, at any level of photographic skill. The function does not evaluate technical quality, resolution, or composition — only whether the image feels like a single frame pulled from a longer, ongoing scene.

```json
{
  "type": "array",
  "items": { "type": "image" },
  "minItems": 2
}
```

## Output

A score vector of the same length as the input array. Each score corresponds to the photograph at the same index, representing its relative narrative presence within the set. Higher scores indicate stronger narrative presence.

## What It Evaluates

The function assesses three perceptual qualities across each photograph:

### 1. Kinetic Implication

The degree to which the cat's physical state suggests movement through time. This goes beyond obvious action like leaping or running — it reads the subtler signals of the body:

- **Ear orientation**: Ears rotated toward something off-camera suggest the cat has just heard a sound and is deciding whether it matters.
- **Weight distribution**: Mass shifted forward onto the front paws signals the cat is about to go somewhere.
- **Gaze direction and intensity**: A locked, tracking gaze means something in the world is moving and the cat is following it.
- **Paw position**: A paw lifted or extended mid-reach implies an action in progress.
- **Postural tension**: A low crouch with raised hindquarters radiates coiled potential even in complete stillness.

Self-contained motions that lead nowhere — a yawn, a stretch — score low on kinetic implication because the scene returns to where it started. The question is whether the cat's body implies a *trajectory* toward a different future.

### 2. Relational Tension

The degree to which elements in the scene exist in an unresolved relationship to one another. This transforms a portrait into a situation:

- **Cat and person**: A hand reaching toward a cat that hasn't decided whether to accept the touch.
- **Cat and environment**: A cat poised at the edge of a surface with the ground visible below, or peering through a doorway.
- **Cat and another animal**: Two creatures locked in mutual awareness, outcome undecided.
- **Cat and the unseen**: A cat staring intently at something beyond the edge of the frame, recruiting the viewer's imagination to complete the scene.

Settled relationships — a cat curled in a lap, resting against a companion — carry little relational tension. The key is whether the interaction is *approaching*, *in progress*, or *suspended*, not already resolved.

### 3. Temporal Atmosphere

The degree to which the environment itself — independent of the cat's body language — evokes the passage of time:

- **Transitional light**: Dawn, dusk, or shifting shadows that tell you the world is moving between states.
- **Weather evidence**: Rain-wet surfaces, gathering clouds, or snow beginning to fall.
- **Aftermath cues**: Scattered objects, disturbed surfaces, or signs that something happened before the photograph was taken.
- **Seasonal or temporal anchoring**: Any quality that makes the scene feel like it could only have happened at this specific point in time.

Scenes that feel timeless and interchangeable — a cat against a blank background, photographed under neutral studio lighting — score lowest. Scenes anchored in the flow of time, where the viewer senses the stream of experience continuing beyond the frame, score highest.

## How the Qualities Combine

These three qualities are evaluated holistically. The strongest narrative presence emerges when all three converge — a cat whose body suggests imminent action, positioned in unresolved relationship to another element, within an environment that evokes the passage of time. But a photograph can rank highly with strength in only one or two dimensions. A perfectly still cat in a window at twilight, watching snow begin to fall, may carry extraordinary narrative presence through temporal atmosphere and relational tension alone.

## Use Cases

- **Content platforms**: Prioritize cat imagery that holds attention longer, since images implying a story invite viewers to linger and wonder.
- **Photography review**: Audit a set of shots to identify which carry the sense of life-in-progress and which fall flat.
- **Creative reference**: Find photographs that already contain the seeds of narrative — images that feel like illustrations for stories not yet written.
- **Collection curation**: Select images for galleries, social media, or editorial use that do more than document — images that communicate and invite the viewer into a moment.