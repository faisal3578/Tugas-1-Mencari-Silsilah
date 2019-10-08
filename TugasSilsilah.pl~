ank(raihan,ani).
ank(afif,raihan).
ank(farah,raihan).
ank(farhan,afif).
ank(arfan,afif).
ank(naura,farah).


orangTua(Y,X):-ank(Y,X),
    write('Orang tuanya adalah '),
    write(X),nl.

anak(Y,X):-ank(X,Y),
    write('Anaknya adalah '),
    write(X),nl.

saudara(Saus1,Saus2):-
    ank(Saus1,Ortu),
    ank(Saus2,Ortu),
    (   Saus1)\=(Saus2),
    write('Saudaranya adalah '),
    write(Saus2),nl.


sepupu(Spp1,Spp2):-
    ank(Spp1,Ortu1),
    ank(Spp2,Ortu2),
    ank(Ortu1,Kakek),
    ank(Ortu2,Kakek),
    (   Ortu1)\=(Ortu2),
    format('Sepupunya adalah ~w',[Spp2]).


 bolang(Anak,Kakek):-
    ank(Anak,Ortu),
    ank(Ortu,Kakek),
    write('Kakek/Neneknya adalah '),
    write(Kakek),nl.
