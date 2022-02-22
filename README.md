# italtone
random docs about sound


```mermaid
flowchart TD
    subgraph speaker3[Mid Top]
        speaker3_spk1((.))
        speaker3_spk2((.))
    end

    subgraph speaker4[Bass]
        speaker4_spk1((.))
        speaker4_spk2((.))
    end

    subgraph speaker2[Sub]
        speaker2_spk1((.))
    end

    subgraph speaker1[Sub]
        speaker1_spk1((.))
    end

    subgraph extras[For The Future]
        vinyl[Grammari]
        preamp[NanoPreamp]
    end

    crossover[Behringer 2496]
    mixer[Soundcraft Note 12FX]
    amp1[Qsc 1]
    amp2[Qsc 2]
    amp3[Crown]
    microphone1[Shure SM58]
    controller[DDJ-400]

    mixer ---|xlr|crossover & crossover
    crossover ---|xlr| amp1
    crossover ---|xlr| amp2 & amp2
    crossover ---|xlr| amp3

    amp3 o==o|spk| speaker4_spk1
    amp1 o==o|spk| speaker1_spk1 & speaker2_spk1
    amp2 o==o|spk| speaker3_spk1 & speaker3_spk2

    microphone1 ---|xlr| mixer
    controller  x--x|rca| mixer
    controller -.-|rca| preamp

    amp1 <--->|jack| amp1
    preamp <-.->|rca or jack| mixer
    vinyl <-.->|rca or jack| mixer
    vinyl x-.-x|rca| preamp

    subgraph cabletypes[Cable Types]
        direction TB
        xlr((xlr))--- xlr
        spk((spk))o==ospk
        rca((rca))x--xrca
        jack((jack))<-->jack
        opt((optional))-.- opt
     end
```
