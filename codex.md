Vi får forskjellig hjelp som programmerer.

 - egen kunnskap, ferdighet, kompetanse 
 - feilmeldinger når vi skriver
 - kjøretidsfeil når vi ... kjører
 - fra andre som leser koden, par-programmering
 - testing
 - kunstig intelligens

# Feil

## Syntaksfeil

Språkreglene må vanligvis følges.  Noen språk har noe fleksibilitet, mens andre har lite.
Uansett, hvis vi ikke følger språkreglene har vi begått en syntaksfeil.

Syntaksfeil oppdages mens vi koder, hvis verktøyet har innebygd støtte for å følge med.
Hvis ikke, vil vi se syntaksfeilen når vi forsøker å kompilere koden.
En av kompilatorens hovedoppgaver er å sjekke språket. Den går ikke videre hvis den finner
syntaksfeil.

Vårt IDE vil som oftest følge med og markere syntaksfeil.  Veldig enkle editorer kan også
ofte utvides med språkregler som gjør det mulig å markere syntaksfeil.


## Linkefeil

Hvis programmet er bygd korrekt, vil det passere syntakstesten.
Et viktig neste steg, er å linke programmet med andre programressurser, såkalte støttebibliotek.
Har vi brukt funksjonen Math.random(.) er den sannsynligvis å finne i et annet programsystem.
Dette må linkes sammen.
Linkingen kan skje før vi lager den ferdige kjørbare filen ("exefilen")

En statisk linking betyr at eksefilen inneholder både vårt program og kopi av innlinkede program.
Det skaper større exefiler.

En dynamisk linking betyr at eksefilen kun inneholder vårt program, mens innlinkede program forutsettes å være tilgjengelig når kjøring.
Ved kjøring kan vi få linkefeil hvis den ikke finner det som trengs.  Linkefeilen kan oppstå
ved oppstart hvis man har "hard linking", eller underveis hvis man har "slow linking".

## Kjøretidsfeil

Hvis programmet er fritt for syntaksfeil og vi ikke har linkefeil, er det fortsatt problemer som 
kan oppstå.  Det er som oftest at eksterne dataressurser ikke er tilgjengelig når de trengs.


## Logisk feil

Regner feil, gir feil resultat.

## Skjulte feil

Av sikkerhetsmessig art, som at data lekker.


# Automatisk testing

CodeRunner for Moodle kan teste automatisk. Brukt av de fra New Zealand.

# Kunstig intelligens

Det vi i dag (2023) kaller "kunstig intelligens" eller KI eller AI, er program
som er trent opp til å gi gode svar på gode spørsmål.  De er mindre god til å svare på
dårlig formulerte (upresise) spørsmål eller på spørsmål om noe den ikke er trent opp på.

Dagens AI-bølge startet rundt 2008 da man med store mengder datakraft klarte å trene opp
en AI til å kjenne igjen bilder og håndskrift. Disse "AI-ene" brukes i mobiltelefoner og mye annet
der man tolker bilder.

## Syntetisk kode

Rundt 2019 fikk man de første AI-ene som er trent til å lage kode basert på et ønske.
Dette kalles gjerne "syntetisk kode", og er noe man har forsket lenge på. 
Man har i forskningen prøvd forskjellige teknikker. 
Først nå har man med lyktes, ved å bruke AI-er som er trent opp på store mengder kode fra
kodeprosjekt på internettet.


## OpenAI Codex

Codex er utviklet av det amerikanske firmaet OpenAI, som er eid av Microsoft.
Det tar imot et "prompt" og genererer et "svar".

Den ble lansert som en gratis beta-versjon i 2021 og var basert på GPT-3.

For eksempel "// regn ut snittet av de første 10 heltallene" er et prompt.
Svaret blir kode den tror løser problemet.  Vi som kodere, må vurdere om svaret er godt nok.
Koden er skrevet i det språket den tror vi ønsker. 
Det tar noe tilvennlig å lære seg å skrive gode "prompts"; noe man kaller "prompt engineering".
(På samme måte som at man kan lære seg å bli god til å spørre Google, "query engineering").

Brukes av Github Copilot som et verktøy for "auto completion".  Github er også eid av Microsoft.
Mange IDE-er kan kobles til Codex, som Microsoft sitt VS Code og NeoVIM.  

Pris for bruk er gjerne en fast pris per måneder pluss en liten pris per kilo token, der det kan koste
0.03 USD for prompten og det dobbelte for svaret (sies det på Wikipedia).

OpenAI tar ned Codex API den 23. mars 2023.
Codexbrukere anbefales å bruke gpt-3.5-turbo i stedet.

Microsoft innførte Copilot basert på GPT-4 den 17. mars 2023, i sine produkt som Office 365 og Teams.
Den kan også brukes fra Visual Studio og oppfører seg da som en par-programmerer.
Se video her fra 22. mars 2023, en uke etter lanseringen av GPT-4; de kaller den Github Copilot X: 
https://devblogs.microsoft.com/visualstudio/github-copilot-chat-for-visual-studio-2022/
https://github.blog/2023-03-22-github-copilot-x-the-ai-powered-developer-experience/

## språkmodell

Codex er basert på GPT, som betyr Generative Pre-trained Transformer.  GPT kan lage tekster (output) basert på et "prompt", som sier hva man ønsker (input).  Man skriver dette i naturlig språk, altså med vanlige setninger.

GPT en såkalt "Large Language Model" (LLM), som kort sagt, er et dypt nevralt nettverk trent opp
på store mengder data med naturlig språk.

Siden programkode er skrevet i et språk har OpenAI laget en variant av GPT som har
spesialisert seg på programmeringsspråk.


## eierskap til input og output

Codex er trent opp med inputkode fra over 50 millioner kodeprosjekt på Github, 
for det meste Python og Javascript.  De intellektuelle rettighetene til denne inputkoden ligger
selvsagt hos de som står bak kodeprosjektene.  Det har vært uklarhet om eierskapet til
den kode som OpenAI konstruerer (output), siden det er uklart hvem som eier input.
Wikipedia  hevder at i ett tilfelle svarte OpenAI med kode direkte uendret fra et kodeprosjekt.

## risikabel kode

Som ellers, kan man injisere dårlig input ved å plassere dårlig kode i kodeprosjekt på Github og
andre steder der OpenAI henter input til opptrening.  De som har onde hensikter kan injisere kode
i kodeprosjekt, og vente på at OpenAI tar i bruk disse.  Resultatet kan skape sikkerhetsproblem hos de som i sin tur er uheldig og tar i bruk svarene fra OpenAI.


## ansvar ved bruk

Hvis man tar i bruk dårlig kode fra OpenAI, er spørsmålet også om OpenAI stiller seg rettslig
ansvarlig.  Det gjør de neppe.


# Forskjellig bruk av en AI

## lage kode

## sammenligning 

Det er som regel flere måter å lage et program som løser et gitt problem.
Man kan sammenligne kode man selv eller andre har laget, med den AI-en laget.  
Vil en tredjepart kunne si hva som er laget av et menneske og hva som er laget av en maskin?
Dette er relatert til Turing-testen.


## oversetting

Codex kan oversette fra ett språk til et annet, som fra Python til Perl.


## forklaring

Codex kan forklare et program.


