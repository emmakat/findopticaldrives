## collection of things to help manage optical drives on ubuntu.

### A nice command which will tell you things about your optical drives:  

ls -l /dev/disk/by-id| grep sr[0-9]$|tr -s ' ' ' '|cut -d ' ' -f 9,11 |sort -k2|grep -e \^a -e \^u|sed 's#../..#/dev#'  
credit: https://ubuntuforums.org/showthread.php?t=2237670
![ls-s](https://github.com/emmakat/findopticaldrives/blob/master/ls-l.png)

### Another useful command:

lsblk -i -o kname,mountpoint,fstype,size,maj:min,name,state,rm,rota,ro,type,label,model,serial  
credit: https://serverfault.com/questions/190685/whats-the-best-way-to-get-info-about-currently-unmounted-drives
![lsblk](https://github.com/emmakat/findopticaldrives/blob/master/lsblk.png)
