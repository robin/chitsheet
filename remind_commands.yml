--- 
remind_commands: |-
  Remind (http://www.roaringpenguin.com/products/remind) is a
  sophisticated calendar and alarm program.
  
  Display TODAY's reminders. For a different day's reminders simply
  follow the rem command with the target date.
      $ rem
  
  Display reminders for some day that is NOT TODAY. For a future date
  replace n by the number of days in the future. For a past date
  replace the plus sign with a minus sign and replace n by the number
  of days in the past.
      $ remind ~/.reminders `(echo 'banner %'; echo 'msg
      [trigger(today()+n)]') | remind -`
  
  Generate a WEEKLY calendar in standard output
      $ remind -c+ ~/.reminders
  
  Generate a MONTHLY calendar in standard output
      $ remind -c ~/.reminders
  
  Generate a POSTSCRIPT version of the remind monthly calendar. Replace
  n with the number of months to display.
      $ remind -p1 ~/.reminders | rem2ps -c -ftshed LucidaGrande -sthd
      11 -se 9 -i -l -m A4 -or 72 -t 0.5 > ~/calendar.ps
  
  Generate and an HTML file of the remind monthly calendar. Replace
  n with the number of months to display.
      $ remind -p4 ~/.reminders | rem2html -b 1 -t 1 -se -1 > ~/cal.html
  
  Display Growl (http://growl.info/) notification of today's reminders
      $ remind ~/.reminders | growlnotify -t 'Reminders for today'
      --appIcon iCal -s
  
  Run remind as a background daemon and display reminders through
  Growl:
      $ nohup remind -z -k'osascript -e "beep"; growlnotify -n remind
      -a iCal -t Reminder -s -m %s &' ~/.reminders &
