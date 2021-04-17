

# Bramy


Modelowana sytuacja :

Turrysci pojawiaja sie na swiecie gdzie mamy M mediow , kazdy z turystow idzie do sklepu gdzie ubiega sie o srodki potrzebne do otwarcia tunelu po czym jak dostanie srodki idzie wynajmowac medium jesli sie uda i chociaz jedno z medium bedzie wolne -> wynajmuje medium (o medium ubiegaja sie tylko turysci z srodkami ze sklepu) . Jak juz medium zostalo wynajete turyst czeka az otworzy ono portal do tunelu , po T turystach medium sie meczy i potrzebuje odpoczynku , po tym jak turysta wyrzucilo z innego swiata idzie on do sklepu ubiegac sie o srodki zeby kolejny raz podrozowac w inne wymiary

  

## Parametry:

M - mediow / tuneli

T - turystow / portalow 

F - pojemnosc sklepu 
  

Typy wiadomosci

 ## Stany
 
 1.  `INIT` -
     1. pojawia sie turzysta , stan w ktorym namierza wejsc do sklepu wysyla `REQUEST FOR S_ENTRY` do wszystkich procesow 
 1.  `SHOP` - 
	 2. `SHOPPING`
	 3. `SHOPPED`
  3.   `MEDIUM`
	2.  `MEDIUM TAKEN`
   4.  `TRIP`
   	4.1 `W8 FOR PORTAL`
     4.2 `ENTER PORTAL`
	4.3 `TOURISM`
	4.4 `FALLBACK` -> `SHOP`  
	
	
## Wiadomosci

	1. `REQUEST FOR SENTRY`(znacznikCzasowy: Int) - wyrazenie zadania wejscia do sklepu

	1. `REQUEST FOR MENTRY`
  
**