# Pokecoin
Pokemon Battle 'Proof of Victory' Based Cryptocurrency Experiment

Note: All copywrited and trademarked material belongs to Nintendo and Pokemon, and is used for educational purposes.  This coin is not intended to be convertable to USD or any other value based currency.

# Pokecoin Basics
Pokecoin is a Pokemon based proof of concept Cryptocurrency that uses a modified "Proof-of-Work" system that is completed by challenging and defeating different difficulties of 'Gym Leaders'.  The logs of the battle are entirely recreatable, and although there are multiple victorious scenarios, the person to reach it first and broadcast the successful mining will generate the next block.  Failure to complete the battle successfully will still reward Trainers (miners) with Rare Candy, and other items they can use to power up their team, making the next iteration of battles more likely to be successful.

## Miner Experience

### Begining the Journey
A Miner picks a starter pokemon and begins their journey.  They can fight small 'Wild Encounters' and attempt to defeat their foe.  Doing so will reward them with Rare Candies.  They can use those Rare Candies to power up their Pokemon until they are strong enough to face a Gym Leader.  Beating the Gym Leader will reward them with a small amount of Pokecoin.  Using that, they can purchase additional Pokemon, items such as Pokeballs (to capture more pokemon) or potions to speed up the recovery of their Pokemon (Pokemon injured in the course of battling take time to recover on their own).

Purchases pending will be stored in the Memcache, where they will wait until a Block is mined successfully, and they'll be added to the blockchain.

### Gym Battles
At first, Gym Battles will be a manual process.  Using an interface similar to the Gameboy Games, Trainers (miners) will battle opponents using Moves known by their Pokemon.  Automated battles will be available for purchase at a certain point, and you can buy and use certain 'Battle Condition Logic' from the Pokemart.  An example of a BCL is 'If enemy is not confused, and the Pokemon I have in battle knows Confuse Ray, use Confuse Ray' (the details of that are still being worked out.

As a security feature, outcomes of Attacks, Turns, and Battles will have to be calculated on the server/cloud to prevent spoofing.  A client (browser) will submit the action to be taken, the server will process that action, calculate the results, and then notify the client of those results.  All the random variables will be stored as to be able to reproduce the battle down to the last Health Point perfectly every time.  That will serve as the Proof of Victory that is difficult to solve, but quickly and easily confirmed by peers.  After a battle is won, the server will issue the results to the network with a hash of the entirety of the log to ensure tampering didn't occur.

### Gym Dynamics
Following the flow of the games, there will be a level of Gym that coorelates with the Canon of the game, but with modified difficulty.  A Gym Battle may be attempted, and won or lost, as many times as the Trainer wants, but with the exponential model of returns, the higher the badge, the higher the reward, and so there is incentive for the Trainer to move on to bigger, more difficult challenges as their team develops and strengthens.

Boulder Badge will be the first and most simple of the badges, followed by Cascade, Thunder, Rainbow, Soul, Marsh, Volcano, Earth Badge and then for futher reward Elite Four, the Elite Four Champion, and then Ash himself.  There may be continuations into the other region and generations, but that is for a later date.  

Unlike the original canon, it wouldn't be difficult enough if we stuck to a specific Elemental Type for each badge (Ground and Rock being the Boulder Badge).  Doing so would lower the difficulty because a Trainer could prime their chances of victory by banking on the elemental advantage.  There would need to be an array of Pokemon, of many Elemental Types, owned by each Gym Leader to keep things interesting.

In the minting process, and to maintain the iterations, the battle difficulty will have to increase, making the Proof of Victory only occuring, on average, at the set rate.  This, too, is a difficult question to answer, and has not been determined at this time.

### Technology Stack
I will not be forking any Coin Core, choosing rather to start from scratch.  Being familiar with Node.js (although I'm not set in stone with it) I'll be building it in Typescript/Node/Express first, and perhaps migrating to C++.  As for a database, I'm not set on the specific one.  I really like Realm, but see more documentation for MongoDB and Cassandra, so I might go with those.  

# Purpose
Although I have been developing for years now, I am constantly trying to learn and challenge myself.  I don't have much time for this project, but want to deeply explore Blockchain.  I will be using Mastering Bitcoin (https://github.com/bitcoinbook/bitcoinbook) as my guide, and although this may never actually happen, any progress in this exercise will benefit me on this path in the blockchain world.
