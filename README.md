Still a work in progress;

financial tables f2 / f3 have some issues ; need to do some cleanup on the variables list. 

one variable (CNFNO4) for some reason not being found (exists in table being read).

The original notebook (make a master merge table of everything first) fails (hangs the kernel) after about 11 files merged.  (I find this peculiar?)  Appears to be a memory issue (thogh the fiels are not huge).  THe findmerge variant (not working fully yet as of 12/20) searches for variables of interest FIRST in each table one at a time as they are read, then with the results, attempts to build a merged dataframe with only the variables we want.  

