gsh_00
======

tc: if cohort=2

vn:

qt:

hl:

in:

q: Hallo Teilnehmer\*innen

is:

it:

ao:

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO gsh_01

hi:

\------------------------------------------------------------

gsh_01
======

tc: if cohort=2

vn: gesund_183a, sf\_ gesund_183a

qt: Einfachauswahl, horizontale ao

hl:

in:

q: Wie würden Sie Ihren Gesundheitszustand im Allgemeinen beschreiben?

is:

it:

ao1:1: sehr gut

ao2:2: gut

ao3:3: mittelmäßig

ao4:4: schlecht

ao5:5: sehr schlecht

mv:

ka:

vc:

av:

kh:

fv: sf\_ gesund_183a: Ihre bisherigen Angaben sind ohne die Beantwortung dieser
Frage leider weniger nützlich für uns. Ich möchte diese Frage dennoch nicht
beantworten.

hv:

fo:

tr:

GOTO gsh_02 if gesund_183a=MISSING AND sf\_ gesund_183a=1

GOTO gsh_02 if gesund_183a !=MISSING

GOTO gsh_01 if gesund_183a=MISSING

hi:

\------------------------------------------------------------

gsh_02
======

tc: if cohort=2

vn: pss01_183a, pss02_183a, pss03_183a, pss04_183a, pss05_183a, pss06_183a,
pss07_183a, pss08_183a, pss09_183a, pss10_183a, sf\_ pss01_183a

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in: Die folgenden Fragen beschäftigen sich damit, wie häufig Sie sich während
des letzten Monats durch Stress belastet fühlten.

q: Wie oft hatten/haben Sie (sich) im letzten Monat ...

is:

It1: ... darüber aufgeregt, dass etwas völlig Unerwartetes eingetreten ist?

It2: ... das Gefühl, wichtige Dinge in Ihrem Leben nicht beeinflussen zu können?

It3: ... nervös und „gestresst“ gefühlt?

It4: ... sicher im Umgang mit persönlichen Aufgaben und Problemen gefühlt?

It5: ... das Gefühl, dass sich die Dinge nach Ihren Vorstellungen entwickeln?

It6: ... das Gefühl, mit all den anstehenden Aufgaben und Problemen nicht
richtig umgehen zu können?

It7: ... das Gefühl, mit Ärger in Ihrem Leben klar zu kommen?

It8: ... das Gefühl, alles im Griff zu haben?

It9: ... darüber geärgert, wichtige Dinge nicht beeinflussen zu können?

it10: ... das Gefühl, dass sich die Probleme so aufgestaut haben, dass Sie diese
nicht mehr bewältigen können?

ao1:1: sehr oft

ao2:2

ao3:3

ao4:4

ao5:5: nie

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

GOTO gsh_03

hi:

\------------------------------------------------------------

gsh_03
======

tc: if cohort=2

vn: kgsndtag_183a

qt: Offene Abfrage

hl:

in:

q: Bitte denken Sie an Ihre körperliche Gesundheit – dazu zählen körperliche
Krankheiten und Verletzungen. An wie vielen Tagen der letzten vier Wochen ging
es Ihnen körperlich nicht gut?

is:

it:

ao: Tage: [number]

mv:

ka:

vc:

av: [number]: 2-stellig: 0 TO 28

kh: Bitte tragen Sie eine Zahl zwischen 0 und 28 ein.

fv:

hv:

fo:

tr:

GOTO gsh_04

hi:

\------------------------------------------------------------

gsh_04
======

tc: if cohort=2

vn: sgsndtag_183a, sf\_ sgsndtag_183a

qt: Offene Abfrage

hl:

in:

q: Bitte denken Sie an Ihr seelisches Befinden – dazu zählen auch Stress,
Depressionen oder Ihre Stimmung ganz allgemein. An wie vielen Tagen der letzten
vier Wochen ging es Ihnen seelisch nicht gut?

is:

it:

ao: Tage: [number]

mv:

ka:

vc:

av: [number]: 2-stellig: 0 TO 28

kh: Bitte tragen Sie eine Zahl zwischen 0 und 28 ein.

fv:

hv:

fo:

tr:

GOTO gsh_05

hi:

\------------------------------------------------------------

gsh_05
======

tc: if cohort=2

vn: gsndtag_183a, sf\_ gsndtag_183a

qt: Offene Abfrage

hl:

in:

q: An wie vielen Tagen der letzten vier Wochen waren Sie durch Ihre körperliche
Gesundheit oder Ihr seelisches Befinden in der Ausübung alltäglicher Aktivitäten
– wie Berufstätigkeit, Ausbildung, Studium, Versorgung, Erholung oder Pflege
sozialer Kontakte – beeinträchtigt?

is:

it:

ao: Tage: [number]

mv:

ka:

vc:

av: [number], 2-stellig: 0 TO 28

kh:

fv: sf\_ gsndtag_183a: Ihre bisherigen Angaben sind ohne die Beantwortung dieser
Frage leider weniger nützlich für uns. Ich möchte diese Frage dennoch nicht
beantworten.

hv:

fo:

tr: GOTO [NEXT MODUL] IF gsndtag_183a!=MISSING

GOTO [NEXT MODUL] IF gsndtag_183a==MISSING & sf\_ gsndtag_183a==1

GOTO gsh_05 IF gsndtag_183a==MISSING

hi:
