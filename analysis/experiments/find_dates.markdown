
# Find dates, try to find match records

## begin csv
```
Medtronic Diabetes CareLink Personal Data Export File (v1.0.1) 
PATIENT INFO

9/1/06
DEVICE INFO
Time Changes: 1

DEVICE DATA (115 records)
7/1/06 08:36:21
Timestamp,Programmed Bolus Duration (hh:mm:ss),BWZ Estimate (U),BWZ Target High BG (mg/dL),BWZ Target Low BG (mg/dL),BWZ Carb Ratio (grams),BWZ Insulin Sensitivity (mg/dL),BWZ Carb Input (grams),BWZ BG Input (mg/dL),BWZ Correction Estimate (U),BWZ Food Estimate (U),BWZ Active Insulin (U),Raw-Type,Raw-Values,Raw-Upload ID
7/1/06 06:10:22,,,,,,,,,,,,ChangeTimeDisplayFormat,"FORMAT=d24,9773719114
7/1/06 06:10:32,,,,,,,,,,,,ChangeTime,"NEW_TIME=1151741400000,9773719113
7/1/06 08:12:38,,,,,,,,,,,,ChangeSuspendEnable,"ENABLE=user_suspend, PRE_ENABLE=null"
7/1/06 08:13:08,,,,,,,,,,,,ChangeSuspendEnable,"ENABLE=normal_pumping, PRE_ENABLE=null"
7/1/06 08:17:45,,,,,,,,,,,,ChangeActiveBasalProfilePattern,"PATTERN_NAME=pattern a, ACTION_REQUESTOR=pump"
7/1/06 08:18:05,,,,,,,,,,,,ChangeActiveBasalProfilePattern,"PATTERN_NAME=pattern b, ACTION_REQUESTOR=pump"
7/1/06 08:19:06,,,,,,,,,,,,ChangeActiveBasalProfilePattern,"PATTERN_NAME=pattern a, ACTION_REQUESTOR=pump"
7/1/06 08:20:08,,,,,,,,,,,,ChangeActiveBasalProfilePattern,"PATTERN_NAME=pattern b, ACTION_REQUESTOR=pump"
7/1/06 08:20:47,,,,,,,,,,,,ChangeTimeDisplayFormat,"FORMAT=d12,9773719106
7/1/06 08:21:13,,,,,,,,,,,,ChangeTimeDisplayFormat,"FORMAT=d24,9773719105
7/1/06 08:22:10,,,,,,,,,,,,ChangeTimeDisplayFormat,"FORMAT=d12,9773719104
```

## 2006-07-01T08:23:47 5b

match with our binary records

```

7/1/06 08:23:47 BolusWizardBolusEstimate
  "BG_INPUT=100, BG_UNITS=mg dl, CARB_INPUT=3, CARB_UNITS=grams,
  CARB_RATIO=10, INSULIN_SENSITIVITY=50, BG_TARGET_LOW=100,
  BG_TARGET_HIGH=100, BOLUS_ESTIMATE=0.3, CORRECTION_ESTIMATE=0,
  FOOD_ESTIMATE=0.3, UNABSORBED_INSULIN_TOTAL=0, UNABSORBED_INSULIN_COUNT=0,
  ACTION_REQUESTOR=pump"
    0: Timestamp: 7/1/06 08:23:47
    1: Bolus Type:
    2: Bolus Volume Selected (U):
    3: Bolus Volume Delivered (U):
    4: Programmed Bolus Duration (hh:mm:ss):
    5: BWZ Estimate (U): 0.3
    6: BWZ Target High BG (mg/dL): 100
    7: BWZ Target Low BG (mg/dL): 100
    8: BWZ Carb Ratio (grams): 10
    9: BWZ Insulin Sensitivity (mg/dL): 50
    10: BWZ Carb Input (grams): 3
    11: BWZ BG Input (mg/dL): 100
    12: BWZ Correction Estimate (U): 0
    13: BWZ Food Estimate (U): 0.3
    14: BWZ Active Insulin (U): 0.0
    15: Raw-Type: BolusWizardBolusEstimate
    16: Raw-Values: "BG_INPUT=100 && BG_UNITS=mg dl && CARB_INPUT=3 && CARB_UNITS=grams && CARB_RATIO=10 && INSULIN_SENSITIVITY=50 && BG_TARGET_LOW=100 && BG_TARGET_HIGH=100 && BOLUS_ESTIMATE=0.3 && CORRECTION_ESTIMATE=0 && FOOD_ESTIMATE=0.3 && UNABSORBED_INSULIN_TOTAL=0 && UNABSORBED_INSULIN_COUNT=0 && ACTION_REQUESTOR=pump"



2006-07-01T08:23:47 5b
0000   0x5b 0x64 0x6f 0xd7 0x08 0x01 0x06 0x03    [do.....
0008   0x50 0x0a 0x32 0x64 0x00 0x03 0x00 0x00    P.2d....
0010   0x00 0x00 0x03 0x64 0x01 0x03 0x03 0x00    ...d....

```


