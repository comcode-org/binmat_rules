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

To begin the game, first both players shall assume a role. One player is to be the 'attacker', and the other player is to be the 'defender'. These terms will be used for the duration of this rulebook without further explanation.

The attacker and defender should be seated opposite each other, and the area between them is hence known as the 'play area'. The play area should be divided into six parallel 'lanes' which traverse the area from attacker to defender or vice versa.

The BINMAT deck being used for gameplay ([The Binmat Deck](#the-binmat-deck)) should be shuffled, and then dealt as follows:

Deal thirteen cards face down into each lane at the defender's end.
Turn the top card in the three left decks (defender's POV) over so they are visible.

These six decks are referred to as 'lane decks'.

Enough space for another deck should be left behind (defender's perspective) the decks in each lane, as this is the location of the 'lane discard pile'.

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

The game is composed of 110 turns (55 for the attacker, 55 for the defender).
Each turn lasts five seconds, though resolving combat typically requires pausing the timer.
When learning or experimenting, the timer can be extended or ignored, though rapid play is encouraged, as time pressure is an intentional part of the game.

The BINMAT app (available for iOS and Android) provides an effective timer and turn counter. If it is not available, any method of counting down from 110 to 0 can be used.

## Gameplay

### The Turn Cycle
The defender and attacker alternate turns, with defender starting first.
On your turn, you may perform one action or pass.
If you do not complete your turn within 5 seconds, you automatically pass your turn with no further penalty.

The actions available are:
- Draw a card. [Drawing a Card](#drawing-a-card)
- Play a card from your hand to a lane's stack. [Playing a Card](#playing-a-card)
- Initiate combat in a lane. This is an attacker-only action. [Combat](#combat)
- Discard a card from your hand into a lane discard pile. This is a defender-only action.

You can inspect any discard pile, face-up stack, or face-down stack you control (attacker stacks for the attacker, defender stacks for the defender) at any time, even if it is not your turn.

### Drawing a Card

The defender can draw a card from any of the six lane decks.
The attacker can only draw from lane decks without a defender stack in front of them.
When either player draws a card from the three lane decks which have their top card face up, turn over the next card in the deck so it is face up and place it on top of the deck.
The attacker can also draw from a special 'attacker deck' which is to be placed at the side of the play area, in front of the attacker discard pile. This deck is not present at the start of the game, but can be formed via the rules below:

When a draw is attempted from an empty deck, the following takes place:
- If the deck has a discard pile with at least one card in it:
  - The deck's corresponding discard pile is shuffled into the deck.
  - If the deck formerly had its top card turned face up, turn the top card face up.
  - The card can then be drawn from the top of the newly formed deck.
- If the deck's associated discard pile is empty, the player who 'controls' that deck loses the game.
  For example, if either player attempts to draw from a lane deck that has no cards available and no cards in its discard pile, the defender loses. If the attacker attempts to draw from the attacker deck in similar circumstances, the attacker loses.
  Note that the attacker cannot be forced into drawing from their deck, nor can the defender be forced to draw from a lane deck, as either player can pass freely. The general case added by and to appease dtr in the hopes that it may trap a poorly programmed BINMAT bot some day.

### Playing a Card

Playing a card is slightly different depending on your role as the attacker or defender.
See the subsections below:

#### DEFENDER:

First, select the card from your hand which you wish to play.
If this card is a number card, BOUNCE modifier (?), TRAP modifier (@), or WILD modifier (\*), it can be placed on any of your six defender stacks. If the defender stack on which you place this card is face up, the card must also be placed face up. If it is face down or empty, it must be placed face down.

If this card is a BREAK modifier (>), it can be placed face-up on any defender stack which already contains at least one card, and does not contain another face-up BREAK modifier (>), or placed face-down on any face-down defender stack which already contains at least one card. When you place this card face-up, immediately initiate combat in the lane to which it was played. See [Combat](#combat).

#### ATTACKER:

First, select the card from your hand which you wish to play.
If this card is a number card, TRAP modifier (@), or WILD modifier (\*), it can be placed on any of your six attacker stacks.

If this card is a BOUNCE modifier (?), you may perform one of the following:
- Place this card face-up on an empty attacker stack. Commence combat immediately in this lane.
- Place this card face-down to any attacker stack.

If this card is a BREAK modifier (>), it can be played face-up or face-down on any attacker stack which already contains at least one card. When you place this card face-up, immediately initiate combat in the lane to which it was played. This combat has slightly modified calculations, as described in [Combat](#combat).

### Combat

Only the attacker is allowed to initiate combat normally.
They can only do this in a lane in which they possess a stack of one or more cards.

When combat is initiated in a lane, the cards in both attacker and defender stacks are revealed.
- For all present TRAP modifiers (@) in the stack of the player who initiated combat:
  - If the TRAP modifier (@) was turned from face-down to face-up by this revealing, discard the most recently played card in your opponent's stack to your discard pile. (lane discard for defender TRAP modifiers (@), attacker discard for attacker TRAP modifiers (@))

Now repeat this for all remaining TRAP modifiers (@) in the stack of the other player.

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
  - The damage value is the attack power of the attacker stack, or the number of cards in the defender's stack, whichever is greater.

For every point of damage, discard the most recently played card in the defender's stack to the attacker's discard pile.
If the defender's stack is empty, the attacker instead draws a card from the lane deck. If the attacker cannot draw from the lane deck (because it is empty and has no lane discard pile), the attacker wins the game ([Win Conditions](#win-conditions))

The attacker stack is now sent to the attacker discard.

### The WILD Modifier (\*)

The WILD modifier (\*) is applied to a stack during combat resolution.
It brings the sum of its stack up to the next highest power of two.
If there are no number cards in a stack, the first WILD modifier (\*) is treated as a 2 card, and all other WILD modifiers (\*) apply as normal to this value.

### Win Conditions

- The game is won by the defender if all 110 turns have elapsed without the attacker achieving victory.
- The game is won by the defender if the attacker attempts to draw a card from the attacker deck when neither it nor the attacker discard pile has any cards in it.
- The game is won by the attacker if they are unable to draw a card from a lane deck as a result of attacking that lane. (see [Combat](#combat))
- The game is won by the attacker if either player attempts to draw a card from a lane deck when neither it nor its associated discard pile has any cards in it.

### Combat Examples and Edge Cases
[now a stub]

### Modifier Quick Reference
This section is meant to be a quick reference of modifier effects for use in game.
Since the rules are in a state of flux, it is entirely possible that a change will be made to the rules without updating this section.
The rules take precedence over this section if they ever are contradictory.

#### Attacker
- **TRAP modifier (@)**
  - Can be played face-down on any attacker stack
  - When combat is initiated, each TRAP modifier revealed (flipped) in initiator's stack discards the most recently played card in the opponent's stack to the initiator's discard pile.
    Then, each remaining TRAP modifier revealed (flipped) in the opponent's stack discards the most recently played card in the initiator's stack to the opponent's discard pile.
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

#### Defender:
- **TRAP modifier (@)**
  - Can be played on any defender stack, matching facing
  - When combat is initiated, each TRAP modifier revealed (flipped) in initiator's stack discards the most recently played card in the opponent's stack to the initiator's discard pile.
    Then, each remaining TRAP modifier revealed (flipped) in the opponent's stack discards the most recently played card in the initiator's stack to the opponent's discard pile.
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
