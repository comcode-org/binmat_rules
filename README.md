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
  - [The Wild Modifier](#the-wild-modifier)
- [Win Conditions](#win-conditions)
- [Combat Examples and Edge Cases](#combat-examples-and-edge-cases)

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

If the competitive rules are being followed, the BINMAT app ([Game Structure](#game-structure)) may now be placed equidistant from the attacker and defender at one side of the play area.

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
Under competitive rules, each turn lasts five seconds. This rule can be ignored for casual play.

If competitive rules are being used, the BINMAT app (available for iOS and Android) provides an effective timer and turn counter. If not, any method of counting down from 110 to 0 can be used.

## Gameplay

### The Turn Cycle
The defender and attacker alternate turns, with defender starting first.
On your turn, you may perform one action or pass. 

The actions available are:
- Draw a card. [Drawing a Card](#drawing-a-card)
- Play a card from your hand to a lane's stack. [Playing a Card](#playing-a-card)
- Initiate combat in a lane. This is an attacker-only action. [Combat](#combat)
- Discard a card from your hand into a lane discard pile. This is a defender-only action.

You can inspect any discard pile, face-up stack, or face-down stack you control (attacker stacks for the attacker, defender stacks for the defender) at any time, even if it is not your turn.

### Drawing a Card
 
The defender can draw a card from any of the six lane decks. When you draw a card from the three lane decks which have their top card face up, turn over the next card in the deck so it is face up and place it on top of the deck.
The attacker can only draw from lane decks without a defender stack in front of them.
The attacker can also draw from a special 'attacker deck' which is to be placed at the side of the play area, in front of the attacker discard pile. This deck is not present at the start of the game, but can be formed via the rules below:

When a draw is attempted from an empty deck, the following takes place:
The deck's corresponding discard pile is shuffled into the deck.
The card can then be drawn from the top of the newly formed deck.

### Playing a Card

Playing a card is slightly different depending on your role as the attacker or defender.
See the subsections below:

#### DEFENDER:

First, select the card from your hand which you wish to play.
If this card is a number card, BOUNCE modifier (?), TRAP modifier (@) or WILD modifier (*) it can be  placed on any of your six defender stacks. If the defender stack on which you place this card is face up, the card must also be placed face up. If it is face down or empty, it must be placed face down. 

If this card is a BREAK modifier (>), it can be placed face-up or face-down on any defender stack which already contains at least one card, and does not contain another face-up break. When you place this card face-up, immediately initiate combat in the lane to which it was played. See [Combat](#combat).

#### ATTACKER:

First, select the card from your hand which you wish to play.
If this card is a number card, TRAP modifier (@) or WILD modifier (*) it can be placed on any of your six attacker stacks.

If this card is a BOUNCE modifier (?), you may perform one of the following:
Place this card face-up on an empty attacker stack. Commence combat immediately in this lane.
Place this card face-down to any attacker stack.

If this card is a BREAK modifier (>), it can be played face-up or face-down on any attacker stack which already contains at least one card. When you place this card face-up, immediately initiate combat in the lane to which it was played. This combat has slightly modified calculations, as described in [Combat](#combat).

### Combat

Only the attacker is allowed to initiate combat normally.
They can only do this in a lane in which they possess a stack of one or more cards.

When combat is initiated in a lane, the cards in both attacker and defender stacks are revealed.
- For all present TRAP modifiers in the stack of the player who initiated combat:
  - If the TRAP was turned from face-down to face-up by this revealing, send the top card in your opponent's stack to your discard pile. (lane discard for defender TRAPs, attacker discard for attacker TRAPs)

Now repeat this for all present TRAP modifiers in the stack of the other player.

The number cards present in the stack should now have their sum calculated. Any present WILD modifiers should
be resolved now. ([The Wild Modifier](#the-wild-modifier))

If the sum is not now a power of two, the stack has attack power zero. Otherwise, its attack power is the power of two to which the sum is equivalent.

If both stacks have attack power zero, or a BOUNCE modifier is present in either stack:
Send all BOUNCEs in this lane to opposing discard piles. (defender BOUNCE to attacker discard pile, attacker bounce to defender discard pile)
Send attacker stack to attacker discard pile.
Leave defender stack in place.
Combat has concluded.

If the attacker stack has a lower attack power, then the attacker stack goes to the lane's discard pile and the defender stack remains in its lane, face up.

If the attacker stack has an attack power equal to or greater than the defender stack, then the following takes place:

- If a BREAK modifier is not present in the attacker stack:
  - Calculate the absolute difference between attack powers, and then add one to it. This is the damage value.
- If a BREAK modifier is present in the attacker stack:
  - The attack power of the attacker stack is now the damage value.

- While the damage value is greater than zero:
  - If there are cards left in the defender's stack, send the most recently played card there to the attacker discard pile.
  - Else if there are not, but there are cards remaining in the lane's lane deck, send the top card from the lane deck to the attacker's hand.
  - Else if there are no cards remaining in the lane deck either, the attacker has won the game. ([Win Conditions](#win-conditions))
  - Subtract one from the damage value.
 
The attacker stack is now sent to the attacker discard.

### The Wild Modifier

The WILD modifier is applied to a stack during combat resolution.
It brings the sum of its stack up to the next highest power of two.
If there are no number cards in a stack, the first wild is treated as a 2 card, and all other WILDs apply as normal to this value.

### Win Conditions

The game is won by the defender if all 110 turns have elapsed without the attacker achieving victory.
The game is won by the attacker if they deal more damage to a lane deck than the lane deck has cards. This
is mentioned in combat resolution (see [Combat](#combat))

### Combat Examples and Edge Cases
[now a stub]
