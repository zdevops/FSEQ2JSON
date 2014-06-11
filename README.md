FSEQ2JSON
=========

Sending your space delimited Sequential File as a JSON to a WebServer

# Use Case
So, your local systems programmers (or maybe you yourself) have written up some pretty neat code producing 
'management information' in a so-called Sequential File.

Suppose, for arguments' sake this data (resulting or intermediate) is stored in a space delimeted format like for example say a report on VOLUME USAGE (to be used in storage management reports).

As an example, it might look just like this (any likeliness to VOLSER-names used at your site is purely coincidental!)

    VOLSER VOLUME_TYPE USED_CYLS  FREE_CYLS
    SP1200 3390-1           1000       2390       
    SP1201 3390-1            500       2890
    
This list (dataset, sequential file) going on liek that....

