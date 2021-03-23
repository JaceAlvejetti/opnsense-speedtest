# opnsense-speedtest
speedtest plugin for OPNsense

## install
```
sudo pkg install -y libidn2
sudo pkg add https://github.com/mihakralj/opnsense-speedtest/raw/main/work/pkg/os-speedtest-devel-0.6_2.txz
```

## remove
`sudo pkg delete os-speedtest-devel`

### Version 0.6
- we are back with embedded binary copy of speedtest...

### Version 0.5
- removed local binary copy of speedtest - needs to be installed separately
- cleanup, copyright notices, getting ready for a pull request to main OPNsense/plugins repo

### Version 0.4
- better exception-handling logic
- widget for the dashboard
- moved the speedtest menu entry into the Reporting menu structure

### Version 0.3
- added log output at the bottom - with the export and delete actions
- cron job accepts the speedtest serverid as an argument to lock down the target for cron jobs

### Version 0.2
- enabled cron task - you can add it at System-Settings-Cron and add a new command `Run Speedtest`
- added the api call to execute the statistical test: `/api/speedtest/service/run`
- added the api call to get json with statistics: `/api/speedtest/service/stat`
- added the output to .csv file - all tests for statistics are inserted into `/usr/local/opnsense/scripts/OPNsense/speedtest/speedtest.csv`
- deleting `speedtest.csv` will zero-out statistics

### Version 0.1
Core diagnostics (socket test and http test)
