# sotyge'a
sotyge'a is a grammar for the lojban language based on zantufa which is intended to reduce the number of selma'o. It has three primary goals:

* Reduce number of selma'o
* Allow new valid jufra with meanings which are intuitive for speakers of zantufa lojban
* Minimize change in existing texts required to conform to sotyge'a

## Inherited changes from zasni-gerna/zantufa

* **Cmavo merges:**
    * GOhA, CMEVLA -> BRIVLA
    * CUhE, FAhA, KI, PU, TAhE, VA, VEhA, VIhA, ZAhO, ZEhA, ZI -> BAI
    * PEhE -> BAhE
    * CEhE -> BO
    * LAU, TEI, FOI -> BY
    * DOI -> COI
    * A, BIhI, GIhA, JA, ZIhE -> JOI
    * NUhI -> KE
    * NUhU -> KEhE
    * LA -> LE
    * NAhU -> MAhO
    * NUhA -> ME
    * NIhE -> MOhE
    * CAhA -> NA
    * FEhE, MOhI -> NAhE
    * SOI -> SEI
    * ZEI -> SI
    * CAI, DAhO, FUhE, FUhO, GAhO, NAI, RAhO -> UI
    * JOhI -> VUhU
* Eliminated BIhE, GUhA
* `gi'i` moved to own selma'o GIhI
* `iau` with its own selma'o introduced

## FA -> BAI
The selma'o FA has been merged into the selma'o BAI.

### FA Conversion
Under zantufa, FA can be placed before the selbri of a bridi to perform a conversion similarly to SE. Under sotyge'a, this is no longer possible as FA no longer exists. Conversion falls back to SE. The one feature which this change affects is the following construct:

    ko'a fa je fe broda

This cannot be accomplished with SE, however can be approximated with `jai`:

    ko'a jai fa je fe broda

This has similar meaning.

Note however that SE is not equivalent to `jai` FA. Place structure is different:

    x1 broda x2 x3 x4 x5
    x2 se broda x1 x3 x4 x5
    x2 jai fe broda x2 x3 x4 x5 fai x1

### I BAI BO-linked bridi
In zantufa lojban two bridi can be linked by a BAI, semantically equal to making the second bridi into an abstraction under the BAI in the first bridi.

    broda .iki'ubo brode

This can now be extended to the `fa` series of cmavo:

    broda .ifebo brode

The following is an example sentence with translation:

    .i mi troci .ifebo mi tavla do bau la .lojban.

> I try to talk to you in lojban.

## LAhE -> BAI
The selma'o LAhE has been merged into the selma'o BAI.

cmavo of the `la'e` series will take up a slot in the place structure of the bridi of which they are a part, advancing the place structure as before. This change does not affect semantics, it is only a consequence of the fact that both BAI and LAhE take structures that behave like sumti as inputs and also output such structures. The terminator for both is still LUhU. The following example does not change in meaning after this merger.

    ko'a broda tu'a ko'e ko'i

This merge makes standard `jai`, used on its own, equivalent to `jai tu'a`. Other useful `jai` conversions are now possible, including but not limited to `jai la'e` and `jai lu'o`.

Under zantufa lojban, multiple BAI are allowed to be chained before consuming a single sumti. `la'e` series cmavo will be considered to combine with the `fa` series of cmavo with identical meaning regardless of order. Both of the following jufra have the same meaning.

    broda fi tu'a ko'a
    broda tu'a fi ko'a

Currently there are no semantics for a `la'e`-series cmavo when used in an I BAI BO compound cmavo.

### BAI ... LUhU
In order to disambiguate in some cases with the LAhE/BAI merger a way to terminate a single BAI before the scope of an enclosing one becomes necessary. Contemplate the following jufra:

    broda fi la'e ko'a je ko'e

Under this new grammar, both `ko'a` and `ko'e` are under the influence of both BAI. The selma'o LUhU can be appropriated to become a new BAI terminator.

    broda fi la'e ko'a lu'u je ko'e

This allows the scope of `la'e` to extend over `ko'a`, while `fi` is scoped over `la'e ko'a lu'u je ko'e`.

As a part of this change, the grammar of the BAI clause changes such that it matches the grammar of a sumti, and is viable any place a sumti is viable.

## NAhE (and NAhE+BO) -> BAI
The selma'o NAhE, as well as the pseudo-selma'o NAhE+BO, have both been merged into the selma'o BAI.

When placed before a sumti, it has the semantics of NAhE+BO. When placed before a selbri or followed by KU, it applies the effect of the NAhE to the main selbri in the contained bridi, with the usual left-to-right scope rules. Terminator: LUhU, as with all other selma'o merged into BAI.

Note that NAhE+BO has already become redundant to plain NAhE under zantufa. Here both have become redundant.

## JAI -> BAI
The selma'o JAI has been merged into the selma'o BAI.

