# DeckSwipe

This is a skeleton for a simple card game. There are 5 gameplay resources (predefined as Coal, Food, Health, Hope, and Population), each contributing to the chances of survival for the player's city. Choices that the player makes through swiping each card left or right will influence those resources in various ways. If any one of the resources depletes (reaches zero), the game is lost and reset. The player's objective is to make decisions such that depletion doesn't happen, and the city survives, for as long as they can manage.

The core mechanics and visuals are heavily based on Reigns, and its clone, Lapse: The Forgotten Future. The sample content is mostly inspired by Frostpunk and its neverending winter.

Created with Unity on Linux, primarily targetting Android.

![Screen capture of the game running on Android](screencap-android.gif)

## Updates Added

This fork has added the following items to the game.
- Population resource: This resource is never directly changed by any cards, and instead is changed based on what other stats are whenever a card is resolved.
- Weather: This adds a new card that warns about a specific weather condition that is approaching in a few cards. Then after a few cards the weather is activated, warned with another card. Weather can add or subtract from resources every card it is active, and will last for a predetermined time. Only 1 weather can be active at a time.
- Card Rebalancing: Many cards had values changed to make it more likely to lose the game. Additionally, more cards were added to make more difficult decisions.
- A tutorial and story mode was added. These are different versions of the base game that only last for a set number of cards. The tutorial has preset cards that teach the game, while the story mode is random like the endless mode.
- Further changes listed under the "Our Contribution (Brisk)" section at the bottom of the page.

## Contributing

This project is not actively maintained. Some PRs may end up merged, but I do not have a Unity installation for testing. If you wish to make use of the repo, I recommend forking and adapting it to your needs.

Changes accepted in PRs will be released under the license terms provided in [LICENSE](./LICENSE).

## License

All content published in this repository, be it software, in source code or binary form, or other works, is released under the MIT License, as documented in [LICENSE](./LICENSE), with the following exceptions:

* **TextMesh Pro**

	Bundled with Unity and distributed on Unity license terms

	https://unity3d.com/legal

	Files:

	* `DeckSwipe/Assets/Dependencies/TextMesh Pro/*`

# Our Contribution (Brisk)
The group, Brisk, chose this project as our 3 week class assignment to modify and add changes to. Below we will list all the contributions we have made including project structure changes, mode chnages, mechanics, etc.

## Project Structure
Project structure was pretty unique to itself before we got our hands on it, but for a general developer it was hard to navigate and understand the code base. 

**Before**
- Had scripts, resources, and prefabs all thrown together, no organization
- Chaotic and hard ot understand

**After**
- More in line with standardized Unity practices.
- Much more traversable and immediately understandable.

## Tackling Issues (left by the original team in the original repo)
There are only a couple of issues in the original repo. Brisk decided to take most of these and fix them as part of our goals to modify the project.

__Issues__
- *Issue 1*: Eliminate need for dummy cards. To make other cards not randomly drawable, a dummy card was needed. We simply added a drawable property to the cards so they wouldn't need it as suggested by the issue.
- *Issue 2*: Visual preview of action outcomes. Players didn't have a way to see how the choices will affect their stats. They just swiped and it would take affect. We fixed this by changing the progress bar on a stat to show red for negative effects and green for negative effects.
- *Issue 4*: Update ReadME. ReadME needed a general update as well as updates with our (Brisk's) contributions. :)

## Other Changes
Outside of fixes to the proposed issues, we came up with a handful of changes we wnated to add to the game to make flesh it out more and make it more fun and interactive.

__Additional Changes (Baseline Goals)__
- *Mechanics Expansion*: We wanted to add more substance to the game. We came up with a couple on concepts:
  - A.) More stats for the player to manage - We settled on adding population management
  - B.) incoming events - Incoming events are just random events that occur. They're just a random card that can be pulled and could have an affect on the player's stats. Ultimately, the best outcome would have been if we could have provided some visual effect change or some seasonal mode to make the game more challenging.
  
- *Main Menu*: The game started up on the gameplay scene. To feel more complete and put together, we thoguht to add a Main Menu where users could choose between Survival Mode or Endless Mode.
  
- *New Game Mode*: The game only supported endless mode. We thought it would be way more interesting if the player could choose between a Survival mode where they had to make it to (number) days and hit a win screen. From there, they could switch to naother mode if they wanted. Endless mode was already a part of and was the default of DecksSwipe before we got to it.
  
- *More Cards*: There just weren't enouh cards to maintain player interest. There were also a lot of placeholder or dummy cards. We filled those out and added more of our own (including incoming events).



