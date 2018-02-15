# ResaleNotificationService
Resident Advisor has a resale program, but wouldn't tell you if tickets became available for resale. This script will email you when tickets become available

To use this script, in script.php:

* Replace $contents = file_get_contents("https://www.residentadvisor.net/events/1053089"); with whatever URL you're trying to purchase tickets from
* Replace the $mail->setFrom('', '');, mail username/password, etc. with your own username password

If you're using it on another site, you will have to replace $search   = "buynow"; with whatever you're trying to search for

To get this to work for gmail, I had to turn 'Allow less secure apps' to 'Off' in https://myaccount.google.com/security.

Then, in crontab, I ran:

*/5 * * * * php /path/to/script.php                                                 │

