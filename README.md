Still a work in progress;

# Notes
- financial tables f2 / f3 have some issues ; need to do some cleanup on the variables list. 
- one variable (CNFNO4) for some reason not being found (exists in table being read).
- The original notebook (make a master merge table of everything first) fails (hangs the kernel) after about 11 files merged.  (I find this peculiar?)  Appears to be a memory issue (thogh the fiels are not huge).  THe findmerge variant (not working fully yet as of 12/20) searches for variables of interest FIRST in each table one at a time as they are read, then with the results, attempts to build a merged dataframe with only the variables we want.  
- Many of the tables have two versions
    1. table.csv
    	- Initial submission of responses to IPEDS
    	- Happens at the end of the year; available the next year (usually)
    2. table_rv.csv
    	- This appears to be the version that IPEDS reviews a year after the first submission
    	- We should use this version if it is available (won't be available for the most recent year submission)
    	- Not every table gets changed/reviewed in which case there is only the initial table
