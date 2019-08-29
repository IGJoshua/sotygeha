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

cmavo of the la'e series will take up a slot in the place structure of the bridi of which they are a part, advancing the place structure as before. This change does not affect semantics, it is only a consequence of the fact that both BAI and LAhE take structures that behave like sumti as inputs and also output such structures. The terminator for both is still LUhU. The following example does not change in meaning after this merger.

    ko'a broda tu'a ko'e ko'i

This merge makes standard JAI, used on its own, equivalent to JAI tu'a. Other useful JAI conversions are now possible, including but not limited to: JAI la'e, JAI lu'e, and JAI zo'ei.

Under zantufa lojban, multiple BAI are allowed to be chained before consuming a single sumti. la'e series cmavo will be considered to combine with the fa series of cmavo with identical meaning regardless of order. Both of the following jufra have the same meaning.

    broda fi tu'a ko'a
    broda tu'a fi ko'a

Currently there are no semantics for a la'e-series cmavo when used in an I BAI BO compound cmavo.

### BAI ... LUhU
In order to disambiguate in some cases with the LAhE/BAI merger a way to terminate a single BAI before the scope of an enclosing one becomes necessary. Contemplate the following jufra:

    broda fi la'e ko'a je ko'e

Under this new grammar, both ko'a and ko'e are under the influence of both BAI. The selma'o LUhU can be appropriated to become a new BAI terminator.

    broda fi la'e ko'a lu'u je ko'e

This allows the scope of la'e to extend over ko'a, while fi is scoped over ko'a je ko'e. This becomes the one exception to how JA functions, in that it can now combine any two things which are the same, but it may also combine a completed BAI 

As a part of this change, the grammar of the BAI clause changes such that it matches the grammar of a sumti, and is viable any place a sumti is viable.

## List of eliminated selma'o

The following is a list of all selma'o in the standard (CLL) Lojban grammar.

**A BAI BAhE BE BEI BEhO BIhE BIhI BO BOI BU BY CAI CAhA CEI CEhE CO COI CU CUhE DAhO DOI DOhU FA FAhA FAhO FEhE FEhU FIhO FOI FUhA FUhE FUhO GA GAhO GEhU GI GIhA GOI GOhA GUhA I JA JAI JOI JOhI KE KEI KEhE KI KOhA KU KUhE KUhO LA LAU LAhE LE LEhU LI LIhU LOhO LOhU LU LUhU MAI MAhO ME MEhU MOI MOhE MOhI NA NAhE NAhE+BO NAhU NIhE NIhO NOI NU NUhA NUhI NUhU PA PEhE PEhO PU RAhO ROI SA SE SEI SEhU SI SOI SU TAhE TEI TEhU TO TOI TUhE TUhU UI VA VAU VEI VEhA VEhO VIhA VUhO VUhU XI Y ZAhO ZEI ZEhA ZI ZIhE ZO ZOI ZOhU BRIVLA CMENE**

Here is the sotyge'a list.

**BAI BAhE BE BEI BEhO BO BOI BU BY CEI CO COI CU DOhU FAhO FEhU FIhO FOI FUhA GA GEhU GI GOI I JAI JOI KE KEI KEhE KOhA KU KUhE KUhO LE LEhU LI LIhU LOhO LOhU LU LUhU MAI MAhO ME MEhU MOI MOhE NA NAhE NAhE+BO NAhU NIhE NIhO NOI NU PA PEhO PU ROI SA SE SEI SEhU SI SU TEI TEhU TO TOI TUhE TUhU UI VAU VEI VEhO VUhO VUhU XI Y ZEI ZO ZOI ZOhU BRIVLA**
