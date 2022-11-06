# CSE 471 Project 1: Multi-Component Music Synthesizer

Group members: Rachel Townson and Zane Aridi

## Music Selection

Title: Anti Hero

Score file (as .txt): [sample_txt.txt](https://github.com/townsonr/CSE471-Project1-website/files/9945066/sample_txt.txt)

Audio file (as .wav): [sample_output.zip](https://github.com/townsonr/CSE471-Project1-website/files/9945071/sample_output.zip)


## Score file format

```
<score bpm="120" beatspermeasure="2">
    <instrument instrument="Piano" send0="1.0" send1="0.0" send2="0.0" send3="0.0" send4="0.0">
        <note measure="1" beat="2" duration="0.33" note="F4" pedal="true" speed=".01"/>
        <note measure="1" beat="2.33" duration="0.33" note="G4" pedal="false" speed=".1"/>
    </instrument>
    <instrument instrument="chorus">
        <note measure="1" beat="2.33" wet="0.7" gain="1.0" pitchModulation="50" />
    </instrument>
    <instrument instrument="compression">
        <note measure="1" beat="2.33" wet="0.7" gain="1.0" type="down" />
    </instrument>
    <instrument instrument="noise">
        <note measure="1" beat="2.33" wet="0.7" gain="1.0" threshold="0" />
    </instrument>
    <instrument instrument="reverb">
        <note measure="1" beat="2.33" wet="0.7" gain="1.0" />
    </instrument>
<score/>
```

- `instrument`s indicate instruments or effects that are applied to all of the notes that are children of that `instrument`
- when `instrument` is `Piano` or `ToneInstrument`, each note below it is generated through the synthesizer
- when `instrument` is `none`, `reverb`, `noise`, `compression`, or `chorus`, the corresponsing effect is used on any sound generated during the specified beat
- the `send0` through `send4` attributes of an instrument indicate which effects send that instrument's audio is sent to. These are later processed by the effects applied to each send
- each effect has different attributes depending on the functionality of the effect


## Components:

[Piano Synthesizer](https://townsonr.github.io/CSE471-Project1-website/PianoSynthesizer)

[Effects Component](https://townsonr.github.io/CSE471-Project1-website/EffectsComponent)
