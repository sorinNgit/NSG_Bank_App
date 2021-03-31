#NSG Bank App Java OOP Project

## Account
Account este o clasa abstracta utilizata pentru a mosteni Current Account si Savings Account. </br>
Account contine doua metode abstracte, **deposit** si **withdrawal**, actiuni ce pot fi realizate cu orice tip de cont bancar si care trebuie suprascrise in Current Account si Savings Account. </br>
De asemenea, clasa Account contine si metodele pentru conversia monetara, conversie ce se poate realiza intre LEI, EUR, USD, GBP si RUB. Moneda standard cu care este initializat contul este RON.

## Current Account
Current Account are ca parametrii doua liste pentru stocarea tranzactiilor efectuate si a cardurilor asociate contului bancar precum si un comision afenrent tranzactiilor la bancomat. </br>
Metodele **deposit** si **withdrawal** sunt realizate folosind cardul la un bancomat. La printarea acestora se va evidentia numarul contului, cardul ce a fost folosit pentru tranzactie precum si suma tranzactionata si fondurile totale din cont. </br>

Folosind un cont curent putem face plati dar si incasa bani, pentru aceste actiuni avem metodele **payment** si **cashing** ce reprezinta tranzactii si instantiaza o noua tranzactie si o adauga in lista. </br>

Metoda **check_balance** are rol de interogare sold si afiseaza balanta in moneda aferenta contului. </br>

Metoda **addCard** adauga un nou card Contului Bancar, ce este stocat intr-o lista de tip ArrayList<>(). </br>

## Savings Account

Savings Account nu concepe plati, insa are avantajul ca poti ramane indatorat bancii in cazul in care faci cumparaturi peste balanta actuala. Si acest tip de cont suporta tranzactiile de la bancomat si are carduri. </br>


## Card

Clasa **Card** prezinta ca parametrii toate elementele regasite pe un card: numarul cardului, numele detinatorului, data de expirare precum si codul CVC si deserveste pentru tranzactiile online/offline. </br>

## Transaction

In clasa **Transaction** regasim detaliile referitoare la tranzactiile ce au fost facute de catre un cont bancar (data, suma tranzactionata si banca/compania cu care s-a facut tranzactia). </br>

## Client

Clasa **Client** primeste un nume si creaza un client caruia ii atribuie o lista cu Conturi Bancare oferindu-i posibilitatea sa-si deschida mai mult decat unul singur. </br>

## Client Service

**Client Service** creaza un ArrayList sortat cu clientii inregistrati si are ca metode **registerClient** - inregistreaza un client nou; **printClients** - printeaza toti clientii;  **printCards** - printeaza toate cardurile tuturor clientilor;  **addAccount** - adauga un cont nou unui client;  **findClientByName** - gaseste un client dupa numele sau. </br>

## Main

In main sunt prezentate interogarile ce se pot face in aplicatie:
* Printarea clientilor + conturilor sale
* Printarea cardurilor tuturor clientilor
* Deposit de la bancomat
* Withdrawal de la bancomat
* Verificare sold
* Achizitionare de bunuri de la comercianti
* Primire de bani
* Conversie valutara
* Refund de obiecte
* Afisare transaction history