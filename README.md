Lightware_Library
=================

Arduino Lightware Library ported for the Spark Core

LightwaveRF 434MHz interface
Author: Lawrie Griffiths (lawrie.griffiths@ntlworld.com)
Copyright (C) 2013 Lawrie Griffiths
Adapted for Spark Core by Paul Kourany, May 22, 2014

NOTE: Default pins assignment for Spark Core:

Lightwave   Spark
tx          D3
rx          D2

Unlike Arduino, pin designation and interrupt numbers on the Spark are the same.  So in the setup call:

  lw_setup(tx_pin, rx_pin, interrupt);  -> rx_pin and interrupt are the same
  
Thus, for tx = D5 and rx = D4, the call becomes:

  lw_setup(D5, D4, D4);
