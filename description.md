De 3DMiB-challenge

Binnen FyE werken we aan verschillende uitdagingen binnen de energietransitie. Veel van deze activiteiten zijn gebaat bij de in- en uitvoer van allerlei datastromen. Om deze reden hebben we een datalake voor de woonwijk, dat is een verzameling databronnen die in hun eigen, ruwe vorm bewaard worden zonder vooraf dichtgetimmerd databasemodel. Je legt pas betekenis en samenhang op het moment dat je een vraag stelt.

Momenteel omvat het datalake o.a. de volgende bronnen:

- Net: capaciteitskaart (afname=tekort in Elsweide) + Netbewust-laden  trafo-headroom.

- Eigendom: BRK kadastrale percelen (honderden percelen per buurt maken versnippering inspecteerbaar).

- Draagvlak/sociaal: Leefbarometer, energiearmoede (CBS), gezondheid (RIVM).

- Vergunning/ruimte: de bestemmingsplannen (Arnhem-zoning, incl. het nog-niet-formele appartementenplan).

- Klimaat-risico & leefomgeving: Klimaateffectatlas (overstroming + bodemdaling) —  deze categorie kan óók de biodiversiteit/leefomgeving-impact dragen (groen, hittestress),  het FyE-cross-cutting-concern dat anders buiten beeld blijft.

- Economisch: de research-agenda + businesscase-brief als economisch  obstakel

 

De 3DMiB-challenge is gericht op de betekenislaag (wat betekent de data?) en de toegangslaag (hoe stel je er een vraag aan?) voor dit datalake.

We gaan in 3 projecten de data nuttig maken:

P1. Structureren: de buurt-energie elementen en de obstakels in kaart brengen:

A. Domeinontologie (de datalake semantisch maken, wat er is): Welke begrippen beschrijft de datasnapshot, hoe hangen ze samen, en welke databron vult welk begrip? (Bv. Gebouw ← 3D-BAG + energielabel; Net-aansluiting ← capaciteitskaart + Liander; Huishouden ← CBS;  Energiestroom ← load-curve.)

B. Obstakel-laag (de bril erbovenop, wat is er mis): obstakels zijn ongewenste toestanden en relaties over die begrippen

Onderzoeksvragen:

1. Welke begrippen leven in de buurt op het gebied van energie (gebouw, net-asset, huishouden, energiestroom, eigendom, …), en welke FyE-databron vult elk begrip?   (= laag A.)

2. Welke obstakels staan realisatie van een PED in de weg? Breng ze onder in heldere categorieën (net/techniek · eigendom & organisatie · draagvlak & sociaal · vergunning & ruimte · economisch/businesscase · klimaat-risico & leefomgeving). (= laag B.)

3. Hoe hangen begrippen en obstakels samen (een vol net verzwaart de businesscase; versnipperd eigendom blokkeert collectieve oplossingen)? En waar is er júist géén data — een blinde vlek (een begrip/obstakel zónder bron eraan) is óók een bevinding?

 

Quick-win (week 1): laat een LLM een eerste begrippen- + obstakel-schets voor Elsweide voorstellen, snoei die tegen drie concrete data-ankers, en teken er een één-pagina concept-map van. Let op: dit week-1-resultaat is een begrippen-/concept-map, nog géén ontologie — het wordt er pas een zodra je in de weken erna de relaties en de laag-A/laag-B-scheiding expliciet maakt en verdedigt (dáár zit het cijferwaardige werk;een LLM levert losse begrippen makkelijk, de samenhang niet).

P2. Toegankelijk maken: de data eronder bevraagbaar maken (een agent-ready ingang). onderzoek of je het datalake bevraagbaar kunt maken in gewone taal zodat iemand uit een ander werkpakket (of een bewoner, of een beleidsmaker) kan vragen hoeveel ruimte heeft het net in Elsweide nog?  én, minstens zo belangrijk, karakteriseer wáár dat werkt en wáár het breekt. Een NotebookLM-/LLM-wiki-achtige ingang op FyE-data, kritisch getoetst.

Onderzoeksvragen:

1. Kun je een no-code AI-assistent bouwen die buurt-vragen beantwoordt en bij elk antwoord een bron probeert te tonen? Hoe zit het met de licenties van de data t.o.v. de tools die je gebruikt?

2. Waar klopt het antwoord, en waar produceert de tool een *citatie-gedecoreerd fout antwoord* — en waarom (getalsvragen? ontbrekende data? bronnen die elkaar tegenspreken)? Scoor juistheid van het getal los van de aanwezigheid van een citatie.

3. Hoe ziet een stakeholder-specifieke ingang eruit (een bewoner vraagt iets anders dan een netbeheerder)?

Quick-win (week 1): laad 3–5 snapshot-documenten in NotebookLM, stel 5 realistische stakeholder-vragen, en scoor per antwoord: klopt het getal? / is er een bron? / hallucineert het? (de eerste twee apart!) → een eerste evaluatie-tabel. Die tabel is meteen het meetinstrument voor de rest van het project.

 

P3. Verkennen: hoe obstakels uit gedrag ontstaan (een simulatie / simulacra). een lichte simulatie met AI-persona's ("simulacra") die hypotheses genereert over hoe bewoners op interventies zouden kunnen reageren (dynamisch tarief,

netbewust laden, zonnepanelen, een buurtbatterij) — en welke gedrags-obstakels dat zou kunnen opleveren (free-riding, split-incentive, lage deelname). Een serious-game-/scenario-bril, expliciet als denkgereedschap.

Onderzoeksvragen:

1. Bouw een set bewoners-persona's geseed op de buurt-realiteit (woningvoorraad, energielabels, energiearmoede-aandeel, dag-load-curve) en laat ze — AI-gedreven — kwalitatief reageren op één of meer interventies.

2. Welke gedrags-obstakels komen naar voren als hypothesen (wie zou afhaken, en waarom)? Hoe verschuift het beeld onder verschillende beleidskeuzes?

3. Wat zegt dit over draagvlak en ontwerp — welke interventie lijkt niet alleen technisch/financieel, maar ook gedragsmatig haalbaar, en wat moet je dus mét bewoners verifiëren?


Quick-win (week 1): definieer 3 persona's uit de aggregaat-verdelingen (bv. huurder-energiearm / eigenaar-koopwoning / jong-gezin-met-EV) en laat een LLM ze op één interventie (dynamisch tarief) kwalitatief reageren → een eerste lijst hypothetische gedrags-obstakels. Klein, uitlegbaar, en meteen de kern-loop.