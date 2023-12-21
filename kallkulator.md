# Kalkulator

En kalkulator er en som regner med tall.  
Før datamaskinene var dette folk.
En bank kunne ha mange titalls kalkulatorer (personer) som bare regnet med tall.

Den viktigste kalkulatoren i datamaskinen er sentralenheten, det vi kaller en Central Processing Unit (CPU).

Den kan plusse to tall.

Ganging gjøres vanligvis med Booth's algoritme, navngitt etter Andrew Booth.  Kona Kathleen Booth skrev 
det første assemblyspråket og laget et veldig tidlig nevralt nettverk som vi kjenner fra maskinlæring.
https://en.wikipedia.org/wiki/Booth%27s_multiplication_algorithm



I dette kapitlet skal du lære å sette opp regneuttrykk.

Vi begynner med de vanlige regneartene.

Fra et prompt kan vi skrive regneuttrykk som 2+2, 3-7 og 2.5/4.

Python kjøres interaktivt ved å skrive "python" som starter "python.exe".
>>> 2.5/4

Javascript kjøres interaktivt fra nettleseren sitt utviklervindu, velg Console.
> 2.5/4

PHP kan også kjøres interaktivt med
"php -a"

Dette kalles en REPL, som betyr Read, Evaluate, Print Loop.

## Tall

Fra matematikk er tall tall.
Av og til skiller vi mellom heltall og desimaltall.

I programmering er det vanligvis likens.  
De kalles "integers" og "floating point numbers" eller bare "ints" og "floats".
På norsk: "inter" og "flåuter".
Nynorsk: "inta" og "flåuta".
Mer om forskjellene senere.

## Tallsystem

Når vi programmerer kan vi oppgi tall på flere måter.
Vi skriver tall ved hjelp av tallsiffer.
Sifrene settes sammen på en posisjonsbestemt måte.
De mest signifikante står lengst til venstre.

### Desimalt
Det vanlige (default) er det kjente 10-tallssystemet.
Desi betyr 10, derav desimal, desiliter osv.
Der har vi 10 ulike tallsiffer:  0, 1, 2, 3, 4, 5, 6, 7, 8 og 9.

La oss si at vi har solgt 257 av noe.  Tallet 257 er 2\*100 + 5\*10 + 7\*1.

La oss si at prisen vi fikk per solgte enhet var 32.75.  Tallet 32.75 er 3\*10 + 2\*1 + 7\*0.1 + 5\*0.01.



### Binært

Digitale maskiner jobber med binære tall.
Binær betyr to-sidig.
Vi har 2 ulike tallsiffer:  0 og 1.

Tallet 1011 er 1*8 + 1*2 + 1*1 = 8+2+1 = 11.
Tallet 10.011 er 2+1*(1/4)+1*(1/8).

### Heksadesimalt

Av og til er tall oppgitt heksadesimalt.
Da har vi 16 ulike siffer:  0, 1, ..., 9, A, B, C, D, E og F.
Sifrene A til F tilsvarer det desimale 10, 11, 12, 13, 14 og 15.

Tallet 237 er 2*256 + 3*16 + 7*1.
Tallet 4E er 4*16 + 14*1.
FF er 15*16 + 15*1 = 255.








2+3-4 er samme som 2+(3-4)
### 
Gange og dele gjøres før pluss og minus.
Vi sier de har høyere presedens.

Derfor blir 2+3*4 lik 2+12 og ikke 5*4.


### Paranteser først
Som i vanlig matematikk skal paranteser evalueres først.
2+3*4 er 2+12, mens (2+3)*4 er 5*4.


