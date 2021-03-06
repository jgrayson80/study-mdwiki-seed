# Nova overview

<script src="mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>

<div class="mermaid">
graph LR

subgraph NOVA

    A>Sample Probe]-->|Air Detector|c1[Splitter Valve]
    A-->RotaryValve[Rotary Valve]
    RotaryValve-->Calibrators
    RotaryValve-->CooxControls
    RotaryValve-->BGControls
    RotaryValve-->ChemControls
    RotaryValve-->CooxCalibrator
    c1-->B
    B[Lysing Reagent] -->|Hemolyzer|C[Cuvette]
    c1-->aso1
    C-->CooxWaste
    ast5-->MainWaste


    subgraph COOX Calibrator
        CooxCalibrator[Calibrator]
        LysingReagent[Lysing Reagent]
        CooxWaste[Waste]
    end

    subgraph COOX Controls
        CooxControls[Controls]
    end

    subgraph Calibrators with Creatine
        Calibrators[Calibrators]
        MainWaste[Waste]
    end

    subgraph Blood Gas Controls
        BGControls[Controls]
    end

    subgraph Chemistry Controls
        ChemControls[Controls]
    end

    subgraph CO-oximiter Module
        subgraph HGBfractions and Total Bilirubin
        C
        end
        B
        C
    end

    subgraph Chemistry Module

        subgraph Analyzing Section One
            aso1[pCO2]-->aso2[pO2]
            aso2-->aso3[LAC]
            aso3-->aso4[BUN]
            aso4-->aso5[GLUCOSE]
            aso5-->aso6[CREATINE]
            aso6-->c2[Reference Probe]
        end

        subgraph Analyzing Section Two
            c2-->ast1[pH]
            ast1-->ast2[Na+]
            ast2-->ast3[K+]
            ast3-->ast4[Cl-]
            ast4-->ast5[Ca++]
        end
    end
end
</div>