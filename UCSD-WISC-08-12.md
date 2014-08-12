* Fixed partitionable slots on murpa (required hard restart of condor daemons). Quick test shows that is working.
* end submissions script to Nate to make the submission a "crondor" job. 
* Question about condor running in IPv6.   Need a different test system for disposable v6 testing.
* Issues on network performance from Wisc
** some paths work OK (eg. wisc border to chpc.utah.edu DMZ connection
** poor performance to nine.usc.edu (1g:  270Mbit wisc-->usc, 900Mbit usc--> wisc)
** Tom/Pat looking at building an AL2S path to remove I2 routing as a possible issue (basic viewability issue is
  that we can't see physical switches in AL3S (I2 routed path)
  
