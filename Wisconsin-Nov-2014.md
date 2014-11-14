Experiment Components  (A single "script" from Condor's viewpoint, called it the placement script)
  * Local file system test
  * Point-to-point network test (iperf, nuttcp)
  * Data placement experiment (end-to-end)
  
Some failure cases:
  *  kill an instance of a recurring job after N minutes, reschedule at next regular interval
  *  Place on hold, if job fails K times in a row. 
  *  Failure/Success of placement script reported by instance 0
  
Need ability to replace a repetitive test (especially if placement script is changed)
  
Need to work with condor team to understand how to use condor_chirp to place information in the job log.

Job log should be parsed (condor has a library), to extract experiment results (success/failure, MB/s, total time, etc)

Development configuration of the pool
 * Each site will configure 4 slots (Beihang, CNIC, UCSD, UWISC)
 * A schedd at each site, will handle the scheduling of the named dedicated slots (this pushes strong user authentication to be solved as future problem)
 * Effectively creates 4 independently-scheduled pools on the same physical pool. Can result in performance collisions. 
 
