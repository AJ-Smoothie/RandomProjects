# RandomProjects
This repository contains files for things such as my instructables and other internet posts

You've used the wrong resistance to calculate the cross-over (break, or cut-off) frequency. The formula is

$$ f_c = \frac{1}{2\pi R_fC_i} $$

You've also named \$C_i\$ rather oddly. In the convention of such circuits, the subscript \$f\$ means feedback, and \$i\$ is used for inputs. Why not call that capacitor \$C_f\$, as it's clearly feedback? From this point on, that's the name I shall give the capacitor, \$C_f\$.

The actual cross-over frequency of your circuit is:

$$ f_c = \frac{1}{2\pi R_fC_f} = \frac{1}{2\pi \times 90\rm{\ k\Omega} \times 1.77\rm{\ nF}} = 1\rm{\ kHz} $$

If the frequency of square wave input approaches the cross-over frequency, then the circuit behaves less like an integrator, and more like a regular low-pass filter, which is why you are seeing <strike>unstable</strike> curved sections in the output waveform, instead of straight slopes. If you want those nice straight "integrator" slopes, then:

$$ f_{in} << f_c $$

Your input waveform does not satisfy this condition. Input frequency is 500Hz, which is way too close to 1kHz for you to see the expected straight slopes. 500Hz may be fine if the cross-over frequency were actually 10kHz, as required.

By the way, you also use the term "unstable" somewhat loosely. This circuit is not unstable, as you put it. The blue line is not "linear" or "straight", or is "curved" is probably what you meant.

