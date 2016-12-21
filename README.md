# Website-blocker
Blocks certain website URL's by modifying the redirect address in the hosts file using Python and Task scheduler
The hosts file sitting in the C:\Windows\System32\drivers\etc can contain IP addresses which can be hit directly without the need od resolving the domain name to an IP address using DNS. This hosts file can be used to contain URL's of websites which need to be blocked and can be redirected to localhost in order to block them.
Steps followed:
1.Check the condition every 5 seconds
2.If the current time is within a timeframe when the websites should be blocked, add them to the hosts file; redirecting them to loaclhost if they don't already exist in the hosts file.
3.If the current time is not within the timeframe when the websites should be blocked, delete the website names and redirect addresses if any
4.Schedule this python program to run at System startup using Task scheduler
