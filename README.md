# i3bar-conky
Collection of scripts I use with conky in i3bar

![GitHub Logo](/img/i3bar.png)

#### Cryptocompare
There are two Cryptocompare scripts. One for fetching and saving data to textual file and one for displaying the results.
##### Get API data
For a given currency pairs fetches data from the API. Last two values are saved in the local file `~/.cryptocompare-last`.
Should be a cron script.

##### Parse data
Reads data from `~/.cryptocompare-last` and displays colored data depending on the market trend (up/down).

#### Dwarfpool status
![crypto](/img/crypto.png)

For a given ETH wallet and a monitoring email get a worker statistics from official dwarfpool.com API.
Monitoring email is used as a API key, and only statistics for miners that have this monitoring email set will be fetched.


#### Work time
Script showing how much hours of work is left for today. Worktime is represented by 8 dots
that are filled (from empty to full) as the day passes by.

![status](/img/status.png)

#### DNS check
Checks if DNS servers resolve queries. List of DNS servers to check is defined in the script.
All dns servers are queried for A record of google.com.

#### ICMP check
Checks if devices responds to ICMP requests. List of hostnames (or IP addresses) to be pinged is defined in the script.

#### Port listening check
Checks if localhost listens for specific services. Services to be checked are defined in the script itself.
Script parses `netstat` output and tries to find services defined. Default checks Bacula, VNC, SSH, DNS and MySQL.
