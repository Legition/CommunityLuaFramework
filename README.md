# Welcome to Community Lua Framework Repository (CLF Repository)

![Community Lua Framework Poster](/OtherResources/Graphics/poster.png "Community Lua Framework Poster")

## About

This project main mission is to create easy to use set of LUA libraries for Project Zomboid (Hereinafter referred to as PZ) modder in order for them to focus more on their idea of the mod instead of coding helper functions to work with PZ Lua Api.
This motivation comes from my personal experience where I was working on simple idea which then forced me to write functions to interact with inventory, functions to properly run timed actions, detections of positions. And I was thinking, that anybody who use these essentials of PZ game in their mod, must be coding this kind of the functions over and over again. Sometimes, modders steal others code just so they can focus on their idea.
Hopefully, this project will allow faster mod creation, lower the entry barrier of LUA modding and mainly lower the need of stealing others code. 

### Backward Compatibility

This project started while the latest PZ version was 42.16.3. Therefore this framework will not be supporting version 41.*.* as the game experience a huge changes of the inner working.
Since version 42 is marked as unstable and has very frequent changes, this project will always focus on latest version of 42.

For the future Major releases (like 43.*.*, 44.*.*), we will try to keep all the functionalities working for the latest version of that Major release.

### Roadmap

All planed functionalities and its status can be found at [Roadmap](/Roadmap.md "Roadmap with all planed functions").

## How To Use it

For simple usage and single point of truth, this project will be packed as any other PZ mod on the Steam Workshop.

### How To Install

Go to [Steam Workshop Page](www.NotReleasedYet.com "Community Lua Framework Repository Workshop Page") and "follow" this mod, just like you would with any other PZ mod.

### How To Include In Other Mod

In order to be able to use our libraries in other mod, you should applies following steps:
- Install CLF as mentioned above
- Add following lines to your mod.info (The main and version one) 
``` 
require=CommunityLuaFramework
loadModAfter=CommunityLuaFramework
```
- (Optional) In each lua script which use CLF, cache the root library with fast fail mechanism. 
F.E.:
```
local CLF 
if not _G.CommunityLuaFramework then 
  DebugLog.log(DebugType.Mod,"[<YOUR_MODE_NAME>][FATAL] - Missing dependency: Community Lua Framework Mod")
  return
else 
  CLF = _G.CommunityLuaFramework
end
``` 
This way you will make easier for the user to understand what is wrong.

### Documentation

All libraries, its functions and examples are documented at the project [repository wiki](https://github.com/Legition/CommunityLuaFramework/wiki)

## How To Contribute

This project should be an Community effort therefore any help is welcome. You can contribute in 4 ways

### Idea For New Function

If you have new idea for library or new function, first check if similar idea is not already in our [Roadmap](/Roadmap.md "Roadmap with all planed functions"). If not, you can start a new [discussions](https://github.com/Legition/CommunityLuaFramework/discussions) (discussion category - Ideas) where you should describe your idea and a way how it should work. You can use following template:
```
Discussion Category: Ideas
Title: Function Proposition <proposed function/library name>
Write: 
Describe what the function/library should do. 
Describe why the function/library should be part of CLF?
Describe how the function would be beneficial for others. Ideally add some examples of theoretical usage of such function/library.
```

### Bug Reporting

If you find an issue, first make sure its an issue of CLF and not issue of the mod using CLF. If its truly an CLF issue you can report it [here](https://github.com/Legition/CommunityLuaFramework/issues). You can use following template:
```
Title: 5-7 word name for the issue
Write:
On what version of CLF is the issue happening? (Aka, Steam Workshop vs Test Branch)
What the issue is.
How to reproduce the issue.
How easy is to reproduce the issue. (Aka, its happening always, or only sometimes?)
What would be the expected behavior.
```

### Framework Testing

Anybody can test the CLF and report any bugs. But testers should not be using version from the steam, but directly clone this repository to their mod folder and switch to "test" branch.

Additionally tester will need separate mod of their own making, which will be using the test version of CLF and validate that its behavior is as expected.

NOTE: If you have already install version from steam and you want to be active tester, you will first need to unfollow the steam version of CLF.

### Framework Coding

If you want to directly push new code to the CLF Repository, please contact me on discord (legition#1637). Before you contact me, please prepare some of your work from past to show and think of what you can bring to the project. 