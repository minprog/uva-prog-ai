# Homework Week 6

The homework for this week covers the chapters 13, 14 from [Think Java]. You
should read these chapters before you start on the exercises.

Please take note that the exercises are based on the exercises in *Think Java*,
but are not identical.

Submit your answers on the submit tab when you are finished.

[Think Java]: http://www.greenteapress.com/thinkapjava/

## Chapter 13

### Exercise 1
Encapsulate the code in Section 13.5 in a method. Then modify it so that the
aces are ranked higher that Kings.

### Exercise 2
Encapsulate the deck-building code of Section 13.6 in a method called `makeDeck`
that takes no parameters and returns a fully-populated array of Cards.

### Exercise 3
In Blackjack the object of the game is to get a collection of cards with a score
of 21. The score for a hand is the sum of scores for all cards. The score for an
ace is 1, for all face cards is ten, and for all other cards the score is the
same as the rank. Example: the hand (Ace, 10, Jack, 3) has a total score of 1 +
10 + 10 + 3 = 24.

Write a method called `handScore` that takes an array of cards as an argument
and that returns the total score.

### Exercise 4
In Poker a "flush" is a hand that contains five or more cards of the same
suit. A hand can contain any number of cards.

1. Write a method called `suitHist` that takes an array of Cards as a parameter
   and that returns a histogram of the suits in the hand. Your solution should
   only traverse the array once.
2. Write a method called `hasFlush` that takes an array of Cards as a parameter
   and that returns `true` if the hand contains a flush, and `false` otherwise.

## Chapter 14

### Exercise 1
The goal of this exercise is to implement the shuffling and sorting algorithms
from this chapter.

1. Download the code from this chapter from
   http://thinkapjava.com/code/Card2.java and import it into your development
   environment. I have provided outlines for the methods you will write, so the
   program should compile. But when it runs it prints messages indicating that
   the empty methods are not working. When you fill them in correctly, the
   messages should go away.
2. If you did Exercise 3 of Chapter 12, you already wrote
   `randomInt`. Otherwise, write it now and add code to test it.
3. Write a method called `swapCards` that takes a deck (array of cards) and two
   indices, and that switches the cards at those two locations.

   HINT: it should switch references, not the contents of the objects. This is
   faster; also, it correctly handles the case where cards are aliased.
4. Write a method called `shuffleDeck` that uses the algorithm in Section
   14.2. You might want to use the `randomInt` method from Exercise 3 of
   Chapter 12.
5. Write a method called `indexLowestCard` that uses the `compareCard` method to
   find the lowest card in a given range of the deck (from `lowIndex` to
   `highIndex`, including both).
6. Write a method called `sortDeck` that arranges a deck of cards from lowest to
   highest.
7. Using the pseudocode in Section 14.6, write the method called `merge`. Be sure
   to test it before trying to use it as part of a `mergeSort`.
8. Write the simple version of `mergeSort`, the one that divides the deck in
   half, uses `sortDeck` to sort the two halves, and uses `merge` to create a
   new, fully-sorted deck.
9. Write the fully recursive version of `mergeSort`. Remember that `sortDeck` is
   a modifier and `mergeSort` is a function, which means that they get invoked
   differently:
   
    sortDeck(deck);           // modifies existing deck
    deck = mergeSort(deck);   // replaces old deck with new
