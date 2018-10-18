Create a report (text file) containing the list and status of IOS and NXOS interface

status [ongoing]
reports-interface.yml is calling
 - reports/reports-ios2.yml to gather IOS facts
 - reports/reports-nxos2.yml to gather NXOS facts
 - reports/reports-interface-status.yml to create report file based on a jinja2 template
