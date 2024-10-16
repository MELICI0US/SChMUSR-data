# SChMUSR-data

Data from SChMUSR training

## File organization

Each results folder contains the data from a single run of the genetic algorithm with the following parameters:
- numGens: 200
- gamesPerGen: 50
- agentsPerGame: 10
- roundsPerGame: 30

The subfolders in each folder are:
- `gameInfos` - game data for each game sorted by generation. The game data contains all transactions and chat information
- `generations` - the gene population for each generation. The files contain the gene strings, number of games played, relative fitness, and absolute fitness
- `logs` - debug files, can be ignored
- `players` - gene strings that were selected for each game

## Possible routes of data exploration

I am particularly interested in how chatting changes among the agents as they learn.

Some different ideas for dissecting the chat data:
- Plot average number of chats sent per generation
- Plot average number of chats per round, per generation (This would be a 3-dimensional graph, or a graph with a slider)
- Plot topic of chats over generations
- Plot topic of chats per round, per generation
- Anything else you think of that might be interesting

Some things to look at that are not chat related (all by generation)
- Collective action
    - How much the agents are attacking together
    - How much they are giving in groups
- Reciprocity - if A gives to B, does B give to A?
- Triadic closure - if A and B have a relationship and B and C have a relationship, how often do A and C have one?
- Structual balance - if A and B are friends and B attacks C, how often does A also attack C?
- Anything else you think of that might be interesting

## List of vocab
 This is what you will find in the chat data (a few of these aren't used by the bots). It is slightly different from the limited chat vocab. I am still working on making them match.

- [PlayerNames] I am sending you [amount]
- [PlayerNames] we want you to join our group
- [PlayerNames] how much are you giving to me?
- [PlayerNames] how much are you stealing from them?
- [PlayerNames] how much are you keeping?
- [PlayerNames] what are your observations?
- Friends?
- We should group up
- Let's form a team
- Can we be friends?
- We would work well together
- Group up?
- we should drop [PlayerNames]
- We should add [PlayerNames]
- We should replace [PlayerName] with [PlayerName]
- [PlayerNames] did not give to me like they said
- [PlayerNames] attacked me
- I am attacking [PlayerName] with [amount]
- Same as last round
- Sending you each [amount] 
- Yes
- No
