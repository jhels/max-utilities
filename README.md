# max-utilities

A collection of simple abstractions for Max/MSP that make patching a little bit faster.

All signal-rate objects listed below have multichannel equivalents included alongside them: just prefix any object ending in `~` with `.mc` to use these.

### DSP

#### Synths and Oscillators

* fm\~. Frequency modulation (FM) synth with adjustable envelopes.

* karplus\~. A gen\~ implementation of the [Karplus-Strong string synthesis](https://en.wikipedia.org/wiki/Karplus%E2%80%93Strong_string_synthesis).

* oscs\~. A wrapper for the four basic oscillators provided by Max/MSP: cycle\~, saw\~, tri\~ and rect\~ (sine, sawtooth, triangluar and rectangular waves). Allows you to choose one and switch between them quickly.

* vsts\~. A wrapper for the vst\~ object which lets you input {pitch, velocity} MIDI note pairs to output notes without having to do any additional patching.

#### Effects

* bandstop\~. A simple bandstop filter.

* biquadUI\~. Integrates the biquad\~ audio filter with an interface so you can initialise the filter and control it without further patching..

* envdraw\~. Allows you to draw an signal envelope with your mouse and trigger it with a bang, for use with other DSP objects. Applies smoothing as desired using a simple moving average.

* filterknob\~. Filter knob similar to those found on certain DJ mixers. Turning it below 0 activates and allows you to control a low-pass filter; turning it above 0 does likewise with a high-pass filter. Also has adjustable resonance.

* gendelay\~. Simple sample-based delay with adjustable delay time, decay, and feedback.

* hires\~. A simple, resonant, high-pass filter.

### Utilities

* beatdetector\~. Partitions the output of [bonk\~](https://github.com/v7b1/bonk_64bit-version) into different outlets. The result is that different drums and cymbals are generally output from different outlets, allowing you to use audio to trigger elements of your patches.

* counters and counters-off. Allows you to create a named group of counters which can be reset simultaneously using the counters-off object. This can be useful for timing and rhythm purposes.

* hot.operators. Versions of the standard operator objects (+, - \*, /, pow, etc.) which are triggered by inputs from either inlet, instead of only the left inlet.

* makenotelist. Outputs {pitch, velocity} pairs in a list, instead of from different outlets as with the native makenote object.

* mixer\~ and monomixer\~. Simple mixers similar to a DJ mixer. Connect your audio inputs and easily adjust their levels or filter them. Uses filterknob\~.