## 2006-07-01T08:24:43 5b

match with our binary records

```
7/1/06 08:24:43 BolusWizardBolusEstimate
  "BG_INPUT=103, BG_UNITS=mg dl, CARB_INPUT=7, CARB_UNITS=grams,
  CARB_RATIO=10, INSULIN_SENSITIVITY=50, BG_TARGET_LOW=100,
  BG_TARGET_HIGH=100, BOLUS_ESTIMATE=0.7, CORRECTION_ESTIMATE=0,
  FOOD_ESTIMATE=0.7, UNABSORBED_INSULIN_TOTAL=0.3,
  UNABSORBED_INSULIN_COUNT=1, ACTION_REQUESTOR=pump"
    0: Timestamp: 7/1/06 08:24:43
    1: Bolus Type:
    2: Bolus Volume Selected (U):
    3: Bolus Volume Delivered (U):
    4: Programmed Bolus Duration (hh:mm:ss):
    5: BWZ Estimate (U): 0.7
    6: BWZ Target High BG (mg/dL): 100
    7: BWZ Target Low BG (mg/dL): 100
    8: BWZ Carb Ratio (grams): 10
    9: BWZ Insulin Sensitivity (mg/dL): 50
    10: BWZ Carb Input (grams): 7
    11: BWZ BG Input (mg/dL): 103
    12: BWZ Correction Estimate (U): 0
    13: BWZ Food Estimate (U): 0.7
    14: BWZ Active Insulin (U): 0.3
    15: Raw-Type: BolusWizardBolusEstimate
    16: Raw-Values: "BG_INPUT=103 && BG_UNITS=mg dl && CARB_INPUT=7 && CARB_UNITS=grams && CARB_RATIO=10 && INSULIN_SENSITIVITY=50 && BG_TARGET_LOW=100 && BG_TARGET_HIGH=100 && BOLUS_ESTIMATE=0.7 && CORRECTION_ESTIMATE=0 && FOOD_ESTIMATE=0.7 && UNABSORBED_INSULIN_TOTAL=0.3 && UNABSORBED_INSULIN_COUNT=1 && ACTION_REQUESTOR=pump"

7/1/06 08:24:43 UnabsorbedInsulin
  "BOLUS_ESTIMATE_DATUM=9773719100, INDEX=0, AMOUNT=0.3, RECORD_AGE=1,
  INSULIN_TYPE=null, INSULIN_ACTION_CURVE=300"
    0: Timestamp: 7/1/06 08:24:43
    1: Bolus Type:
    2: Bolus Volume Selected (U):
    3: Bolus Volume Delivered (U):
    4: Programmed Bolus Duration (hh:mm:ss):
    5: BWZ Estimate (U):
    6: BWZ Target High BG (mg/dL):
    7: BWZ Target Low BG (mg/dL):
    8: BWZ Carb Ratio (grams):
    9: BWZ Insulin Sensitivity (mg/dL):
    10: BWZ Carb Input (grams):
    11: BWZ BG Input (mg/dL):
    12: BWZ Correction Estimate (U):
    13: BWZ Food Estimate (U):
    14: BWZ Active Insulin (U):
    15: Raw-Type: UnabsorbedInsulin
    16: Raw-Values: "BOLUS_ESTIMATE_DATUM=9773719100 && INDEX=0 && AMOUNT=0.3 && RECORD_AGE=1 && INSULIN_TYPE=null && INSULIN_ACTION_CURVE=300"

7/1/06 08:24:43 BolusNormal
  "AMOUNT=0.7, CONCENTRATION=null, PROGRAMMED_AMOUNT=0.7,
  ACTION_REQUESTOR=pump, ENABLE=false, IS_DUAL_COMPONENT=false,
  UNABSORBED_INSULIN_TOTAL=null"
    0: Timestamp: 7/1/06 08:24:43
    1: Bolus Type: Normal
    2: Bolus Volume Selected (U): 0.7
    3: Bolus Volume Delivered (U): 0.7
    4: Programmed Bolus Duration (hh:mm:ss):
    5: BWZ Estimate (U):
    6: BWZ Target High BG (mg/dL):
    7: BWZ Target Low BG (mg/dL):
    8: BWZ Carb Ratio (grams):
    9: BWZ Insulin Sensitivity (mg/dL):
    10: BWZ Carb Input (grams):
    11: BWZ BG Input (mg/dL):
    12: BWZ Correction Estimate (U):
    13: BWZ Food Estimate (U):
    14: BWZ Active Insulin (U):
    15: Raw-Type: BolusNormal
    16: Raw-Values: "AMOUNT=0.7 && CONCENTRATION=null && PROGRAMMED_AMOUNT=0.7 && ACTION_REQUESTOR=pump && ENABLE=false && IS_DUAL_COMPONENT=false && UNABSORBED_INSULIN_TOTAL=null"





2006-07-01T08:24:43 5b
0000   0x5b 0x67 0x6b 0xd8 0x08 0x01 0x06 0x07    [gk.....
0008   0x50 0x0a 0x32 0x64 0x00 0x07 0x00 0x00    P.2d....
0010   0x03 0x00 0x07 0x64 0x5c 0x05 0x0c 0x01    ...d\...

```

