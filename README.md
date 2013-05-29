puppet-ls 
======


This script is helping you to figure out whether particular file or directory is managed by puppet or not.  

### USAGE
**puppet-ls [-r [-d N]]  [-i] [file1, directory2, fileN]**

### OPTIONS
**-r, --recursive**     find all files recursively      
**-d, --depth**         specify the depth during recursion      
**-i, --invert-match**  invert results, means print what is not managed by puppet    
**-h, --help**          print help and exit    

### EXAMPLES

print all files managed by puppet from directory /etc with depth 1:     
`puppet-ls -r -d 1 /etc`     

print all files which arn't managed by puppet in /etc/cron.d:     
`puppet-ls -r -i /etc/cron.d`     

print all files from list which are mananged by puppet:    
`puppet-ls /etc/motd.conf /etc/init.d/syslog-ng /etc/sysconfig/network`

### EXIT STATUS 
**0** - if found at least one file     
**1** - if nothing found