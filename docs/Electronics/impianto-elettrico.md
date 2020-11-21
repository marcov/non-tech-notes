# Tipo di Interruttori


## Differenziale
**RCD**: _residual current device_
**RCCB**: _residual circuit current breaker_

* Protegge da dispersioni
* Misura delta tra Iin e Iout
* Quando delta > *rating*, interruttore apre tramite meccanismo elettromagnetico
* Rating tipici: 30mA (indoor) 300mA (outdoor, a valle del contatore)

### Differenziale Selettivo

Un differenziale che, quando misura un delta positivo, apre con un certo ritardo.
Quando si usa? Quando ci sono piu' int. differenziali in serie, e si vuole che il
selettivo apra "per ultimo".


## Magnetotermico
**MCB**: _Miniature circuit breaker_

* Protegge da sovraccarichi e corto circuiti.

## Differenziale + Magnetotermico
**RCBO**: residual circuit breaker with overcurrent protection
Aka Salvavita

## Impianto Tipico

Legenda:

- DF = Differenziale
- MT = Magnetotermico


```
[Contatore]
    \
     \___
         [DF selettivo 300mA]
              \
               \
                \
                 \___ [Appartamento 1]
                 |      \
                 |       \
                 |        \___[DF normale 30mA]
                 |                      \
                 |                       \
                 |                        \__[MT 4500A luci zona giorno]
                 |                        |
                 |                        \__[MT 4500A luci zona notte]
                 |                        |
                 |                        \__[MT 4500A prese zona giorno]
                 |                        |
                 |                        \__[MT 4500A prese zona notte]
                 |
                 \___ [Appartamento 2]
                        \
                         \
                          \___[DF normale 30mA]
                                        \
                                         \
                                          \__[MT 4500A luci zona giorno]
                                          |
                                          \__[MT 4500A luci zona notte]
                                          |
                                          \__[MT 4500A prese zona giorno]
                                          |
                                          \__[MT 4500A prese zona notte]
```
