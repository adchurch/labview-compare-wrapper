## Overview
This repository contains a shell script which can be used to launch LabVIEW Compare from a Source Code Management tool. This script has been used specifically with [Atlassian's SourceTree SCM tool](https://www.sourcetreeapp.com/). A wrapper script is necessary to convert path strings provided by the SCM tool into a format compatible with LabVIEW Compare.

This script was originally obtained from this LAVA forum discussion: [Configuring Git to work with LVCompare and LVMerge](https://lavag.org/topic/17934-configuring-git-to-work-with-lvcompare-and-lvmerge/#entry108533).

## Installation Instructions
1. Place **_LVCompareWrapper.sh** in *C:\Users\admin*. 
2. In SourceTree, open **Tools>>Options** from the menu bar and select the **Diff** tab. 
3. Under **External Diff/Merge** change the **External Diff Tool** selection to **Custom**. 
4. Enter the path to **_LVCompareWrapper.sh** in the **Diff Command** field. If using the default paths this would be: 
       C:\Users\admin\_LVCompareWrapper.sh
5. In the **Arguments** field enter the string below and click OK. 
       $LOCAL $REMOTE
       
## Usage Instructions
1. Open a repository in SourceTree and locate a commit containing a changed LabVIEW .vi file. 
2. Select the **.vi file** you wish to perform a diff on within the **Log/History** view.
3. Select **Actions>>External Diff** from the menu bar. 
4. LVCompare should open automatically and perform a diff between version of the .vi in the commit and the version it replaces. 