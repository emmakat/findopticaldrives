## collection of things to help manage optical drives on ubuntu.

finder.txt has a nice command which will tell you things about your optical drives:  

ls -l /dev/disk/by-id| grep sr[0-9]$|tr -s ' ' ' '|cut -d ' ' -f 9,11 |sort -k2|grep -e \^a -e \^u|sed 's#../..#/dev#'
credit: https://ubuntuforums.org/showthread.php?t=2237670
