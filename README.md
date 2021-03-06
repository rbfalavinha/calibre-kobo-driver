**Looking for the `no-database` branch? It's gone now, the database code has been removed from `master` so this is the same as the old `no-database` branch.**

# Calibre driver for Kobo Touch/Glo/Mini
An extension of the existing KoboTouch driver provided with Calibre. This plugin allows modifying ePub files to enable 
extra Kobo features.

**Please note**: Modified books are not saved back into your Calibre library to prevent issues with overwriting library 
configurations unexpectedly, so books are processed in transit to your device every time. In most cases, the extra time 
required should not be noticeable.

#Installation
To install this plugin from source, you must create a ZIP file named `KoboTouchExtended.zip` and include these files:

1. \_\_init\_\_.py
1. container.py
1. driver.py
1. plugin-import-name-kobotouch\_extended.txt

To create the ZIP file:

1. Windows users can run the `create-plugin.ps1` script (requires that Powershell allow running unsigned scripts, which is not the default setting).
1. Linux and Mac OS X users can run the `create-plugin.sh` script (either grant it executable permissions first, or run `sh create-plugin.sh`).
1. Create an empty ZIP file and add the files noted above.
1. Select the files noted-above, right-click, and add the files to a new ZIP file. This may also be referred to as a "Compressed Folder" or only be available once you choose the "Archive" option, depending on your operating system.

Add the resulting ZIP file to calibre:

1. Preferences
1. Plugins
1. Load plugin from file

You may also shut down Calibre and run `calibre-customize -b /path/to/calibre-kobo-driver` from the command line to have calibre add the plugin itself.

# Usage
To use this plugin after installing:

1. Connect your Kobo Touch/Glo/Mini device and wait for it to be detected by calibre
1. Select the book(s) you want to send to your device.
1. Click the **Send to device** button.

# Reporting a Bug
Found a bug with this plugin? Great! Please use the Github issue tracker to send me reports of issues or questions. Under no circumstances should I be emailed directly unless I have asked to have something sent to me. Any emails I haven't asked for will be silently ignored. Everyone can benefit from a public bug tracker, but only one person benefits from a private email.

When submitting a bug, I require the following information as a minimum, but any additional information is good to include:

1. What version of calibre you are using. If you are not on the latet version I will require that you update before I accept any report.
1. The full error message reported by calibre.
1. For issues processing books, whether or not you have a book that you are able to send me that demonstrates the issue. Please be aware of any copyright restrictions that may prohibit sending me a book.

# Known Issues
If you have previously installed this plugin in calibre 0.9.18 or earlier, then you upgrade to calibre 0.9.19 or later and can't update the plugin, you must manually replace the plugin ZIP file:

1. Download the latest version of the code.
1. Generate a new plugin ZIP file. **Do not** use the `calibre-customize` method.
1. Shut down calibre entirely.
1. Open the calibre plugin directory.
	1. Don't know where this is? Before you close calibre, open calibre's preferences, choose **Miscellaneous**, and click the **Open calibre configuration directory** button. The plugin directory is in there.
1. Replace the file named **KoboTouchExtended.zip** with the new version you created. Please make sure the file name remains the same.
