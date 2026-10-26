# Introducing Pocket Planet: Tamagotchi in 30 seconds
Here's my take on the popular simulated pet game, Tamagotchi, reimagined for single-session play. Try it here 🔗https://ramakronym.github.io/pocket-planet/

## Why Tamagotchi
Growing up as a single child, Tamagotchi was one of my favorite games to play as it was portable, addictive, while serving the role of a friend and a therapy animal all rolled up in one. I'd be excited to hear the device beep, indicating my attention was most needed to help my digital pet survive and thrive. And the best part was Tamagotchi was immortal - you could always restart the game with a fresh life!

<img width="335" height="597" alt="image" src="https://github.com/user-attachments/assets/e38bff6f-befe-4b80-afe1-0baa5e5e7cd1" />


## The game, reimagined
I started out exploring a thesis on how the best parts of Tamagotchi could be translated into a single-session game while still inflicting similar emotions of supervision, care and belonging. 

## The first real iteration: make choices matter
The first release used twelve care choices across three chapters and upon playing around with it, I felt like clicking buttons felt too simple. I proposed thirty seconds, scarce credits, and pets whose needs could conflict with the available budget.

A randomized briefing before the clock. Players can inspect one of four temperaments, initial needs, prices, and activity supplies. Budgets vary from 13 to 34 credits. Planning is unhurried; execution takes thirty seconds.

Scarcity plus time. Needs continuously fall at temperament-specific rates. Care spends credits and supplies. Activity time, individual cooldowns, energy requirements, and reduced repeat benefits make timing matter.

React or stay the course? Wishes appear at 6 and 18 seconds, with six-second response windows. A temporary discount from 12–18 seconds creates another spending decision.

A transparent outcome. Care score rewards needs maintained over the whole round (65 points), wishes answered (20), and care variety (15). Players also receive an evolution and a downloadable keepsake. Random loadouts mean scores across different rounds are not a standardized skill comparison.

<img width="514" height="757" alt="Screenshot 2026-10-25 at 8 38 40 PM" src="https://github.com/user-attachments/assets/d73fb887-8981-46dd-b00b-5ec6a64e3e53" />

## Building with an agentic tool
I set the goal of adapting the Tamagotchi concept for short play sessions, shaped the initial requirements and visual direction, and approved the MVP. ChatGPT Work translated that direction into a static web game, implemented the interface and game rules, and prepared the hosted release.

The implementation uses original CSS creature art, browser-local persistence, optional synthesized audio, and a generated PNG keepsake. The second iteration translated Anu’s gameplay critique into a pure rules engine and a live timed interface. Gameplay uses fixed rules and curated text; it does not call a language model at runtime.

## A deliberately small architecture
index.html provides the interface. style.css provides the console, responsive layouts, creature art, and animation. engine.js contains testable rules for budgets, need decay, requests, scoring, and evolution. game.js connects those rules to the interface and saving.

No account or backend is required. Progress stays in the current browser; clearing browser storage removes it. A saved deadline makes the timer continue through tab changes and refreshes. Sound is opt-in, interactions support keyboard input, and animation respects reduced-motion preferences.

## What comes next
This is a first playable release, not a validated product. Automated checks cover 300 simulated rounds, credit and supply limits, cooldowns, wishes, discount boundaries, and expiry after refresh. Next: observe first-time players and tune difficulty, cost distributions, and whether thirty seconds gives enough room for strategy. Physical phone playtesting remains outstanding.

The next journey entries should capture real feedback, bugs, rejected ideas, and before-and-after iterations. No user research results or performance metrics are claimed yet.


