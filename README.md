# BINMAT - The Human Compatible Rulebook

## Credits
'thx alic' alice ([@alicehmd](https://github.com/alicehmd)), 'uncle deetr' dtr

## Index

- [The Binmat Deck](#the-binmat-deck)
- [Game Setup](#game-setup)
- [Game Structure](#game-structure)
- [Gameplay](#gameplay)
  - [The Turn Cycle](#the-turn-cycle)
  - [Drawing a Card](#drawing-a-card)
  - [Playing a Card](#playing-a-card)
  - [Combat](#combat)
  - [The Wild Modifier](#the-wild-modifier-)
- [Win Conditions](#win-conditions)
- [Combat Examples and Edge Cases](#combat-examples-and-edge-cases)
- [Modifier Quick Reference](#modifier-quick-reference)

## The Binmat Deck

The standard BINMAT deck is composed of seventy-eight (78) cards.
These cards are distributed in six suits, displayed below:

\& - FORM

\% - KIN

\+ - DATA

\! - CHAOS

\^ - VOID

\# - CHOICE

Every suit contains thirteen cards. Nine of these cards are numbered 2 to 10, and are referred to as such.
The other four cards are as follows:

\@ - TRAP

\* - WILD

\? - BOUNCE

\> - BREAK

These cards are known as 'modifiers'.

## Game Setup

To begin the game, first all players shall pick a team, 'attacker' or 'defender'. It is generally suggested that the players divide themselves evenly, but this is not strictly required. The only limitation is that each team may contain 16 players at most.

The attackers and defenders should be seated opposite each other, and the area between them is hence known as the 'play area'. The play area should be divided into six parallel 'lanes' which traverse the area from attacker to defender or vice versa.

The BINMAT deck being used for gameplay ([The Binmat Deck](#the-binmat-deck)) should be shuffled, and then dealt as follows:

Deal thirteen cards face down into each lane at the defender team's end.
Turn the top card in the three left decks (defender POV) over so they are visible.

These six decks are referred to as 'lane decks'.

Enough space for another deck should be left behind (defender team's perspective) the decks in each lane, as this is the location of the 'lane discard pile'.

Enough space should also be left beside the play area for another deck, the 'attacker deck', and behind it space for the 'attacker discard pile'.

The BINMAT app ([Game Structure](#game-structure)) or other turn counter and timer may now be placed equidistant from the attacker and defender at one side of the play area.

The following is an ASCII representation of the play area at the conclusion of setup:

```
                     defender's position


|         |         |         |         |         |         |
|         |         |         |         |         |         |
|         |         |         |         |         |         |
|         |      lane discard pile locations      |         |
|         |         |         |         |         |         |
|         |         |         |         |         |         |
|         |         |         |         |         |         |
| +-----+ | +-----+ | +-----+ | +-----+ | +-----+ | +-----+ |
| |     | | |     | | |     | | |4    | | |3    | | |2    | |
| | {h} | | | {h} | | | {h} | | |!    | | |!    | | |!    | |
| |     | | |     | | |   lane decks !| | |    !| | |    !| |
| |     | | |     | | |     | | |    4| | |    3| | |    2| |
| +-----+ | +-----+ | +-----+ | +-----+ | +-----+ | +-----+ |
|         |         |         |         |         |         |
|         |         |         |         |         |         |
|         |         |         |         |         |         |
|         |        defender stack location        |         |
|         |         |         |         |         |         |
|         |         |         |         |         |         |
|         |         |         |         |         |         |
|         |         |         |         |         |         |
|         |         |         |         |         |         | +-----+
|         |         |         |         |         |         | |     | attacker deck location
|         |         |         |         |         |         | |     |
|         |         |         |         |         |         | |     |
|         |         |         |         |         |         | |     |
|         |         |         |         |         |         | +-----+
|         |         |         |         |         |         |
|         |         |         |         |         |         | +-----+
|         |         |         |         |         |         | |     | attacker discard pile location
|         |        attacker stack location        |         | |     |
|         |         |         |         |         |         | |     |
|         |         |         |         |         |         | |     |
|         |         |         |         |         |         | +-----+


                     attacker's position


```

## Game Structure

The game is composed of 110 turns (55 for the attackers, 55 for the defenders).
Each turn lasts five seconds, though resolving combat typically requires pausing the timer.
When learning or experimenting, the timer can be extended or ignored, though rapid play is encouraged, as time pressure is an intentional part of the game.

The BINMAT app (available for iOS and Android) provides an effective timer and turn counter. If it is not available, any method of counting down from 110 to 0 can be used.

## Gameplay

### The Turn Cycle
The defenders and attackers alternate turns, with defenders starting first.
On each turn, every member of the corresponding team may perform one action. These actions will be resolved in sequential order, as detailed in [Turn Order](#turn-order).
If you do not complete your turn within 5 seconds, you automatically pass your turn with no further penalty.

The actions available are:
- Draw a card. [Drawing a Card](#drawing-a-card)
- Play a card from your hand to a lane's stack. [Playing a Card](#playing-a-card)
- Initiate combat in a lane. This is an attacker-only action. [Combat](#combat)
- Discard a card from your hand into a lane discard pile. This is a defender-only action.

You can inspect any discard pile, face-up stack, or face-down stack your team controls (attacker stacks for the attackers, defender stacks for the defenders) at any time, even if it is not your turn.

### Turn Order
Each member of a team is assigned a number within that team. As a result of the maximum number of team members being 16, this number is generally expressed through 1 hex character, 0 through f.

For casual human play, it is suggested that the turn order be fixed, with member 0's action resolving first, then 1's, through to f.
In a 'real game' (for instance in hackmud), turn order changes each turn according to an as-of-yet poorly understood algorithm. The only constant is that member 0 always goes first. (This is not technically constant in hackmud as a result of certain edge cases, but this is beyond the scope of this rulebook.)

It should be noted that a consequence of the sequential resolution of actions is that a member of your team whose action resolves before yours may result in your own action becoming invalid. For instance, if attacker 0 declares combat in a lane, resulting in the stack in that lane being cleared out, and attacker 1's action is also to declare combat in that lane, attacker 1's action has become invalid, since there is no longer a stack in that lane.

### Drawing a Card

A defender can draw a card from any of the six lane decks.
An attacker can only draw from lane decks without a defender stack in front of them.
When any player draws a card from the three lane decks which have their top card face up, turn over the next card in the deck so it is face up and place it on top of the deck.
Attackers can also draw from a special 'attacker deck' which is to be placed at the side of the play area, in front of the attacker discard pile. This deck is not present at the start of the game, but can be formed via the rules below:

When a draw is attempted from an empty deck, the following takes place:
- If the deck has a discard pile with at least one card in it:
  - The deck's corresponding discard pile is shuffled into the deck.
  - If the deck formerly had its top card turned face up, turn the top card face up.
  - The card can then be drawn from the top of the newly formed deck.
- If the deck's associated discard pile is empty, the team that controls that deck loses the game.
  For example, if any player attempts to draw from a lane deck that has no cards available and no cards in its discard pile, the defenders lose. If an attacker attempts to draw from the attacker deck in similar circumstances, the attackers lose.
  Note that attackers cannot be forced into drawing from their deck, nor can defenders be forced to draw from a lane deck, as any player can pass freely. The general case added by and to appease dtr in the hopes that it may trap a poorly programmed BINMAT bot some day.

An attacker can also choose to discard a card from their hand to the attacker discard pile in order to draw two cards from their deck. Note that these draws follow the above rules like any other draws, and so can trigger attacker loss.

### Playing a Card

You can play one card to one of your team's stacks as your action. Generally, this card should be played matching the facing of the stack - an empty stack is face down.
The BREAK (>) and BOUNCE (?) modifiers are subject to special rules concerning how they are played, which are detailed below.

#### Special Rules: BREAK (>)

A BREAK can only be played to a stack that contains another card, it cannot be the first card in a stack.
A BREAK can be played face up to a face down stack.
When a BREAK is played face up to a stack (whether through the above rule or by playing it normally to a stack that is already face up), combat is immediately initiated in the lane to which it was played. This rule allows defenders to initiate combat. This combat has slightly modified calculations, as described in [Combat](#combat).

#### Special Rules: BOUNCE (?)

For defenders, there are no special rules concerning the BOUNCE. It should be played normally as described above.
For attackers, the BOUNCE can be played face up to an empty stack. This action commences combat in the lane to which it was played.

### Combat

Only attackers are allowed to initiate combat normally.
They can only do this in a lane in which they possess a stack of one or more cards.

When combat is initiated in a lane, the cards in both attacker and defender stacks are revealed.
- For all present TRAP modifiers (@) in the stack of the team that initiated combat:
  - If the TRAP modifier (@) was turned from face-down to face-up by this revealing, discard the most recently played card in the opposing stack to your discard pile. (lane discard for defender TRAP modifiers (@), attacker discard for attacker TRAP modifiers (@))

Now repeat this for all remaining TRAP modifiers (@) in the stack of the other team.

The number cards present in the stack should now have their sum calculated. Any present WILD modifiers (\*) should
be resolved now. ([The WILD Modifier (\*)](#the-wild-modifier-))

If the sum is not now a power of two, the stack has attack power zero. Otherwise, its attack power is the power of two to which the sum is equivalent.

If both stacks have attack power zero, or a BOUNCE modifier (?) is present in either stack:
Discard all BOUNCE modifiers (?) in this lane to opposing discard piles. (defender BOUNCE modifiers (?) to attacker discard pile, attacker BOUNCE modifiers (?) to defender discard pile)
Discard attacker stack to attacker discard pile.
Leave defender stack in place.
Combat has concluded.

If the attacker stack has a lower attack power than the defender stack, the attacker stack is discarded to the lane's discard pile and the defender stack remains in its lane, face up.

If the attacker stack has an attack power equal to or greater than the defender stack, then the following takes place:

- If a BREAK modifier (>) is not present in either stack:
  - Calculate the absolute difference between attack powers, and then add one to it. This is the damage value.
- If a BREAK modifier (>) is present in either stack:
  - The damage value is the attack power of the attacker stack, or the number of cards in the defender stack, whichever is greater.

For every point of damage, discard the most recently played card in the defender stack to the attacker discard pile.
If the defender stack is empty, then a draw from the lane deck takes place. If the combat was initiated by an attacker, then this attacker performs these draws. If combat was initiated by a defender through the use of a BREAK, then attacker 0 performs the first draw, then attacker 1, cycling the attackers until the remaining points of damage have been consumed. If the attackers cannot draw from the lane deck (because it is empty and so is its discard pile), the attackers win the game ([Win Conditions](#win-conditions))

The attacker stack is now sent to the attacker discard.

### The WILD Modifier (\*)

The WILD modifier (\*) is applied to a stack during combat resolution.
It brings the sum of its stack up to the next highest power of two.
If there are no number cards in a stack, the first WILD modifier (\*) is treated as a 2 card, and all other WILD modifiers (\*) apply as normal to this value.

### Win Conditions

- The game is won by the defenders if all 110 turns have elapsed without the attacker achieving victory.
- The game is won by the defenders if the attackers attempt to draw a card from the attacker deck when neither it nor the attacker discard pile has any cards in it.
- The game is won by the attackers if they are unable to draw a card from a lane deck as a result of attacking that lane. (see [Combat](#combat))
- The game is won by the attackers if either team attempts to draw a card from a lane deck when neither it nor its associated discard pile has any cards in it.

### Combat Examples and Edge Cases
[now a stub]

### Modifier Quick Reference
This section is meant to be a quick reference of modifier effects for use in game.
Since the rules are in a state of flux, it is entirely possible that a change will be made to the rules without updating this section.
The rules take precedence over this section if they ever are contradictory.

#### Attackers:
- **TRAP modifier (@)**
  - Can be played face-down on any attacker stack
  - When combat is initiated, each TRAP modifier revealed (flipped) in initiator's stack discards the most recently played card in the opponent's stack to the initiator's discard pile.
    Then, each remaining TRAP modifier revealed (flipped) in the opposing stack discards the most recently played card in the initiator's stack to the opponent's discard pile.
- **WILD modifier (\*)**
  - Can be played face-down on any attacker stack
  - When damage is calculated, bring your attack power to the next highest power of 2. If there are no number cards in the stack, the first WILD modifier (\*) is treated as a 2 instead
- **BOUNCE modifier (?)**
  - Can be played...
    - ... face-up on any attacker stack with no cards in it
      - When played this way, immediately initiate combat in the lane it was played
    - ... face-down on any attacker stack
  - When combat is affected by a BOUNCE modifier, discard all BOUNCE modifiers (?) in either stack to the opposing discard pile (attacker BOUNCE modifiers (?) to lane discard, defender BOUNCE modifiers (?) to attacker discard), discard the attacker stack to attacker discard, and end the combat (no damage is caused)
- **BREAK modifier (>)**
  - Can be played...
    - ... face-down on any attacker stack with at least one card in it
    - ... face-up on any attacker stack with at least one card in it
      - When played this way, immediately initiate combat in the lane it was played
  - If combat is not affected by a BOUNCE modifier (?) and either stack still has a BREAK modifier (>) that has not been destroyed by a TRAP modifier (@), your damage for this attack is your attack power or the number of cards in the defender's stack, whichever is greater. (rather than the difference plus 1)

#### Defenders:
- **TRAP modifier (@)**
  - Can be played on any defender stack, matching facing
  - When combat is initiated, each TRAP modifier revealed (flipped) in initiator's stack discards the most recently played card in the opponent's stack to the initiator's discard pile.
    Then, each remaining TRAP modifier revealed (flipped) in the opposing stack discards the most recently played card in the initiator's stack to the opponent's discard pile.
- **WILD modifier (\*)**
  - Can be played on any defender stack, matching facing
  - When damage is calculated, bring your attack power to the next highest power of 2. If there are no number cards in the stack, the first WILD modifier (\*) is treated as a 2 instead
- **BOUNCE modifier (?)**
  - Can be played on any defender stack, matching facing
  - When combat is affected by a BOUNCE modifier, discard all BOUNCE modifiers (?) in either stack to the opposing discard pile (attacker BOUNCE modifiers (?) to lane discard, defender BOUNCE modifiers (?) to attacker discard), discard the attacker stack to attacker discard, and end the combat (no damage is caused)
- **BREAK modifier (>)**
  - Can be played...
    - ... face-down on any face-down defender stack with at least one card in it
    - ... face-up on any defender stack, regardless of facing, so long as it does not have another face-up BREAK modifier (>) in it
      - When played this way, immediately initiate combat in the lane it was played.
  - If combat is not affected by a BOUNCE modifier (?) and either stack still has a BREAK modifier (>) that has not been destroyed by a TRAP modifier (@), the attacker's damage for this attack is their attack power or the number of cards in the your stack, whichever is greater. (rather than the difference plus 1)
