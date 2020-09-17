# *METRICITY* - CoderSchool FTW Final Capstone Project
### Created with love by: Khoa Dam
### View online at: https://damanhkhoa.com
### [Watch the Demo](https://www.loom.com/share/3b1f0ba0f5b64d8889742f77fb74426a)

![Screenshot](https://github.com/kyakaze/Metricity-backend/blob/master/screenshot.png)


## Test info:
- email: **test@gmail.com**
- password: **foobar**
- [sample csv file to import](https://www.dropbox.com/s/tv2dfn647so9ypz/avocadodate.csv?dl=0)


## Notes: 
 - App was not maintained at all.
 - Some functionalities (especially emails) stop working since the app was made long time ago without maintenance. 
 - App is deployed to a free dyno on heroku and there's a limitation on the number of record in the database (10k rows). Hence, users cannot import more files.
 - Speed is super slow since it takes 30 seconds for free dyno to wake up.
 - Lazy to deploy to my vps since I've gotta fix environments and cronjobs

## Current features:
 - User can create an account and login/logout  with Facebook or Metricity system.
 - User can create their own: 
      - tags
      - metrics (name, and value) which belong to a specific tag
      - assignee's email belongs to a specify metric

 - User can submit new value for each metric in a given form base on user's selection of tag and metric
 - User can also import from their csv files to the database
  
 - User can see the data for each tag in 2 ways :
      - Table
      - Chart Widgets (currently supports Line, bar and pie chart for "date" base data)

 - Shareable Charts feature: User can share their charts to other people using a token. User could be able to copy or delete those links easily  
 - Send an email (with a token form) to request data input for each metric from co-worker,  each token form can be used only once, if used, the token will be deleted and not usable.
 - Reminder email : User can set a reminder rule to send email for each metric. A rule can be any day (or mon - fri) and hour in a week.

####  For Table view mode:
- User can choose a specific tag and click to view a table contains value of metrics belong to that tag
- User can also filter wich column he wants to see in that tag using a multi-select form
- Pagination for a long data list

####  For Charts view mode, User can choose different options for a chart widget: 
- **chart widget type**: Line,  Bar or Pie chart
- **Line:** Single or multi line,
- **Operations:** currently support: sum, avg 
- **Timeframe:** x number of latest ticks OR a selected period
- **Group by:** daily, weekly, monthly, quarterly or yearly
- **Resizable** the chart widgets are resizeable;
- **Move:** drag and drop to move the widgets around and they don't stack on each other 
- **Chart dashboard is saved**: the current widgets on the dashboard will be saved to the database, the next time User log in (or login on another device)  will still see them




## Change logs:
- 1.0.0 : Initial release  (31/07/2019)
- 1.1.0 : Added some features for user experience (02/08/2019) 
     - Change dropdown layout in Dashboard for better UX,
     - Changed background, added reset password form in login page, 
     - Added Reset password page,
     - Added Reset password feature (with email token),
     - Added Change password feature.

