# Notion.so
![Alt text](https://github.com/pocketvince/Notion.so/blob/main/notion.gif?raw=true "notion")

Script to add tasks on Notion in command line

## Installation
Download the script and place it in /bin/notion

## Usage

```shell
root@pocketvince:~# notion LMP Test Todo
```
## Automate your recurring tasks
To automate your tasks by day (Monday, Tuesday...), first day of the month, the middle of the month,... You can make a basic shell script and add it on crontab and ask for execution every day.

## Contributing

Readme generator: https://www.makeareadme.com/

Notion API: https://developers.notion.com

Inspiration "Micode - Cette appli va BOULEVERSER votre vie": https://www.youtube.com/watch?v=LN9n2vGkZyQ

## Extra info
The fight of the century:
My "sense of time" vs "daily tasks."

I often mix up the days, so I've started to complete an agenda in Teams;
But, did I already do this task or not?
What was the new topic?
,...

With notion, I can make quick notes in meetings, or at the coffee break write small reminders that I can edit/delete/complete from my tablet, smartphone, work computer or personal computer... For my private or professional life;
The new problem is to remember to write down what I have to do😐

the first step was to make a script to complete a task via my terminal
the 2nd step was to make a script and add it on crontab 😌

Example: sorry 🇫🇷

```shell
root@pocketvince:~# cat notion/todo_notion.sh 
#!/bin/bash
#définition date
lejour=`date +%d`
lemois=`date +%m`
lannee=`date +%Y`
jourchiffre=$(date +%u)
#définition jour
lundi=1
mardi=2
mercredi=3
jeudi=4
vendredi=5
samedi=6
dimanche=7
premierjourdumois=01
findumois=15
###Lundi
if [ "$jourchiffre" == "$lundi" ]; then
notion LMP "💾 ### Slide" Todo
notion REP "📨 Data ###" Todo
notion LUM "💾 Check SFTP" Todo
notion LMP "📨 ###" Todo
notion LUM "💾 Backup ###" Todo
notion Private "💊 ###" Todo
notion LMP "📨 ###" Todo
notion LMP "📨 ###" Todo
#notion LMP "📨 ### B2B" Todo
notion LUM "📨 ###" Todo
#notion DPG "💾 PBI" Todo
notion LUM "💾 PBI" Todo
notion LMP "💾 PBI" Todo
notion LMP "💾 Creation WBR" Todo
notion LMP "📨 Operation Contact Center Results" Todo
notion LUM "📨 Cases Closed" Todo
notion LUM "📨 Cases Closed ###" Todo
notion LMP "📨 ### Results" Todo
notion REP "📞 Standup" Meeting
notion LMP "📨 ### Contact Status" Todo
notion LMP "💾 Preparation KPI" Todo
notion LMP "💾 Heure ###" Todo
notion LUM "💾 Update Status" Todo
notion LMP "💾 Individual Results" Todo
else
    echo "Lundi: NOK"
fi
###Mardi
if [ "$jourchiffre" == "$mardi" ]; then
notion REP "📨 Data ###" Todo
notion LUM "💾 Check SFTP" Todo
notion LMP "📨 ###" Todo
notion LUM "💾 Backup ###" Todo
notion Private "💊 ###" Todo
notion LUM "📨 ###" Todo
#notion DPG "💾 PBI" Todo
notion LUM "💾 PBI" Todo
notion LMP "💾 PBI" Todo
notion LMP "📨 Send WBR" Todo
notion REP "📞 Standup" Meeting
notion LMP "📞 Tactical" Meeting
notion LMP "💾 Individual Results" Todo
else
    echo "Mardi: NOK"
fi
###Mercredi
if [ "$jourchiffre" == "$mercredi" ]; then
notion REP "📨 Data ###" Todo
notion LUM "💾 Check SFTP" Todo
notion Private "💊 ###" Todo
notion LMP "📨 ###" Todo
notion LUM "💾 Backup ###" Todo
notion LUM "📨 Dapcom" Todo
notion LUM "###" Todo
#notion DPG "💾 PBI" Todo
notion LUM "💾 PBI" Todo
notion LMP "💾 PBI" Todo
notion REP "📞 Standup" Meeting
notion LMP "💾 Individual Results" Todo
else
    echo "Mercredi: NOK"
fi
###Jeudi
if [ "$jourchiffre" == "$jeudi" ]; then
notion REP "📨 Data ###" Todo
notion LUM "💾 Check SFTP" Todo
notion Private "💊 ###" Todo
notion LUM "📨 ###" Todo
notion LMP "📨 ###" Todo
notion LUM "💾 Backup ###" Todo
#notion DPG "💾 PBI" Todo
notion LUM "💾 PBI" Todo
notion LMP "💾 PBI" Todo
notion REP "📞 Standup" Meeting
notion LMP "📞 Weekly" Meeting
notion LMP "💾 Individual Results" Todo
notion LUM "💾 Update A-###" Todo
else
    echo "Jeudi: NOK"
fi
###Vendredi
if [ "$jourchiffre" == "$vendredi" ]; then
notion Private "💊 ###" Todo
#notion REP "📨 Data ###" Todo
#notion LUM "💾 Check SFTP" Todo
#notion LUM "📨 ###" Todo
#notion LMP "📨 ###" Todo
#notion DPG "💾 PBI" Todo
#notion LUM "💾 Backup ###" Todo
#notion LUM "💾 PBI" Todo
#notion LMP "💾 PBI" Todo
#notion REP "💾 Update ###" Todo
#notion REP "📞 Standup" Meeting
#notion LMP "💾 Individual Results" Todo
else
    echo "Vendredi: NOK"
fi
###Samedi
if [ "$jourchiffre" == "$samedi" ]; then
notion Private "💊 ###" Todo
else
    echo "Samedi: NOK"
fi
###Dimanche
if [ "$jourchiffre" == "$dimanche" ]; then
notion Private "💊 ###" Todo
else
    echo "Dimanche: NOK"
fi
###Premier jour du mois
if [ "$lejour" == "$premierjourdumois" ]; then
notion LMP "💾 ### Slide" Todo
notion LUM "💾 Changer Filtre" Todo
notion Private "💊 ###" Todo
notion LMP "💾 ### Slide" Todo
notion Private "💳 Loyer" Todo
notion LMP "📨 ###" Todo
notion LUM "💾 Creation Template Dapcom" Todo
notion LUM "💾 Billing" Todo
notion LUM "📨 Request Forecast" Todo
notion LMP "📨 Request Forecast" Todo
notion LMP "📨 ###-FULLMONTH" Todo
notion LMP "📨 ### B2B-FULLMONTH" Todo
notion LMP "💾 Creation MBR" Todo
notion LMP "📨 Operation Contact Center Results" Todo
notion LUM "📨 Cases Closed" Todo
notion LUM "📨 Cases Closed ###" Todo
notion LMP "📨 ### Results" Todo
notion LMP "📨 Outbound Contact Status" Todo
notion LMP "💾 Preparation KPI" Todo
notion LMP "💾 Heure ###" Todo
notion LUM "💾 Update SFTP" Todo
notion LMP "💾 Connexion SF" Todo
notion LUM "### Filtre" Todo
else
    echo "Premier jour du mois: NOK"
fi
###Fin du mois
if [ "$lejour" == "$findumois" ]; then
notion LMP "💾 ###" Todo
notion LUM "💾 Update SFTP" Todo
notion Private "💊 ###" Todo
notion LUM "### Filtre" Todo
else
    echo "Fin du mois: NOK"
fi
```
