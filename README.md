# Kata-Object-Calisthenics


Object Calisthenics ?
---------

>Do a simple project using far stricter coding standards than you’ve ever used in your life.
>Below, you’ll find 9 “rules of thumb” that will help push your code into good object-oriented
>shape.
>By suspending disbelief, and rigidly applying these rules on a small, 1000 line project, you’ll
>start to see a significantly different approach to designing software. Once you’ve written 1000
>lines of code, the exercise is done, and you can relax and go back to using these 9 rules as
>guidelines.

-  [Object Calisthenics pdf](http://www.cs.helsinki.fi/u/luontola/tdd-2009/ext/ObjectCalisthenics.pdf)
-  Object Calisthenics (full book), Jeff Bay in: The ThoughtWorks Anthology.
Pragmatic Bookshelf 2008
-  Original idea for the kata: How Object-Oriented Are You Feeling Today? - Krzysztof Jelski (Session on the Software Craftsmanship UK 2011 conference)

The Rules
---------

1. One level of indentation per method
2. Don’t use the ELSE keyword
3. Wrap all primitives and Strings
4. First class collections
5. One dot per line
6. Don’t abbreviate
7. Keep all entities small (50 lines)
8. No classes with more than two instance variables
9. No getters/setters/properties

The Kata
---------
- 1h20 : Let's code ! TDD et Pair programming obligatoires
- 30min : Chaque groupe explique son code. Quelles règle sont été respectées, lesquelles ont été enfreintes? Pourquoi ? Quel design a émergé de l'exercice ?

Tests D'acceptation (US)
---------
**US** : Can depose and withdraw money on my account

```
Given a client makes a deposit of 1000€ on 10-01-2012
  And a deposit of 2000€ on 13-01-2012
  And a withdrawal of 500€ on 14-01-2012
When she prints her bank statement
Then she would see
Date       || Credit    || Debit  || Balance
14/01/2012 ||           || 500.00 || 2500.00
13/01/2012 || 2000.00   ||        || 3000.00
10/01/2012 || 1000.00   ||        || 1000.00
```

**US** : Can depose money on my account with different currencies

```
Given the exchange rate USD to EUR is 0.8924 
Given a client makes a deposit of 1000€ on 10-01-2012
  And a deposit of 2000$ on 13-01-2012
When she prints her bank statement
Then she would see
Date       || Credit    || Debit  || Balance
14/01/2012 ||           || 500.00 || 2500.00
13/01/2012 || 2000.00   ||        || 3000.00
10/01/2012 || 1000.00   ||        || 1000.00
```

**US** : Can withdraw money on my account with different currencies

```
Given the exchange rate EUR to USD is 1.206 
Given a client makes a deposit of 1000€ on 10-01-2012
    And a withdrawal of 500$ on 14-01-2012
When she prints her bank statement
Then she would see
Date       || Credit    || Debit  || Balance
14/01/2012 ||           || 500.00 || 2500.00
13/01/2012 || 2000.00   ||        || 3000.00
10/01/2012 || 1000.00   ||        || 1000.00
```
