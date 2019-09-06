msg_00
======

tc: IF cohort=1 OR 2

vn:

qt:

hl:

in:

q: Fragen zur Person

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

tr: GOTO msg_01

hi:

\--------------------------

msg_01
======

tc: IF cohort=1 OR 2

vn: finanz,

qt: Einfachauswahl, horizontale ao

hl:

in:

q: Wie kommen Sie mit dem Geld aus, das Sie durchschnittlich im Monat zur
Verfügung haben?

is:

st:

it:

ao1:1:sehr gut

ao2:2

ao3:3

ao4:4

ao5:5: sehr schlecht

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr:

>   GOTO msg_02 IF cohort=1

>   GOTO msg_03 IF cohort=2

hi:

\--------------------------

msg_02
======

tc: IF cohort=1

vn: ausbmob01_154, ausbmob02_154, ausbmob03_154, ausbmob04_154, ausbmob05_154,
ausbmob06_154, ausbmob07_154,

qt: Einfachauswahlmatrix mit horizontalen ao

hl:

in:

q: Inwieweit treffen die folgenden Aussagen auf Sie persönlich zu?

is:

st:

it1: Ich kann mir gut vorstellen, im Verlauf meines Lebens an ganz
unterschiedlichen Orten zu leben.

it2: Es gibt kaum Orte in Deutschland, an denen ich nicht bereit wäre zu leben
und zu arbeiten.

It3: Für einen besseren Arbeitsplatz würde ich an einen anderen Ort ziehen.

it4: Ich kann mir gut vorstellen, für eine begrenzte Zeit im Ausland zu
arbeiten.

it5: Die Vorstellung beruflich bedingt umziehen zu müssen, ist mir ein Gräuel.

it6: Eine Tätigkeit im Ausland auf unbestimmte Zeit kommt für mich nicht in
Betracht.

it7: Es würde mir schwer fallen, wegen eines Arbeitsplatzes meine Heimat zu
verlassen.

ao1:1 trifft voll und ganz zu

ao2:2

ao3:3

ao4:4

ao5:5: trifft überhaupt nicht zu

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO msg_03

hi:

\--------------------------

msg_03
======

tc: IF cohort=1 OR 2

vn: wohnelt, auszmon, auszjahr,

qt: Einfachauswahl, vertikale ao mit 2 x Offene Abfrage

hl:

in:

q: Leben Sie im Haushalt Ihrer Eltern?

is:

st:

it:

ao1:1: ja

ao2:2: nein, seit [number] (Monat) / [number] (Jahr) nicht mehr (ausz4mon,
ausz4jahr)

mv:

ka:

vc:

av1: [number] (auszmon): 2-stellig: 1 TO 12

av2: [number] (auszjahr): 4-stellig: 1950 TO 2020

kh1: Bitte geben Sie den Monat zweistellig (zwischen 1 und 12) an.

kh2: Bitte geben Sie eine vierstellige Jahreszahl an.

fv:

hv:

fo:

tr: GOTO msg_04

hi: Die Datumseingabe möglichst folgendermaßen darstellen: \_\_ / \___\_
(Monat/Jahr)

\--------------------------

msg_04
======

tc: IF cohort=1 OR 2

vn: plz, wohnort

qt: 2 Offene Abfragen

hl:

in:

q1: Bitte geben Sie die Postleitzahl Ihres Wohnortes an.

is:

st:

it:

ao1: Postleitzahl: [number]

ao2: Ich wohne nicht in Deutschland, sondern in: [string]

mv:

ka:

vc:

av: [number], 5-stellig

kh: Bitte geben Sie eine 5-stellige Postleitzahl an.

fv:

hv:

fo:

tr:

>   GOTO msg_05 IF cohort=2

>   GOTO msg_06 IF cohort=1

hi:

\--------------------------

msg_05
======

tc: IF cohort=2

vn: geschl_183a

qt: Einfachauswahl, vertikale ao

hl:

in:

q: Welches Geschlecht haben Sie?

is:

st:

it:

ao1:1: männlich

ao2:2: weiblich

ao3:3: divers

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO msg_12 IF cohort=2

hi:

\--------------------------

msg_06
======

tc: IF cohort=1

vn: landeltvat_154, landeltmut_154, eltvat1_154, eltvat2_154, eltvat3_154,
eltmut1_154, eltmut2_154, eltmut3_154

