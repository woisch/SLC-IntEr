\--------------------------------

aus_00
======

tc: if cohort=1

vn:

qt:

hl:

in:

q: Im Folgenden geht es um das Thema Berufsausbildung.

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

tr:

GOTO aus_01 IF h_ausbever=0

GOTO aus_03 IF h_ausbever=1

hi:

\--------------------------------

aus_01
======

tc: if cohort=1 AND h_ausbever=0

vn: beau_154, sf_beau_154

qt: Einfachauswahl mit vertikalen ao

hl:

in:

q: Haben Sie nach dem Abitur/der Fachhochschulreife eine berufliche Ausbildung
aufgenommen?

is: Falls Sie mehr als eine berufliche Ausbildung aufgenommen haben, beziehen
Sie Ihre Angaben bitte auf die letzte Ausbildung.

it:

ao1:1: ja, eine betriebliche Ausbildung/Lehre

ao2:2: ja, eine Beamtenausbildung für den mittleren Dienst

ao3:3: ja, eine Ausbildung im Rahmen eines dualen Studiums (nicht
Praktikum/Praxisphase)

ao4:4: ja, an einer Berufsfachschule/einer Schule des Gesundheitswesens

ao5:5: ja, an einer Fachakademie

ao6:6: nein, aber ich werde demnächst eine Ausbildung aufnehmen

ao7:7: nein, weder angefangen noch beabsichtigt

mv:

ka:

vc:

av:

kh:

fv: sf_beau_154: Die Beantwortung dieser Frage ist für den weiteren Verlauf des
Fragebogens wichtig. Ich möchte diese Frage dennoch nicht beantworten.

hv:

fo:

tr:

GOTO [NEXT MODUL] IF beau_154=MISSING AND sf_beau_154=1

GOTO aus_02 IF beau_154=1 OR beau_154=2 OR beau_154=3 OR beau_154=4 OR
beau_154=5

GOTO [NEXT MODUL] IF beau_154=6 OR beau_154=7

hi:

\--------------------------------

aus_02
======

tc: if cohort=1 AND h_ausbever=0

vn: ausabs_154/

qt: Einfachauswahl mit vertikalen ao und zwei offenen Fragen

hl:

in:

q: Haben Sie diese Berufsausbildung bereits abgeschlossen?

is:

it:

ao1:1: ja

ao2:2: nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO aus_03

hi:

\--------------------------------

aus_03
======

tc: if cohort=1 AND h_ausbever=0

vn: notepruef_154/ noteschul_154

qt: zwei offenen Fragen

hl:

in:

q: Bitte geben Sie uns die Abschlussnoten dieser Ausbildung an.

is:

it:

Abschlussnote:

ao1:1: Präfix: Prüfungszeugnis: [number],[number] (notepruef_154)

ao2:2: Präfix: Schulzeugnis: [number],[number] (noteschul_154)

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO aus_04

hi:

\--------------------------------

aus_04
======

=========

tc: if cohort=1

vn: auzufint_154/ auzuffaeh_154/ auzufkont_154/ auzufausb_154/ auzuflehr_154/
auzufprax_154/ auzufcha_154/ auzufauf_154/ auzufinsg_154

qt: Einfachauswahlmatrix, horizontale ao

hl:

in: [visible IF ausbever=1] Sie haben angegeben, dass Sie seit Januar 2018 in
einer beruflichen Ausbildung waren oder aktuell noch sind. Falls Sie nach dem
Erwerb der Hochschulreife mehr als eine berufliche Ausbildung aufgenommen haben,
beziehen Sie Ihre Angaben bitte auf die letzte Ausbildung.

q: Wie zufrieden sind bzw. waren Sie mit Ihrer Ausbildung hinsichtlich...

is:

st:

it1: (auzufint_154) der Übereinstimmung mit Ihren Interessen?

It2: (auzuffaeh_154 ) der Übereinstimmung mit Ihren Fähigkeiten?

It3: (auzufkont_154) des Kontaktes zu anderen Auszubildenden?

It4: (auzufausb_154) der Ausbilder/innen (im Betrieb)?

It5: (auzuflehr_154) der Lehrer/innen (in der Schule)?

It6: (auzufprax_154) der Vorbereitung auf die Berufspraxis?

It7: (auzufcha_154) der Arbeitsmarktchancen?

It8: (auzufauf_154 )der beruflichen Aufstiegsmöglichkeiten?

It9: (auzufinsg_154 )der Ausbildung insgesamt?

Ao1:1: sehr zufrieden

Ao2:2

Ao3:3

Ao4:4

Ao5:5: sehr unzufrieden

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO aus_05

hi:

\--------------------------------

aus_05
======

tc: if cohort=1

vn: wquaauf_154/ wquaausb_154 / wquason_154/ wquasona_154

qt: Einfachauswahl mit vertikalen ao und einer offene Angabe

hl:

in:

q: Planen Sie in Zukunft folgende Qualifizierungen?

is:

it1: Aufstiegsfortbildung (z. B. Techniker(in), Fachwirt(in), Meister(in))

it2: weitere Berufsausbildung

it3: sonstige Zusatzqualifikation, und zwar: [string] (wquasona_154)

ao1:1: ja

ao2:2: nein

ao3:3: weiß noch nicht

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO [NEXT MODUL]

hi:
