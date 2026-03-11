10.03.2026
IP-ul pentru procesorul MIPS: https://github.com/OmarMongy/Single_Cycle_MIPS_processor?utm_source=chatgpt.com
<img width="1348" height="656" alt="diagramaMIPS" src="https://github.com/user-attachments/assets/b38452ad-dce2-437f-b888-a600b647adc2" />
Procesorul bazat pe arhitectura MIPS este un procesor de tip RISC (Reduced Instruction Set Computer) care utilizează un set redus de instrucțiuni simple și o structură hardware optimizată pentru execuție rapidă. Varianta analizată este un procesor MIPS single-cycle, în care fiecare instrucțiune este executată într-un singur ciclu de ceas.
În arhitectura single-cycle, toate etapele execuției unei instrucțiuni – fetch, decode, execute, memory access și write-back – sunt realizate în cadrul aceluiași ciclu de ceas. Această abordare simplifică controlul procesorului și facilitează implementarea și simularea în limbaje de descriere hardware precum Verilog.
Lățimea instrucțiunilor
Instrucțiunile procesorului au o lățime de 16 biți. Această dimensiune permite codificarea compactă a instrucțiunilor și a operanzilor. Instrucțiunile sunt împărțite în câmpuri care conțin:
opcode – codul operației
registre sursă
registru destinație
immediate (valoare constantă)
Lățimea datelor
Procesorul utilizează o lățime a datelor de 8 biți pentru operațiile aritmetice și logice. Toate registrele generale și unitatea aritmetică și logică operează pe date de 8 biți.
Fișierul de registre
Procesorul conține 8 registre generale, fiecare cu lățimea de 8 biți. Aceste registre sunt utilizate pentru stocarea temporară a operanzilor și a rezultatelor operațiilor. Fișierul de registre permite citirea simultană a două registre și scrierea într-un registru în timpul execuției unei instrucțiuni.
Setul de instrucțiuni (ISA)
Procesorul implementează un subset simplificat al ISA MIPS, care include instrucțiuni aritmetice, logice, de acces la memorie și de control al fluxului de execuție. Exemple de instrucțiuni suportate:
ADD – adunare
SUB – scădere
AND – operație logică AND
OR – operație logică OR
ADDI – adunare cu operand imediat
LOAD – încărcare din memorie
STORE – scriere în memorie
BEQ – branch dacă egal
JUMP – salt necondiționat
În total, implementarea simplificată conține aproximativ 8–10 instrucțiuni.
Componentele principale ale procesorului
Structura procesorului este formată din mai multe module hardware principale:
Program Counter (PC) – stochează adresa instrucțiunii curente
Instruction Memory – memorie care conține programul
Control Unit – generează semnalele de control
Register File – setul de registre generale
ALU (Arithmetic Logic Unit) – execută operațiile aritmetice și logice
Data Memory – memorie pentru date
Multiplexoare – selectează sursele de date
Adder pentru PC – calculează adresa următoarei instrucțiuni
