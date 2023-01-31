# Instructions for flashing firmwares:

* Unplug your module from your case.
* Download the desired firmware above.
* Attach your module to your mac/pc using a micro usb cable.
* Use the [daisy web programmer](https://electro-smith.github.io/Programmer/) to flash the firmware.

> Note: The daisy web programmer requires a chrome browser to work correctly. The daisy web programmer page also has additional instructions that can be viewed by pressing 'Display Help'.

# Release Notes:

### [Monolith.0.0.2-beta.4.bin](https://github.com/rawyawmedia/eurorack/raw/main/firmware/Monolith.0.0.4-beta.2.bin)

#### changes:
* fm effect is louder in the mix

### [Monolith.0.0.2-beta.3.bin](https://github.com/rawyawmedia/eurorack/raw/main/firmware/Monolith.0.0.3-beta.2.bin)

#### changes:
* audio input has different saturation behavior

### [Monolith.0.0.2-beta.2.bin](https://github.com/rawyawmedia/eurorack/raw/main/firmware/Monolith.0.0.2-beta.2.bin)

#### changes:
* dj filter frequency responses are different
* reverb delay lines have different saturation behaviors to reduce digital noise

### [Dizygote.0.0.2-beta.1.bin](https://github.com/rawyawmedia/eurorack/raw/main/firmware/Dizygote.0.0.2-beta.1.bin)

#### changes:
* pressing and holding the trig button puts the envelope into a loop state
* pressing and holding the switch button converts the two stereo voices into two mono outputs
* if the switch leds are flashing, the module is in the new mono state


### [Monolith.0.0.2-beta.1.bin](https://github.com/rawyawmedia/eurorack/raw/main/firmware/Monolith.0.0.2-beta.1.bin)

#### changes:
* pop reduction was added to the fm processing
* the input audio signal is now fed through the dj filter when fm is off and the blend knob is turned up
* fm output is fed through the dj filter
* mod cv input now has a different response
* dj filter frequencies have changed; dj filter cv input now has a different response
* wet cv input now has a different response

### [Dizygote.0.0.1.bin](https://github.com/rawyawmedia/eurorack/raw/main/firmware/Dizygote.0.0.1.bin)

dizygote is an a-side/b-side digital oscillator with a built-in envelope generator. the a-side builds harmonies with a square waveform and frequency modulation. the b-side distorts a sine waveform with phase modulation.

#### inputs:

trig - button and gate in to trigger oscillator amplitude envelopes
switch - button and gate in for toggling between the a and b sides
length - knob and cv in for changing the envelope length
mod - knob and cv in for changing the phase and fm modulation amounts
mfreq - knob and cv in for changing the phase and fm modulation frequencies
freq - knob for setting the oscillator frequency
v/oct - voltage per octave cv for modulating the oscillator frequency

#### outputs:

out l and out r - audio output
env - cv envelope out

### [Monolith.0.0.1.bin](https://github.com/rawyawmedia/eurorack/raw/main/firmware/Monolith.0.0.1.bin)

monolith is a pitch-shifter reverb inspired by west coast synthesis techniques. It utilizes a time-domain based FM algorithm that acts as a shimmer.

#### inputs:

in l and in r - audio input, left will be converted to stereo if there is no right input
blend - knob and CV for controlling the fade between the dry and fm audio signals
dj filter - knob and CV for controlling the reverb delay line filtering
wet - knob and CV for controlling the reverb decay
mod - knob and CV for controlling the scale of FM modulation. low mod values correspond with microtonal pitch regions. high mod values correspond with multiple octave shifts.
on - button and CV gate for toggling on/off FM modulation. when FM modulation is turned on/off, the FM modulator oscillator is reset.
quant - button and CV gate for toggling on/off FM pitch quantization.
freq and v/oct - knob and CV for controlling the frequency of the FM modulator oscillator. also control reverb pre-delay.
shape - knob and CV for controlling FM modulator oscillator shape. shape wavetable transitions from sine wave (8 o’clock) to triangle wave (12 o’clock) to square wave (4 o’clock).
clock - CV gate for tempo syncing modulator oscillator period.

#### outputs:

out l and out r - audio output
gate - CV gate out that is period synced with the FM modulator oscillator