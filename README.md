# RFC - modpacks
## Scope of this document
This document will discuss the implementation of modpacks within MultiMC and the methodology behind the formats used to create instances. This RFC hopes to create a better experience to users by making things easier for developers and producers within the community by having a flexible standardization of modpacks.

## What formats modpacks exist in
1. Distributed archives
  - Zips
  - Version Control
      - Git
2. Platforms
  - FTB
  - Technic
  - Mojang (Soon™)
3. Others

## Exporting an instance in MultiMC
Exporting an instance in MultiMC will give the users a choice of what they want to include in their modpack

Among these options will include:
- Config pack
- Mod pack

Both of these options can be customized and by default MultiMC won't include what are considered sensitive configs. Ultimately however it is up to the user to double check that they aren't including a config that could include sensitive data.

### Libraries
By default, MultiMC will include a copy of the libraries needed to run that instance. While MultiMC itself won't run instances with the libraries with them (Because they are logically separated) - *Needs to be reviewed*

Including these libraries will provide a user the ability to run the instance with everything they need, and no reliance on outside systems (Besides Mojang's services for obvious reasons)

### Save Format
**Needs discussion**

A zip file would be a fine, but having a easy to distinguish file format would make finding the modpack easier to find and provide simple expectations for developers.

## Importing an instance in MultiMC
###Distributed archives
Distributed archives will be imported by dragging and dropping the modpack onto the front screen of MultiMC

**Needs to be expanded upon to include a standard layout**

###Platforms
Platforms will require a little bit more work if they are to be handled by MultiMC in that they **should** use a standard format in json to represent the various components of a modpack and where to find them.

**JSON API formats will be up for example in the "apis" folder under "proposals".**

Feel free to submit a Pull Request for review.
