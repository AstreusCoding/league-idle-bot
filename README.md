# **Champion Manager Idle Bot Concept**

## **1. Core Gameplay Loop**

- Players choose a starting champion, pulled from the same pool of starter champions available in the official League of Legends game.

- Champions start at level 1, with no level cap, making progression continuous. The core stats of each champion are based on their default League values but with tweaks to adapt to an idle setting (e.g., scaling some values up, percentage changes, etc.).

- Players initially have to actively interact with the bot, using their champion to battle enemies like caster minions, melee minions, and occasionally encountering random champion fights.

- **Death Penalty**: If the champion dies, they are put on a death timer. The timer scales with level, so it’s short at early levels, allowing players to get back into action quickly. At higher levels, the timer becomes longer, encouraging careful strategy rather than just rushing in.

## **2. Currency System**

- There are **two main currencies**:

- **Blue Essence**: Collected through progression and completing objectives. It can be used for champion upgrades or acquiring new champions.

- **Gold**: Earned by killing minions, monsters, and enemy champions. Used to purchase items and upgrade existing ones.

## **3. Items and Crafting**

- All **items** from League are available, spanning multiple patches, which brings in nostalgia and adds variety. Some items are only **craftable** rather than buyable, making them rarer and more rewarding.

- Champions have no hard cap on how many items they can have equipped. Instead, items can be **upgraded infinitely**, adding a star modifier (e.g., **Thornmail ★ 10** if upgraded 10 times). This gives players the freedom to customize builds without limitations.

- Items can be upgraded using gold and crafting materials.

- **Crafting Materials**: Players can obtain crafting materials from defeating random champion encounters. Materials dropped are based on the items in the enemy champion's inventory. For example, defeating a champion with **Rabadon's Deathcap** may reward a **Needlessly Large Rod**.

## **4. Champion Combat and Spells**

- Champions have their **standard spells** from League, but with tweaks to adapt to the text-based, non-visual environment of Discord.

  - For example, **Ahri's Q** would target all enemies on the board, while **Ahri's E (Charm)** could only target a single enemy. This encourages players to strategize and use spells at the right time.

- Combat starts out manually, with players picking which abilities to use in battles against minions and champions.

- As players progress, more idle features unlock, such as **automated spell-casting**, allowing the bot to automatically use certain abilities in combat, shifting the focus from micromanaging fights to making strategic choices for your champion.

## **5. Progression System**

- Early-game gameplay is more active, allowing players to make choices about abilities, targets, and items in real-time to maximize efficiency.

- As champions level up, they unlock **idle features** that automate more of the gameplay (e.g., auto-casting spells, auto-targeting minions). This way, early players feel more involved, while late-game players enjoy a more hands-off, strategic experience.

- **Enemies** scale with champion level, starting with basic minions and moving up to tougher units and powerful random champion encounters.

- Defeating champions and tougher enemies rewards **Blue Essence** and sometimes **rare crafting materials**.

## **6. Balancing Risk and Reward**

- Early game has minimal punishment for dying, which makes the game more accessible for new players.

- Later in the game, dying incurs a longer death timer, making players consider their strategies more carefully.

- This gradual increase in challenge keeps the gameplay engaging, rewarding players who learn how to optimize their champions and items.

## **7. Future Features**

### **Champion Roster Expansion**

- Players can use Blue Essence to unlock additional champions, expanding their roster. Initially, players can have up to 3 champions to participate in normal wave battles. Eventually, they can unlock up to 5 champions to participate in full simulated Summoner's Rift matches, facing off against another team of 5. These matches follow the standard ranked mode champion picks, allowing players to place champions in any lane and strategize with counterpicks.

### **Team Battles**

- Players can control multiple champions as they expand their roster. In normal "wave" battles, up to 3 champions can be used. For special Summoner's Rift matches, players need to have at least 5 champions, giving them the ability to recreate the feeling of a full League match. The ability to mix and match champions and strategize based on lane matchups adds depth to gameplay.

### **Guild System**

#### Overview

Players can join guilds to collaborate on challenges, earn rewards, and compete as a team, adding a strong community element to the game. Guild members can contribute to joint challenges and participate in cooperative battles.

#### Roles

Guilds can have roles such as Leader, Officer, and Member. Leaders and Officers can initiate guild battles, recruit new members, and manage guild activities. Roles give structure to the guild and help organize team efforts effectively.

List of roles:

- **Leader**: The guild leader, has all available permissions in the guild.

- **Officer**: Has the ability to invite, kick members and manage guild activities.

- **Member**: no special permissions

#### Levels and rewards

Guilds can level up by completing joint missions, winning battles, and contributing resources. Higher-level guilds unlock exclusive features such as special guild-only items, buffs that benefit all members, or unique guild quests. Rewards for leveling up can include crafting materials, exclusive items, or increased battle bonuses.

#### Quests

Guild quests track each member's contributions, encouraging players to stay active and support their guild. High contributions could lead to personal rewards or higher ranks within the guild.

##### Contribution System

Guild quests track each member's contributions, encouraging players to stay active and support their guild. High contributions could lead to personal rewards or higher ranks within the guild.

##### Types of Guild Quests

- **Daily Quests**: These are small tasks that refresh every day and can be completed by individual members. Completing daily quests earns rewards for the guild and helps members contribute to the guild's progress.

- Weekly Quests: These are quests that refresh every week and require guild members to achieve collective goals, such as defeating a certain number of enemies or crafting specific items.

- Monthly Quests: Larger-scale quests that require more significant contributions, like winning a certain number of guild battles or reaching a milestone in resource collection. Completing monthly quests provides rare rewards for the entire guild.

#### Guild Currency

Guilds can earn a separate currency, Guild Tokens, which can be used to purchase guild upgrades, shared buffs, or unique customization options like a clan tag, banners, and emblems to represent the guild.

#### Guild Battles

- **Guild Battles**: Guilds can initiate battles against each other in 5v5 matches. Here’s an example: Guild "Rose" challenges Guild "Dose" to a battle. Guild members from both sides can participate, and a 5v5 battle is initiated. When a player from Guild Rose initiates a fight, the opponent from Guild Dose has 10 minutes to either accept a live match or default to an automated roster battle.

   **Live Match**: If the opponent chooses a live match, the battle is conducted like a normal ranked draft, where both players are online.

- **Default Roster Battle**: If the opponent doesn’t respond or chooses the automated option, their default roster is used. In this case, the enemys champion lanes are hidden from the attacker, adding an element of unpredictability.

- After 7 minutes of the timer, another guild member who has not yet participated can "protect" or take over the fight. This feature is crucial as default roster battles can be at a disadvantage due to the opponent being able to fully counterpick their champions. This mechanic encourages guild members to be active and strategically plan their battles to counter threats effectively.

#### Guild Chat and Coordination

##### Chat

Adding a dedicated guild chat inside the Discord bot allows guild members to communicate directly, coordinate battles, or plan quests. This helps to foster teamwork and makes participating in guild activities more streamlined.

##### Coordination Tools

Guild chat can be enhanced with coordination tools, such as reminders for upcoming guild battles, and the ability to create polls for deciding on strategies or participation in events. These tools help members stay informed and engaged in guild activities.
