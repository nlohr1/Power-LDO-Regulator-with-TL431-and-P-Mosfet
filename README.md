# Power-LDO-Regulator with TL431 and P-Mosfet
Power-LDO to regulate voltages above +5V protecting USB-connectors from incoming overvoltages.

This Layout adds a simple way to eliminate dangerous incoming Over-Voltages on USB (above 5,25V) coming f.ex. from
odd Power-Supplies which don't acomplish the USB-specifications (but often are usable and cheap enough to be used as 5V-Supply).

Usually generic LDO-chips can output between 100 mAmp upto 1 Ampére. But what if you have a Power-Supply which can supply 4 or
more Amps but the voltage is too high for savely connect to the USB-Power-Input? (f.ex. on the new Raspberry Pi 4).
So here you can go with a small Layout, whith a board needing only few space with 20 x 9 mm and can provide more than 4A –
with a Heat-Sink upto 10A or more...

Provided files here with 2 alternative solutions:
- first solution with a TL431-Shunt-Regulator + OPAmp and a *Power-P-Mosfet*,
- second solution with same TL431 + OPAmp but with a Power-*N-Mosfet*, due to this Mosfets generally have fewer resistance
  (=more "power"), are cheaper and there are more available types (of N-Mosfets) on the market.

A caveat from this second solution is that it has only a common +5V line but no common ground with the Main-Supply. But
in most cases this is no problem for the End-Load, bec. the providing 5V-Supplies normally are built with an isolated topology,
so GND may be seen here as the negative 5V-difference from the common +5V line.
