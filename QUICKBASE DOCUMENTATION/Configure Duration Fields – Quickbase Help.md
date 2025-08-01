## Configure Duration Fields

Duration fields display a length of time. You determine how the Duration field measures and displays time. To do so, edit the Duration field's properties.

When entering durations, Quickbase recognizes the following:

**Seconds**: sec, secs, second, seconds

**Minutes**: min, mins, minute, minutes

**Hours**: hr, hrs, hour, hours

**Days**: day, days

**Weeks**: wk, wks, week, weeks

## Set Format

The Display section lets you tell Quickbase what unit of time you want the duration to display; for example, an expanse of time in days or hours. Choose an option from the Value display dropdown.

| 
Select this option...

 | 

To display the duration in...

 |
| --- | --- |
| 

HH:MM

 | 

Hours and minutes. For example: **03:45**

 |
| 

HH:MM:SS

 | 

Hours, minutes, and seconds. For example: **03:45:22**

 |
| 

:MM

 | 

Minutes only. For example, if you enter "45 min," it displays as **:45**. If you enter more than 59 minutes, this format will display as HH:MM instead of just :MM.

 |
| 

:MM:SS

 | 

Minutes and seconds. For example, if you enter ":45.25 min," it displays as **:45:15**.

 |
| 

Smart Units

 | 

This is the default. The most appropriate format for the entered value. For example, "120 min" displays as **2 hours**. "84 hrs" displays as **3.5 days**.

 |
| 

Weeks

 | 

Number of weeks. For example, if you enter "84 hrs," it displays as **.5**.

 |
| 

Days

 | 

Number of days. For example, if you enter "84 hrs," it displays as **3.5**.

 |
| 

Hours

 | 

Number of hours. For example, if you enter "3.5 days," it displays as: **84**.

 |
| 

Minutes

 | 

Number of minutes. For example, if you enter "3.5 days," it displays as **5040**.

 |
| 

Seconds

 | 

Number of seconds. For example, if you enter "3.5 days," it displays as **302400**.

 |

## Decimals

If you want, you can add decimals into the mix. Just go to the **Decimal places** option and enter the number of digits you want to display after the decimal point. Leave it blank for a floating point number. If a user enters more digits after the decimal point than you've entered here, Quickbase rounds the number and extends it only to the number of decimal places you specified. The fraction .5 rounds the number away from 0.  For example, 3.5 rounds to 4, and -3.5 rounds to -4.  If you would rather .5 always round up, meaning that -3.5 would round to -3, use the Round formula instead of the decimal places option for rounding. Usually, decimals are most appropriate when the format calls for less exact time measurements, like Days for example (as opposed to a more precise measurement like HH:MM:SS).

## Total or Average Durations

The **Totals and averages** option tells Quickbase how to wrap up the numbers when the duration field appears in a table. The program either totals or averages all the durations. The result appears at the bottom of the column. To set this option, open the field's properties page and turn on the appropriate checkbox.