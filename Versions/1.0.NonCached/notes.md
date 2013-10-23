This version acts like this:

* It does not remember timestamps for checks values - all values for all checks will always be written to AppDynamics metric writer
* No StdOut debug statements
* Does not loop the process in memory - program starts up, executes and shuts down.