qt: 2x Einfachauswahl vertikale ao mit je 3 offenen Angaben

hl:

in:

q: Ist eines Ihrer Großelternteile väterlicherseits bzw. mütterlicherseits im
Ausland geboren?

is: Bitte beziehen Sie Ihre Angaben auf die heutigen Staatsgrenzen.

st:

it:

ao1:1: beide Großeltern im Ausland geboren, und zwar in: [string]/ [string]
(eltvat1_154, eltvat2_154)

ao2:2: ein Großelternteil im Ausland geboren, und zwar in: [string]
(eltvat2_154)

ao3:3: kein Großelternteil im Ausland geboren

ao4:4: Ist mir nicht bekannt

ao5:1: beide Großeltern im Ausland geboren, und zwar in: [string]/ [string]
(eltmut1_154, eltmut2_154)

ao6:2: ein Großelternteil im Ausland geboren, und zwar in: [string]
(eltmut3_154)

ao7:3: kein Großelternteil im Ausland geboren

ao8:4: Ist mir nicht bekannt

mv:

ka1: ka1 (ao1 TO ao4) väterlicherseits

ka2: ka2 (ao5 TO ao8) mütterlicherseits

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO msg_07

hi: Umsetzung siehe Studienberechtigte 18.2 (block712)

\--------------------------

msg_07
======

tc: IF cohort=1

vn: studgev_154, studgem_154

qt: 2x Einfachauswahl vertikale ao

hl:

in:

q: Haben Ihre Großeltern ein Studium abgeschlossen?

is:

st:

it1:

ao1:1: Mindestens ein Großelternteil hat ein Hochschulstudium abgeschlossen

ao2:2: Beide Großelternteile haben *kein* Hochschulstudium abgeschlossen

ao3:3: Ist mir nicht bekannt

ao4:1: Mindestens ein Großelternteil hat ein Hochschulstudium abgeschlossen

ao5:2: Beide Großelternteile haben *kein* Hochschulstudium abgeschlossen

ao6:3: Ist mir nicht bekannt

mv:

ka1: aus der Familie des Vaters (studgev_154) ka1 (ao1 TO ao3)

ka2: aus der Familie der Mutter (studgem_154) ka1 (ao4 TO ao6)

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO msg_08

hi: Umsetzung siehe Studienberechtigte 18.2 (block711)

Umsetzung ka1 und ka2 in zwei Fragen (?)

\--------------------------

msg_08
======

tc: IF cohort=1

vn: bezstand_154, sf_bezstand_154

qt: Einfachauswahl, vertikale ao

hl:

in:

q: Sind Sie in einer festen Partnerschaft?

is:

st:

it:

ao1:1: Ja, in fester Partnerschaft

ao2:2: Ja, verheiratet oder in eingetragener Lebenspartnerschaft

ao3:3: Nein, ich bin ohne feste(n) Partner(in)

mv:

ka:

vc:

av:

kh:

fv: sf\_ bezstand_154: Ihre bisherigen Angaben sind ohne die Beantwortung dieser
Frage leider weniger nützlich für uns. Ich möchte diese Frage dennoch nicht
beantworten.

hv:

fo:

tr:

>   GOTO msg_09 IF bezstand_154=MISSING AND sf_bezstand_154=1

>   GOTO msg_09 IF bezstand_154=1 OR bezstand_154=2

>   GOTO msg_10 IF bezstand_154=3

>   GOTO msg_08 IF bezstand_154=MISSING

hi:

\--------------------------

msg_09
======

tc: IF cohort=1

vn: famhsh_154

qt: Einfachauswahl, vertikale ao

hl:

in:

q: Leben Sie mit Ihrem/Ihrer Parter(in) in einem gemeinsamen Haushalt?

is:

st:

it:

ao1:1: Ja, wir haben einen gemeinsamen Haushalt

ao2:2: Ja, aber neben dem gemeinsamen Haushalt führen ich bzw. mein(e)
Partner(in) einen zweiten Haushalt (z. B. wegen Erwerbstätigkeit in anderer
Stadt)

ao3:3: nein

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO msg_10

hi:

\--------------------------

msg_10
======

tc: IF cohort=1

vn: kinder_154, kinderanz_154

