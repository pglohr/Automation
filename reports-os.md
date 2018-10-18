Create a report (text file) containing the list of IOS and NXOS host and there OS version

status [first version publisehd]
reports-os.yml is calling
 - reports/reports-ios2.yml to gather IOS facts
 - reports/reports-nxos2.yml to gather NXOS facts
 - reports/reports-os-version.yml to create report file
