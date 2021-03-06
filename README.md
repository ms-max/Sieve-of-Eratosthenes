# Sieve-of-Eratosthenes
În matematică, ciurul lui Eratostene - un algoritm simplu de descoperire a tuturor numerelor prime până la un întreg specificat.<br>

Pentru a rula proiectul accesați acest link: https://repl.it/@Mariaicova/Sieve-of-Eratosthenes

## 1. SCOPUL

Scopul algoritmului este (determinarea numerelor prime) filtrarea numerelor. Numere prime rămân, iar restul se modifică în zeroouru(se filtrează cu ajutorul ciurului)
![Ciurul lui Eratostene](https://user-images.githubusercontent.com/69718491/106371390-5cd4cd80-636c-11eb-90fd-28382638bbf9.jpg)<br>

## 2. Algoritmul

1.Se scrie pe o foaie o listă cu toate numerele naturale de la 2 la n.<br>
2.Se caută în listă primul număr care nu a fost tăiat (și pe care încă nu l-am folosit).<br>
3.Se taie de pe foaie toți multiplii numărului ales mai înainte, cu excepția lui.<br>
4.Dacă încă nu am ajuns la finalul listei căutând numere netăiate, se revine la pasul 2.<br>
![ciurul-lui-eratostene](https://user-images.githubusercontent.com/69718491/106371628-5bf16b00-636f-11eb-9f14-64c9e09f722e.jpg)<br>
La final, toate numerele netăiate din listă sunt cele prime. De fiecare dată, numărul găsit la pasul 2 chiar este prim, pentru că, dacă ar fi fost divizibil cu vreun număr prim mai mic decât el, ar fi fost tăiat deja. Apoi, evident că numerele tăiate la pasul 3, fiind divizibile cu un număr prim mai mic decât ele, sunt numere compuse.

## 3. Screen din program

![](https://user-images.githubusercontent.com/69718491/106371404-a32a2c80-636c-11eb-9bd1-b63b7585127f.jpg)
<br> Am aflat că e posibil de înlocuit în rîndul nr.13 codul<br>
for(int s=2; s<N; s++){ 
<br>cu<br>
for(int s=2; s*s<N; s++){ <br>
adică să verificăm până s e mai mic ca radical din N. Am verificat pentru N=100, până la s=7, într-adevăr lucrează!

![tabel](https://user-images.githubusercontent.com/69718491/106371633-67dd2d00-636f-11eb-8d08-b78c36101654.jpg)

## 4. Concluzii
în urma studierii acestui algoritm am observat că de fiecare dată când se ajunge la pasul 2, algoritmul face n/i pași pentru a tăia numerele compuse multipli de i. În total, asta înseamnă:<br>
n/2+n/3+n/5+n/7+⋯+n/k.<br>
(”— Ой! — сказал Фило озадаченно. — Шестерка уже вычеркнута. <br>
— Не беда, вычеркнем еще раз.” https://math.wikireading.ru/1092)<br>
Unde k este cel mai mare număr prim mai mic sau egal cu n. Factorizându-l pe n obținem:<br>
n(1/2+1/3+1/5+1/7+⋯+1/k).<br>
Al doilea factor, adică suma inverselor numerelor prime până la k, crește la fel de repede ca funcția ln(ln(n)), conform lui Euler. Așadar, complexitatea algoritmului este O(nln(ln(n))).
Am învățat mai bine algoritmi elementari,    m-a impresionat -  de ce anume așa se numește algoritmul - Ciur. 
