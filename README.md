There are several items in this directory:

- ManifestFiles.zip
- E-R Diagrams
- AndrosecData.sqlite

These are described below:


# ManifestFiles.zip
This directory contains AndroidManifest files for all recorded commits from open source Android applications stored on the F-Droid website.

Each folder in the top level directory represents a different app. For example, the directory 'aarddict.android' represents one Android app. More information about each app including its name, and website may found in the .sqlite database file which may be downloaded from this research project's repository using information from the "name" column in the appData table. 

Inside of each folder, all commits made to the project where the AndroidManifest.xml file was altered are stored. Correlating information for each of these commits may be found in in the .sqlite database in the "Android_Manifest_CommitInfo" table in the "commit_val" column. The AndroidManifest.xml file may be found inside of this commit directory.

# E-R Diagrams
Contains E-R Digrams for the AndroSecData.sqlite DB




# AndrosecData.sqlite

This contains the SQLite database containing the following tables:


AndroRiskRun: Information used by tools for analysis

AppData: Information pertaining to the overall app being examined including name, category and source code location.

CodingStandard: Various results returned from SonarCube. For more information on these results, please see the SonarCube website: http://docs.sonarqube.org/display/SONAR/Metric+definitions

GitHistory: Commit history recorded from the GIT version control systems for each app.

Intent: A listing of intents

Intent_version: A listing of intents for each version. IntentID relates to Intent.IntentID while versionID relates to version.VersionID

Permission: Contains list of recorded permission names

OverPermission: A join table for listing the over permissions for each app. VersionID relates to Version.VersionID, while PermissionID relates to Permission.PermissionID

SonarRun: Used only for analysis tool.

UnderPermission: Contains information of underpermissions for each app. PermissionID relates to Permission.PermissionID, while versionID relates to version.versionID

Version: Contains information about each application version. AppID relates to appdata.appID

Vulnerability: Contains risk rating for app from AndroRisk. VersionID relates to version.VersionID
