# CSVtoTeamsChannels
I created these scripts to automatically setup Teams channels for groups of users on Microsoft Teams using the Teams API and Windows PowerShell. I use these scripts to setup group channels for my students on Microsoft Teams. 

## Prerequisites:
- Windows PowerShell 5.1 or higher to be installed on your machine. 
- Install Microsoft Teams PowerShell Module Preview version. You can check the latest version number at https://www.powershellgallery.com/packages/MicrosoftTeams/. Note that the version you need is ending with -preview (for advanced features). As of writing this guide, the latest preview version is 2.5.2-preview. To install it, open Windows PowerShell and type the following command: `Install-Module MicrosoftTeams -AllowPrerelease -RequiredVersion 2.5.2-preview`

## How to use the scripts:
- Connect to Microsoft Teams API using your username and password by typing the following command in Windows PowerShell: `Connect-MicrosoftTeams`
It takes some time for the login window to pop-up.
- Once logged-in, you can start executing the scripts as follows:
	- Add members to Teams
		- Populate the template CSV file provided (members.csv). Please note that the CSV file has a header row (do not change the first row). The first column corresponds to email addresses (must be registered users on Office365) and the second column corresponds to the Team name on Microsoft Teams (must have been created beforehand).
		- Open the script provided (addMembers.txt), update the path to the CSV file members.csv to match your local copy edited in the previous step, and copy the entire content of the script, then paste it onto Windows PowerShell and hit ENTER. The execution should take some time.
	- Create channels in Teams and add channel members
		- Populate the template CSV file provided (channels.csv). Please note that the CSV file does not have a header row. The first column corresponds to email addresses (must be registered users on Office365), the second column corresponds to the Team name on Microsoft Teams, and the third row is the channel name.
		- Open the script provided (addChannels.txt), update the path to the CSV file channels.csv to match your local copy edited in the previous step, and copy the entire content of the script, then paste the script onto Windows PowerShell and hit ENTER. The execution should take some time.