This is possible because of how zantufa allows for compound tags, e.g. `bai bau`, parsed as follows:

    (bai bau KU) (jo'au zantufa)
    (bai KU bau KU) (jo'au catni)

The semantics of `jai` is still the same as before. When placed before a selbri or followed by KU in a compound tag with another BAI (which can itself be a compound tag), it moves the old x1 of its bridi to fai and replaces it with the tagged place. When on its own, it assumes `tu'a` to be the other BAI.

## CEI -> SEI
The selma'o CEI has been merged into the selma'o SEI.

CEI has only one member, and its only use is to appear in a bridi followed by a selbri of the broda-series. It is clear that this grammar corresponds to that of SEI. No change to semantics.

## VUhU -> JOI
The selma'o VUhU has been merged into the selma'o JOI.

JOI is already possible with the syntax of VUhU in mekso under zantufa, and JOI can already be controlled by PEhO and FUhA in these mekso. This change simplifies this further by allowing VUhU as non-logical connectives outside mekso, in phrases such as

    ti su'i ta

PEhO and FUhA remain mekso-exclusive. Operators of arity other than 2 are still handled the old-school way using `zi'o`/`tu'o` and `ge'a`.

## NA -> SE
The selma'o NA has been merged into the selma'o SE.

NA occurs before selbri, before connectives, or before `ku`. SE occurs before selbri, before connectives, or before tags. (It also occurs before operators but those have already been merged with connectives.) Two of these uses already overlap, therefore NA is close to SE even under standard grammar. The other uses are made equal.

"SE ku" can now occur and move SE somewhere else than before the main selbri. Scope is the same as with NA - from left to right, and with SE before the main selbri having outermost scope. The following three jufra are identical in meaning:

    .i broda se ku te ku .i se te broda .i se broda te ku .i te ku se broda

"na BAI" now means the same as "BAI nai".

In addition, any number of SE, as opposed to just one, is now allowed before connectives and tags - since NA is now part of SE. The following become grammatical:

    .i se te pi'o .i na se pi'o .i se na pi'o .i mi se te .u do .i mi na se .u do .i mi se na .u do

Note that `na se .u` is not the same as `se na .u`. The first one negates input 1 to `se .u`, i.e. it is true when input 2 is true. The second one swaps the places of `na .u`, i.e. it is true when input 2 is false.

(Under zantufa, NA also includes CAhA. CAhA is therefore now also part of SE.)

## Other changes

* Relative clauses are allowed after selbri, as in zasni-gerna and zantufa.
* Due to the VUhU-JOI merge, PEhO now becomes obligatory.
* n-ary `gi` now also allows the degenerate case of only one term.
* SA remains in the grammar, but always erases back to the last mulno jufra (marked by explicit or elidable `iau`).

## List of eliminated selma'o

The following is a list of all selma'o in the standard (CLL) Lojban grammar.

**A BAI BAhE BE BEI BEhO BIhE BIhI BO BOI BU BY CAI CAhA CEI CEhE CO COI CU CUhE DAhO DOI DOhU FA FAhA FAhO FEhE FEhU FIhO FOI FUhA FUhE FUhO GA GAhO GEhU GI GIhA GOI GOhA GUhA I JA JAI JOI JOhI KE KEI KEhE KI KOhA KU KUhE KUhO LA LAU LAhE LE LEhU LI LIhU LOhO LOhU LU LUhU MAI MAhO ME MEhU MOI MOhE MOhI NA NAhE NAhE+BO NAhU NIhE NIhO NOI NU NUhA NUhI NUhU PA PEhE PEhO PU RAhO ROI SA SE SEI SEhU SI SOI SU TAhE TEI TEhU TO TOI TUhE TUhU UI VA VAU VEI VEhA VEhO VIhA VUhO VUhU XI Y ZAhO ZEI ZEhA ZI ZIhE ZO ZOI ZOhU BRIVLA CMEVLA**

The following selma'o from the above list survive in sotyge'a.

**BAI BAhE BE BEI BEhO BO BOI BU BY CO COI CU DOhU FAhO FEhU FIhO FUhA GA GEhU GI GOI GOhA I JOI KE KEI KEhE KOhA KU KUhE KUhO LE LEhU LI LIhU LOhO LOhU LU LUhU MAI MAhO ME MEhU MOI MOhE NIhO NOI NU PA ROI SA SE SEI SEhU SI SU TEI TEhU TO TOI TUhE TUhU UI VAU VEI VEhO VUhO XI Y ZO ZOI ZOhU**

In addition, **GIhI** and **IAU** are two new selma'o in sotyge'a (inherited from zantufa) which are not in the CLL grammar.

# Optional Merges
Occasionally there are some selma'o which can be merged but which would have a more significant impact on intercompatibility between old and new texts. Merges like those which can be considered a part of sotyge'a but which are not required for its use are listed below.

## BEI -> BE
The selma'o BEI has been merged into the selma'o BE.

So far, BEI has been used to add sumti to a selbri after the first one. This is done in order to disambiguate between:

    broda be lo brode bei lo brodi = (broda (be lo brode KU) (bei lo brodi KU) BEhO)
    broda be lo brode be lo brodi  = (broda (be lo brode (be lo brodi KU) BEhO KU) BEhO)

However, such disambiguation is only needed for sumti of the type `lo broda` with an omitted KU, which is quite wasteful.

Wherever the sumti is more simple, e.g. just a KOhA, BY, ZO, or similar, `bei` simply becomes `be`, with no loss of ambiguity. For example:

    lo broda be .abu bei by -> lo broda be .abu be by

In the only case which creates ambiguity, which is LE SELBRI, bei becomes `ku be`:

    lo broda be lo brode bei lo brodi -> lo brode be lo brode ku be lo brodi

Optionally, one can instead use `be ke`, a termset (since `nu'i` is now in KE), and then terminate with `ke'e [be'o]`.

    lo broda be lo brode ku be lo brodi = lo broda be ke lo brode lo brodi [ke'e] [be'o]

## CU -> ZOhU
The selma'o CU has been merged into the selma'o ZOhU.

The functions of CU and ZOhU are already very similar, with the only important difference being that `je cu` is by far the most common way (in grammars that no longer use GIhA) to link bridi-tails. In order to completely merge CU with ZOhU, it is necessary to unlearn `je cu` and use `vau je` instead for bridi-tail connecting.

## CU -> BAI
Alternatively, CU can be merged into BAI.

The cmavo `cu` becomes a modal for `ku'ai'i`. This has no significant impact on current usage patterns.
