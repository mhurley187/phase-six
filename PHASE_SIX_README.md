# Phase Six (disting NT plug-in)

Six LFOs from one master clock, each hardwired to its own output (LFO 1-6 -> buses 13-18 by default; every output
can be re-assigned and set to Add/Replace).

- **Rate** (+ **Range**: Slow 0.001-1 Hz, Medium 0.05-51 Hz, Fast 5 Hz-5 kHz) and **Rate CV** (1 V/oct).
- **Phase**: 0 = all LFOs together; 100% = the six LFOs evenly spaced around one cycle (60 degrees apart);
  negative reverses the order. **Phase CV**: 5 V = 100%.
- **Rate spread**: time-stretch across the bank; at 100% LFO 1 runs 1 octave slower and LFO 6 one octave faster than Rate.
- **Reset** input: rising edge through 1 V restarts all LFOs.
- **Shape** (20): Sine, Triangle, Ramp up/down, Square, Smooth/Stepped/Glide random, Staircase, Folded sine, Rect sine, Pump,
  Bounce, Chirp, FM wobble, Wander, Ratchet, Triple ramp, Jitter, Zigzag. **Skew** bends the cycle (duty cycle for Square).
  Random shapes use one shared random sequence, so phase-shifted LFOs play the same values at offset times.
- **Depth**, **Polarity** (bipolar / unipolar +/-), **Offset** (+/-5 V).

Build: same GitHub repo as Comb Voice. The Actions build now makes both plug-ins and saves them in one artifact called `plugins`.
