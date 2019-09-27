\--------------------------------

beg_00
======

tc:

vn:

qt:

hl: Bildungs- und Berufswege

in:

q: Zu Beginn unserer Befragung möchten wir etwas über Ihren bisherigen Werdegang
und Ihre Pläne erfahren.

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

tr: GOTO beg_01

hi:

\--------------------------------

beg_01
======

tc:

vn: bbfried

qt: Einfachauswahl mit horizontaler ao

hl: Werdegang

in:

q: Wie zufrieden sind Sie mit Ihrem bisherigen Bildungs- und Berufsweg?

is:

it:

ao1:1 sehr zufrieden

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

tr: GOTO beg_02 IF cohort=1

GOTO beg_03 IF cohort=2

hi:

\--------------------------------

beg_02
======

tc: IF cohort=1

vn: planber_154

qt: offene Frage

hl: Werdegang

in:

q: Welchen Beruf streben Sie langfristig an?

is: Bitte angeben, z. B. Arzt/Ärztin, Kfz-Mechatroniker/in

it:

ao: offene Frage mit 60 Zeichen (Breite des Textfeldes=7cm)

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO beg_07 IF cohort=1

hi:

\--------------------------------

beg_03
======

tc: IF cohort=2

vn: wuber_183a

qt: offene Frage

hl: Werdegang

in:

q: Unabhängig von Ihrer aktuellen Situation, welchen Beruf würden Sie später
einmal am liebsten ergreifen?

is:

it:

ao: offene Frage mit 60 Zeichen (Breite des Textfeldes=7cm)

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO beg_04 IF cohort=2

hi:

\--------------------------------

beg_04
======

tc: IF cohort=2

vn: planber_183a

qt: offene Frage

hl: Werdegang

in:

q: Und wenn Sie einmal an alles denken, was Sie jetzt wissen: welchen Beruf
werden Sie wohl tatsächlich einmal ergreifen?

is:

it:

ao: offene Frage mit 60 Zeichen

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO beg_08 IF cohort=2

hi:

\--------------------------------

beg_07
======

tc: IF cohort=1

vn: z4 (z4wunsch_154 / z4komp_154 / z4pers_154 / z4gutverd_154 / z4aufst_154 /
z4prest_154 / z4allg_154 / z4selbst_154 / z4ueber_154 / z4freiz_154 /
z4leitp_154 / z4leist_154 / z4sicher_154 / z4famil_154 / z4karri_154 /
z4vereinb_154)

qt: Einfachauswahlmatrix mit horizontalen ao

hl: Werdegang

in:

q: Wie stark verfolgen Sie die nachstehenden Berufs- und Lebensziele?

is:

it1:… meinen lang gehegten Berufswunsch zu verwirklichen.

it2:... fundierte, ausbaufähige berufliche Kompetenzen zu erwerben.

it3:... meine Persönlichkeit zu entfalten.

it4:... ein möglichst hohes Einkommen zu erzielen.

it5:... Chancen für den beruflichen Aufstieg zu bekommen.

it6:...ein hohes Ansehen und berufliches Prestige zu erwerben.

it7:... mir eine möglichst umfassende Allgemeinbildung anzueignen.

it8:... selbstverantwortliche Tätigkeiten ausüben zu können.

it9:... in beruflicher Hinsicht Überdurchschnittliches zu leisten.

it10:... das Leben zu genießen und genügend Freizeit zu haben.

it11:... eine leitende Funktion einzunehmen.

it12:... mein Leistungsvermögen voll auszuschöpfen.

it13:... einen sicheren Arbeitsplatz zu haben.

it14:... mich intensiv um Familie bzw. Partnerschaft zu kümmern.

it15:... auf alle Fälle Karriere zu machen.

it16:… Familie und Beruf vereinbaren zu können.

st: Mir geht es darum,…

ao1:1 sehr stark

ao2:2

ao3:3

ao4:4

ao5:5: überhaupt nicht

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO beg_08 IF cohort=1

