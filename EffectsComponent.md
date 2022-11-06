# Effects Component

Owner: Rachel Townson

## Functionality

For the effects component, I implemented reverb, noise gating, compression, and chorus effects. These effects take in audio one smaple at a time as produced by the synthesizer and changes the audioto have that effect. In my implementation, there are 5 effect "channels" that each instrument can send to. This is specified in the attributes of the <instrument> XML node as `send0` through `send4`. If `"send0"=0.0`, then none of the audio from that instrument is sent to the channel. If `"send0"=1.0`, then all of the audio from that instrument is sent to the channel.Each effect channel has a specified effect that is applied to any audio in that channel when it is time to process the effects (0 for no effects, 1 for reverb, 2 for noise gating, 3 for compression, 4 for chorus). This way, each instrument can select how much effect is applied to it and how those efects are mixed together. I Implemented my sends in series. When the current sample is done being processed, the effects component combines all those sends together with their specified gain.
  
Each effect has a few unique parameters that can be specified in the .score file. Chorus has pitch modulation. Compression can be downard or upward. The noise gate has a specified threshold. I had trouble with the reverb effect, so there are no extra parameters to make it as simple as possible.

## Generated Audio
[effects_sample_output.zip](https://github.com/townsonr/CSE471-Project1-website/files/9945094/effects_sample_output.zip)


## Grading elements

10 - Component passes audio ✓

20 - 1 Effect ✓

30 - 3 Effects ✓

40 - Controllable effects send ✓

50 - 4 Effects ✓
