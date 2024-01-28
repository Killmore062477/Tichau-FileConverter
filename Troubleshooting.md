## Report an Issue

You can report an issue on the [bug tracker](https://github.com/Tichau/FileConverter/issues).

When you report an issue, please join the following informations:

* Registry.xml
* Settings.user.xml
* The Diagnostics folder of the session that encountered the issue.
* A screenshot (if possible) and a description that shows/explain the issue.

You will find the xml files and diagnostics folder in `c:\Users\[UserName]\AppData\Local\FileConverter\`.

## Known Issues

### Installer failed to succeed
Maybe you don't have Microsoft .NET Framework 4.5 installed on your PC. You can download the installer [here](https://www.microsoft.com/download/details.aspx?id=30653).

### Incompatibility with Avast antivirus [<v1.0]
An incompatibility has been found with Avast antivirus program. When the Avast file watcher is activated, file converter cannot be launch and freeze the window explorer. To fix that issue you need to deactivate the file watcher or uninstall Avast. No other workaround has been found for now.

This issue is fixed since version 1.0.