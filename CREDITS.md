# Credits

## Audio

Two different licences cover the clips in this mod family, and the difference
matters if you are thinking of reusing them.

**The canid and felid voices are commercially licensed.** They are derived from
libraries bought from [Sonniss](https://sonniss.com/), whose licence permits use
in an unlimited number of projects, free or commercial, without attribution — but
explicitly forbids passing the sounds on to anyone else. So they are credited
here because provenance is worth recording, **not** because the licence demands
it, and the reuse grant in `ASSETS-LICENSE.md` deliberately does not extend to
them. See that file.

**The squirrel is CC0** from [Freesound](https://freesound.org/), where the
number leading each row is the sound ID and can be checked at
`https://freesound.org/s/<id>/`.

### Coyote — Discover Oregon, recorded by Tyler Hulett

| clip | source recording |
|---|---|
| idle, idle2, idle3, stressed, stressed2, pain | *Coyotes*, Discover Oregon Audio Library |
| death | *Arctic Fox, Animal* (Digiffects) |

Wild coyotes recorded in Oregon's Great Basin. The death clip is the exception —
see the substitutions note below.

### Fox — AudioHero

| clip | source recording |
|---|---|
| idle, idle2, idle3 | *Fox, Young, Fighting, Animal, Grumbles* (Digiffects) |
| stressed, stressed2 | *Fox* (AudioHero, Animals Vol. 3) |
| pain, death | *Arctic Fox, Animal* (Digiffects) |

### Bobcat — AudioHero

| clip | source recording |
|---|---|
| idle | *Cat Purr Close Up* |
| idle2 | *Domestic House Cat: Soft Meow* |
| idle3 | *Sad Cat Moans* |
| stressed, stressed2 | *Wild Bobcat: Growls and Snarls* |
| pain, death | *Cat, Meowing, Animal* (Digiffects) |

### Squirrel — Freesound, CC0

| # | uploader | recording | used for |
|---|---|---|---|
| 494745 | mzimny | Squirrel chirping | idle |
| 18515 | cognito-perceptu | Squirrel upset | stressed |
| 640992 | burgersmoke | Ground squirrel, first chirp | pain |
| 640993 | burgersmoke | Ground squirrel, second chirp | death |

### Substitutions, declared

Three species stand in for others somewhere in the set. None of this is hidden
in the audio; it is listed so nobody has to reverse-engineer it.

- **The bobcat is mostly a domestic cat.** Only *stressed* and *stressed2* are a
  real bobcat — a caged one, which is why they are growls and snarls rather than
  anything calm. The three idles and the pain and death clips are a house cat,
  pitched down. That is a closer substitution than it sounds: a bobcat is *Lynx
  rufus*, a small cat, and its calm vocabulary really is close to a house cat's.
  An earlier version used a **caracal** for the same slots and it was worse —
  wrong genus, raspier voice, and all three idles were hiss.
- **The coyote death is an arctic fox.** Coyote death vocalisations are not
  something anyone has recorded and released.
- **The fox pain and death are an arctic fox**, not the red fox the mod depicts.

### Juveniles

Every baby clip is its adult counterpart pitched up by a factor of 1.22, baked
offline because the engine parses a `pitch` key on a sound clip and never reads
it. No separate recordings were needed for the young animals.

The one place this is a real compromise is the **coyote pup**: coyote pups yip and
whine rather than howl, so a pitched-up adult call is a smaller adult rather than
a young animal. Real coyote pup recordings exist but the ones found were too quiet
to use.

### Reproducing these

The clips were cut by hand from the source libraries rather than by the automatic
span-picker, because hand cuts kept their attacks and the picker did not. The
edited sources live in the development repo under `audio/`, and
`tools/import_all_sounds.sh` turns them into the shipped files. They are derived
files: change the source and re-run rather than editing audio by hand.

## Models

Meshes were generated with [Meshy](https://www.meshy.ai/), then retopologised to
the vanilla vertex budget and skinned to Project Zomboid's own Raccoon and Rat
skeletons, so the animals move using the game's existing animation sets. The
build is reproducible from the development repo's `art/ai-models/` sources via
its `tools/build_critters.sh`.

## Project Zomboid

Raccoon and Rat skeletons, animation sets and the animal behaviour this addon
inherits are the work of The Indie Stone. Nothing from the base game is
redistributed here — the mod references vanilla assets by name and ships only its
own meshes, textures and audio.
