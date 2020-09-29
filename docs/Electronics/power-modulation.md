# Power output modulation / dimming

## AC
- Thyristor (aka SCR):
  * current flow only in one direction (only positive or only negative)
  * The voltage on the other half waveform stays to ~ zero.
  * Max duty cycle 50%

- TRIAC:
  * current flows in both directions
  * Better to use opto TRIAC
  * Max duty cycle 100%

- Thyristor / TRIAC control methods:
  * zero cross trigger
  * random turn ON

- Zero cross trigger:
  * switch ON / OFF only occurs when zero crossing
  * When zero crossing:
    + Signal on gate is ON: output is ON until the next zero cross
    + Signal on gate is OFF: output is OFF until the next zero cross

- Random turn ON trigger:
  * switch ON occurs any time
  * switch OFF occurs when zero crossing

- GTO (gate turn off) thyristor:
  * Random turn ON AND turn OFF
  * It can be switched off with a trigger on the gate.

### Modulating power on AC
- Random turn ON TRIAC: any duty cycle from 0 - 100%
- zero cross detector: when is the right time to send signal on the gate?
- timer capture compare:
  * start on zero cross
  * set comparator to the duty cycle desired (AC frequency is well known, 50 or 60Hz)
  * Automatically turns ON signal on gate when reaching the desired D.C.

## DC
- MOSFET (e.g. IRF540N) + PWM