hi:

\--------------------------------

beg_08
======

tc: IF cohort=1

vn: ch (chakaall_154 / chbacall_154 / chmasall_154 / chaduall_154 / chabaall_154
/ chselbst_154)

qt: Einfachauswahlmatrix mit horizontalen ao

hl: Werdegang

in:

q: Wie schätzen Sie…

is: Bitte jeweils den zutreffenden Skalenwert ankreuzen.

it1: … allgemein die Berufsaussichten für Absolventen eines Studiums ein?

it2: … allgemein die Berufsaussichten für Absolventen eines Bachelorstudiums
ein?

it3: … allgemein die Berufsaussichten für Absolventen eines Masterstudiums ein?

it4: … allgemein die Berufsaussichten für Absolventen eines dualen Studiums ein?

it5: … allgemein die Berufsaussichten für Absolventen eines beruflichen
Ausbildungsweges ohne Studium ein?

it6: … Ihre persönlichen Berufsaussichten ein?

st:

ao1:1 sehr gut

ao2:2

ao3:3

ao4:4

ao5:5: sehr schlecht

ao6:6: weiß nicht

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO beg_10 IF cohort=1

hi:

\--------------------------------

beg_09
======

tc: IF cohort=2

vn: ch (chakaall_183a / chabaall_183a / chselbst_183a)

qt: Einfachauswahlmatrix mit horizontalen ao

hl: Werdegang

in:

q: Wie schätzen Sie…

is: Bitte jeweils den zutreffenden Skalenwert ankreuzen.

it1: … allgemein die Berufsaussichten für Absolventen eines Studiums ein?

it2: … allgemein die Berufsaussichten für Absolventen eines beruflichen
Ausbildungsweges ohne Studium ein?

it3: … Ihre persönlichen Berufsaussichten ein?

st:

ao1:1 sehr gut

ao2:2

ao3:3

ao4:4

ao5:5: sehr schlecht

ao6:6: weiß nicht

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO beg_13 IF cohort=2

hi:

\--------------------------------

beg_10
======

tc: IF cohort=1

vn: ziwichmu_154 / ziwichva_154

qt: Einfachauswahlmatrix mit horizontalen ao

hl: Werdegang

in:

q: Wie wichtig ist es Ihnen, später einen ähnlich guten oder besseren Beruf zu
haben…

is: Bitte jeweils den zutreffenden Skalenwert ankreuzen.

it1: … als Ihre Mutter?

it2: … als Ihr Vater?

st:

ao1:1 sehr wichtig

ao2:2

ao3:3

ao4:4

ao5:5: sehr unwichtig

ao6:6: hat noch nie einen Beruf gehabt

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO beg_11 IF cohort=1

hi:

\--------------------------------

beg_11
======

tc: IF cohort=1

vn1: mu (gutbaumu_154 / gutbbamu_154 / gutbmamu_154 / gutbstmu_154)

vn2: va (gutbauva_154 / gutbbava_154 / gutbmava_154 / gutbstva_154)

qt: Einfachauswahlmatrix mit horizontalen ao

hl: Werdegang

in:

q: Wie gut sind die Aussichten auf einen ähnlich guten Beruf wie…

is: Bitte jeweils den zutreffenden Skalenwert ankreuzen.

it1: mit einem beruflichen Ausbildungsabschluss

it2: mit einem Bachelorabschluss

it3: mit einem Masterabschluss

it4: mit einem Staatsexamen

st1 (mu): … Ihre Mutter?

st2 (va): … Ihr Vater?

ao1:1 sehr gut

ao2:2

ao3:3

ao4:4

ao5:5: sehr schlecht

ao6:6: hat noch nie einen Beruf gehabt

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo: ao6 absetzen

tr: GOTO beg_12 IF cohort=1

hi:

\--------------------------------

beg_12
======

tc: IF cohort=1

