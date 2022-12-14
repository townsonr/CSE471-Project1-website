# Piano Synthesizer Component

Owner: Zane Aridi

## Functionality

1. Piano class dervived from tone instrument handles the playing of the instrument
2. PianoAR is the envelope for the piano and has a default release that's about as long as a piano's
3. Each note has an xml pedal pressed option which increases the sustain of the note by extending duration and release
4. The amplitude of notes varies based on the speed attribute specified in the xml that mimicks the speed at which a key is pressed (providing dynamics). In addition, the attack of the piano note envelope is shortened with higher press speeds to provide advanced dynamics.
5. The pedal noise should be generated by a sample at the beggining of a notes generation, however I commented it out because for some reason I get Link error 2019 for an unresloved external symbol. I created a resource for it and used the resource ID, but I couldn't figure out why I can't find the wav file. I would very much appreciate partial credit <3.

## Generated Audio
[AridizanPianoComponentSample.zip](https://github.com/townsonr/CSE471-Project1-website/files/9945056/AridizanPianoComponentSample.zip)

Score:
```
<score bpm="60" beatspermeasure="4">
     <instrument instrument="Piano" send0="1.0" send1="0.0" send2="0.0" send3="0.0" send4="0.0">
          <note measure="1" beat="1" duration=".5" note="G5" speed=".02"/>
          <note measure="1" beat="1.5" duration=".5" note="E5" speed="0.04"/>

          <note measure="1" beat="2" duration=".5" note="G5" speed="0.06"/>
          <note measure="1" beat="2.5" duration=".5" note="A#6" speed="0.06" pedal = "true"/>

          <note measure="1" beat="3.5" duration="1" note="G5" speed="0.04"/>
          <note measure="1" beat="3.5" duration="1" note="E5" speed="0.04"/>
          <note measure="1" beat="3.5" duration="1" note="B6" pedal="true" speed="0.02"/>

          <note measure="2" beat="1" duration=".5" note="G4" speed="0.01"/>
          <note measure="2" beat="1.5" duration=".5" note="A5" speed="0.02"/>
          <note measure="2" beat="2" duration=".5" note="Bb5" speed="0.03"/>
          <note measure="2" beat="2.5" duration=".5" note="C5" speed="0.04"/>
          <note measure="2" beat="3" duration=".5" note="D5" speed="0.05"/>
          <note measure="2" beat="3.5" duration=".5" note="Eb5" pedal="false" speed="0.06"/>
          <note measure="2" beat="4" duration=".5" note="F5" pedal="false" speed="0.07"/>
          <note measure="2" beat="4.5" duration=".5" note="G5" pedal="false" speed="0.08"/>

          <note measure="3" beat="1" duration=".5" note="F5" pedal="false" speed="0.07"/>
          <note measure="3" beat="1.5" duration=".5" note="Eb5" pedal="false" speed="0.06"/>
          <note measure="3" beat="2" duration=".5" note="D5" pedal="false" speed="0.05"/>
          <note measure="3" beat="2.5" duration=".5" note="C5" pedal="false" speed="0.04"/>
          <note measure="3" beat="3" duration=".5" note="Bb5" pedal="false" speed="0.03"/>
          <note measure="3" beat="3.5" duration=".5" note="A5" pedal="false" speed="0.02"/>
          <note measure="3" beat="4" duration="1" note="G4" pedal="true" speed="0.01"/>
          <note measure="3" beat="4" duration="1" note="Bb5" pedal="true" speed="0.01"/>
          <note measure="3" beat="4" duration="1" note="D5" pedal="true" speed="0.01"/>
     </instrument>
</score>
```
## Grading elements

10 - Plays piano notes ???

20 - Envelope generation ???

30 - Pedal simulation ???

35 - Basic dynamics ???

40 - Pedal noise ~

50 - Advanced dynamics ???
