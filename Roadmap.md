# Community Lua Framework RoadMap

This is a live document as the roadmap is still in planning state
Don't take this as any commitment so far.

## Logging

- [ ] Logger Library
  - [ ] Internal function for mod id detection
  - [ ] Log info with automatic message formatting
  - [ ] Log warn with automatic message formatting
  - [ ] Log debug with automatic message formatting
  - [ ] Log fatal with automatic message formatting and callstack listing

## Item Manipulation

- [ ] Item Manager Library
  - [ ] Item struc wrapper
    - [ ] Wrap item
    - [ ] Get item from wrap
    - [ ] Internal function to populate metadata
  - [ ] Search inventory for item (return list of candidates)
  - [ ] Search tiles around player for item (return list of candidates)
  - [ ] Merge candidates
  - [ ] Filter candidates

## Timed Action Manipulation 
- [ ] Timed Action Planner Library
  - [ ] Get new plan
  - [ ] Add action to plan
    - [ ] Move item to root inventory
    - [ ] Move item to sub inventory/tile
    - [ ] Equip item
    - [ ] Unequip item
    - [ ] Move to world object
    - [ ] Custom timed action
  - [ ] Translate plan to instances
  - [ ] Finish Plan
  - [ ] Get plan status 
- [ ] Timed Action Runner Library
- [ ] Run Plan
  - [ ] Timed Action Wrapper
  - [ ] Dynamic queueing of actions
  - [ ] Time action result propagating to plan