Anomalies
MTCNN() didn’t detect a face in:
00561.jpg
01148.jpg
01518.jpg
03469.jpg
03888.jpg
06398.jpg


00119.jpg
00702
00661
00039
00683
04256
04062
03892
03859
03657
03500
03204
03194
03074
03039
02831
02830
02573
02511
02050
01863
01766
01721
01589
01417
01416
01415
01414
01412
01407
01406
01067
00728
07897
07896
07889
07097
06881
06700
06699
06396
06283
05968
05950
05949
05948
05935
05601
05502
05463
05462
05461
05460
05096
04594
04561
04273
04269
07898
07904
08274
08320
08450
09903
Problem: Black grid for the box negative coordinates
Solution: I set x/y to 0 and decreased width/height accordingly.


00573.jpg
00577
07214
Problem: There was a picture / a second person in the image and its coordinates were taken as the subject’s coordinates.

Solution: We can pick the largest face box.


03887.jpg
05113
Problem: One eye/picture was detected as the only face in the image.
No Solution!


02637.jpg
00893.jpg
00845.jpg
00837.jpg
00527.jpg
00048.jpg
Closed-Eyes Frames Problem
Maybe no problem, cause it’s like they blinked for a fraction of second and before and after that the gaze was pointed at… After all the original paper also used these frames. Frames like

01023.jpg
08957
03800
Averted-look Problem
In some frames, the person is somehow clearly looking away from the screen, but we still have a gaze coordinate and these are not some rare frames.