qt: Einfachauswahl, vertikale ao mit offener Antwortoption

hl:

in:

q: Haben Sie Kinder?

is:

st:

it:

ao1:1: ja , und zwar [number] Kinder (kinderanz_154)

ao2:2:nein

mv:

ka:

vc:

av: soft Rangecheck 0 TO 9, siehe Datumscheck SLC-Pretest

kh: Bitte überprüfen Sie Ihre Eingabe. Sie haben einen Wert kleiner 0 oder
größer 9 eingegeben. Wenn Ihre Angabe korrekt ist können Sie diesen Hinweis
ignorieren.

fv:

hv:

fo:

tr:

>   GOTO msg_11 IF kinder_154=1

>   GOTO msg_11 IF kinder_154=MISSING AND kinderanz_154\<\>MISSING

>   GOTO msg_12 IF kinder_154=2 OR kinderanz_154==MISSING

hi: Die Angabe der Kinderanzahl darf nicht in Kombination mit „nein“ möglich
sein!

Aus dem SLC QML adaptierter Vorschlag:

\--------------------------

msg_11
======

tc: IF cohort=1

vn: kind1mon, kind1ja, kind1wo, kind2mon, kind2ja, kind2wo

qt1: offene Angabe (kind1mon, kind1ja, kind2mon, kind2ja)

qt2: Einfachauswahl mit horizontalen ao (kind1wo, kind2wo)

hl:

in:

q1: Wann wurde dieses Kind geboren?

q2: Wann wurden diese Kinder geboren?

q3: Wann wurde(n) diese(s) Kind(er) geboren?

is: Geben Sie bitte sowohl eigene Kinder (leibliche Kinder oder Adoptivkinder)
an als auch Kinder Ihres Partners/Ihrer Partnerin, die in Ihrem Haushalt leben.
[VISIBLE IF kinderanz_154\>2 OR kinderanz_154=MISSING] Wenn Sie mehr als zwei
Kinder haben, machen Sie bitte Angaben zu Ihrem ältesten und jüngsten Kind.

it:

ao1:1: 1. Kind [number] (Monat) / [number] (Jahr)

q4: Lebt dieses Kind in Ihrem Haushalt?

ao2:2: ja

ao3:3: nein

ao4:4: 2. Kind [number] (Monat) / [number] (Jahr)

q5: Lebt dieses Kind in Ihrem Haushalt?

ao5:5: ja

ao6:6: nein

mv:

ka1: ka1 (ao1 TO ao3) 1. Kind

ka2: ka2 (ao4 TO ao6) 2. Kind

vc: SHOW q1 IF kinderanz_154==1

SHOW q2 IF kinderanz_154\>1

SHOW q3 IF kinderanz_154==MISSING

SHOW ao4 q5 ao5 ao6 IF kinderanz_154\>1 OR kinderanz_154==MISSING

av:

av1: [number] (kind1mon): 2-stellig: 1 TO 12

av2: [number] (kind1ja): 4-stellig: 1950 TO 2020

av3: [number] (kind2mon): 2-stellig: 1 TO 12

av4: [number] (kind2ja): 4-stellig: 1950 TO 2020

kh1: Bitte geben Sie den Monat zweistellig (zwischen 1 und 12) an.

kh2: Bitte geben Sie eine vierstellige Jahreszahl an.

kh3: Bitte geben Sie den Monat zweistellig (zwischen 1 und 12) an.

kh4: Bitte geben Sie eine vierstellige Jahreszahl an.

fv:

hv:

fo:

tr: GOTO msg_12

hi: mehrere Fragen und Fragetypen gleichzeitig auf einer Seite (je 2 mal, für
erstes und zweites Kind, eine offene Abfrage, wann Kind geboren und
Einfachauswahl, ob im eigenen Haushalt wohnhaft ja/nein

\--------------------------

msg_12
======

tc:

vn: zuf4leben

qt: Einfachauswahl, horizontale ao

hl:

in:

q: Wie zufrieden sind Sie gegenwärtig alles in allem mit Ihrem Leben?

is:

st:

it:

ao1:1: sehr zufrieden

ao2:2

ao3:3

ao4:4

ao5:5: sehr unzufrieden

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO Endpage

hi:

\--------------------------

end
===

tc:

vn:

qt:

hl:

in:

q:

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

hi:
