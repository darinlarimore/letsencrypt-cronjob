# letsencrypt-cronjob
Instructions on how to automate renewals for lets encrypt on a digital ocean lamp server

## Step 1
Set up  the letsencrypt ssl certificate.

## Step 2 
Make sure cron is running and open the cron file to edit with `sudo crontab -e`
Note that using sudo here will run commands as root.^

## Step 3
Setup the commands that you would like to run and also specify an email to send the log/output everytime the command runs.

`MAILTO=darinlarimore@gmail.com`

`0 1 * * * letsencrypt renew`

This runs every day at 1 o'clock and emails me the output so I can confirm that it ran.

Done!
