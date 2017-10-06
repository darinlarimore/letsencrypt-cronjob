# letsencrypt-cronjob
Instructions on how to automate renewals for Let's encrypt on a Digital ocean Ubuntu 16.04 LAMP stack.

## Step 1
Set up  the letsencrypt ssl certificate.

## Step 2 
Make sure cron is running and open the cron file to edit with `sudo crontab -e`
Note that using sudo here will run commands as root.^

## Step 3
Setup the commands that you would like to run and also specify an email to send the log/output everytime the command runs.

`MAILTO=emailaddress@gmail.com`

`0 1 * * * letsencrypt renew`

This runs every day at 1 o'clock and emails me the output so I can confirm that it ran.

Done!
