To configure LArASIC (THIS SHOULD BE DONE AUTOMATICALLY!)
Only check in -> arduino, tools, serial monitor, type “H”, that the hex code is “BC”, corresponding to the following parameters:

G TPD 0 (test pulse off)
C STS 0
C SNC 0
C SG 11
C ST 11
C SDC 0  (v4) / C SMN 0 (v7)
C SBF 1
-> Should be 0xBC = 10111100
    (Note: SNC is set to 0 = 900 mV non-collecting mode instead of 1 = 200 mV collecting mode. Reason: Signal would be saturated early).

To configure LArASIC for a test pulse run (with 100 us test pulse length):
C STS 1
G TPD 96
(96 corresponds to 100 us length, checked on oscilloscope)

To configure LArASIC (from scratch, this is not necessary under normal conditions):
-> arduino, load LARASIC_AdHoc_ino

