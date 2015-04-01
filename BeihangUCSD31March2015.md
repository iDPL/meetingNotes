* dates for visit to China
   20th of June is Holiday
   Checking week july 13, 20, 27.
   Hailong will send email.
* Try to use a different email reflector for Git Notifications  (Maybe Azure/Microsoft)
* log rotation  (nothing special in Condor)
   Beihang figured out how to read rotated log files.
   (Add Experiment name to log file)
* should implement "Absent" ads (Greg Thain has Configuration) 
From Greg's Email
We can have all the events written to the global event log.  To enable this, on the submit machine,  set

EVENT_LOG = path_to_log_file
EVENT_LOG_MAX_SIZE = size_in_bytes_of_one_log_file_before_rotation
EVENT_LOG_MAX_ROTATIONS = number_of_rotated_log_files

All the events from every job in the schedd will be sent to this file and rotated.

There's no current way to put GMT into the event logs, let me file a bug report, and we'll get this fixed.

To detect AWOL nodes, we can use the absent ads feature of HTCondor:

COLLECTOR_PERSISTENT_AD_LOG = some_file
ABSENT_REQUIREMENTS = true
EXPIRE_INVALIDATED_ADS = true

TOdo List:
     * move generic DataMover code to regular testing with actual file movement
     * Put test files in place (Beihang has completed,  CNIC, Wisc, UCSD to complete).
     * Jarvis, Allen  to figure out a simple mechanism to replicate log files.
     * Phil Hiring an undergrad.
     
  Next Skype Meeting:   21st April (7pm California, 22nd April 10AM Beijing).
  