## 2006-07-01T08:26:55 6b

match with our binary records

```
7/1/06 08:26:55 BolusWizardBolusEstimate
  "BG_INPUT=599, BG_UNITS=mg dl, CARB_INPUT=1, CARB_UNITS=grams,
  CARB_RATIO=10, INSULIN_SENSITIVITY=50, BG_TARGET_LOW=100,
  BG_TARGET_HIGH=100, BOLUS_ESTIMATE=9, CORRECTION_ESTIMATE=9.9,
  FOOD_ESTIMATE=0.1, UNABSORBED_INSULIN_TOTAL=1, UNABSORBED_INSULIN_COUNT=1,
  ACTION_REQUESTOR=pump"
    0: Timestamp: 7/1/06 08:26:55
    1: Bolus Type:
    2: Bolus Volume Selected (U):
    3: Bolus Volume Delivered (U):
    4: Programmed Bolus Duration (hh:mm:ss):
    5: BWZ Estimate (U): 9.0
    6: BWZ Target High BG (mg/dL): 100
    7: BWZ Target Low BG (mg/dL): 100
    8: BWZ Carb Ratio (grams): 10
    9: BWZ Insulin Sensitivity (mg/dL): 50
    10: BWZ Carb Input (grams): 1
    11: BWZ BG Input (mg/dL): 599
    12: BWZ Correction Estimate (U): 9.9
    13: BWZ Food Estimate (U): 0.1
    14: BWZ Active Insulin (U): 1.0
    15: Raw-Type: BolusWizardBolusEstimate
    16: Raw-Values: "BG_INPUT=599 && BG_UNITS=mg dl && CARB_INPUT=1 && CARB_UNITS=grams && CARB_RATIO=10 && INSULIN_SENSITIVITY=50 && BG_TARGET_LOW=100 && BG_TARGET_HIGH=100 && BOLUS_ESTIMATE=9 && CORRECTION_ESTIMATE=9.9 && FOOD_ESTIMATE=0.1 && UNABSORBED_INSULIN_TOTAL=1 && UNABSORBED_INSULIN_COUNT=1 && ACTION_REQUESTOR=pump"

7/1/06 08:26:55 BolusNormal
  "AMOUNT=9, CONCENTRATION=null, PROGRAMMED_AMOUNT=9, ACTION_REQUESTOR=pump,
  ENABLE=false, IS_DUAL_COMPONENT=false, UNABSORBED_INSULIN_TOTAL=null"
    0: Timestamp: 7/1/06 08:26:55
    1: Bolus Type: Normal
    2: Bolus Volume Selected (U): 9.0
    3: Bolus Volume Delivered (U): 9.0
    4: Programmed Bolus Duration (hh:mm:ss):
    5: BWZ Estimate (U):
    6: BWZ Target High BG (mg/dL):
    7: BWZ Target Low BG (mg/dL):
    8: BWZ Carb Ratio (grams):
    9: BWZ Insulin Sensitivity (mg/dL):
    10: BWZ Carb Input (grams):
    11: BWZ BG Input (mg/dL):
    12: BWZ Correction Estimate (U):
    13: BWZ Food Estimate (U):
    14: BWZ Active Insulin (U):
    15: Raw-Type: BolusNormal
    16: Raw-Values: "AMOUNT=9 && CONCENTRATION=null && PROGRAMMED_AMOUNT=9 && ACTION_REQUESTOR=pump && ENABLE=false && IS_DUAL_COMPONENT=false && UNABSORBED_INSULIN_TOTAL=null"

7/1/06 08:26:55 UnabsorbedInsulin
  "BOLUS_ESTIMATE_DATUM=9773719097, INDEX=0, AMOUNT=1, RECORD_AGE=3,
  INSULIN_TYPE=null, INSULIN_ACTION_CURVE=300"
    0: Timestamp: 7/1/06 08:26:55
    1: Bolus Type:
    2: Bolus Volume Selected (U):
    3: Bolus Volume Delivered (U):
    4: Programmed Bolus Duration (hh:mm:ss):
    5: BWZ Estimate (U):
    6: BWZ Target High BG (mg/dL):
    7: BWZ Target Low BG (mg/dL):
    8: BWZ Carb Ratio (grams):
    9: BWZ Insulin Sensitivity (mg/dL):
    10: BWZ Carb Input (grams):
    11: BWZ BG Input (mg/dL):
    12: BWZ Correction Estimate (U):
    13: BWZ Food Estimate (U):
    14: BWZ Active Insulin (U):
    15: Raw-Type: UnabsorbedInsulin
    16: Raw-Values: "BOLUS_ESTIMATE_DATUM=9773719097 && INDEX=0 && AMOUNT=1 && RECORD_AGE=3 && INSULIN_TYPE=null && INSULIN_ACTION_CURVE=300"


2006-07-01T08:26:55 6b
0000   0x6b 0xd8 0x28 0x01 0x06 0x5b 0x57 0x77    k.(..[Ww
0008   0xda 0x08 0x01 0x06 0x01 0x52 0x0a 0x32    .....R.2
0010   0x64 0x63 0x01 0x00 0x00 0x0a 0x00 0x5a    dc.....Z
0018   0x64 0x5c 0x05 0x28 0x03 0x44 0x01 0x5a    d\.(.D.Z
0020   0x5a 0x00                                  Z.




```


