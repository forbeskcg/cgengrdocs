# Series and Parallel Circuits

Below we explore how various components in a circuit can be simplified, or collapsed into one value, depending on whether they are placed inline (series, tip-to-tail) or next to each other (parallel, tip-to-tip and tail-to-tail).

This is useful in many scenarios: perhaps you need a specific value and only have a fixed assortment of parts on hand, or you would like to estimate total power draw among several branches in a circuit.

We can approximate most circuits as resistors, capacitors, inductors, or some combination of those.

![Common electrical components in series and parallel](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a6/Resistors_inductors_capacitors_in_series_and_parallel.svg/1024px-Resistors_inductors_capacitors_in_series_and_parallel.svg.png)
[https://en.wikipedia.org/wiki/Series_and_parallel_circuits](https://en.wikipedia.org/wiki/Series_and_parallel_circuits)

## Resistors

### Resistors in Series

Resistors in series are pretty straightforward: just add each value to find the total resistors! 

$$R_{series} = R_1 + R_2 + ... + R_n$$

### Resistors in Parallel

To calculate two resistors in parallel, the inverse of the sum is equal to the sum of inverse resistances.

??? tip "Resistance vs Conductance"
    The inverse of electrical resistance ($\Omega$) is conductance, where a higher value means more current can flow rather than less. The unit is the Siemen, $S$, where $S = 1/\Omega$. What happens if you sum two conductances in series and substitute $1/\Omega_n$ for $S_n$?

$$\frac{1}{R_{parallel}} = \frac{1}{R_1}+\frac{1}{R_2}$$

$$R_{parallel} = \frac{R_1 R_2}{R_1 + R_2}$$

## Capacitors

[Capacitance](https://en.wikipedia.org/wiki/Capacitance#Capacitance_of_conductors_with_simple_shapes) (in farads) between two plates is proportional to the plate area, $A$, and inversely proportional to the distance between the plates, $d$:

$$ C = \frac{\epsilon A}{d} $$

### Capacitors in Parallel

Therefore, capacitors in *parallel* add directly, just as resistors in series, because we are increasing the size of the plate $A$ with each adjacent capacitor:

$$C_{parallel} = C_1 + C_2 + ... + C_n$$

### Capacitors in Series

Capacitors in *series* add as resistors do in parallel, as the total gap distance $d$ increases:

$$C_{series} = \frac{C_1 C_2}{C_1 + C_2}$$

## Inductors

### Inductors in Series

Inductance follows the same formulas as resistance, as it is proportional to the number of turns in a coil which are inherently series in nature:

$$L_{series} = L_1 + L_2 + ... + L_n$$

### Inductors in Parallel

Inductance in parallel follows the same formula as resistors in parallel:

$$L_{parallel} = \frac{L_1 L_2}{L_1 + L_2}$$

## Example Circuit

This example shows how multiple resistors can add up to the same total resistance (and thus current).

Try creating the same circuits with capacitors and inductors.

<iframe src="https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKACcQ09wNDP9OAFipUw8FmAwp+3SXy7gU3KuSRIRUaEgBqAewA2AFwCGAczotTMkNgTSFwjZBYB3aymHu8s9pyk95fw8NMThXa2w0CLtwSxAGSJtCbgTpRygocJQEPjk-aTznNwU87NzeTOKBJW5Me29MyWlicr4WxWUQVWonLRA9IzMLK3bsZJB29JFfdrz24IzcZw55z1HIQQy0ZfjEvNShDUpnJt2CioOwJQzu9QyYHQMTc3CDhbf-VjcP6QOx5XC602ozGsTco3GIL4RXyh1hNTBESiCgRziAA" width="800" height="600"></iframe>

