Debugging condor connection
* address in Beihang is 115.25.138.244
* Able to successfully ssh to 115.25.138.244 from murpa.rocksclusters.org 
* However, when making an ssh connection back to San Diego the real address is 219.239.227.19 
[phil@murpa ~]$ who
phil     pts/4        2014-09-16 19:27 (99-21-193-125.lightspeed.sndgca.sbcglobal.net)
phil     pts/5        2014-09-16 19:54 (219.239.227.195)

Adjusted firewall on Komatsu to accept 219.239.227.19 and adjusted condor config to allow 219.239.227.19. ssk beihang-> wisc
works. But still have a SECMAN error for condor
This may be due to the dual IP address nature of the Beihang machine. Need Condor Team consultation to figure out the issue
verified that the datamovementpoolpassword file was correct on both machines.

* Hailong and Luo Ze will investigate the networking at Beihang/CERNET to understand where the translation is occuring
* Condor team will downgrade komatsu from devel version 8.3.1 to production version 8.2.2 (which is running on the rest of iDPL
* 
Followup: From Hailong. "I justconfirmed with the staff from university network center. They do map our IP address into several external IP addresses dynamically when we are going outside. They will give us the range of the external IP addresses as soon as possible, so that you can add them to your firewall access control."

Next phone call: Sept 23 @ 7:00pm (San Diego), Sept 24 @ 10am (Beijing)