## 2006-07-01T08:36:21 64

match with our binary records

```

7/1/06 08:36:21,,,,,,,,,,,ChangeSuspendEnable,"ENABLE=user_suspend, PRE_ENABLE=null"
7/1/06 08:36:21 ChangeSuspendEnable
  "ENABLE=user_suspend, ACTION_REQUESTOR=rf_diagnostic, PRE_ENABLE=null"
    0: Timestamp: 7/1/06 08:36:21
    1: Bolus Type:
    2: Bolus Volume Selected (U):
    3: Bolus Volume Delivered (U):
    4: Programmed Bolus Duration (hh:mm:ss):
    5: BWZ Estimate (U):
    6: BWZ Target High BG (mg/dL):
    7: BWZ Target Low BG (mg/dL):
    8: BWZ Carb Ratio (grams):
    9: BWZ Insulin Sensitivity (mg/dL):
    10: BWZ Carb Input (grams):
    11: BWZ BG Input (mg/dL):
    12: BWZ Correction Estimate (U):
    13: BWZ Food Estimate (U):
    14: BWZ Active Insulin (U):
    15: Raw-Type: ChangeSuspendEnable
    16: Raw-Values: "ENABLE=user_suspend && ACTION_REQUESTOR=rf_diagnostic && PRE_ENABLE=null"


2006-07-01T08:36:21 1e
0000   0x1e 0x00                                  ..

hmm... my csv runs out
we know the previous event is only two bytes though, [0x1e 0x00]

2006-07-01T08:36:43 1f
0000   0x1f 0x00                                  ..

```

## rest of data

