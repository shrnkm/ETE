## Anomalies

MTCNN() didn’t detect a face in.
|**00561.jpg**|**01148.jpg**|**01518.jpg**|
|-|-|-|
|**03469.jpg**|**03888.jpg**|**06398.jpg**|

<br/><br/>**Problem:** Black grid for the box negative coordinates<br/>
**Solution:** I set x/y to 0 and decreased width/height accordingly.
|**09903**|**08450**|**08320**|**08274**|**07904**|**07898**|**04269**|**04273**|
|-|-|-|-|-|-|-|-|
|**04561**|**04594**|**05096**|**05460**|**05461**|**05462**|**05463**|**05502**|
|**05601**|**05935**|**05948**|**05949**|**05950**|**05968**|**06283**|**06396**|
|**06699**|**06700**|**06881**|**07097**|**07889**|**07896**|**07897**|**00728**|
|**01067**|**01406**|**01407**|**01412**|**01414**|**01415**|**01416**|**01417**|
|**01589**|**01721**|**01766**|**01863**|**02050**|**02511**|**02573**|**02830**|
|**02831**|**03039**|**03074**|**03194**|**03204**|**03500**|**03657**|**03859**|
|**03892**|**04062**|**04256**|**00683**|**00039**|**00661**|**00702**|**00119**|


<br/><br/>**Problem:** There was a picture / a second person in the image and its coordinates were taken as the subject’s coordinates.<br/>
**Solution:** We can pick the largest face box.
|**00573**|**00577**|**07214**|
|-|-|-|

<br/><br/>**Problem:** One eye/picture was detected as the only face in the image.<br/>
No Solution!
|**03887**|**05113**|
|-|-|


<br/><br/>**Closed-Eyes Frames Problem**<br/>
Maybe no problem, cause it’s like they blinked for a fraction of second and before and after that the gaze was pointed at… After all the original paper also used these frames. Frames like:
|**02637**|**00893**|**00845**|
|-|-|-|
|**00837**|**00527**|**00048**|


<br/><br/>**Averted-look Problem**<br/>
In some frames, the person is somehow clearly looking away from the screen, but we still have a gaze coordinate and these are not some rare frames.
|**01023**|**08957**|**03800**|
|-|-|-|

