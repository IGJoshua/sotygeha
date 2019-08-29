# sotyge'a
sotyge'a is a grammar for the lojban language based on zantufa which is intended to reduce the number of selma'o.

## FA -> BAI
The selma'o FA has been merged into the selma'o BAI.

### FA Conversion
Under zantufa, FA can be placed before the selbri of a bridi to perform a conversion similarly to SE. Under sotyge'a, this is no longer possible as FA no longer exists. Conversion falls back to SE. The one feature which this change affects is the following construct:

    ko'a fa je fe broda

This cannot be accomplished with SE, however can be approximated with JAI:

    ko'a jai fa je fe broda

This has similar meaning.

Note however that SE is not equivalent to JAI FA. Place structure is different:

    x1 broda x2 x3 x4 x5
    x2 se broda x1 x3 x4 x5
    x2 jai fe broda x2 x3 x4 x5 fai x1

### I BAI BO-linked bridi
In zantufa lojban two bridi can be linked by a BAI, semantically equal to making the second bridi into an abstraction under the BAI in the first bridi.

    broda .iki'ubo brode

This can now be extended to the fa series of cmavo:

    broda .ifebo brode

The following is an example sentence with translation:

    .i mi troci .ifebo mi tavla do bau la .lojban.

> I try to talk to you in lojban.

## LAhE -> BAI
The selma'o LAhE has been merged into the selma'o BAI.

cmavo of the la'e series will take up a slot in the place structure of the bridi of which they are a part, advancing the place structure as before. The following example does not change in meaning after this merger.

    ko'a broda tu'a ko'e ko'i

Under zantufa lojban, multiple BAI are allowed to be chained before consuming a single sumti. la'e series cmavo will be considered to combine with the fa series of cmavo with identical meaning regardless of order. Both of the following jufra have the same meaning.

    broda fi tu'a ko'a
    broda tu'a fi ko'a

Currently there are no semantics for a la'e-series cmavo when used in an I BAI BO compound cmavo.
