# Introduction to ctapipe

Very basic notebooks on ctapipe to explain functionality

ctapipe: https://ctapipe.readthedocs.io/en/latest/

## Starting level

1. ctapipe starts at "DL0/R1 level", ie pixel waveform data calibrated to units of photo electrons
2. Every instrument team needs to write an EventSource plugin for ctapipe, that can read your data files and fills them into the ctapipe data structures:
https://ctapipe.readthedocs.io/en/latest/api-reference/io/index.html#creating-a-new-eventsource-plugin
3. Dummy plugin example https://github.com/cta-observatory/ctapipe/tree/main/test_plugin
4. Supports multiple reconstruction techniques, etc
5. Sample DL1 data from CTAO avaliable on CTAO Monte Carlo Simulations - Eventlists on DL2 data level - prod5
6. DL2 -> DL3 irf builder, ie pyirf (https://pyirf.readthedocs.io/en/latest/) now part of ctapipe
7. DL3 onwards is handled by Gammapy (https://docs.gammapy.org/1.3/)