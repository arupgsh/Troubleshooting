
## R studio server "address already in use" fix

Kill the process associated with 8787 port and restart the server.

Source: https://stackoverflow.com/questions/31081426/initctl-unknown-instance-error-after-rstudio-conf-change/32851419#32851419
Original source: https://support.rstudio.com/hc/communities/public/questions/201681013-Rstudio-V0-98-1028-spawning-port-error

1) check the process that used 8787

sudo fuser 8787/tcp

2) with the -k option to kill all process.

sudo fuser -k 8787/tcp

3) Start RStudio Server

sudo rstudio-server start

The solution above is provided here by Leon Zhang.