```
logs/ReadHistoryData-page-1.data: 49 records

2011-06-01T05:06:33 07
0000   0x07 0x00 0x00 0x04 0x52 0x61 0x86 0x6c    ....Ra.l
2011-08-12T00:36:16 64
0000   0x64 0x57 0x03 0x00 0x00 0x04 0x52 0x02    dW....R.
0008   0xc2 0x40 0x01 0x90 0x24 0x00 0x0b 0x01    .@..$...
2006-07-02T18:29:32 01
0000   0x01 0x64 0x59 0x00 0x00 0x00 0x03 0x02    .dY.....
0008   0x00 0x01 0x00 0x1e 0x00                   .....
2006-07-02T18:30:24 1f
0000   0x1f 0x00                                  ..
2006-07-02T18:37:23 1e
0000   0x1e 0x00                                  ..
2006-07-02T18:37:41 1f
0000   0x1f 0x00                                  ..
2006-07-02T18:57:35 1e
0000   0x1e 0x00                                  ..
2006-07-02T18:58:58 1f
0000   0x1f 0x00                                  ..
2006-07-03T10:00:14 07
0000   0x07 0x00 0x00 0x03 0x32 0x62 0x86 0x6c    ....2b.l
0008   0x62 0x86 0x05 0x0c 0x00 0xe8 0x00 0x00    b.......
0010   0x00 0x00 0x03 0x32 0x03 0x32 0x64 0x00    ...2.2d.
0018   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0020   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0028   0x00 0x00 0x00 0x00 0x00 0x1e 0x00         .......
2006-07-03T10:00:32 1f
0000   0x1f 0x00                                  ..
2006-07-06T15:12:00 07
0000   0x07 0x00 0x00 0x03 0x36 0x63 0x86 0x6c    ....6c.l
0008   0x63 0x86 0x05 0x0c 0x00 0xe8 0x00 0x00    c.......
0010   0x00 0x00 0x03 0x36 0x03 0x36 0x64 0x00    ...6.6d.
0018   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0020   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0028   0x00 0x00 0x00 0x00 0x00 0x07 0x00 0x00    ........
0030   0x03 0x36 0x64 0x86 0x6c 0x64 0x86 0x05    .6d.ld..
0038   0x0c 0x00 0xe8 0x00 0x00 0x00 0x00 0x03    ........
0040   0x36 0x03 0x36 0x64 0x00 0x00 0x00 0x00    6.6d....
0048   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0050   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0058   0x00 0x00 0x07 0x00 0x00 0x03 0x36 0x65    ......6e
0060   0x86 0x6c 0x65 0x86 0x05 0x0c 0x00 0xe8    .le.....
0068   0x00 0x00 0x00 0x00 0x03 0x36 0x03 0x36    .....6.6
0070   0x64 0x00 0x00 0x00 0x00 0x00 0x00 0x00    d.......
0078   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0080   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x34    .......4
0088   0xc8                                       .
2006-07-07T02:30:01 07
0000   0x07 0x00 0x00 0x03 0x36 0x66 0x86 0x6c    ....6f.l
0008   0x66 0x86 0x05 0x0c 0x00 0xe8 0x00 0x00    f.......
0010   0x00 0x00 0x03 0x36 0x03 0x36 0x64 0x00    ...6.6d.
0018   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0020   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0028   0x00 0x00 0x00 0x00 0x00 0x34 0x64         .....4d
2006-07-07T15:05:03 5b
0000   0x5b 0x75 0x43 0xc5 0x0f 0x07 0x06 0x03    [uC.....
0008   0x50 0x0a 0x32 0x64 0x03 0x03 0x00 0x00    P.2d....
0010   0x00 0x00 0x06 0x64 0x01 0x06 0x06 0x00    ...d....
2006-07-07T16:14:05 5b
0000   0x5b 0x75 0x45 0xce 0x10 0x07 0x06 0x06    [uE.....
0008   0x50 0x0a 0x32 0x64 0x03 0x06 0x00 0x00    P.2d....
0010   0x05 0x00 0x06 0x64 0x5c 0x05 0x18 0x47    ...d\..G
2006-07-07T16:47:57 45
0000   0x45 0xce 0x30 0x07 0x06 0x21 0x00         E.0..!.
2003-12-06T07:48:48 03
0000   0x03 0x00 0x00 0x00 0x13 0x74 0xf0 0x30    .....t.0
0008   0x07 0x06                                  ..
2003-12-06T07:16:49 4c
0000   0x4c                                       L
2006-07-07T17:10:38 00
0000   0x00 0x03 0x00 0x03                        ....
2006-07-07T17:28:51 03
0000   0x03 0x00 0x03 0x00 0x03 0x73 0xdc 0x11    .....s..
0008   0x07                                       .
2006-07-07T17:41:14 03
0000   0x03 0x4e 0xe9 0x11 0x07                   .N...
2006-07-07T17:57:02 03
0000   0x03 0x42 0xf9 0x11 0x07                   .B...
2006-07-07T18:02:05 03
0000   0x03 0x45 0xc2 0x12 0x07                   .E...
2006-07-07T18:22:51 12
0000   0x12 0x47 0x06 0x1f 0x00                   .G...
2006-07-08T05:22:49 07
0000   0x07 0x00 0x00 0x03 0x64 0x67 0x86 0x6c    ....dg.l
0008   0x67 0x86 0x05 0x00 0x75 0x75 0x75 0x05    g...uuu.
0010   0x00 0x00 0x03 0x64 0x03 0x34 0x5e 0x00    ...d.4^.
0018   0x30 0x06 0x00 0x09 0x00 0x30 0x06 0x00    0....0..
0020   0x24 0x4b 0x00 0x0c 0x19 0x00 0x00 0x00    $K......
0028   0x02 0x01 0x00 0x01 0x00 0x03 0x00 0x03    ........
0030   0x00 0x03                                  ..
2006-07-08T05:49:07 1e
0000   0x1e 0x00                                  ..
2006-07-08T05:49:26 1f
0000   0x1f 0x00                                  ..
2006-07-08T07:11:37 64
0000   0x64 0x00                                  d.
2006-07-08T07:12:12 17
0000   0x17 0x00                                  ..
2006-08-15T23:30:00 18
0000   0x18 0x00                                  ..
2006-08-15T23:33:28 07
0000   0x07 0x00 0x00 0x00 0x58 0x68 0x86 0x6c    ....Xh.l
0008   0x68 0x86 0x05 0x0c 0x00 0xe8 0x00 0x00    h.......
0010   0x00 0x00 0x00 0x58 0x00 0x58 0x64 0x00    ...X.Xd.
0018   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0020   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0028   0x00 0x00 0x00 0x00 0x00 0x03 0x00 0x03    ........
0030   0x00 0x03                                  ..
2006-08-15T23:33:54 03
0000   0x03 0x00 0x05 0x00 0x05 0xb6 0x21 0x17    ......!.
0008   0x1f                                       .
2006-08-15T23:34:28 03
0000   0x03 0x9c 0x22 0x17 0x1f                   .."..
2012-06-05T06:31:44 06
0000   0x06 0x9f 0x06                             ...
2006-09-01T00:12:41 00
0000   0x00 0xe8 0x00 0x00 0x00 0x00 0x00 0x06    ........
0008   0x00 0x06 0x64 0x00 0x00 0x00 0x00 0x00    ..d.....
0010   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0018   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0020   0x00 0x03 0x00 0x03 0x00 0x03              ......
2006-09-01T00:44:29 1e
0000   0x1e 0x00                                  ..
2006-09-01T00:44:48 1f
0000   0x1f 0x00                                  ..
2006-09-01T01:19:10 64
0000   0x64 0x00                                  d.
2006-09-01T01:19:34 17
0000   0x17 0x00                                  ..
2006-10-01T11:20:00 18
0000   0x18 0x00                                  ..
2006-10-01T11:30:18 07
0000   0x07 0x00 0x00 0x00 0x02 0x81 0x86 0x6c    .......l
0008   0x81 0x86 0x05 0x0c 0x00 0xe8 0x00 0x00    ........
0010   0x00 0x00 0x00 0x02 0x00 0x02 0x64 0x00    ......d.
0018   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0020   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0028   0x00 0x00 0x00 0x00 0x00 0x03 0x00 0x03    ........
0030   0x00 0x03                                  ..
2012-06-05T06:33:44 07
0000   0x07 0x00 0x00 0x02 0x4c 0xa1 0x06         ....L..
2006-10-02T19:45:47 00
0000   0x00 0xe8 0x00 0x00 0x00 0x00 0x02 0x4c    .......L
0008   0x02 0x4c 0x64 0x00 0x00 0x00 0x00 0x00    .Ld.....
0010   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0018   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0020   0x00 0x34 0xc8                             .4.
2012-06-05T06:34:44 07
0000   0x07 0x00 0x00 0x03 0x36 0xa2 0x06         ....6..
2006-10-03T13:09:13 00
0000   0x00 0xe8 0x00 0x00 0x00 0x00 0x03 0x36    .......6
0008   0x03 0x36 0x64 0x00 0x00 0x00 0x00 0x00    .6d.....
0010   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0018   0x00 0x00 0x00 0x00 0x00 0x00 0x00 0x00    ........
0020   0x00 0x34 0x64                             .4d
```
