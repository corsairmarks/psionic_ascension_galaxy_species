# Overview

Have you ever noticed that the notification event when other empires pick the "Mind Over Matter" or "Transcendence" ascension perks indicates that members of the Latent/Fully Psionic species manifest abilities _regardless_ of their current empire?  Have you _also_ noticed how members of that species in your empire don't actually gain the Latent Psionic trait?  Then this mod is for you!  Now, every Pop and leaders of the same species as the main species of the empire that picked "Mind Over Matter" or "Transcendence" will gain the Latent Psionic or Psionic species trait (respectively).

# Changes

The notification event when another empire picks "Mind Over Matter" ends with

> The \<Mind Over Matter species\> population within our borders have **_begun exhibiting similar changes as well,_** so whatever is happening to their species is **_not localized to any single region of space_**" [emphases added]

and the notification for empires picking "Transcendence" mentions that

> "**_All \<Transcendence species\> throughout the galaxy have undergone a great change._** Whereas before their latent psionic power had only blossomed in a small minority, the entire species has now unlocked its full psychic potential. Although these changes seem to have originated in the \<Transcendence empire\>, **_they have now manifested in all members of their species regardless of where they reside_**" [emphasis added]

This mod does exactly what this original-to-the-game text says: any members of the newly Latent Psionic or Psionic species gain the appropriate species traits regardless of which empire controls them.

## Compatibility

Preempts the `utopia.2600` event that is responsible for the initial species upgrade with the Latent Psionic trait and `utopia.2650` event that is responsible for the initial species upgrade with the Psionic trait.  That means this mod is likely to conflict with other mods that want to alter the conversion process for normal -> latent psionic and/or latent psionic -> psionic.

Mods altering or allowing assimilation/ascension with different conditions aren't always a conflict.  For example [Two and half Ascension by kERHUS [RELOADED]](https://steamcommunity.com/sharedfiles/filedetails/?id=2373793047) has no conflicts.

Built for Stellaris version 3.2.\* "Herbert."  Not compatible with achievements.

### Required Mod Dependencies

[Leader Traits: All Eligible Species Traits](https://steamcommunity.com/sharedfiles/filedetails/?id=2499031295) - this mod ensures your leaders always gain the correct leader traits (such as Psionic) and contains a minor enhancement that leaders of _any_ Latent Psionic species have a chance to manifest full Psionic powers and gain the appropriate leader trait. This was previously restricted to occur for leaders that are both Latent Psionic and the same species as the empire's founder species.

### When to Install

This mod can be safely added to or removed from your savegame after the game has started.  It is implemented through events without adding or removing gameplay objects.  If you remove it, you will keep any modified species and leaders of those species with their existing traits, but further empires taking Mind Over Matter or Transcendence will only upgrade their own Pops and leaders.  Back up your savegame before trying to remove a mod.

## Known Issues

This mod overwrites preempts two events from the base game.  Expect to see two lines in error.log like this:

```
[23:17:20][eventmanager.cpp:355]: an event with id [utopia.2600] already exists!  file: events/utopia_on_action_events.txt line: 1328
[23:17:20][eventmanager.cpp:355]: an event with id [utopia.2650] already exists!  file: events/utopia_on_action_events.txt line: 1587
```

## Changelog

* 1.0.0 Initial version
* 1.1.0 Mark as compatible for Stellaris 3.1 "Lem" - no functionality changes
* 1.2.0 Mark as compatible for Stellaris 3.2 "Herbert" - no script changes
* 1.2.1 Fix not properly iterating all subspecies

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/psionic_ascension_galaxy_species)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.