vn1: umf4fam (umf4fam01_154 / umf4fam02_154 / umf4fam03_154 / umf4fam04_154 /
umf4fam05_154 / umf4fam06_154 / umf4fam07_154 / umf4fam08_154 / umf4fam09_154 /
umf4fam10_154 / umf4fam11_154 / umf4fam12_154 / umf4fam13_154 / umf4fam14_154 /
umf4fam15_154)

vn2: umf4frd (umf4frd01_154 / umf4frd02_154 / umf4frd03_154 / umf4frd04_154 /
umf4frd05_154 / umf4frd06_154 / umf4frd07_154 / umf4frd08_154 / umf4frd09_154 /
umf4frd10_154 / umf4frd11_154 / umf4frd12_154 / umf4frd13_154 / umf4frd14_154 /
umf4frd15_154)

vn3: um4bek (umf4bek01_154 / umf4bek02_154 / umf4bek03_154 / umf4bek04_154 /
umf4bek05_154 / umf4bek06_154 / umf4bek07_154 / umf4bek08_154 / umf4bek09_154 /
umf4bek10_154 / umf4bek11_154 / umf4bek12_154 / umf4bek13_154 / umf4bek14_154 /
umf4bek15_154)

vn4: um4nmd (umf4nmd01_154 / umf4nmd02_154 / umf4nmd03_154 / umf4nmd04_154 /
umf4nmd05_154 / umf4nmd06_154 / umf4nmd07_154 / umf4nmd08_154 / umf4nmd09_154 /
umf4nmd10_154 / umf4nmd11_154 / umf4nmd12_154 / umf4nmd13_154 / umf4nmd14_154 /
umf4nmd15_154)

qt: Einfachauswahlmatrix mit horizontalen ao

hl: Werdegang

in:

q: Kennen Sie jemanden in Ihrem Familien-, Freundes- oder Bekanntenkreis, …

is: Bitte alles Zutreffende ankreuzen.

it1: der Ihnen bei einem Umzug helfen würde?

it2: der eine Fremdsprache fließend sprechen und schreiben kann?

it3: der Ihnen 1.000 Euro leihen würde?

it4: der für Sie da ist, nur um über den Tag zu reden?

it5: der Ihnen beim Ausfüllen von amtlichen Anträgen (z. B. BAföG,
Steuererklärung) hilft?

it6: der Ihnen einen Job/ein Praktikum vermitteln kann?

it7: der Ihnen Rat geben kann, wenn es Probleme gibt?

it8: der aktiv in einer politischen Partei mitarbeitet?

it9: der monatlich mehr als 3.000 Euro netto verdient?

it10: der wissenschaftliche Fachzeitschriften liest?

it11: der länger als 6 Monate arbeitslos war oder ist?

it12: der studien-, ausbildungsbezogen oder beruflich länger als 3 Monate im
Ausland war?

it13: der Ihnen eine gute Referenz bieten kann (z. B. für Job, Stipendium,
Praktikum)?

it14: der sich gut mit Literatur auskennt?

it15: der Ihnen bei Reparaturen im Haushalt behilflich sein würde?

st:

ao1 (fam): Familie

ao2 (frd): Freunde

ao3 (bek): Bekannte

ao4 (nmd): niemand

mv:

ka:

vc:

av:

kh:

fv:

hv:

fo:

tr: GOTO beg_13 IF cohort=1

hi:

\--------------------------------

beg_13
======

tc:

vn: simgeh3

qt: Einfachauswahl mit vertikalen ao

hl: Werdegang

in:

q: Stellen Sie sich vor, Ihnen werden drei verschiedene Jobs mit
unterschiedlichem Anfangsgehalt angeboten, welchen würden Sie wählen?

is:

it:

st:

ao1:1 den Job mit durchschnittlichem Gehalt von Beginn an

ao2:2 den Job mit geringem Gehalt in den ersten beiden Jahren und anschließend
hohem Gehalt

ao3:3 den Job mit geringem Gehalt in den ersten vier Jahren und anschließend
sehr hohem Gehalt

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
