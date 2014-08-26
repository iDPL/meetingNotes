Added Hailong to the calls and discussed next stage of Condor
Goal:  International Condor Pool by 2 Sept 2014 (Beihang, UCSD, Wisc, [CNIC if possible])

For Rocks deployment:  central server is http://central-x86-64.calit2.optiputer.net/isos
* updating Condor Roll to 8.2.2 (latest production release)
* updating perfSONAR roll with latest security updates for version 3.2.2

Different approaches to using Condor 
* US/Wisc are using the Condor Parallel Universe.  Example code uses netcat (nc) to set up a server and a client
* * regular testing via cron.  Working with Condor team to run under Condor's internal Cron
* * code is posted on github:  http://github.com/idpl/swtools
* Beihang using DAGMAN + Vanilla universe.  Also run a network performance test
* * have a web portal that they would like to test
* * Currently have ftp and wget as testing runs

International Pool
*  Simple at first, Single pool, at least one system per site. Condor Master in Wisconsin (komatsu.chtc.wisc.edu)
*  Ask Condor team about Flocking pools (more complicated, but more general)
*  Ask Condor team about submission from any node in the pool
*  Pool will be managed via IPv4, but v6 data placement tests should be supported. 
*  TODO: Phil to send email for detailed implementation

Next meeting: Sept 16 (UCSD)/Sept 17(Beijing)


